# Drug and Compound Questions

### What is a ‘drug’ or a ‘clinical candidate drug’ in ChEMBL? And how does this differ from a compound?

ChEMBL contains a large number of preclinical compounds with bioactivity data from experimental sources. However, ChEMBL also curates information for marketed drugs, and drugs that are progressing through the clinical development pipeline (‘clinical candidate drugs’).

In essence, although a preclinical compound must have associated bioactivity data, a drug or clinical candidate drug does not require experimental data for inclusion in ChEMBL. However, an approved drug could also be a clinical candidate drug and/or a preclinical compound and therefore it may also have additional attributes as shown in the table below.

| ChEMBL 34                                     | Defining feature for inclusion in ChEMBL                                                   | Typical features in ChEMBL                                                                                                                              | Occasional or absent features in ChEMBL                                                                                                               |
| --------------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Preclinical Compound<br>(~2.4 million)</p> | Must have bioactivity data                                                                 | <p>Usually measured in an assay against a target.<br>Usually comes from scientific literature or a deposited dataset</p>                                | <p>Normally does not have a pref_name (unless also a drug).<br>Sometimes has indication, safety warning or mechanism information (if also a drug)</p> |
| <p>Clinical Candidate Drug<br>(~14 k)</p>     | Must come from a source of clinical candidate information (e.g. USAN, INN, ClinicalTrials) | <p>Has a pref_name, can be recognisable drug name, or a research code.<br>May have indication and mechanism information.</p>                            | <p>Usually does not have bioactivity data.<br>Does not have safety warning data.</p>                                                                  |
| <p>Approved Drug<br>(~4 k)</p>                | Must come from a source of approved drug information (e.g. FDA, EMA, WHO ATC)              | <p>Has a pref_name, usually a recognisable drug name.<br>Normally has indication and mechanism information.<br>May have safety warning information.</p> | <p>Often has bioactivity data (i.e. it is also a preclinical compound).<br>May also be a clinical candidate drug.</p>                                 |

### What is max phase?

ChEMBL contains information on drugs that have been approved for treatment of a specific disease / diagnosis (an indication) within a region of the world (e.g. FDA drugs are approved for use in the United States), and clinical candidate drugs that are being investigated for an indication during the clinical trials process.

The maximum phase of development for the compound across all indications is assigned a category called 'max\_phase' (the value in brackets is used in the downloadable ChEMBL database in the 'molecule\_dictionary' table):

* Approved (4): A marketed drug e.g. AMINOPHYLLINE ([CHEMBL1370561](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL1370561/)) is an FDA approved drug for treatment of asthma.
* Phase 3 (3): A clinical candidate drug in [Phase 3 Clinical Trials](https://prsinfo.clinicaltrials.gov/definitions.html) e.g. TEGOPRAZAN ([CHEMBL4297583](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL4297583/)) is under clinical investigation for treatment of peptic ulcer at Phase 3, and also liver disease at Phase 1.
* Phase 2 (2): A clinical candidate drug in [Phase 2 Clinical Trials](https://prsinfo.clinicaltrials.gov/definitions.html) e.g. NEVANIMIBE HYDROCHLORIDE ([CHEMBL542103](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL542103/)) is under clinical investigation for treatment of Cushing syndrome at Phase 2. Note that this category also includes a small number of trials that are defined by ClinicalTrials.gov as "[Phase 2/Phase 3](https://prsinfo.clinicaltrials.gov/definitions.html)". In addition, INN applications are assigned as Phase 2 because their [guidance](https://www.who.int/publications/m/item/guidance-on-the-use-of-inns) that states “As a general guide, the development of a drug should progress up to the point of clinical trials (phase II) before an application is submitted to the INN Secretariat for name selection.”
* Phase 1 (1): A clinical candidate drug in [Phase 1 Clinical Trials](https://prsinfo.clinicaltrials.gov/definitions.html) e.g. SALCAPROZATE SODIUM ([CHEMBL2107027](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL2107027/)) is under clinical investigation for treatment of diabetes mellitus. Note that this category also includes a small number of trials that are defined by ClinicalTrials.gov as "[Phase 1/Phase 2](https://prsinfo.clinicaltrials.gov/definitions.html)". In addition, USAN applications as assigned as Phase 1 because their [guidance](https://www.ama-assn.org/about/united-states-adopted-names/apply-united-states-adopted-name) states “Firms usually apply for a USAN when the investigational therapy is in Phase I or Phase II trials”
* Early Phase 1 (0.5): A clinical candidate drug in [Early Phase 1 Clinical Trials](https://prsinfo.clinicaltrials.gov/definitions.html) e.g. CITRULLINE MALATE ([CHEMBL4297667](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL4297667/)) is under clinical investigation for coronary artery disease at Early Phase 1.
* Unknown (-1): Clinical Phase unknown for drug or clinical candidate drug ie where ChEMBL cannot assign a clinical phase e.g. NALIDIXATE SODIUM ([CHEMBL1255939](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL1255939/)) is known to be a clinical candidate drug because it has a USAN name, however ChEMBL has not been able to map a disease indication for this compound via its clinical trials pipeline and therefore its max\_phase is assigned as Unknown. By contrast, the parent compound (NALIDIXIC ACID, [CHEMBL5](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL5/)) is an approved drug (Phase 4) for treatment of bacterial disease.
* Preclinical (NULL): preclinical compounds with bioactivity data e.g. [CHEMBL6300](https://www.ebi.ac.uk/chembl/compound_report_card/CHEMBL6300/) is a preclinical compound with bioactivity data that has been extracted from scientific literature. However, the sources of drug and clinical candidate drug information in ChEMBL do not show that this compound has reached clinical trials and therefore the max\_phase is set to null.

By contrast, the 'max\_phase\_for\_ind' field in the 'drug\_indication' table in the downloadable ChEMBL database contains the maximum phase of development for the drug or clinical candidate drug for a specified indication. The numbering system remains identical to that described above for max\_phase.

### **Why is the molecule\_type for some drugs "Unknown"?**

The molecule\_type category that is assigned can be one of: small molecule, inorganic small molecule or polymeric small molecule, antibody, antibody drug conjugate, cell-based, enzyme, gene, oligosaccharide, oligonucleotide, protein, vaccine component, or unknown. In ChEMBL, a small molecule is loosely defined as any bioactive compound (usually an organic molecule that is chemically synthesised) where the chemical structure can be precisely drawn, and it is not a biotherapeutic with a complex structure that is not easily identified or characterised. Based on the inherent difficulties of an imprecise definition of a small molecule, ChEMBL instead applies a practical approach to determine the molecule\_type category for drugs and clinical candidate drugs (in the molecule\_dictionary table). Any remaining compounds where the molecule\_type cannot be clearly identified are assigned as 'unknown'.

### **What information is available on withdrawn drugs?**

In the database, information on withdrawn drugs can be found in the drug\_warning table. On the interface, these fields are available as filters for compounds/drugs. Further details can also be found in this [Blog post](http://chembl.blogspot.com/2018/06/withdrawn-drugs.html).

### How can I extract ontology (EFO, MeSH) terms for drug indications?

Using the interface:

Browse drug indications by clicking on the "Drug Indications" bubble on the ChEMBL homepage ([https://www.ebi.ac.uk/chembl/explore/drug\_indications/](https://www.ebi.ac.uk/chembl/explore/drug_indications/)).

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 06.52.01.png" alt=""><figcaption></figcaption></figure>



It's possible to download data as CSV or TSV files using the download icons at the top tight of the page.

<figure><img src="../.gitbook/assets/Screenshot 2026-01-13 at 06.53.00.png" alt=""><figcaption></figcaption></figure>

You will then have a dataset containing EFO\_IDs.

Alternatively, download the database dump and use this SQL query to extract EFO and MeSH IDs:

```
select md.pref_name, md.chembl_ID as molecule_chembl_ID, ind.max_phase_for_ind, mesh_ID, mesh_heading, efo_ID, efo_term
from chembl.drug_indication ind, chembl.molecule_dictionary md
where md.molregno=ind.molregno
order by pref_name
;
```



### **Can you provide more details on the chirality flag?**

The chirality flag shows whether a drug is dosed as a racemic mixture (0), single stereoisomer (1) or as an achiral molecule (2), for unchecked compounds the chirality flag = -1. This information is curated for drugs and clinical candidates.

### Can you provide more details on the removal of Metal-Containing compounds?

The molfiles and images of a proportion of metal-containing compounds we removed from the ChEMBL interface and downloads set in ChEMBL\_17. This was partially due to some of these compounds having coordinated metal bonds. As InChI limitations are such that these coordinate bonds could not generate a Standard InChI, our main compound indicator of uniqueness in ChEMBL, it was decided to exclude the structures altogether.

The compound image on the interface was replaced with an icon that shows it is a metal-containing compound and the molfiles were removed from the download set on the FTP site. We will retain the molecular formula in both the download files and on the ChEMBL interface, so that the elemental make up of the compound is visible. This change does not affect the storage or display of the associated bioactivity data for these compounds.

### Can you provide some details on how ChEMBL compound physicochemical properties (e.g. LogP, MW, PSA,..) are calculated?

All properties are calculated on the parent form of the molecule i.e after any salts have been removed. The exception is the FULL\_WT, which, where applicable, is the molecular weight of the salt, plus any present hydrates.

Properties are only calculated on single component compounds (not mixtures) with molecular weight<1000 and containing only atoms H, C, N, O, S, P, F, Cl, Br and I. The exception is MW\_freebase which is calculated for all molecules.

**Section 1**

These calculations are performed using algorithms available in RDKit.

1. MW\_freebase

Molecular weight of the parent form of the molecule

2. MW\_Monoisotopic

The monoisotopic mass of the compound calculated as the sum of the masses of the most abundant isotopes in the compound.

3. AlogP

Calculated value for the lipophilicity of a molecule expressed as log (octanol/water partition coefficient). Method used for the calculation is as described in:

Prediction of Physicochemical Parameters by Atomic Contributions

Scott A. Wildman and and Gordon M. Crippen, Journal of Chemical Information and Computer Sciences 1999 39 (5), 868-873. DOI: 10.1021/ci990307l

4. PSA

Polar surface area is calculated by the method by P Ertl.

Fast calculation of molecular polar surface area as a sum of fragment based contributions and its application to the prediction of drug transport properties, Ertl, P., Rohde, B., Selzer, P., J. Med. Chem. 2000, 43, 3714-3717.

5. HBA

Count of the number of Hydrogen Bond Acceptors. Based on matching these SMARTS patterns:

\[$(\[N;!H0;v3]),$(\[N;!H0;+1;v4]),$(\[O,S;H1;+0]),$(\[n;H1;+0])]

6. HBD

Count of the number of Hydrogen Bond Donors. Based on matching these SMARTS patterns:

\[$(\[O,S;H1;v2]-\[!$(\*=\[O,N,P,S])]),$(\[O,S;H0;v2]),$(\[O,S;-]),$(\[N;v3;!$(N-\*=!@\[O,N,P,S])]),$(\[nH0,o,s;+0])]

7. HBA\_Lipinski

Count of nitrogen and oxygen atoms in the molecule

8. HBD\_Lipinski

Count of hydrogens attached to nitrogen or oxygen atoms

9. RTB

Number of rotatable bonds in the molecule. Based on matching this SMARTS pattern:

\[!$(\*#\*)&!D1]-&!@\[!$(\*#\*)&!D1]

10. Num\_RO5\_Violations

Number of properties defined in Lipinski’s Rule of 5 (RO5) that the compound fails. Conditions which violate the RO5 are: Molecular weight>500, AlogP>5, HBD>5, HBA>=10

11. Num\_Lipinski\_RO5\_Violations

As above except used HBA\_Lipinski and HBD\_Lipinski instead of HBA and HBD

Lipinski, C. A.; Lombardo, F.; Dominy, B. W.; Feeney, P. J. Experimental and Computational Approaches to Estimate Solubility and Permeability in Drug Discovery and Development Settings. Adv. Drug Deliv. Rev., 1997, 23, 3-25.

12. RO3\_Pass

Rule of 3 passes. It is suggested that compounds that pass all these criteria are more likely to be hits in fragment screening.

molecular weight <=300, number of hydrogen bond donors <=3, number of hydrogen bond acceptors <=3, AlogP <=3, RTB <=3, PSA<=60

A ‘Rule of Three’ for fragment-based lead discovery? Miles Congreve, Robin Carr,

Chris Murray and Harren Jhoti. Drug Discovery Today, 2003,8(19), 876-877

13. Aromatic\_Rings

The number of aromatic rings in the molecule

14. Heavy\_Atoms

The number of non-hydrogen atoms in the molecule

15. QED\_Weighted

This is the quantitative estimate of drug-likeness as described in:

“Quantifying the chemical beauty of drugs”

G. Richard Bickerton, Gaia V. Paolini, Jeremy Besnard, Sorel Muresan and Andrew L. Hopkins. Nature Chemistry, 2012, 4, 90-98

The values range from 0 -1 where 1 is the most drug-like and 0 the least drug-like.

**Section 2**

These properties are calculated using ChemAxon tools (ChEMBL\_26 onwards).

1. CX\_LogP

This is the calculated Octanol/Water Partition Coefficient.

2. CX\_LogD

This is the calculated Octanol/Water Distribution Coefficient at pH7.4. This is defined as the ratio of concentrations of all molecular species (neutral & ionized) in octanol divided by the concentration of all species in aqueous media at the pH specified.

3\. pKa

pKa is defined as -log10 Ka, where Ka is the dissociation constant:

4. CX\_MOST\_APKA

Acidic pKa is the pKa for the most acidic group of the molecule

5. CX\_MOST\_BPKA

Basic pKa is the pKa for the most basic group of the molecule

6. Molecular Species

An approximation of the species occurring at pH7.4 and can be ACID, BASE, NEUTRAL or ZWITTERION

These are defined according to the definitions:

Acid(A) ACD\_MOST\_ApKa <6.5 and ACD\_MOST\_BpKa<8.5

Base (B) ACD\_MOST\_ApKa >6.5 and ACD\_MOST\_BpKa>8.5

Neutral (N) ACD\_MOST\_ApKa >6.5 and ACD\_MOST\_BpKa<8.5

Zwitterion (ZW) ACD\_MOST\_ApKa <6.5 and ACD\_MOST\_BpKa>8.5

The molecular species is an approximation. This does not use absolute pKa and considers both most acidic and most basic pKa; compounds may be polyprotic. The calculation of pKa is temperature-dependant; further details on the ChemAxon pKa calculations can be found here - https://docs.chemaxon.com/display/docs/calculators\_pka-calculation.md

### How are the SMILES and InChI created for ChEMBL?

The canonical SMILES are calculated using RDKit. The standard InChI is calculated using the command line InChI generator and was developed by the InChI Trust ([http://www.inchi-trust.org/inchi/](http://www.inchi-trust.org/inchi/)) and is executed via the command line. The version of InChI used in ChEMBL is 1.06

### **Why is a mechanism for my compound shown on the interface but not in the downloaded database?**

ChEMBL compounds can be found as alternative forms (e.g. salts, hydrates, isotopes). On the ChEMBL interface, we typically map mechanisms to the parent compound. In the mechanisms table, mechanisms are mapped to the approved drug form (may be a parent or salt). Alternative forms can be linked through the molecule\_hierarchy table to retrieve a mechanism mapped to any member of a compound family.

More details can be found in this [Blog](http://chembl.blogspot.com/2020/09/molecule-hierarchy.html) post.

### How does the molecule hierarchy work?

ChEMBL uses the concept of compound 'families' so that each molecule (typically a salt) has a parent compound, and all the compounds in the family can be considered to have the same bioactivity.

Alternative forms of a compound (e.g. different salts, isotopes) can be viewed on the interface and activity data from alternative forms can be included or excluded using the ‘Exclude/include alternative forms’ button (see screenshot). The molecule form API endpoint or molecule\_hierarchy table can be used to gather more information about all the salts of a given parent or salt.

<figure><img src="../.gitbook/assets/Screenshot 2023-07-12 at 16.54.11.png" alt=""><figcaption></figcaption></figure>

### ...and why is the molecule hierarchy null for some compounds?

This difference is due to the fact that some compounds are 'virtual parents' and we do not have records of documents nor activities related with this compound itself but only for a salt of it (e.g. CHEMBL1207557).

### How can I cross-reference ChEMBL compounds across databases?

UniChem ([https://www.ebi.ac.uk/unichem/](https://www.ebi.ac.uk/unichem/)) can be used to map between 2 sets of identifiers. UniChem sources are listed [here](https://www.ebi.ac.uk/unichem/sources) and the WholeSourceMapping Table is [here](https://ftp.ebi.ac.uk/pub/databases/chembl/UniChem/data/wholeSourceMapping/). There is also REST API access to the UniChem webservices and an accompanying [webinar](https://www.youtube.com/watch?v=6GOU_7Doajw).

### **What are the parameters for the similarity search?**

Since ChEMBL version 26, the similarity search is run with FPSim2, using 2048 bit, radius 2 RDKit calculated Morgan fingerprints.

The FPSim2 file is available in the main release downloads folder here: [https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest/](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest/) by clicking on the link for chembl\_XX.h5.

We also have some background information in this [Blog post](http://chembl.blogspot.com/2019/01/fpsim2-simple-python3-molecular.html) - and some documentation on the similarity search can be found on [GitHub](https://github.com/chembl/FPSim2).

The similarity searches are run against the parent structures and running a similarity search using, for example, aspirin smiles ([https://www.ebi.ac.uk/chembl/g/#similarity\_search\_results/CC(%3DO)Oc1ccccc1C(%3DO)O/95](https://www.ebi.ac.uk/chembl/g/#similarity_search_results/CC\(=O\)Oc1ccccc1C\(=O\)O/95)) will return 3 compounds with a 100% of similarity. The two additional compounds are salt forms of aspirin.

It’s possible to perform structure similarity searches using the ChEMBL interface or the API endpoint.

### **Does ChEMBL contain agrochemical data?**

Agrochemicals are classified within ChEMBL using the IRAC, FRAC and HRAC classifications.

It’s also possible to use keywords on the interface to search assay descriptions for herbicidal, fungicidal and/or insecticidal assays. Alternatively, bespoke SQL queries using regular expressions (e.g. regexp\_like (description, '(h|H)erbicid(e|al) activity|Phytotoxic(|ity)|Antialgal activity')) can be constructed to search assay descriptions using a local version of the database. The target dictionary contains details of plant, insect and fungal targets within ChEMBL and can be used as a starting point to identify compounds with activity against these targets.

### **Why is the substructure search failing with my molecule?**

The substructure search is challenging for low complexity molecules (and sometimes can’t be executed in a reasonable time). The substructure search works well with more complex molecules such as rifampin. We’re working on improving this feature but unfortunately don’t have a workaround for this at the moment.

In searches for compounds containing simple functional groups e.g. nitrile, another possibility is to mine the SMILES information.

### **I'm searching ChEMBL by InChi key but no compounds are returned, why is this?**

Unfortunately, if the InChi key search does not return results it means that we do not have that molecule registered in ChEMBL. However, if you have a smiles or a mol-file then it is possible to run a structure flexmatch search on our web interface.

The 'Draw a structure' search functionality will open an editor where you can paste a smiles or a molfile, and create/edit a molecule for your search. There are 3 types of search. Connectivity (similar to exact match but it does not consider stereochemistry, isotopes etc.), similarity, and substructure.

For InChi keys that are not present in ChEMBL, [UniChem](https://www.ebi.ac.uk/unichem/) can be used to search other chemistry databases where they might be present.

### **H**ow are structures standardised?

You can find more information on compound curation in this [Blog post](https://chembl.blogspot.com/2020/02/chembl-compound-curation-pipeline.html) and on the structure standardiser [here](https://github.com/chembl/ChEMBL_Structure_Pipeline).

### **H**ow can I download the structures for all ChEMBL compounds?

We would suggest downloading the full SDF from the [FTP site](https://ftp.ebi.ac.uk/pub/databases/chembl/ChEMBLdb/latest/) rather than using the interface. The interface download may not be possible for extremely large files.

### What is the Rule of Five?

The ‘Rule of Five’ refers to the drug-like properties defined by [Lipinski](https://pubmed.ncbi.nlm.nih.gov/11259830/) (oral drugs should have a molecular weight < 500, no more than 5 H-bond donors, no more than 10 H-bond acceptors and a CLogP not greater than 5). A compound that complies with the Rule of Five has 0 or 1 violations of these rules.

The number of violations of the Rule of Five is recorded in the ChEMBL database (within the MOLECULE\_DICTIONARY) and is also available as a filter when browsing compounds on the interface (see below).

<figure><img src="../.gitbook/assets/Screenshot 2023-11-08 at 10.26.26.png" alt="" width="375"><figcaption><p>Molecule filters include the number of Ro5 violations.</p></figcaption></figure>

Whether compounds are compliant with the Rule of Five is also displayed as an icon in the molecule features section of the compound report card. The Ro5 flag shows as **True** for compounds with 0 or 1 violations. The exception is metal-containing compounds where the Ro5 is not calculated and is recorded as null in the database and the Ro5 icon shows **False** on the ChEMBL interface.

<figure><img src="../.gitbook/assets/Screenshot 2023-11-08 at 10.29.30.png" alt=""><figcaption><p>The Rule of Five shows as True for aspirin (CHEMB25)</p></figcaption></figure>

### How does ChEMBL define 'virtual parents'?

Virtual parents may arise when bioactivity data has been deposited for salts or hydrates of a drug-like compound but no data is recorded for the parent compound itself. The parent compound is registered in ChEMBL but is not directly linked to bioactivity data.

A virtual parent compound has an entry (i.e. its own row) in the MOLECULE\_DICTIONARY but does NOT have an entry in its own right in the MOLECULE\_HIERARCHY i.e. the virtual parent is present in the MOLECULE\_HIERARCHY.parent\_molregno field but does not have an entry in the MOLECULE\_HIERARCHY.molregno field. Also, there is no entry for the virtual parent in the COMPOUND\_RECORDS table.

### Could you provide more information on the source of the structural alerts, and why some were removed after ChEMBL 26?

The current version of ChEMBL includes five sets of structural alerts, from the following sources:

* Glaxo Wellcome Hard Filters, PMID: 10529988
* University of Dundee NTD Screening Library Filters, PMID: 18064617
* Bristol-Myers Squibb HTS Deck Filters, PMID: 16711725
* Pan Assay Interference Compounds (PAINS) Filters, PMID: 20131845
* NIH MLSMR Excluded Functionality Filters.

We removed some structural alerts during the RDKit conversion for version 26. In summary, we kept datasets with a clear literature reference and removed poorly documented sets.

### How can I find out whether my compound is a covalent or non-covalent inhibitor?

Unfortunately, we don’t curate covalent/non-covalent inhibitors so this information is not readily extracted from ChEMBL.

However, there is the option of mining document titles/abstracts for terms such as ‘covalent inhibitor’, either through the interface or web services. On the interface, you would need to type your search terms into the search bar and select 'Documents' from the dropdown menu.\
\
This type of search can also be performed using the web services ‘documents’, ‘similar documents’ and ‘document term’ tools (see [https://chembl.gitbook.io/chembl-interface-documentation/web-services/chembl-data-web-services](https://chembl.gitbook.io/chembl-interface-documentation/web-services/chembl-data-web-services)).\
\
You will need to review the identified documents to check that these are describing covalent inhibitors. However, this approach is unlikely to identify all covalent inhibitors in ChEMBL.

### How can I find out if my compound binds well to a target and is specific?

There isn’t a general ‘specificity’ metric in ChEMBL but ChEMBL includes a range of affinity and selectivity data that can be explored.

Selectivity data is included in ChEMBL if this is reported in a publication (selectivity ratios may have been calculated from comparable assays in a single paper). Compound activity against two targets may provide some information on selectivity towards therapeutic targets versus related targets or toxicity targets but this will be limited to those targets tested for a given compound. Selectivity towards targets can also be investigated by comparison of the results of different assays. However, it should be noted that assays can vary widely.
