# ChEMBL Data Web Services

## Getting Started

To best way to get started is to have a look at some example URLs requesting data from the ChEMBL web services. The table below provides a list of examples and a description of the data being returned.

| Description | Example URL |
| :--- | :--- |
| Return all molecules | [https://www.ebi.ac.uk/chembl/api/data/molecule](https://www.ebi.ac.uk/chembl/api/data/molecule) |
| Keyword search for targets that contain 'cyclin' in pref\_name | [https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_contains=cyclin](https://www.ebi.ac.uk/chembl/api/data/target?pref_name__contains=cyclin) |
| Return molecules with molecular weight &lt;= 300 | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_mw\_freebase\_\_lte=300](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__mw_freebase__lte=300) |
| Return molecules with molecular weight &lt;= 300 AND pref\_name ends with nib | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_mw\_freebase\_\_lte=300&pref\_name\_\_iendswith=nib](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__mw_freebase__lte=300&pref_name__iendswith=nib) |
| Return image for CHEMBL25 | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25) |
| Substructure search with SMILES CC\(=O\)Oc1ccccc1C\(=O\)O \(Aspirin\) | [https://www.ebi.ac.uk/chembl/api/data/substructure/CC\(=O\)Oc1ccccc1C\(=O\)O](https://www.ebi.ac.uk/chembl/api/data/substructure/CC%28=O%29Oc1ccccc1C%28=O%29O) |
| Similarity search with SMILES CN1C\(=O\)C=C\(c2cccc\(Cl\)c2\)c3cc\(ccc13\)\[C@@\]\(N\)\(c4ccc\(Cl\)cc4\)c5cncn5C with 80% tanimoto similarity cut off | [https://www.ebi.ac.uk/chembl/api/data/similarity/CN1C\(=O\)C=C\(c2cccc\(Cl\)c2\)c3cc\(ccc13\)\[C@@\]\(N\)\(c4ccc\(Cl\)cc4\)c5cncn5C/80](https://www.ebi.ac.uk/chembl/api/data/similarity/CN1C%28=O%29C=C%28c2cccc%28Cl%29c2%29c3cc%28ccc13%29[C@@]%28N%29%28c4ccc%28Cl%29cc4%29c5cncn5C/80) |

## Resources

The following table provides a list of all ChEMBL web service resources currently available.  


| Resource Name | Description | URL |
| :--- | :--- | :--- |
| Activity | Activity values recorded in an Assay | [https://www.ebi.ac.uk/chembl/api/data/activity](https://www.ebi.ac.uk/chembl/api/data/activity) |
| Assay | Assay details as reported in source Document/Dataset | [https://www.ebi.ac.uk/chembl/api/data/assay](https://www.ebi.ac.uk/chembl/api/data/assay) |
| ATC | WHO ATC Classification for drugs | [https://www.ebi.ac.uk/chembl/api/data/atc\_class](https://www.ebi.ac.uk/chembl/api/data/atc_class) |
| Binding Site | Target binding site definition | [https://www.ebi.ac.uk/chembl/api/data/binding\_site](https://www.ebi.ac.uk/chembl/api/data/binding_site) |
| Biotherapeutic | Biotherapeutic molecules, which includes HELM notation and sequence data | [https://www.ebi.ac.uk/chembl/api/data/biotherapeutic](https://www.ebi.ac.uk/chembl/api/data/biotherapeutic) |
| Cell Line | Cell line information | [https://www.ebi.ac.uk/chembl/api/data/cell\_line](https://www.ebi.ac.uk/chembl/api/data/cell_line) |
| ChEMBL ID Lookup | Look up ChEMBL Id entity type | [https://www.ebi.ac.uk/chembl/api/data/chembl\_id\_lookup](https://www.ebi.ac.uk/chembl/api/data/chembl_id_lookup) |
| Compound Record | Occurence of a given compound in a spcecific document | [https://www.ebi.ac.uk/chembl/api/data/compound\_record](https://www.ebi.ac.uk/chembl/api/data/compound_record) |
| Compound Structural Alert | Indicates certain anomaly in compound structure | [https://www.ebi.ac.uk/chembl/api/data/compound\_structural\_alert](https://www.ebi.ac.uk/chembl/api/data/compound_structural_alert) |
| Document | Document/Dataset from which Assays have been extracted | [https://www.ebi.ac.uk/chembl/api/data/document](https://www.ebi.ac.uk/chembl/api/data/document) |
| Document Similarity | Provides documents similar to a given one | [https://www.ebi.ac.uk/chembl/api/data/document\_similarity](https://www.ebi.ac.uk/chembl/api/data/document_similarity) |
| Document Term | Provides keywords extracted from a document using the TextRank algorithm | [https://www.ebi.ac.uk/chembl/api/data/document\_term](https://www.ebi.ac.uk/chembl/api/data/document_term) |
| Drug | Approved drugs information, icluding \(but not limited to\) applicants, patent numbers and research codes | [https://www.ebi.ac.uk/chembl/api/data/drug](https://www.ebi.ac.uk/chembl/api/data/drug) |
| Drug Indication | Joins drugs with diseases providing references to relevant sources | [https://www.ebi.ac.uk/chembl/api/data/drug\_indication](https://www.ebi.ac.uk/chembl/api/data/drug_indication) |
| GO Slim | GO slim ontology | [https://www.ebi.ac.uk/chembl/api/data/go\_slim](https://www.ebi.ac.uk/chembl/api/data/go_slim) |
| Image | Graphical \(png, svg, json\) representation of Molecule | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL1](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL1) |
| Mechanism | Mechanism of action information for FDA-approved drugs | [https://www.ebi.ac.uk/chembl/api/data/mechanism](https://www.ebi.ac.uk/chembl/api/data/mechanism) |
| Metabolism | Metabolic pathways with references | [https://www.ebi.ac.uk/chembl/api/data/metabolism](https://www.ebi.ac.uk/chembl/api/data/metabolism) |
| Molecule | Molecule information, including properties, structural representations and synonyms | [https://www.ebi.ac.uk/chembl/api/data/molecule](https://www.ebi.ac.uk/chembl/api/data/molecule) |
| Molecule Form | Relationships between molecule parents and salts | [https://www.ebi.ac.uk/chembl/api/data/molecule\_form](https://www.ebi.ac.uk/chembl/api/data/molecule_form) |
| Protein Classification | Protein family classification of TargetComponents | [https://www.ebi.ac.uk/chembl/api/data/protein\_class](https://www.ebi.ac.uk/chembl/api/data/protein_class) |
| Substructure | Molecule substructure search | [https://www.ebi.ac.uk/chembl/api/data/substructure/CN%28CCCN%29c1cccc2ccccc12](https://www.ebi.ac.uk/chembl/api/data/substructure/CN%28CCCN%29c1cccc2ccccc12) |
| Similarity | Molecule similarity search | [https://www.ebi.ac.uk/chembl/api/data/similarity/CC%28=O%29Oc1ccccc1C%28=O%29O/70](https://www.ebi.ac.uk/chembl/api/data/similarity/CC%28=O%29Oc1ccccc1C%28=O%29O/70) |
| Source | Document/Dataset source | [https://www.ebi.ac.uk/chembl/api/data/source](https://www.ebi.ac.uk/chembl/api/data/source) |
| Status | API status with chembl DB version number and API software version number | [https://www.ebi.ac.uk/chembl/api/data/status](https://www.ebi.ac.uk/chembl/api/data/status) |
| Target | Targets \(protein and non-protein\) defined in Assay | [https://www.ebi.ac.uk/chembl/api/data/target](https://www.ebi.ac.uk/chembl/api/data/target) |
| Target Component | Target sequence information \(A Target may have 1 or more sequences\) | [https://www.ebi.ac.uk/chembl/api/data/target\_component](https://www.ebi.ac.uk/chembl/api/data/target_component) |
| Target Prediction | Predictied binding of a molecule to a given biological target | [https://www.ebi.ac.uk/chembl/api/data/target\_prediction](https://www.ebi.ac.uk/chembl/api/data/target_prediction) |
| Target Relation | Describes relations between targets | [https://www.ebi.ac.uk/chembl/api/data/target\_relation](https://www.ebi.ac.uk/chembl/api/data/target_relation) |
| Tissue | Tissue classification | [https://www.ebi.ac.uk/chembl/api/data/tissue](https://www.ebi.ac.uk/chembl/api/data/tissue) |

## Supported formats

These are formats currently supported by the API:

| Format Name | Example URL | Comments |
| :--- | :--- | :--- |
| XML | [https://www.ebi.ac.uk/chembl/api/data/assay.xml](https://www.ebi.ac.uk/chembl/api/data/assay.xml) [https://www.ebi.ac.uk/chembl/api/data/assay?format=xml](https://www.ebi.ac.uk/chembl/api/data/assay?format=xml) [https://www.ebi.ac.uk/chembl/api/data/assay](https://www.ebi.ac.uk/chembl/api/data/assay) | If format is not specified it defaults to XML. |
| JSON | [https://www.ebi.ac.uk/chembl/api/data/molecule.json](https://www.ebi.ac.uk/chembl/api/data/molecule.json) [https://www.ebi.ac.uk/chembl/api/data/molecule?format=json](https://www.ebi.ac.uk/chembl/api/data/molecule?format=json) |  |
| YAML | [https://wwwdev.ebi.ac.uk/chembl/api/data/document.yaml](https://wwwdev.ebi.ac.uk/chembl/api/data/document.yaml) [https://wwwdev.ebi.ac.uk/chembl/api/data/document?format=yaml](https://wwwdev.ebi.ac.uk/chembl/api/data/document?format=yaml) |  |
| PNG | [https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.png](https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.png) [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25.png](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25.png) [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=png](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=png) [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25) | Only compound images, default image format |
| SVG | [https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.svg](https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.svg) [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25.svg](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25.svg) [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=svg](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=svg) | Only compound images |
| FPS |  | as a result of sdf2fps method |
| SDF | [https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.sdf](%20https://www.ebi.ac.uk/chembl/api/data/molecule/CHEMBL25.sdf) | Only compounds |

## Meta Data and Pagination

It is now possible to download all data from a specific ChEMBL web service resource. This is made possible by returning responses from the web services in 'pages', which can be navigated through using a **'page\_meta'** section. The **'page\_meta'** section includes information about total number of hits, total number of pages and links to the next and previous pages. An example 'page\_meta' section is displayed below:

```javascript
"page_meta": {

    "limit": 20,
    "next": "/chembl/api/data/activity.json?limit=20&offset=20",
    "offset": 0,
    "previous": null,
    "total_count": 13520737

}
```

To download all ChEMBL activity endpoints \(&gt;13 million\), the following URL can be used: [https://www.ebi.ac.uk/chembl/api/data/activity](https://www.ebi.ac.uk/chembl/api/data/activity). By inspecting the the 'page\_meta' section the link to page 2 can be found, e.g. [https://www.ebi.ac.uk/chembl/api/data/activity?limit=20&offset=20](https://www.ebi.ac.uk/chembl/api/data/activity?limit=20&offset=20).

## Filtering and Ordering

It is possible to apply search filters to all resource requests using a URL friendly query language. For example, it is possible to return all ChEMBL targets that contain the term 'kinase' in the pref\_name attribute with the following URL: [https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_contains=kinase](https://www.ebi.ac.uk/chembl/api/data/target?pref_name__contains=kinase).

The pattern for applying a filter is as follows:

```text
https://www.ebi.ac.uk/chembl/api/data/[resource]?[field]__[filter_type]=[value]
```

Examples of other filter type are listed in the table below.  


| Filter Type | Description | Example URL |
| :--- | :--- | :--- |
| exact \(iexact\) | Exact match with query | [https://www.ebi.ac.uk/chembl/api/data/assay?assay\_type\_\_exact=B](https://www.ebi.ac.uk/chembl/api/data/assay?assay_type__exact=B) |
| contains \(icontains\) | Wild card search with query | [https://www.ebi.ac.uk/chembl/api/data/assay?description\_\_icontains=toxicity](https://www.ebi.ac.uk/chembl/api/data/assay?description__icontains=toxicity) |
| startswith \(istartswith\) | Starts with query | [https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_istartswith=serotonin](https://www.ebi.ac.uk/chembl/api/data/target?pref_name__istartswith=serotonin) |
| endswith \(iendswith\) | Ends with query | [https://www.ebi.ac.uk/chembl/api/data/cell\_line?cell\_source\_tissue\_\_iendswith=carcinoma](https://www.ebi.ac.uk/chembl/api/data/cell_line?cell_source_tissue__iendswith=carcinoma) |
| regex \(iregex\) | Regular expression query | [https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_iregex=\(cdk1\|cdk2\)](https://www.ebi.ac.uk/chembl/api/data/target?pref_name__iregex=%28cdk1%7Ccdk2%29) |
| gt \(gte\) | Greater than \(or equal\) | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_full\_mwt\_\_gte=100](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__full_mwt__gte=100) |
| lt \(lte\) | Less than \(or equal\) | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_alogp\_\_lte=5](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__alogp__lte=5) |
| range | Within a range of values | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_full\_mwt\_\_range=200,500](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__full_mwt__range=200,500) |
| in | Appears within list of query values | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_chembl\_id\_\_in=CHEMBL25,CHEMBL941,CHEMBL1000](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_chembl_id__in=CHEMBL25,CHEMBL941,CHEMBL1000) |
| isnull | Field is null | [https://www.ebi.ac.uk/chembl/api/data/molecule?helm\_notation\_\_isnull=false](https://www.ebi.ac.uk/chembl/api/data/molecule?helm_notation__isnull=false) |
| search | Special type of filter allowing a full text search based on Solr queries. | [https://www.ebi.ac.uk/chembl/api/data/molecule/search.json?q=aspirin](https://www.ebi.ac.uk/chembl/api/data/molecule/search.json?q=aspirin) [https://www.ebi.ac.uk/chembl/api/data/target/search.json?q=lipoxygenase](https://www.ebi.ac.uk/chembl/api/data/target/search.json?q=lipoxygenase) [https://www.ebi.ac.uk/chembl/api/data/chembl\_id\_lookup/search?q=morphine](https://www.ebi.ac.uk/chembl/api/data/chembl_id_lookup/search?q=morphine) [https://www.ebi.ac.uk/chembl/api/data/activity/search?q=%22TG-GATES%22](https://www.ebi.ac.uk/chembl/api/data/activity/search?q=%22TG-GATES%22)  |

To order the results returned by a particular field the 'order=\[field\]' argument as added to a request. For example a user can sort targets based on the pref\_name using the following URL: [https://www.ebi.ac.uk/chembl/api/data/target?order\_by=pref\_name](https://www.ebi.ac.uk/chembl/api/data/target?order_by=pref_name)

The default ordering is in ascending order. To return the results in descending orede place a '-' before the field name: [https://www.ebi.ac.uk/chembl/api/data/target?order\_by=-pref\_name](https://www.ebi.ac.uk/chembl/api/data/target?order_by=-pref_name)

Note that it is possible combine order\_by and filter arguments:[https://www.ebi.ac.uk/chembl/api/data/target?pref\_name\_\_contains=kinase&order\_by=-pref\_name](https://www.ebi.ac.uk/chembl/api/data/target?pref_name__contains=kinase&order_by=-pref_name)  


## Chemical Searching

The 'Substructure' and 'Similarity' web service resources allow for the chemical content of ChEMBL to be searched. Similar to the other resources, these search based resources except filtering, paging and ordering arguments. These methods accept SMILES, InChI Key and molecule ChEMBL\_ID as arguments and in the case of similarity searches an additional identity cut-off is needed. Some example molecule searches are provided in the table below.  


| Chemical Search Description | Example URL |
| :--- | :--- |
| Substructure search for against ChEMBL using aspirin SMILES string | [https://www.ebi.ac.uk/chembl/api/data/substructure/CC\(=O\)Oc1ccccc1C\(=O\)O](https://www.ebi.ac.uk/chembl/api/data/substructure/CC%28=O%29Oc1ccccc1C%28=O%29O) |
| Substructure search for against ChEMBL using aspirin CHEMBL\_ID | [https://www.ebi.ac.uk/chembl/api/data/substructure/CHEMBL25](https://www.ebi.ac.uk/chembl/api/data/substructure/CHEMBL25) |
| Substructure search for against ChEMBL using aspirin InChI Key | [https://www.ebi.ac.uk/chembl/api/data/substructure/BSYNRYMUTXBXSQ-UHFFFAOYSA-N](https://www.ebi.ac.uk/chembl/api/data/substructure/BSYNRYMUTXBXSQ-UHFFFAOYSA-N) |
| Similarity \(80% cut off\) search for against ChEMBL using aspirin SMILES string | [https://www.ebi.ac.uk/chembl/api/data/similarity/CC\(=O\)Oc1ccccc1C\(=O\)O/80](https://www.ebi.ac.uk/chembl/api/data/similarity/CC%28=O%29Oc1ccccc1C%28=O%29O/80) |
| Similarity \(80% cut off\) search for against ChEMBL using aspirin CHEMBL\_ID | [https://www.ebi.ac.uk/chembl/api/data/similarity/CHEMBL25/80](https://www.ebi.ac.uk/chembl/api/data/similarity/CHEMBL25/80) |
| Similarity \(80% cut off\) search for against ChEMBL using aspirin InChI Key | [https://www.ebi.ac.uk/chembl/api/data/similarity/BSYNRYMUTXBXSQ-UHFFFAOYSA-N/80](https://www.ebi.ac.uk/chembl/api/data/similarity/BSYNRYMUTXBXSQ-UHFFFAOYSA-N/80) |

Searching with InChI key is only possible for InChI keys found in the ChEMBL database. The system **does not** try and convert InChI key to a chemical representation.  


## Molecule Images

The Image resource returns a graphical representation of a ChEMBL molecule. Unlike the other resources it does not except filtering and paging arguments, but does except image specific arguments. These are defined in the table below.  


| Image Argument | Description | Allowed Values | Default Value | Example URL |
| :--- | :--- | :--- | :--- | :--- |
| format | Image format | png, svg and json | png | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=svg](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?format=svg) |
| dimensions | Size of image in pixels | 1-500 | 500 | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?dimensions=200](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?dimensions=200) |
| ignoreCoords | Choose to use or ignore coordinates in ChEMBL molfiles | 1 or 0 | 0 \(Use ChEMBL molfile coordinates\) | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?ignoreCoords=1](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?ignoreCoords=1) |
| engine | Chemical toolkit used to generate image | rdkit or indigo | rdkit | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?engine=indigo](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL25?engine=indigo) |
| bgColor | Background color | Full list [here](https://github.com/chembl/chembl_webservices_2/blob/b42b1dbaf96339651a9c10c2864e983f180208f8/chembl_webservices/core/utils.py) | transparent | [https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL1.png?bgColor=orange](https://www.ebi.ac.uk/chembl/api/data/image/CHEMBL1.png?bgColor=orange) |

## GET, POST and special characters

In GET request all the parameters has to be encoded into URL. Because there is a limitation of how long a URL can be it's often more convenient to use POST requests instead. POST parameters are embedded into request body and can be of any size. This is especially important when retrieving a long list of entities identified by \(random\) IDs.

ChEMBL API supports both GET and POST but since POST has a special meaning in REST protocol \(CREATE\), a special header has to be added to every POST request:

```text
X-HTTP-Method-Override:GET
```

Another issue is character encoding. SMILES strings often contain characters \(such as \#, % or \\) that have a special meaning in URLs. This is why when using GET, all parameters should be percent-encoded.

One example is a following SMILES string:

```text
[Na+].CO[C@@H](CCC#C\C=C/CCCC(C)CCCCC=C)C(=O)[O-]
```

Which can be encoded into URL in a following way: [https://www.ebi.ac.uk/chembl/api/data/molecule/%5BNa+%5D.CO%5BC@@H%5D\(CCC%23C%5CC=C/CCCC\(C\)CCCCC=C\)C\(=O\)%5BO-%5D](https://www.ebi.ac.uk/chembl/api/data/molecule/%5BNa+%5D.CO%5BC@@H%5D%28CCC%23C%5CC=C/CCCC%28C%29CCCCC=C%29C%28=O%29%5BO-%5D)

Below is another example of retrieving a molecule \(CHEMBL1628285\) that has the longest SMILES string currently stored in ChEMBL. The original SMILES string is:

```text
CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC1OC(CO)C(O)C(O)C1O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC2OC(CO)C(O)C(O)C2O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC3OC(CO)C(O)C(O)C3O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC4OC(CO)C(O)C(O)C4O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC5OC(CO)C(O)C(O)C5O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC6OC(CO)C(O)C(O)C6O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC7OC(CO)C(O)C(O)C7O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC8OC(CO)C(O)C(O)C8O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC9OC(CO)C(O)C(O)C9O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC%10OC(CO)C(O)C(O)C%10O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC%11OC(CO)C(O)C(O)C%11O)C(O)CO.CCCCCCCCCCCCCCCC[NH2+]OC(CO)C(O)C(OC%12OC(CO)C(O)C(O)C%12O)C(O)CO.CCCCCCCCCC(C(=O)NCCc%13ccc(OP(=S)(Oc%14ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%14)N(C)\\N=C\\c%15ccc(Op%16(Oc%17ccc(\\C=N\\N(C)P(=S)(Oc%18ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%18)Oc%19ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%19)cc%17)np(Oc%20ccc(\\C=N\\N(C)P(=S)(Oc%21ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%21)Oc%22ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%22)cc%20)(Oc%23ccc(\\C=N\\N(C)P(=S)(Oc%24ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%24)Oc%25ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%25)cc%23)np(Oc%26ccc(\\C=N\\N(C)P(=S)(Oc%27ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%27)Oc%28ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%28)cc%26)(Oc%29ccc(\\C=N\\N(C)P(=S)(Oc%30ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%30)Oc%31ccc(CCNC(=O)C(CCCCCCCCC)P(=O)(O)[O-])cc%31)cc%29)n%16)cc%15)cc%13)P(=O)(O)[O-]	
```

After encoding, the URL becomes [this](https://www.ebi.ac.uk/chembl/api/data/molecule/CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC1OC%28CO%29C%28O%29C%28O%29C1O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC2OC%28CO%29C%28O%29C%28O%29C2O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC3OC%28CO%29C%28O%29C%28O%29C3O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC4OC%28CO%29C%28O%29C%28O%29C4O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC5OC%28CO%29C%28O%29C%28O%29C5O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC6OC%28CO%29C%28O%29C%28O%29C6O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC7OC%28CO%29C%28O%29C%28O%29C7O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC8OC%28CO%29C%28O%29C%28O%29C8O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC9OC%28CO%29C%28O%29C%28O%29C9O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC%2510OC%28CO%29C%28O%29C%28O%29C%2510O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC%2511OC%28CO%29C%28O%29C%28O%29C%2511O%29C%28O%29CO.CCCCCCCCCCCCCCCC%5BNH2%2B%5DOC%28CO%29C%28O%29C%28OC%2512OC%28CO%29C%28O%29C%28O%29C%2512O%29C%28O%29CO.CCCCCCCCCC%28C%28%3DO%29NCCc%2513ccc%28OP%28%3DS%29%28Oc%2514ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2514%29N%28C%29%5CN%3DC%5Cc%2515ccc%28Op%2516%28Oc%2517ccc%28%5CC%3DN%5CN%28C%29P%28%3DS%29%28Oc%2518ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2518%29Oc%2519ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2519%29cc%2517%29np%28Oc%2520ccc%28%5CC%3DN%5CN%28C%29P%28%3DS%29%28Oc%2521ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2521%29Oc%2522ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2522%29cc%2520%29%28Oc%2523ccc%28%5CC%3DN%5CN%28C%29P%28%3DS%29%28Oc%2524ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2524%29Oc%2525ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2525%29cc%2523%29np%28Oc%2526ccc%28%5CC%3DN%5CN%28C%29P%28%3DS%29%28Oc%2527ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2527%29Oc%2528ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2528%29cc%2526%29%28Oc%2529ccc%28%5CC%3DN%5CN%28C%29P%28%3DS%29%28Oc%2530ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2530%29Oc%2531ccc%28CCNC%28%3DO%29C%28CCCCCCCCC%29P%28%3DO%29%28O%29%5BO-%5D%29cc%2531%29cc%2529%29n%2516%29cc%2515%29cc%2513%29P%28%3DO%29%28O%29%5BO-%5D.json)  


## CORS and JSONP

Both techniques are supported

## Web Service Client

To help users get started with using the updated ChEMBL web services the existing web service client has also been released. This is written in the Python programming language and is available to install from Python Package Index by typing:

```bash
pip install chembl_webresource_client
```

The client code is open and hosted on GitHub: [https://github.com/chembl/chembl\_webresource\_client](https://github.com/chembl/chembl_webresource_client).

The following list provides some example use cases of the client:

### Search molecule by synonym

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
res = molecule.search('viagra')
```

### Search target by gene name

```python
from chembl_webresource_client.new_client import new_client
target = new_client.target
gene_name = 'GABRB2'
res = target.search(gene_name)
```

### Search target by synonym

```python
from chembl_webresource_client.new_client import new_client
target = new_client.target
gene_name = 'GABRB2'
res = target.filter(target_synonym__icontains=gene_name)
```

### Having a list of molecules ChEMBL IDs in a CSV file, produce another CSV file that maps every compound ID into a list of UniProt accession numbers and save the mapping into output csv file



```python
import csv
from chembl_webresource_client.new_client import new_client

# This will be our resulting structure mapping compound ChEMBL IDs into target uniprot IDs
compounds2targets = dict()

# First, let's just parse the csv file to extract compounds ChEMBL IDs:
with open('compounds_list.csv', 'rb') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        compounds2targets[row[0]] = set()

# OK, we have our source IDs, let's process them in chunks:
chunk_size = 50
keys = compounds2targets.keys()

for i in range(0, len(keys), chunk_size):
    # we jump from compounds to targets through activities:
    activities = new_client.activity.filter(molecule_chembl_id__in=keys[i:i + chunk_size])
    # extracting target ChEMBL IDs from activities:
    for act in activities:
        compounds2targets[act['molecule_chembl_id']].add(act['target_chembl_id'])

# OK, now our dictionary maps from compound ChEMBL IDs into target ChEMBL IDs
# We would like to replace target ChEMBL IDs with uniprot IDs

for key, val in compounds2targets.items():
    # We don't know how many targets are assigned to a given compound so again it's
    # better to process targets in chunks:
    lval = list(val)
    uniprots = set()
    for i in range(0, len(val), chunk_size):
        targets = new_client.target.filter(target_chembl_id__in=lval[i:i + chunk_size])
        uniprots |= set(sum([[comp['accession'] for comp in t['target_components']] for t in targets],[]))
    compounds2targets[key] = uniprots

# Finally write it to the output csv file
with open('compounds_2_targets.csv', 'wb') as csvfile:
    writer = csv.writer(csvfile)
    for key, val in compounds2targets.items():
        writer.writerow([key] + list(val))
```

### Having a list of molecules ChEMBL IDs in a CSV file, produce another CSV file that maps every compound ID into a list of human gene names.

```python
import csv
from chembl_webresource_client.new_client import new_client

# This will be our resulting structure mapping compound ChEMBL IDs into target uniprot IDs
compounds2targets = dict()

# First, let's just parse the csv file to extract compounds ChEMBL IDs:
with open('compounds_list.csv', 'rb') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        compounds2targets[row[0]] = set()

# OK, we have our source IDs, let's process them in chunks:
chunk_size = 50
keys = compounds2targets.keys()

for i in range(0, len(keys), chunk_size):
    # we jump from compounds to targets through activities:
    activities = new_client.activity.filter(molecule_chembl_id__in=keys[i:i + chunk_size])
    # extracting target ChEMBL IDs from activities:
    for act in activities:
        compounds2targets[act['molecule_chembl_id']].add(act['target_chembl_id'])

# OK, now our dictionary maps from compound ChEMBL IDs into target ChEMBL IDs
# We would like to replace target ChEMBL IDs with uniprot IDs

for key, val in compounds2targets.items():
    # We don't know how many targets are assigned to a given compound so again it's
    # better to process targets in chunks:
    lval = list(val)
    genes = set()
    for i in range(0, len(val), chunk_size):
        targets = new_client.target.filter(target_chembl_id__in=lval[i:i + chunk_size])
        for target in targets:
            for component in target['target_components']:
                for synonym in component['target_component_synonyms']:
                    if synonym['syn_type'] == "GENE_SYMBOL":
                        genes.add(synonym['component_synonym'])
    compounds2targets[key] = genes

# Finally write it to the output csv file
with open('compounds_2_genes.csv', 'wb') as csvfile:
    writer = csv.writer(csvfile)
    for key, val in compounds2targets.items():
        writer.writerow([key] + list(val))
  		
```

### Find compounds similar to given SMILES query with similarity threshold of 85%

```python
from chembl_webresource_client.new_client import new_client
similarity = new_client.similarity
res = similarity.filter(smiles="CO[C@@H](CCC#C\C=C/CCCC(C)CCCCC=C)C(=O)[O-]", similarity=85)
```

### Find compounds similar to aspirin \(CHEMBL25\) with similarity threshold of 70%

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
similarity = new_client.similarity
aspirin_chembl_id = molecule.search('aspirin')[0]['molecule_chembl_id']
res = similarity.filter(chembl_id="CHEMBL25", similarity=70)
```

### Perform substructure search using SMILES

```python
from chembl_webresource_client.new_client import new_client
substructure = new_client.substructure
res = substructure.filter(smiles="CN(CCCN)c1cccc2ccccc12")
```

### Perform substructure search using ChEMBL ID

```python
from chembl_webresource_client.new_client import new_client
substructure = new_client.substructure
substructure.filter(chembl_id="CHEMBL25")
```

### Get a single molecule by ChEMBL ID

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
m1 = molecule.get('CHEMBL25')
```

### Get a single molecule by SMILES

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
m1 = molecule.get('CC(=O)Oc1ccccc1C(=O)O')
```

### Get a single molecule by InChi Key

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
molecule.get('BSYNRYMUTXBXSQ-UHFFFAOYSA-N')
```

### Get many compounds by their ChEMBL IDs

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
records = molecule.get(['CHEMBL6498', 'CHEMBL6499', 'CHEMBL6505'])
```

### Get many compounds by a list of SMILES

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
records = molecule.get(['CNC(=O)c1ccc(cc1)N(CC#C)Cc2ccc3nc(C)nc(O)c3c2',
      'Cc1cc2SC(C)(C)CC(C)(C)c2cc1\\N=C(/S)\\Nc3ccc(cc3)S(=O)(=O)N',
      'CC(C)C[C@H](NC(=O)[C@@H](NC(=O)[C@H](Cc1c[nH]c2ccccc12)NC(=O)[C@H]3CCCN3C(=O)C(CCCCN)CCCCN)C(C)(C)C)C(=O)O'])
```

### Get many compounds by a list of InChi Keys

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
records = molecule.get(['XSQLHVPPXBBUPP-UHFFFAOYSA-N', 'JXHVRXRRSSBGPY-UHFFFAOYSA-N', 'TUHYVXGNMOGVMR-GASGPIRDSA-N'])
```

### Obtain the pChEMBL values for compound

```python
from chembl_webresource_client.new_client import new_client
activities = new_client.activity
res = activities.filter(molecule_chembl_id="CHEMBL25", pchembl_value__isnull=False)
```

### Obtain the pChEMBL value for a specific compound AND a specific target

```python
from chembl_webresource_client.new_client import new_client
activities = new_client.activity
activities.filter(molecule_chembl_id="CHEMBL25", target_chembl_id="CHEMBL612545", pchembl_value__isnull=False)
```

### Get all approved drugs

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
approved_drugs = molecule.filter(max_phase=4)
```

### Get approved drugs for lung cancer

```python
from chembl_webresource_client.new_client import new_client
drug_indication = new_client.drug_indication
molecules = new_client.molecule
lung_cancer_ind = drug_indication.filter(efo_term__icontains="LUNG CARCINOMA")
lung_cancer_mols = molecules.filter(molecule_chembl_id__in=[x['molecule_chembl_id'] for x in lung_cancer_ind])
```

### Get all molecules in ChEMBL with no Rule-of-Five violations

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
no_violations = molecule.filter(molecule_properties__num_ro5_violations=0)
```

### Get all biotherapeutic molecules

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
biotherapeutics = molecule.filter(biotherapeutic__isnull=False)
```

### Return molecules with molecular weight &lt;= 300

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
light_molecules = molecule.filter(molecule_properties__mw_freebase__lte=300)
```

### Return molecules with molecular weight &lt;= 300 AND pref\_name ends with nib

```python
from chembl_webresource_client.new_client import new_client
molecule = new_client.molecule
light_nib_molecules = molecule.filter(molecule_properties__mw_freebase__lte=300).filter(pref_name__iendswith="nib")
```

### Get all Ki activities related to the hERG target

```python
from chembl_webresource_client.new_client import new_client
target = new_client.target
activity = new_client.activity
herg = target.search('herg')[0]
herg_activities = activity.filter(target_chembl_id=herg['target_chembl_id']).filter(standard_type="Ki")
```

### Get all activities related to the Open TG-GATES project

```python
from chembl_webresource_client.new_client import new_client
activity = new_client.activity
res = activity.search('"TG-GATES"')
```

### Get all activities for a specific target with assay type 'B' OR 'F'

```python
from chembl_webresource_client.new_client import new_client
activity = new_client.activity
res = activity.filter(target_chembl_id='CHEMBL3938', assay_type__iregex='(B|F)')
```

### Search for ADMET-reated inhibitor assays

```python
from chembl_webresource_client.new_client import new_client
assay = new_client.assay
res = assay.search('inhibitor').filter(assay_type='A')
```

### Get cell line by cellosaurus id

```python
from chembl_webresource_client.new_client import new_client
cell_line = new_client.cell_line
res = cell_line.filter(cellosaurus_id="CVCL_0417")
```

### Filter drugs by approval year and name

```python
from chembl_webresource_client.new_client import new_client
drug = new_client.drug
res = drug.filter(first_approval=1976).filter(usan_stem="-azosin")
```

### Get tissue by BTO ID

```python
from chembl_webresource_client.new_client import new_client
tissue = new_client.tissue
res = tissue.filter(bto_id="BTO:0001073")
```

### Get tissue by Caloha id

```python
from chembl_webresource_client.new_client import new_client
tissue = new_client.tissue
res = tissue.filter(caloha_id="TS-0490")
```

### Get tissue by Uberon id

```python
from chembl_webresource_client.new_client import new_client
tissue = new_client.tissue
res = tissue.filter(uberon_id="UBERON:0000173")
```

### Get tissue by name

```python
from chembl_webresource_client.new_client import new_client
tissue = new_client.tissue
res = tissue.filter(pref_name__istartswith='blood')
```

### Search documents for 'cytokine'

```python
from chembl_webresource_client.new_client import new_client
document = new_client.document
res = document.search('cytokine')
```

### Search for compound in Unichem

```python
from chembl_webresource_client.new_client import new_client
ret = unichem.get('AIN')
```

### Resolve InChi Key to Inchi using Unichem

```python
from chembl_webresource_client.unichem import unichem_client as unichem
ret = unichem.inchiFromKey('AAOVKJBEBIDNHE-UHFFFAOYSA-N')
```

### Convert SMILES to CTAB

```python
from chembl_webresource_client.unichem import unichem_client as unichem
aspirin = utils.smiles2ctab('O=C(Oc1ccccc1C(=O)O)C')
```

### Convert SMILES to image and image back to SMILES

```python
from chembl_webresource_client.utils import utils
aspirin = 'CC(=O)Oc1ccccc1C(=O)O'
im = utils.smiles2image(aspirin)
mol = utils.image2ctab(im)
smiles = utils.ctab2smiles(mol).split()[2]
self.assertEqual(smiles, aspirin)
```

### Compute fingerprints

```python
from chembl_webresource_client.utils import utils
aspirin = utils.smiles2ctab('O=C(Oc1ccccc1C(=O)O)C')
fingerprints = utils.sdf2fps(aspirin)
```

### Compute Maximal Common Substructure

```python
from chembl_webresource_client.utils import utils
smiles = ["O=C(NCc1cc(OC)c(O)cc1)CCCC/C=C/C(C)C", "CC(C)CCCCCC(=O)NCC1=CC(=C(C=C1)O)OC", "c1(C=O)cc(OC)c(O)cc1"]
mols = [utils.smiles2ctab(smile) for smile in smiles]
sdf = ''.join(mols)
result = utils.mcs(sdf)
```

### Compute various molecular descriptors

```python
from chembl_webresource_client.utils import utils
aspirin = utils.smiles2ctab('O=C(Oc1ccccc1C(=O)O)C')
num_atoms = json.loads(utils.getNumAtoms(aspirin))[0]
mol_wt = json.loads(utils.molWt(aspirin))[0]
log_p = json.loads(utils.logP(aspirin))[0]
tpsa = json.loads(utils.tpsa(aspirin))[0]
descriptors = json.loads(utils.descriptors(aspirin))[0]
```

### Standardise molecule

```python
from chembl_webresource_client.utils import utils
mol = utils.smiles2ctab("[Na]OC(=O)Cc1ccc(C[NH3+])cc1.c1nnn[n-]1.O")
st = utils.standardise(mol)
```

### Example Queries

The table below provides a list of example searches a user may wish to carry out using the ChEMBL web services. The aim of the list is highlight the type of data that can be retrieved from ChEMBL using the web services. The examples can be adapted, extended and chained together to build up more complex workflows.

| Description | Example URL |
| :--- | :--- |
| Get all approved drugs | [https://www.ebi.ac.uk/chembl/api/data/molecule?max\_phase=4](https://www.ebi.ac.uk/chembl/api/data/molecule?max_phase=4) |
| Get all molecules in ChEMBL with no Rule-of-Five violations | [https://www.ebi.ac.uk/chembl/api/data/molecule?molecule\_properties\_\_num\_ro5\_violations=0](https://www.ebi.ac.uk/chembl/api/data/molecule?molecule_properties__num_ro5_violations=0) |
| Get all biotherapeutic molecules | [https://www.ebi.ac.uk/chembl/api/data/molecule?biotherapeutic\_\_isnull=false](https://www.ebi.ac.uk/chembl/api/data/molecule?biotherapeutic__isnull=false) |
| Get all functional/phenotypic assays \(assay\_type=F\), from the literature \(src\_id 1\) | [https://www.ebi.ac.uk/chembl/api/data/assay?assay\_type=F&src\_id=1](https://www.ebi.ac.uk/chembl/api/data/assay?assay_type=F&src_id=1) |
| Get all binding assays \(assay\_type=B\), which also contain the term 'insulin' | [https://www.ebi.ac.uk/chembl/api/data/assay?assay\_type=B&description\_\_icontains=insulin](https://www.ebi.ac.uk/chembl/api/data/assay?assay_type=B&description__icontains=insulin) |
| Get all Clearance activity values \(standard\_type=CL\), for rat, mouse and human | [https://www.ebi.ac.uk/chembl/api/data/activity?standard\_type=CL&target\_organism\_\_in=Homo%20sapiens,Rattus%20norvegicus,Mus%20musculus](https://www.ebi.ac.uk/chembl/api/data/activity?standard_type=CL&target_organism__in=Homo%20sapiens,Rattus%20norvegicus,Mus%20musculus) |
| Get all cell lines, which end with the term 'carcinoma' | [https://www.ebi.ac.uk/chembl/api/data/cell\_line?cell\_source\_tissue\_\_iendswith=carcinoma](https://www.ebi.ac.uk/chembl/api/data/cell_line?cell_source_tissue__iendswith=carcinoma) |
| Get all mechanism of action details muscarinic acetylcholine receptor antagonists | [https://www.ebi.ac.uk/chembl/api/data/mechanism?mechanism\_of\_action\_\_icontains=Muscarinic%20acetylcholine%20receptor&action\_type=ANTAGONIST](https://www.ebi.ac.uk/chembl/api/data/mechanism?mechanism_of_action__icontains=Muscarinic%20acetylcholine%20receptor&action_type=ANTAGONIST) |
| Get all targets \(single protein, protein complexes, protein families etc.\), which contain UniProt accession Q13936 | [https://www.ebi.ac.uk/chembl/api/data/target?target\_components\_\_accession=Q13936](https://www.ebi.ac.uk/chembl/api/data/target?target_components__accession=Q13936) |
| Get the entity type for CHEMBL1000 | [https://www.ebi.ac.uk/chembl/api/data/chembl\_id\_lookup?chembl\_id=CHEMBL1000](https://www.ebi.ac.uk/chembl/api/data/chembl_id_lookup?chembl_id=CHEMBL1000) |

### Use Cases

The following use cases are provided as an example of how it is possible to chain together ChEMBL web service calls to answer to complicated questions using ChEMBL data.

#### **Investigating the potency of approved drugs against their efficacy targets** 

Since ChEMBL includes both mechanism of action information for approved drugs and pharmacology data from published assays, it is interesting to combine this information and investigate the potency of a drug against its efficacy target. This might be done either to confirm or refute the proposed target assignment, or to better understand how the in-vitro potency of a compound might relate to clinical efficacy or ADMET properties. The following example shows how this type of analysis could be carried out using the ChEMBL web services.

1.  Use the molecule end point to retrieve a list of approved drugs \(max\_phase=4\):   [https://www.ebi.ac.uk/chembl/api/data/molecule?max\_phase=4](https://www.ebi.ac.uk/chembl/api/data/molecule?max_phase=4)   Using ChEMBL\_20, this will retrieve 2795 drugs in total. We will use CHEMBL998 \(loratadine\) as an example, but the same workflow could be repeated for the others.  
2. Use the mechanism end point to retrieve the mechanism of action and target of each drug:   [https://www.ebi.ac.uk/chembl/api/data/mechanism?molecule\_chembl\_id=CHEMBL998](https://www.ebi.ac.uk/chembl/api/data/mechanism?molecule_chembl_id=CHEMBL998)   Loratadine is reported to be a histamine H1 receptor antagonist, represented by the ChEMBL target CHEMBL231.  
3. Use the assay end point to identify any binding assays \(assay\_type=B\) for the human histamine H1 receptor:   [https://www.ebi.ac.uk/chembl/api/data/assay?target\_chembl\_id=CHEMBL231&relationship\_type=D&assay\_type=B](https://www.ebi.ac.uk/chembl/api/data/assay?target_chembl_id=CHEMBL231&relationship_type=D&assay_type=B)   Note the relationship\_type=D filter restricts the results to assays where we are confident that the human receptor was tested and not an orthologue. A total of 213 assays are identified. We will take CHEMBL1909156 as an example.  
4. Combine the results of the above queries to identify any potency measurements for loratadine in these assays:   [https://www.ebi.ac.uk/chembl/api/data/activity?molecule\_chembl\_id=CHEMBL998&assay\_chembl\_id=CHEMBL1909156](https://www.ebi.ac.uk/chembl/api/data/activity?molecule_chembl_id=CHEMBL998&assay_chembl_id=CHEMBL1909156)   This assay reports an IC50 value of 170 nM and a Ki measurement of 20 nM for loratadine against the histamine H1 receptor.   This process could be repeated for the other 212 assays by either iterating through them individually or, where a sufficiently small number of assays are returned, using the \_\_in filter on the activity end point to retrieve several assays at once e.g.,   [https://www.ebi.ac.uk/chembl/api/data/activity?molecule\_chembl\_id=CHEMBL998&assay\_chembl\_id\_\_in=CHEMBL830379,CHEMBL1909156,CHEMBL882906,CHEMBL691450](https://www.ebi.ac.uk/chembl/api/data/activity?molecule_chembl_id=CHEMBL998&assay_chembl_id__in=CHEMBL830379,CHEMBL1909156,CHEMBL882906,CHEMBL691450)   An additional 2 assays are identified in this way, reporting an IC50 value of 290 nM and a Ki value of 414 nM. These values could be averaged, or the lowest taken, to give an indication of the average potency of the compound, or the assay conditions could be investigated further to try to identify which assay might be most reliable or informative \(the ChEMBL identifier for the document from which the data are extracted is also provided by the activity end point\).

#### **More examples**

As mentioned above, there is an IPython notebook with example API calls and the corresponsing Python client code [https://github.com/chembl/mychembl/blob/master/ipython\_notebooks/09\_myChEMBL\_web\_services.ipynb](https://github.com/chembl/mychembl/blob/master/ipython_notebooks/09_myChEMBL_web_services.ipynb). Additionally there is a comprehensive test suite, covering almost all the functionality offered by the API. It can be found in the Python client library: [https://github.com/chembl/chembl\_webresource\_client/blob/master/chembl\_webresource\_client/tests.py](https://github.com/chembl/chembl_webresource_client/blob/master/chembl_webresource_client/tests.py).

