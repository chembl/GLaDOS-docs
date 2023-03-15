# General Questions

### How often do you update the data?

The data is updated regularly, with releases approximately 2-3 times a year.

### What is the ChEMBLID?

The ChEMBLID is a unique ID that has been assigned to compounds, targets, assays, documents, tissues and cell types in ChEMBL. It can be used to retrieve a Report Card page for these entities, or to search for them using the keyword search.

### **How can I interconvert PubChem and ChEMBL\_IDs?**

1\) [UniChem](https://www.ebi.ac.uk/unichem/) can be used to map between 2 sets of identifiers.&#x20;

The [source mapping tables](ftp://ftp.ebi.ac.uk/pub/databases/chembl/UniChem/data/wholeSourceMapping/) are on the FTP website and include a ChEMBL\_ID to PubChem\_ID mapping table (source mapping table for src1 to src22).&#x20;

2\) In the ChEMBL database, identifiers may be found in the compound\_records table (as the compound\_key).

### What literature coverage is there in ChEMBL?

Data are routinely extracted from seven core journals:

* Bioorg Med Chem Lett ([https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry-letters](https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry-letters))
* J Med Chem ([https://pubs.acs.org/journal/jmcmar](https://pubs.acs.org/journal/jmcmar))
* Bioorg Med Chem ([https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry](https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry))
* J Nat Prod ([https://pubs.acs.org/journal/jnprdf](https://pubs.acs.org/journal/jnprdf))
* Eur J Med Chem ([https://www.sciencedirect.com/journal/european-journal-of-medicinal-chemistry](https://www.sciencedirect.com/journal/european-journal-of-medicinal-chemistry))
* ACS Med Chem Lett ([https://pubs.acs.org/journal/amclct](https://pubs.acs.org/journal/amclct))
* MedChemComm ([http://www.rsc.org/journals-books-databases/about-journals/medchemcomm/](http://www.rsc.org/journals-books-databases/about-journals/medchemcomm/)).

However, we also have data from selected articles in more than 200 journals including Antimicrob Agents Chemother, Med Chem Res, J Agric Food Chem and Drug Metab Dispos. ChEMBL currently contains data from more than 86,000 journal articles, and we also now include data from selected patents.

### How can I be informed of updates in ChEMBL?

You can sign up to our ChEMBL Announce mailing list ([http://listserver.ebi.ac.uk/mailman/listinfo/chembl-announce](http://listserver.ebi.ac.uk/mailman/listinfo/chembl-announce)), where you will be kept up to date with all new releases and changes to the database.

### Do you show which compounds and/or bioactivity data has been changed or deleted with each release of ChEMBL?

As the data and the compounds are continually being curated, it is not possible to keep a track of these alterations or additions. The CHEMBL\_ID\_LOOKUP table stores a list of all active and inactive (obsolete) entities under the status field: ACTIVE OBS.  It is also possible to download previous releases and identify changes through a comparison of the data.&#x20;

If you need help, please [contact us](general-questions.md#how-do-i-report-errors-or-make-suggestions-for-the-interface) and we will be able to let you know what, if anything, has happened to the data you are interested in.

## The publications used to cite ChEMBL are:

**ChEMBL Database:**

Mendez D, Gaulton A, Bento AP, Chambers J, De Veij M, Félix E, Magariños MP, Mosquera JF, Mutowo P, Nowotka M, Gordillo-Marañón M, Hunter F, Junco L, Mugumbate G, Rodriguez-Lopez M, Atkinson F, Bosc N, Radoux CJ, Segura-Cabrera A, Hersey A, Leach AR. (2019) 'ChEMBL: towards direct deposition of bioassay data.' Nucleic Acids Res., 47(D1) D930-D940.

DOI: [10.1093/nar/gky1075](https://doi.org/10.1093/nar/gky1075) PMC: [PMC6323927](https://europepmc.org/article/MED/30398643)

**ChEMBL Web Services:**

Davies M, Nowotka M, Papadatos G, Dedman N, Gaulton A, Atkinson F, Bellis L, Overington JP. (2015) 'ChEMBL web services: streamlining access to drug discovery data and utilities.' Nucleic Acids Res., 43(W1) W612-W620.

DOI: [10.1093/nar/gkv352](http://dx.doi.org/10.1093/nar/gkv352) PMC: [PMC4489243](http://europepmc.org/articles/PMC4489243)

**ChEMBL RDF:**

S. Jupp, J. Malone, J. Bolleman, M. Brandizi, M. Davies, L. Garcia, A. Gaulton, S. Gehant, C. Laibe, N. Redaschi, S.M Wimalaratne, M. Martin, N. Le Novère, H. Parkinson, E. Birney and A.M Jenkinson (2014) The EBI RDF Platform: Linked Open Data for the Life Sciences Bioinformatics 30 1338-1339

DOI: [10.1093/bioinformatics/btt765](http://dx.doi.org/10.1093/bioinformatics/btt765) PMID: [24413672](http://europepmc.org/abstract/MED/24413672)

### How do I report errors or make suggestions for the interface?

1. We have a dedicated email address for data queries, error reporting or help requests. This is: [chembl-help@ebi.ac.uk](mailto:chembl-help@ebi.ac.uk)
2. You can [create an issue](https://github.com/chembl/GLaDOS/issues/new) in our [GitHub Repository](https://github.com/chembl/GLaDOS) to report issues with the interface only.

### What is the difference between Molregno and ChEMBLID?

Molregno is our ChEMBL internal identification given to each compound. The ChEMBLID is the externally viewed identification for each compound.

### What is the best way to access large amounts of data in ChEMBL?

The best way to access large amounts of data is to install a database instance on your own computer using MySQL.

### Is there a ChEMBL RDF?

Yes, there is a ChEMBL RDF. It is stored on the FTP site.

### Why do Assays and Documents both have ChEMBLIDs?

ChEMBLIDs are assigned to targets, assays, documents, tissues, cell types and compounds in ChEMBL and they are used as the unique identifiers for each.

### What is the difference between the different releases of ChEMBL, e.g. ChEMBL\_14 and ChEMBL\_15?

ChEMBL\_14 is an earlier release of the data, with ChEMBL\_15 being an updated version. Subsequent updates will have consecutive numbers, so the one with the highest number will be the most recent full version of the data.

### What is the difference between ChEMBL and ChEMBL-NTD?

[ChEMBL](https://www.ebi.ac.uk/chembl/beta/) is a database of bioactive drug-like small molecules, it contains 2-D structures, calculated properties (e.g. logP, Molecular Weight, Lipinski Parameters, etc.) and abstracted bioactivities (e.g. binding constants, pharmacology and ADMET data). We attempt to normalise the bioactivities into a uniform set of end-points and units where possible, and also to tag the links between a molecular target and a published assay with a set of varying confidence levels. The data is abstracted and curated from the primary scientific literature, and cover a significant fraction of the SAR and discovery of modern drugs.

[ChEMBL-NTD](https://chembl.gitbook.io/chembl-ntd/) is a repository for Open Access primary screening and medicinal chemistry data directed at neglected diseases - endemic tropical diseases of the developing regions of the Africa, Asia, and the Americas. The primary purpose of ChEMBL-NTD is to provide a freely accessible and permanent archive and distribution centre for deposited data. ChEMBL-NTD is a subset of the data in the free medicinal chemistry and drug discovery database ChEMBLdb.

### Can you provide more details on how to detect potentially duplicated data?

We detect and flag duplicated activity entries and potential transcription errors in activity records that come from publications. The former are records with identical compound, target, activity, type and unit values that were most likely reported as citations of measurements from previous papers, even when these measurements were subsequently rounded. The latter cases consist of otherwise identical entries whose activity values differ by exactly 3 or 6 orders of magnitude indicating a likely error in the units (e.g. uM instead of nM).

### **Where can I find more details on the assay classification?**

More details can be found in this [Blog post](https://chembl.blogspot.com/2018/10/annotation-of-in-vivo-pharmacology.html).

### How do you use the Web Services?

Web Service documentation and example queries can be found at: [https://www.ebi.ac.uk/chembl/ws](https://www.ebi.ac.uk/chembl/ws)

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

## Useful Links

Links to webinar slides and PDFs:

* [ChEMBL Interface and Searching Walkthrough](https://www.ebi.ac.uk/training/events/exploring-chembl-data-new-chembl-interface-0/)
* [UniChem Walkthrough](https://www.ebi.ac.uk/training/online/courses/unichem-quick-tour/)
* [Web Services Overview](https://www.ebi.ac.uk/training/online/course/embl-ebi-programmatically-take-rest-manual-searches/chembl-programmatically)
