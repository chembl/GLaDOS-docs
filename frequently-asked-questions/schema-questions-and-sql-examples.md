# Schema Questions and SQL Examples

## Can you show the relationship between all the tables in the ChEMBL database?

A PNG of the schema relationships can be found on the FTP site in the latest release directory: [ftp://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest](ftp://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest)

## Where can I get more information about the new classifications of target types in ChEMBL\_15?

This can be found in the following slides \(Current for ChEMBL\_15\): [Target Types](https://www.dropbox.com/s/4v8wmffpum1b7jg/target_types.pptx?m)

## Retrieve all the bioactivity data for bacterial targets:

```sql
SELECT md.chembl_id AS compound_chembl_id,
cs.canonical_smiles,
act.standard_type,
act.standard_value,
act.standard_units,
td.chembl_id AS target_chembl_id,
td.organism,   td.pref_name
FROM target_dictionary td
  JOIN assays a ON td.tid = a.tid
  JOIN activities act ON a.assay_id = act.assay_id
  JOIN molecule_dictionary md ON act.molregno = md.molregno
  JOIN compound_structures cs ON md.molregno   = cs.molregno
  JOIN organism_class oc ON td.tax_id = oc.tax_id
    AND oc.L1 = 'Bacteria';
```
## Retrieve activity details for compound and all its salts which have an IC50 bioactivity value in nM against a target of interest:

```sql
-- Compound is Sildenafil (CHEMBL192)
-- Target is human PDE5 (CHEMBL1827)
SELECT m.chembl_id AS compound_chembl_id,
s.canonical_smiles,
r.compound_key,
NVL(TO_CHAR(d.pubmed_id),d.doi) AS pubmed_id_or_doi,
a.description                   AS assay_description,
act.standard_type,
act.standard_relation,
act.standard_value,
act.standard_units,
act.activity_comment,
t.chembl_id                    AS target_chembl_id,
t.pref_name                    AS target_name,
t.organism                     AS target_organism
FROM compound_structures s
  RIGHT JOIN molecule_dictionary m ON s.molregno = m.molregno
  JOIN compound_records r ON m.molregno = r.molregno
  JOIN docs d ON r.doc_id = d.doc_id
  JOIN activities act ON r.record_id = act.record_id
  JOIN assays a ON act.assay_id = a.assay_id
  JOIN target_dictionary t ON a.tid = t.tid
    AND t.chembl_id      = 'CHEMBL1827'
    AND m.chembl_id IN
         (SELECT DISTINCT
            m1.chembl_id
          FROM molecule_dictionary m1
            JOIN molecule_hierarchy mh ON mh.molregno = m1.molregno
            JOIN molecule_dictionary m2 ON mh.parent_molregno = m2.molregno
              AND m2.chembl_id = 'CHEMBL192')
    AND act.standard_type = 'IC50'
    AND act.standard_units = 'nM';
```

## Retrieve compounds which are selective to one target over a second target:

```sql
-- Compounds which are selective for Human CDK2 (CHEMBL301) over Human CDK5 (CHEMBL4036) 
-- Selectivity is based on comparing binding affinities using IC50 values.  
SELECT md.chembl_id,
cs.canonical_smiles
FROM target_dictionary td
  JOIN assays a ON td.tid = a.tid
  JOIN activities act ON a.assay_id = act.assay_id
  JOIN molecule_dictionary md ON md.molregno = act.molregno
  JOIN compound_structures cs ON md.molregno = cs.molregno
    AND act.standard_relation = '='
    AND act.standard_type     IN ('IC50')
    AND act.standard_units    = 'nM'
    AND act.standard_value    < 50
    AND td.chembl_id          = 'CHEMBL301'
INTERSECT
SELECT md.chembl_id,
cs.canonical_smiles
FROM target_dictionary td
  JOIN assays a ON td.tid = a.tid
  JOIN activities act ON a.assay_id = act.assay_id
  JOIN molecule_dictionary md ON md.molregno = act.molregno
  JOIN compound_structures cs ON md.molregno = cs.molregno
AND act.standard_relation     = '='
AND act.standard_type         IN ('IC50')
AND act.standard_units        = 'nM'
AND act.standard_value        > 200
AND td.chembl_id              = 'CHEMBL4036';
```

## Retrieve target ChEMBL_ID, target_name, target_type, protein accessions and sequences for all protein targets:

```sql
SELECT t.chembl_id AS target_chembl_id,
t.pref_name        AS target_name,
t.target_type,
c.accession        AS protein_accession,
c.sequence         AS protein_sequence
FROM target_dictionary t
  JOIN target_type tt ON t.target_type = tt.target_type
  JOIN target_components tc ON t.tid = tc.tid
  JOIN component_sequences c ON tc.component_id = c.component_id
AND tt.parent_type  = 'PROTEIN';
```

## Retrieve PK data from 'Curated Drug Pharmacokinetic Data' source in ChEMBL for drug:

```sql
-- Data for levofloxacin
SELECT DISTINCT
  d.title,
  min(decode(ap.standard_type, 'DATASET', nvl(to_char(ap.standard_value), ap.standard_text_value)))         dataset,
  a.assay_id,
  a.description,
  min(decode(actp.standard_type, 'DOSED_COMPOUND_NAME',
             nvl(to_char(actp.standard_value), actp.standard_text_value) || ' ' ||
             actp.standard_units))                                                                          dosed_compound_name,
  min(decode(actp.standard_type, 'DOSE',
             nvl(to_char(actp.standard_value), actp.standard_text_value) || ' ' || actp.standard_units))    dose,
  min(decode(actp.standard_type, 'DOSAGE_FORM',
             nvl(to_char(actp.standard_value), actp.standard_text_value) || ' ' || actp.standard_units))    dosage_form,
  min(decode(actp.standard_type, 'REGIMEN',
             nvl(to_char(actp.standard_value), actp.standard_text_value) || ' ' || actp.standard_units))    regimen,
  min(decode(actp.standard_type, 'ROUTE', nvl(to_char(actp.standard_value), actp.standard_text_value)))     route,
  min(decode(actp.standard_type, 'GENDER', nvl(to_char(actp.standard_value), actp.standard_text_value)))    gender,
  min(decode(actp.standard_type, 'AGE_RANGE', nvl(to_char(actp.standard_value), actp.standard_text_value))) age_range,
  min(decode(actp.standard_type, 'HEALTH_STATUS', nvl(to_char(actp.standard_value),
                                                      actp.standard_text_value)))                           health_status,
  min(decode(actp.standard_type, 'TISSUE', nvl(to_char(actp.standard_value),
                                                      actp.standard_text_value)))                           tissue,
  cr.molregno,
  cr.compound_name,
  act.activity_id,
  act.toid,
  act.standard_type,
  act.standard_relation,
  act.standard_value,
  act.standard_units,
  act.activity_comment
FROM source s
  JOIN compound_records cr ON s.src_id = cr.src_id
  JOIN docs d ON d.doc_id = cr.doc_id
  JOIN activities act ON cr.record_id = act.record_id AND cr.doc_id = act.doc_id
  JOIN activity_properties actp ON act.activity_id = actp.activity_id
  JOIN assays a ON act.assay_id = a.assay_id
  JOIN assay_parameters ap ON a.assay_id = ap.assay_id
                              AND s.src_description = 'Curated Drug Pharmacokinetic Data'
                              AND cr.compound_name LIKE 'LEVOFLOXACIN%'
GROUP BY d.title, a.assay_id, a.description, cr.molregno, cr.compound_name, act.activity_id, act.toid,
  act.standard_type, act.standard_relation, act.standard_value, act.standard_units, act.activity_comment
ORDER BY cr.compound_name, act.toid, act.standard_type;
```

## Retrieve compound activity details for all targets containing a protein of interest:

```sql
-- Protein of interest is human M2 muscarinic receptor (P08172) 
SELECT DISTINCT
  m.chembl_id                      AS compound_chembl_id,
  s.canonical_smiles,
  r.compound_key,
  NVL(TO_CHAR(d.pubmed_id), d.doi) AS pubmed_id_or_doi,
  a.description                    AS assay_description,
  act.standard_type,
  act.standard_relation,
  act.standard_value,
  act.standard_units,
  act.activity_comment,
  t.chembl_id                      AS target_chembl_id,
  t.pref_name                      AS target_name,
  t.target_type
FROM compound_structures s
  RIGHT JOIN molecule_dictionary m ON s.molregno = m.molregno
  JOIN compound_records r ON m.molregno = r.molregno
  JOIN docs d ON r.doc_id = d.doc_id
  JOIN activities act ON r.record_id = act.record_id
  JOIN assays a ON act.assay_id = a.assay_id
  JOIN target_dictionary t ON a.tid = t.tid
  JOIN target_components tc ON t.tid = tc.tid
  JOIN component_sequences cs ON tc.component_id = cs.component_id
    AND cs.accession = 'P08172';
 ```
 
 ## Retrieve compound activity details for a target:
 
 ```sql
 -- Target is Human PDE5 (CHEMBL1827) 
SELECT m.chembl_id AS compound_chembl_id,   
s.canonical_smiles,   
r.compound_key,   
NVL(TO_CHAR(d.pubmed_id),d.doi) AS pubmed_id_or_doi,   
a.description                   AS assay_description,   act.standard_type,   
act.standard_relation,   
act.standard_value,   
act.standard_units,   
act.activity_comment 
FROM compound_structures s,   
molecule_dictionary m,   
compound_records r,   
docs d,   
activities act,   
assays a,   
target_dictionary t 
WHERE s.molregno (+) = m.molregno 
AND m.molregno       = r.molregno 
AND r.record_id      = act.record_id 
AND r.doc_id         = d.doc_id 
AND act.assay_id     = a.assay_id 
AND a.tid            = t.tid 
AND t.chembl_id      = 'CHEMBL1827';
```

## Can you show me how to use SQL to only extract the PubChem data from ChEMBL?

```sql
-- The source id for PubChem data is found in the SOURCE table and is ‘7’.
-- Please note that this will bring back over 4,000,000 data points
SELECT DISTINCT
  md.molregno,
  cs.canonical_smiles,
  md.chembl_id,
  act.standard_type,
  act.standard_value,
  act.standard_units
FROM activities act
  JOIN molecule_dictionary md ON act.molregno = md.molregno
  JOIN compound_structures cs ON md.molregno = cs.molregno
  JOIN compound_records cr ON cr.molregno = act.molregno
  JOIN source src ON src.src_id = cr.src_id
    AND src.src_id = '7';
```
