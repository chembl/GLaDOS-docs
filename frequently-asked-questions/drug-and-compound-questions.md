# Drug and Compound Questions

### What is max phase?

ChEMBL contains information on drugs that have been approved for treatment of a specific disease / diagnosis (an indication) within a region of the world (e.g. FDA drugs are approved for use in the United States), and clinical candidate drugs that are being investigated for an indication during the clinical trials process.&#x20;

The maximum phase of development for the compound across all indications is assigned a category called 'max\_phase' (the value in brackets is used in the downloadable ChEMBL database in the 'molecule\_dictionary' table):

* Approved (4): A marketed drug e.g. AMINOPHYLLINE ([CHEMBL1370561](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL1370561/)) is an FDA approved drug for treatment of asthma.&#x20;
* Phase 3 (3): A clinical candidate drug in Phase 3 Clinical Trials e.g. TEGOPRAZAN ([CHEMBL4297583](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL4297583/)) is under clinical investigation for treatment of peptic ulcer at Phase 3, and also liver disease at Phase 1.&#x20;
* Phase 2 (2): A clinical candidate drug in Phase 2 Clinical Trials e.g. NEVANIMIBE HYDROCHLORIDE ([CHEMBL542103](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL542103/)) is under clinical investigation for treatment of Cushing syndrome at Phase 2. Note that this category also includes a small number of trials that are defined by ClinicalTrials.gov as "[Phase 2/Phase 3](https://prsinfo.clinicaltrials.gov/definitions.html)".
* Phase 1 (1): A clinical candidate drug in Phase 1 Clinical Trials e.g. SALCAPROZATE SODIUM ([CHEMBL2107027](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL2107027/)) is under clinical investigation for treatment of diabetes mellitus. Note that this category also includes a small number of trials that are defined by ClinicalTrials.gov as "[Phase 1/Phase 2](https://prsinfo.clinicaltrials.gov/definitions.html)".
* Early Phase 1 (0.5): A clinical candidate drug in Early Phase 1 Clinical Trials e.g. CITRULLINE MALATE ([CHEMBL4297667](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL4297667/)) is under clinical investigation for coronary artery disease at Early Phase 1.
* Unknown (-1): Clinical Phase unknown for drug or clinical candidate drug ie where ChEMBL cannot assign a clinical phase e.g. NALIDIXATE SODIUM ([CHEMBL1255939](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL1255939/)) is known to be a clinical candidate drug because it has a USAN name, however ChEMBL has not been able to map a disease indication for this compound via its clinical trials pipeline and therefore its max\_phase is assigned as Unknown. By contrast, the parent compound (NALIDIXIC ACID, [CHEMBL5](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL5/)) is an approved drug (Phase 4) for treatment of bacterial disease. &#x20;
* Preclinical (NULL): preclinical compounds with bioactivity data e.g. [CHEMBL6300](https://www.ebi.ac.uk/chembl/compound\_report\_card/CHEMBL6300/) is a preclinical compound with bioactivity data that has been extracted from scientific literature. However, the sources of drug and clinical candidate drug information in ChEMBL do not show that this compound has reached clinical trials and therefore the max\_phase is set to null.&#x20;

By contrast, the 'max\_phase\_for\_ind' field in the 'drug\_indication' table in the downloadable ChEMBL database contains the maximum phase of development for the drug or clinical candidate drug for a specified indication. The numbering system remains identical to that described above for max\_phase. &#x20;

### **What information is available on withdrawn drugs?**

In the database, information on withdrawn drugs can be found in the molecule\_dictionary table (withdrawn\_flag, withdrawn\_year, withdrawn\_country, withdrawn\_reason, withdrawn\_class). On the interface, these fields are available as filters for compounds/drugs. Further details can also be found in this [Blog post](http://chembl.blogspot.com/2018/06/withdrawn-drugs.html).

### **Can you provide more details on the chirality flag?**

The chirality flag shows whether a drug is dosed as a racemic mixture (0), single stereoisomer (1) or as an achiral molecule (2), for unchecked compounds the chirality flag = -1. This information is curated for drugs and clinical candidates.

### Can you provide more details on the removal of Metal-Containing compounds?

The molfiles and images of a proportion of metal-containing compounds we removed from the ChEMBL interface and downloads set in ChEMBL\_17. This was partially due to some of these compounds having coordinated metal bonds. As InChI limitations are such that these coordinate bonds could not generate a Standard InChI, our main compound indicator of uniqueness in ChEMBL, it was decided to exclude the structures altogether.

The compound image on the interface was replaced with an icon that shows it is a metal-containing compound and the molfiles were removed from the download set on the FTP site. We will retain the molecular formula in both the download files and on the ChEMBL interface, so that the elemental make up of the compound is visible. This change does not affect the storage or display of the associated bioactivity data for these compounds.

### Can you provide some details on how ChEMBL compound properties (e.g. LogP, MW, PSA,..) are calculated?

Yes, please refer to the following document.&#x20;

{% file src="../.gitbook/assets/property_definitions_chembl_26.docx" %}
Property Definitions
{% endfile %}

### How are the SMILES and InChI created for ChEMBL?

The canonical SMILES are calculated using RDKit. The standard InChI is calculated using the command line InChI generator and was developed by the InChI Trust ([http://www.inchi-trust.org/inchi/](http://www.inchi-trust.org/inchi/)) and is executed via the command line. The version of InChI used in ChEMBL is 1.06

### How is the LogP calculated?

The LogP, and other compound properties are calculated using RDKit.

### **Why is a mechanism for my compound shown on the interface but not in the downloaded database?**

ChEMBL compounds can be found as alternative forms (e.g. salts, hydrates, isotopes). On the ChEMBL interface, we typically map mechanisms to the parent compound. In the mechanisms table, mechanisms are mapped to the approved drug form (may be a parent or salt). Alternative forms can be linked through the molecule\_hierarchy table to retrieve a mechanism mapped to any member of a compound family.