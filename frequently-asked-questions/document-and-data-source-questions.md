# Document and Data Source Questions

### **How can I extract patent data from ChEMBL?**

_On the interface:_

Select the documents view from the main ChEMBL homepage -

<figure><img src="../.gitbook/assets/Screenshot 2023-07-13 at 11.17.39.png" alt=""><figcaption></figcaption></figure>

Use the lefthand filter panel to select patents -

<figure><img src="../.gitbook/assets/Screenshot 2023-07-13 at 11.18.18.png" alt=""><figcaption></figcaption></figure>

_Local version of the database:_

Selected patent data is available in ChEMBL under SRC\_ID 38. Patent data from Binding DB is included under SRC\_ID 37.

Details on the selection of patents can be found in this [publication](https://pubmed.ncbi.nlm.nih.gov/37151295/).&#x20;

### How do I perform a document similarity search?

More details can be found in this [Blog post](https://chembl.blogspot.com/2013/09/document-similarity-in-chembl.html).&#x20;

We also have an API endpoint:  [https://www.ebi.ac.uk/chembl/api/data/document\_similarity](https://www.ebi.ac.uk/chembl/api/data/document\_similarity)

### What data sources are stored in ChEMBL?

ChEMBL consists of data from a wide variety of data sources including scientific literature and patents, deposited data sets, PubChem BioAssay and BindingDB databases, toxicology data sets and drug/clinical candidate resources. The current list of sources is:

| Source                                                           | Source ID |
| ---------------------------------------------------------------- | :-------: |
| Scientific Literature                                            |     1     |
| GSK Malaria Screening                                            |     2     |
| Novartis Malaria Screening                                       |     3     |
| St Jude Malaria Screening                                        |     4     |
| Sanger Institute Genomics of Drug Sensitivity in Cancer          |     5     |
| PDBe Ligands                                                     |     6     |
| PubChem BioAssays                                                |     7     |
| Clinical Candidates                                              |     8     |
| Orange Book                                                      |     9     |
| Guide to Receptors and Channels (DEPRECATED)                     |     10    |
| Open TG-GATEs                                                    |     11    |
| Manually Added Drugs                                             |     12    |
| USP Dictionary of USAN and International Drug Names              |     13    |
| Drugs for Neglected Diseases Initiative (DNDi)                   |     14    |
| DrugMatrix                                                       |     15    |
| GSK Published Kinase Inhibitor Set                               |     16    |
| MMV Malaria Box                                                  |     17    |
| TP-search Transporter Database                                   |     18    |
| Harvard Malaria Screening                                        |     19    |
| WHO-TDR Malaria Screening                                        |     20    |
| Deposited Supplementary Bioactivity Data                         |     21    |
| GSK Tuberculosis Screening                                       |     22    |
| Open Source Malaria Screening                                    |     23    |
| Millipore Kinase Screening (DEPRECATED - MERGED WITH SRC\_ID = 1 |     24    |
| External Project Compounds                                       |     25    |
| Gene Expression Atlas Compounds                                  |     26    |
| AstraZeneca Deposited Data                                       |     27    |
| FDA Approval Packages                                            |     28    |
| GSK Kinetoplastid Screening                                      |     29    |
| K4DD Project                                                     |     30    |
| Curated Drug Metabolism Pathways                                 |     31    |
| St Jude Leishmania Screening                                     |     32    |
| Gates Library compound collection                                |     33    |
| MMV Pathogen Box                                                 |     34    |
| HeCaToS Compounds                                                |     35    |
| Withdrawn Drugs                                                  |     36    |
| BindingDB Database                                               |     37    |
| Patent Bioactivity Data                                          |     38    |
| Curated Drug Pharmacokinetic Data                                |     39    |
| CO-ADD antimicrobial screening data                              |     40    |
| WHO Anatomical Therapeutic Chemical Classification               |     41    |
| British National Formulary                                       |     42    |
| Published Kinase Inhibitor Set 2                                 |     43    |
| Kuster lab chemical proteomics drug profiling                    |     48    |
| HESi                                                             |     49    |
| Winzeler Lab Plasmodium Screening Data                           |     51    |
| SARS-CoV-2 Screening Data 2020-21                                |     52    |
| Prodrug active ingredients                                       |     53    |
| Donated Chemical Probes - SGC Frankfurt                          |     54    |
| EUbOPEN Chemogenomic Library                                     |     55    |
| Salvensis and LSHTM Schistosomiasis screening data               |     56    |
| IMI-CARE SARS-CoV-2 Data                                         |     57    |
| Fraunhofer HDAC6                                                 |     59    |
| MMV Malaria HGL                                                  |     60    |
| International Nonproprietary Names                               |     63    |
| Cardiff Schistosomiasis Dataset 2023                             |     64    |
| Literature data from EUbOPEN Chemogenomic Library                |     65    |
