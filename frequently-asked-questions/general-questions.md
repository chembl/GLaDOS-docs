# General Questions

### How often do you update the data?

The data is updated regularly, with releases approximately 2-3 times a year.

### What is the ChEMBLID and why do both Assays and Documents have ChEMBLIDs?

The ChEMBLID is a unique ID that has been assigned to compounds, targets, assays, documents, tissues and cell types in ChEMBL. It can be used to retrieve a Report Card page for these entities, or to search for them using the keyword search.

### What is the difference between Molregno and ChEMBLID?

Molregno is our ChEMBL internal identification given to each compound. The ChEMBLID is the externally viewed identification for each compound.

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
2. You can [create an issue](https://github.com/chembl/GLaDOS/issues/new) in our [GitHub Interface Repository](https://github.com/chembl/GLaDOS) to report issues with the **interface only**.
3. You can [create an issue](https://github.com/chembl/chembl\_data\_issues/issues/new) in our [GitHub Data Repository](https://github.com/chembl/chembl\_data\_issues) to report issues with the **data only**.
4. You can [create an issue](https://github.com/chembl/chembl\_webservices\_2/issues/new) in our [GitHub API Repository](https://github.com/chembl/chembl\_webservices\_2) to report issues with the **ChEMBL API.**
5. You can [create an issue](https://github.com/chembl/chembl\_webresource\_client/issues/new) in our [GitHub Python Client Repository](https://github.com/chembl/chembl\_webservices\_2) to report issues with the **Python client library.**



### What is the best way to access large amounts of data in ChEMBL?

The best way to access large amounts of data is to install a database instance on your own computer using MySQL.

### Is there a ChEMBL RDF?

Yes, there is a ChEMBL RDF. It is stored on the FTP site.

### What is the difference between the different releases of ChEMBL, e.g. ChEMBL\_14 and ChEMBL\_15?

ChEMBL\_14 is an earlier release of the data, with ChEMBL\_15 being an updated version. Subsequent updates will have consecutive numbers, so the one with the highest number will be the most recent full version of the data.

### What is the difference between ChEMBL and ChEMBL-NTD?

[ChEMBL](https://www.ebi.ac.uk/chembl/beta/) is a database of bioactive drug-like small molecules, it contains 2-D structures, calculated properties (e.g. logP, Molecular Weight, Lipinski Parameters, etc.) and abstracted bioactivities (e.g. binding constants, pharmacology and ADMET data). We attempt to normalise the bioactivities into a uniform set of end-points and units where possible, and also to tag the links between a molecular target and a published assay with a set of varying confidence levels. The data is abstracted and curated from the primary scientific literature, and cover a significant fraction of the SAR and discovery of modern drugs.

[ChEMBL-NTD](https://chembl.gitbook.io/chembl-ntd/) is a repository for Open Access primary screening and medicinal chemistry data directed at neglected diseases - endemic tropical diseases of the developing regions of the Africa, Asia, and the Americas. The primary purpose of ChEMBL-NTD is to provide a freely accessible and permanent archive and distribution centre for deposited data. ChEMBL-NTD is a subset of the data in the free medicinal chemistry and drug discovery database ChEMBLdb.

### How do you use the Web Services?

Web Service documentation and example queries can be found at: [https://www.ebi.ac.uk/chembl/ws](https://www.ebi.ac.uk/chembl/ws)

### Can I purchase compounds from ChEMBL?

ChEMBL is a database of bioactivity data and we do not supply compounds.

However, you can use the cross-references on the compound report cards to view commercial chemical providers.

### Can you provide more details on licensing?

The ChEMBL database is licensed under a Creative Commons Attribution-Share Alike 3.0 Unported License ([https://creativecommons.org/licenses/by-sa/3.0/](https://creativecommons.org/licenses/by-sa/3.0/)). This allows use, redistribution and adaption of ChEMBL as long as appropriate attribution is given (e.g., cite the current [ChEMBL paper:](https://europepmc.org/article/MED/30398643)) and ensure that any adaptations are redistributed under the same license.

### Can you provide more details on ChEMBL releases?

Each new ChEMBL release includes literature data from the previous 12-18 months. The precise cutoff point for extraction of literature data varies slightly between ChEMBL releases and for different journals. Occasionally, selected articles are added to ChEMBL at a later date, therefore the ChEMBL version and publication dates are not always associated. A new release may also contain new data for existing compounds.

ChEMBL provide periodic updates to the database that include new data, corrections, additional curation and new features. Subsequent updates will have consecutive numbers, so the version with the highest number will be the most recent full version of the data. Version information is found in the VERSION table.

The API and interface will always reflect the data in the current release and can not currently be used to extract data from previous versions. However, old data dumps remain available for download and can be queried using a database tool and the SQL language to obtain version-specific data.

### What type of data does ChEMBL accept in depositions and how can I deposit data?

ChEMBL is a database of bioactivity data for drug-like compounds and includes data from seven core medicinal chemistry journals, patents and deposited data that fits within the scope of ChEMBL. Deposited data is primarily dose-response and ADMET type data. Please get in touch if you believe your data could be included in ChEMBL.

For regular depositors, you can sign up to the chembl\_depositor mailing list ([https://listserver.ebi.ac.uk/mailman/listinfo/chembl-depositors](https://listserver.ebi.ac.uk/mailman/listinfo/chembl-depositors)) to receive updates on ChEMBL deposition timelines.

Documentation for depositors can be found here - [https://chembl.gitbook.io/chembl-loader/](https://chembl.gitbook.io/chembl-loader/) where you can see the information required to submit to ChEMBL.

### How can I access ChEMBL through KNIME?

The ChEMBL KNIME nodes are no longer maintained but our recommendation is to use the generic KNIME REST nodes to access the ChEMBL web services, as this will be simpler to maintain and adapt to cope with schema changes etc. There are some example workflows available, using this approach, that have been provided by Daria Goldmann e.g.,\
\
[https://www.knime.com/blog/a-restful-way-to-find-and-retrieve-data](https://www.knime.com/blog/a-restful-way-to-find-and-retrieve-data)\
[https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/01\_ChEMBL\_REST\_Services\*qBCbzaFZ85qUMoWZ](https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/01\_ChEMBL\_REST\_Services\*qBCbzaFZ85qUMoWZ)\
[https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/02\_ChEMBL\_Structure\_Search\*wCygb7lTvPqnYXuB](https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/02\_ChEMBL\_Structure\_Search\*wCygb7lTvPqnYXuB)\
[https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/03\_ChEMBL\_Bioactivity\_Search\*tGSG1nPdGg4cW7Qp](https://hub.knime.com/knime/workflows/Examples/50\_Applications/30\_RESTful\_ChEMBL/03\_ChEMBL\_Bioactivity\_Search\*tGSG1nPdGg4cW7Qp)
