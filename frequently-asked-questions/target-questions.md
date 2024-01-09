# Target Questions

### **Where can I find more details on the target prediction?**

More details can be found in this [Blog post](https://chembl.blogspot.com/2020/01/new-chembl-ligand-based-target.html). Target predictions can be found on the interface and predictions can be run using this [Docker image](https://hub.docker.com/repository/docker/chembl/mcp).&#x20;

### What are the main target types in ChEMBL?

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### **How can I find the binding site of my compound?**

We annotate binding site information in two different ways:

1\) For drugs and clinical candidates, where the target is a protein complex and we know which subunit(s) the drug binds to, we indicate this by including a site\_id in the drug\_mechanism table. This information can be viewed on the ChEMBL interface through the Drug Mechanisms view where the data is found in the Binding\_site\_name and Binding\_site\_comment fields.

2\) For assay/bioactivity data, we have an algorithm that attempts to predict the most likely binding-domain of the protein target (based on the domain structure of the protein and a list of all curated known small molecule binding domains). This algorithm is only applied to a subset of the > 15 million bioactivity records - binding or functional assays with a single protein or protein complex targets and dose-response measurements - and is not able to make an unambiguous prediction in all cases. There are around 650 K activity measurements with a predicted domain in the predicted\_binding\_domains table.&#x20;

### **How can I find the Pfam domains for my target?**

Pfam-A domains can be found in the domains table and can be viewed in the Domain Cross References section of the target report card on the ChEMBL interface.

### **What does the target relationship\_type flag mean?**

The relationship\_type flag provides the relation between the reported target in the source document and the assigned target.\
\
D          Direct protein target assigned\
H          Homologous protein target assigned\
M         Molecular target other than protein assigned\
N          Non-molecular target assigned\
S          Subcellular target assigned\
U          Default value - Target has yet to be curated

### **How can I find Entrez\_IDs for my ChEMBL targets?**

UniProt accessions are the main identifier for protein targets. These can be mapped to Entrez IDs using the [UniProt mapping tool](https://www.uniprot.org/uploadlists/).  ChEMBL protein targets may be a single protein (with a single accession) or a protein complex, protein family (with more than one associated accession).

### **My protein isn't in ChEMBL, how can I find similar proteins?**

It’s possible to search ChEMBL for similar proteins using the EBI-wide BLAST search tool through the ChEMBL interface.

On the ChEMBL homepage, click on 'Advanced Search’ and select ‘Biological Sequence’ and then input your target protein. Similar proteins will be returned alongside the E-value.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-14 at 09.38.43.png" alt=""><figcaption></figcaption></figure>

We don’t currently have an API endpoint for the protein similarity searches but all target protein sequences are provided in the component\_sequences table and can be extracted for further analyses.

### Can you provide more details on the target relationship mapping?

This is based on both the target\_type and the component\_type (to deal with RNA targets) and is shown below.

<figure><img src="../.gitbook/assets/Screenshot 2023-06-14 at 10.15.24.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2023-06-14 at 10.18.33.png" alt=""><figcaption></figcaption></figure>

### How does ChEMBL treat protein variants?

We map proteins to UniProt accessions and parent and variant proteins will have the same target ChEMBL\_ID. Variants are also mapped to a variant\_ID that distinguishes these from the wild-type protein (where the variant\_ID is null).

Variants may contain single or multiple mutations which include defined (e.g. single amino acid changes) or undefined (e.g. ‘deletion mutants’, mapped to variant\_ID -1) changes. The variant sequences table contains details of mutated residues and the sequence.

Variant information is also available through the ChEMBL interface and can be viewed when browsing assays by adding additional columns (variant\_sequence\_accession and variant\_sequence\_mutation) and though web services ([https://www.ebi.ac.uk/chembl/api/data/assay.json?variant\_sequence\_\_isnull=false](https://www.ebi.ac.uk/chembl/api/data/assay.json?variant\_sequence\_\_isnull=false)). The variant\_ID can be used to exclude or include protein variants when extracting bioactivity data.

Mutant targets may be associated with with drug resistance or disease but may also include some engineered mutations (users need to review the assay description or references to interpret the data).

### ...and why is there no referential integrity between the variant\_sequences table and component\_sequences table?

The variant\_sequences table is not linked to the component sequences table. It’s possible that two assays, one describing a variant and one describing a wild-type protein, may refer to the same protein target (and share a ChEMBL target ID), but provide different accessions. We keep both accessions in case a slightly different sequence was used as the reference to generate the variant numbering in the corresponding assay.

### **How are isoforms treated by ChEMBL?**

In ChEMBL, we map isoforms to the primary UniProt accession. Sometimes researchers test different isoforms in separate experiments and in these cases one assay is recorded per isoform. The isoform details are recorded in the assay descriptions.&#x20;

For example:

Assay CHEMBL672502 Binding affinity against Dopamine receptor D2L&#x20;

Assay CHEMBL670556 Binding Affinity of Compound of Dopamine receptor D2S

### **Is 'fuzzy' target matching available via the API?**

Although ‘fuzzy’ matching is available though the UI, unfortunately, we don’t have any fuzzy API support at the moment. However, there is the option to use regular expressions - &#x20;

e.g. [https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_iregex=cdk1|cdk2](https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_iregex=cdk1|cdk2)

### **My assay is 'Unchecked', what does this mean?**

We extract bioactivity data from a selected set of journals, patents and deposited data sets and include a range of assays such as cytotoxicity assays, antibacterial assays and protein inhibition assays. The extracted data is curated and mapped to ChEMBL targets where possible. However, the curation is an ongoing process and some assays may not be mapped to a target and appear as ‘Unchecked’.\
\
There are a number of reasons why the target of an assay may be ‘Unchecked’. For example, the assay may be a physiochemical assay (such as solubility determination) where there is no target, a selectivity ratio where there isn’t a single target and/or the target may be ambiguous, has not yet been created or has not yet been reviewed.

### How can I extract gene symbols for my target?&#x20;

ChEMBL targets are all associated with a unique target ChEMBL\_ID. We use UniProt accessions as our primary identifier for protein targets. However, gene symbols can be obtained from the component\_synonyms table:

```
select td.chembl_ID as target_chembl_ID, td.organism, td.tax_ID, td.pref_name, cs.component_synonym
from chembl.target_dictionary td
left join chembl.target_components tc on td.tid=tc.tid
left join chembl.component_synonyms cs on tc.component_ID=cs.component_ID
where syn_type = 'GENE_SYMBOL' -- you can include other synonym types if needed
and chembl_ID = 'CHEMBL204' -- Melanocortin receptor 1 as an example
```

This webservices example may also be useful - [https://chembl.gitbook.io/chembl-interface-documentation/web-services/chembl-data-web-services#having-a-list-of-molecules-chembl-ids-in-a-csv-file-produce-another-csv-file-that-maps-every-compound-id-into-a-list-of-human-gene-names](https://chembl.gitbook.io/chembl-interface-documentation/web-services/chembl-data-web-services#having-a-list-of-molecules-chembl-ids-in-a-csv-file-produce-another-csv-file-that-maps-every-compound-id-into-a-list-of-human-gene-names).
