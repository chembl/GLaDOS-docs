# ChEMBL Data Questions

### How often do you update the data?

The data is updated regularly, with releases approximately every 3-4 months.

### Can you provide of list of all changes and additions you've made since the last release?

We provide a list of all downgraded compounds with each release. However, it would be impossible to note all structural changes and/or changes to compound names etc. If there is something specific that you need to check, please contact us and we will be able to let you know what, if anything, has happened to that compound.

### Are my queries stored and if so, are they routinely deleted?

We do not analyse the nature of any queries or note structures that are processed through the website. However, to implement the link shortening functionality we store the queries and relate them to a hash. This in an example of a shortened url: https://www.ebi.ac.uk/chembl/beta/chembl/beta/g/tiny/GvKCBuljiVr/s1XL8m6Duw==. In our elasticsearch servers, we have a mapping of GvKCBuljiVr/s1XL8m6Duw== to the original query, but nothing else is stored. There is not other data that can identify the user(s) who used that query.

We use https:// wherever possible to maintain the security of the searches. Additionally, the EBI has terms of use and these can be found at: http://www.ebi.ac.uk/Information/termsofuse.html. This will tell you what information is retained by the EBI, if any.


### Why are there so many different types of Standard Units in the database?

The published units are taken directly from the literature and we then attempt to standardise these to report as a standard type. This is an ongoing curation task, which was started with the most common units first.

### What is the 'Confidence Score'?

As part of the manual curation process applied to the data we assign a confidence score to the assay-to-target relationships represented in the database. The confidence score value reflects both the type of target assigned to a particular assay and the confidence that the target assigned is the correct target for that assay. The confidence scores range from 0, for as yet uncurated data entries, to 9, where a single protein target has been assigned a high degree of confidence. Assays assigned a non-molecular target type, for example a cell-line or an organism, receive a confidence score of 1, while assays with assigned protein targets receive a confidence score of at least 4. 

| CONFIDENCE_SCORE | DESCRIPTION |
| --- | --- |
| 0	| 	Default value - Target assignment has yet to be curated |
| 1	|		Target assigned is non-molecular |
| 3	|		Target assigned is molecular non-protein target |
| 4	|		Multiple homologous protein targets may be assigned |
| 5	|		Multiple direct protein targets may be assigned |
| 6	|		Homologous protein complex subunits assigned |
| 7	|	Direct protein complex subunits assigned |
| 8	|	Homologous single protein target assigned |
| 9	|		Direct single protein target assigned |

### Do you show which compounds and/or bioactivity data has been changed or deleted with each release of ChEMBL?

As the data and the compounds are continually being curated, it is not possible to keep a track of these alterations or additions. However, if our users contact us personally, we are always happy to try and give them this type of information on individual data or compounds, wherever possible.


### Is there a list of all the Activity Types in ChEMBL?

No, we do not keep a list of activity types but we are happy to create such a list as and when a user would require it. This can also be found if the ChEMBL data is downloaded from the FTP site and installed into a database.

### What literature coverage is there in ChEMBL?

Data are routinely extracted from seven core journals: 

  - Bioorg Med Chem Lett (https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry-letters)
  - J Med Chem (https://pubs.acs.org/journal/jmcmar)
  - Bioorg Med Chem (https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry)
  - J Nat Prod (https://pubs.acs.org/journal/jnprdf)
  - Eur J Med Chem (https://www.sciencedirect.com/journal/european-journal-of-medicinal-chemistry)
  - ACS Med Chem Lett (https://pubs.acs.org/journal/amclct)
  - MedChemComm (http://www.rsc.org/journals-books-databases/about-journals/medchemcomm/).

However, we also have data from selected articles in more than 200 journals including Antimicrob Agents Chemother, Med Chem Res and Drug Metab Dispos. ChEMBL currently contains data from more than 65,000 journal articles, and we also now include data from selected patents.

### How are the SMILES and InChI created for ChEMBL?

The canonical SMILES are calculated using Accelrys's Pipeline Pilot using an algorithm that belongs to Accelrys but it was derived from Daylight's algorithm (http://www.daylight.com/dayhtml/doc/theory/theory.smiles.html). The standard InChI is calculated using the command line InChI generator and was developed by the InChI Trust (http://www.inchi-trust.org/inchi/) and is executed via the command line. The version of InChI used in ChEMBL is 1.05

### How is the LogP calculated?

The LogP, and other compound properties are calculated according to the following document: [Property_Definitions](https://www.dropbox.com/s/mixm4cn5x7azmg4/property_definitions.docx?dl=0). Please note, we are now using RDKit to calculate many of these properties.

### How can I be informed of updates in ChEMBL?

You can sign up to our ChEMBL Announce mailing list (http://listserver.ebi.ac.uk/mailman/listinfo/chembl-announce), where you will be kept up to date with all new releases and changes to the database.
