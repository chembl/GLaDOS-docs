# Assay and Activity Questions

### What is the Assay Type?

* Binding (B) - Data measuring binding of compound to a molecular target, e.g. Ki, IC50, Kd.
* Functional (F) - Data measuring the biological effect of a compound, e.g. %cell death in a cell line, rat weight.
* ADMET (A) - ADME data e.g. t1/2, oral bioavailability.
* Toxicity (T) - Data measuring toxicity of a compound, e.g., cytotoxicity.
* Physicochemical (P) - Assays measuring physicochemical properties of the compounds in the absence of biological material e.g., chemical stability, solubility.
* Unclassified (U) - A small proportion of assays cannot be classified into one of the above categories e.g., ratio of binding vs efficacy.

Assays are classified into the types above. However, some assays may fit into multiple categories although only a single assay type is assigned.

### Why are there so many different types of Standard Units in the database?

The published units are taken directly from the literature and we then attempt to standardise these to report as a standard type. This is an ongoing curation task, which was started with the most common units first.

### What is the 'Confidence Score'?

As part of the manual curation process applied to the data we assign a confidence score to the assay-to-target relationships represented in the database. The confidence score value reflects both the type of target assigned to a particular assay and the confidence that the target assigned is the correct target for that assay. The confidence scores range from 0, for as yet uncurated data entries, to 9, where a single protein target has been assigned a high degree of confidence. Assays assigned a non-molecular target type, for example a cell-line or an organism, receive a confidence score of 1, while assays with assigned protein targets receive a confidence score of at least 4. If the correct target was unavailable during initial mapping then sometimes assays have been mapped to a homologue from a difference species (with lower confidence i.e. 8). A confidence score of 8 is also assigned when mapping an assay where the source of the target protein is undefined/unknown.&#x20;

<table data-header-hidden><thead><tr><th width="238">CONFIDENCE_SCORE</th><th>DESCRIPTION</th></tr></thead><tbody><tr><td>CONFIDENCE_SCORE</td><td>DESCRIPTION</td></tr><tr><td>0</td><td>Default value - Target assignment has yet to be curated</td></tr><tr><td>1</td><td>Target assigned is non-molecular</td></tr><tr><td>3</td><td>Target assigned is molecular non-protein target</td></tr><tr><td>4</td><td>Multiple homologous protein targets may be assigned</td></tr><tr><td>5</td><td>Multiple direct protein targets may be assigned</td></tr><tr><td>6</td><td>Homologous protein complex subunits assigned</td></tr><tr><td>7</td><td>Direct protein complex subunits assigned</td></tr><tr><td>8</td><td>Homologous single protein target assigned</td></tr><tr><td>9</td><td>Direct single protein target assigned</td></tr></tbody></table>

### Is there a list of all the Activity Types in ChEMBL?&#x20;

No, we do not keep a list of activity or target types but we are happy to create such a list as and when a user would require it.&#x20;

This information can also be found if the ChEMBL data is downloaded from the FTP site and installed into a database. Also, you can browse all the activities in ChEMBL by visiting this url: [https://www.ebi.ac.uk/chembl/beta/g/#browse/activities](https://www.ebi.ac.uk/chembl/beta/g/#browse/activities)

You can see the distribution of the activities by type in the filters on the left.

Many aspects of ChEMBL data can be explored using the ChEMBL web services API live documentation Explorer:

[https://www.ebi.ac.uk/chembl/api/data/docs](https://www.ebi.ac.uk/chembl/api/data/docs)&#x20;

### Which sub-set of the PubChem Bioassay data has been integrated into ChEMBL?

In PubChem, depositors may assign multiple result types to an assay. However, if an assay is deposited as a 'confirmatory' assay (defined as an assay where a range of SID concentrations have been tested, with a view to determining a measurement of potency), then one of the result types must be marked up as an 'Active Concentration' (AC) result type.&#x20;

Panel assays may contain many 'AC' result types, one per panel member. The AC result type is the calculated potency measurement from the data, and is typically an IC50, EC50, AC50, GI50 or Ki. In addition, the PubChem deposition process requires that each SID in an assay must be assigned a single 'Activity Summary', from a controlled vocabulary which includes 'inactive', 'active' and 'inconclusive'. Only assays containing 'AC' result types have been integrated into ChEMBL, and from these assays, only activity data and SIDs associated with 'AC' result types have been integrated.&#x20;

The 'Activity Summary' field in PubChem associated with each integrated activity is also captured and shown in the 'Activity Comment' field in ChEMBL. Panel assays are divided into separate assays in ChEMBL, one ChEMBL assay for each panel member. A number of additional assays which do not match the above criteria, have also been included in the PubChem integration. These have been chosen individually, on the basis that they have been specifically requested to be included by ChEMBL users. These are:&#x20;

AID1, AID3, AID5, AID7, AID9, AID11, AID13, AID15, AID17, AID19, AID21, AID23, AID25, AID27, AID29, AID31, AID33, AID35, AID37, AID39, AID41, AID43, AID45, AID47, AID49, AID51, AID53, AID55, AID57, AID59, AID61, AID63, AID65, AID67, AID69, AID71, AID73, AID75, AID77, AID79, AID81, AID83, AID85, AID87, AID89, AID91, AID93, AID95, AID97, AID99, AID101, AID103, AID105, AID107, AID109, AID111, AID113, AID115, AID117, AID119, AID121, AID123, AID125, AID127, AID129, AID131, AID133, AID135, AID137, AID139, AID141, AID143, AID145, AID1851 and AID493040.&#x20;

A number of assays have been excluded since they contain data already present in ChEMBL. These assays include all ChEMBL-derived assays, and AID1433 (A data set that has been manually added to ChEMBL).&#x20;

An automatic 'standardization' of SID structures downloaded from PubChem is carried out prior to integration (using in house protocols). Standard InChIs are generated from the standardized mol files, and used to normalize with existing ChEMBL structures. SIDs matching exactly on standard InChIs to existing ChEMBL structures are assigned to the existing ChEMBL\_ID (and the mol file already associated with the existing ChEMBL structure is used to represent the searchable structure for this ChEMBL\_ID). Where no match to a standard InChI is achieved, the incoming SID is assigned to a new ChEMBL\_ID, and the standardized mol file for the SID is used to represent the searchable structure.&#x20;

A very small number of SIDs (<0.1%) with standardized mol files that fail to produce valid standard InChIs, or to load into a oracle symyx cartridge without errors, are each assigned a new ChEMBL\_ID, and associated with a 'null' structure (ie: no mol file is associated with this new ChEMBL\_ID).&#x20;

Mappings to ChEMBL targets for each integrated PubChem assay has been automated for the initial load.  However, manual review of these mappings by expert curators may result in ongoing changes.&#x20;

Users who prefer to exclude the integrated PubChem data (or any other integrated external data set) from their ChEMBL web-interface searches can do so by clicking 'Activity Source Filter' next to the main ChEMBL search bar, and deselecting the sources not required in future searches. Note, however, that these deselections persist between browser sessions. Users querying ChEMBL database dumps directly using SQL, and wishing to achieve this same filtering, should inspect the 'source' table, and the foreign keys to this table in the 'assays' and 'compound\_records' tables.

### What is pChEMBL?

In addition to the conversion of published activity types/values/units to standard activity types/values/units, we have now added an additional field called pChEMBL to the Activities table. This value allows a number of roughly comparable measures of half-maximal response concentration/potency/affinity to be compared on a negative logarithmic scale. For example, an IC50 measurement of 1nM would have a pChEMBL value of 9. pChEMBL is defined as: -Log(molar IC50, XC50, EC50, AC50, Ki, Kd or Potency).

**A pChEMBL value is calculated for the following activity data:**&#x20;

"standard\_type" must be one of the following: "IC50", "XC50", "EC50", "AC50", "Ki", "Kd", "Potency", "ED50";&#x20;

"standard\_relation" == "=" & "standard\_units" == "nM";&#x20;

"standard\_value" > 0 & "data\_validity\_comment"].isnull()) | "data\_validity\_comment" == "Manually validated“

### What is the Data Validity column?

The Data Validity column has been added to the interface and to the database (in the ACTIVITIES table as column data\_validity\_comment) to flag activity values that are outside a range typical for that activity type, or even for potentially missing data. For example, an IC50 of 23000000nM would be flagged as Outside Typical Range. The use of the flag will allow users to decide whether or not to retain those values in their results set after running a search on the interface or using the downloaded database. The flags currently in use in this field are:

* Potential missing data
* Potential author error
* Manually validated
* Potential transcription error
* Outside typical range
* Non standard unit for type
* Author confirmed error

More details on Data Checks can be found in this [Blog](http://chembl.blogspot.com/2020/10/data-checks.html) post.

### Can you provide more details on bioactivity data standardisation?

In addition to the conversion of published activity types/values/units to standard activity types/values/units, described in previous releases, a number of further enhancements have been made to the data in the activities table:

1. Conversion of log/-log values to nM concentrations. For example pIC50 and log Ki have been converted to IC50 and Ki values.
2. Rounding of standard values to three significant figures (or 2 decimal places for values > 10)
3. Flagging of data with possible errors (using the data\_validity\_comment field), such as unusual units for the activity type, or very large/small numbers.
4. Identification of potential duplicate values - where an activity measurement is likely to be a repeat citation of an earlier measurement, rather than an independent measurement (flagged using the potential\_duplicate column).

An additional table (ACTIVITY\_STDS\_LOOKUP) has been included in this release, which contains details of the standard\_types that have been standardised, their permitted standard\_units, and acceptable value ranges.

### **Can you provide more details on the activity comments?**

Activity comments may provide the overall activity conclusions from the data depositor (e.g. toxic, non-toxic, active, inactive) after taking into account other factors such as counter screens. This can explain cases where compounds with apparently potent activities are flagged as inactive/inconclusive. For details on the criteria used to generate the activity conclusions, please refer to the original assay source.\
\
Numerical values in the activity comments field are typically Binding DB identifiers that can be used to link the two databases.

More details can be found in this [Blog](http://chembl.blogspot.com/2020/08/using-chembl-activity-comments.html) post.

### **Where can I find more details on the assay classification?**

More details can be found in this [Blog post](https://chembl.blogspot.com/2018/10/annotation-of-in-vivo-pharmacology.html).

### Can you provide more details on how to detect potentially duplicated data?

We detect and flag duplicated activity entries and potential transcription errors in activity records that come from publications. The former are records with identical compound, target, activity, type and unit values that were most likely reported as citations of measurements from previous papers, even when these measurements were subsequently rounded. The latter cases consist of otherwise identical entries whose activity values differ by exactly 3 or 6 orders of magnitude indicating a likely error in the units (e.g. uM instead of nM).

You can find some details on Data Checks in this [Blog](http://chembl.blogspot.com/2020/10/data-checks.html) post.
