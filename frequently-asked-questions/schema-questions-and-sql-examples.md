# Schema Questions and SQL Examples

### Can you show the relationship between all the tables in the ChEMBL database?

A PNG of the schema relationships can be found on the FTP site in the latest release directory: [ftp://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest](ftp://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest)

### Where can I get more information about the new classifications of target types in ChEMBL_15?

This can be found in the following slides (Current for ChEMBL_15): [Target Types](https://www.dropbox.com/s/4v8wmffpum1b7jg/target_types.pptx?m)

### Retrieve all the bioactivity data for bacterial targets:

```
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

