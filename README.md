# New Web Interface

We have developed a new [web interface](https://www.ebi.ac.uk/chembl/beta/) that will eventually replace the [current one](https://www.ebi.ac.uk/chembl/) completely. It is still in a beta stage, this means that it provides all the mayor features, but it is expected to have some known and unknown bugs. We will be working on fixing them as a next stage.

**If you want to suggest a new feature or report a bug, please read** [**this**](frequently-asked-questions/general-questions.md#how-do-i-report-errors-or-make-suggestions-for-the-interface)**.**

## New Features

### Free Text Search

* The bar will provide some suggestions as you write. 
* You don't need to click on a different button to search for different entity types \(Compounds, Targets, Assays, Documents, Cells or Tissues\) anymore , the interface will search among all entities for you. 
* The search bar now appears in all the pages, including report cards, so you don't have to go back to the main page to search for another term. 
* Our new interface uses elasticsearch indexes, you can use a DSL to build complex queries, see our [guide](searching-guide.md). 

### Structure Search

* You can search by using the [Marvin JS sketcher](https://chemaxon.com/products/marvin-js). You can open it just by clicking on the "structure" icon on the search bar:

![](.gitbook/assets/screen-shot-2018-06-20-at-17.06.11.png)

* For the substructure and similarity results we have now included structure highlighting on the results. the highlight can be turned on or off. See for example: [https://www.ebi.ac.uk/chembl/beta/g/tiny/O/X4tGAntE5huqwzOIcrlg==](https://www.ebi.ac.uk/chembl/beta/g/tiny/O/X4tGAntE5huqwzOIcrlg==) 

### Filters

For the search results and other results that you can produce in the interface there are filters available at the left side of the page:

![](https://github.com/chembl/GLaDOS-docs/raw/master/.gitbook/assets/screen-shot-2018-06-21-at-12.39.37.png) [https://www.ebi.ac.uk/chembl/beta/g/\#browse/compounds](https://www.ebi.ac.uk/chembl/beta/g/#browse/compounds)

With these filters you can easily see the distribution of the data. The sizes of the rectangles behind each value represent the proportion of items with that value for that property in the data. You can also click on the filter the data.

By clicking on the "settings" button

![](https://github.com/chembl/GLaDOS-docs/raw/master/.gitbook/assets/screen-shot-2018-06-21-at-13.35.17.png)

You can open a menu to configure the filters panel

![](.gitbook/assets/screen-shot-2018-06-21-at-13.36.42.png)

### Browsing activities

You can see the related activities of compound, target, document, assay, cell line, or tissue by clicking on the visualisations. For example for the compound [CHEMBL59](https://www.ebi.ac.uk/chembl/beta/compound_report_card/CHEMBL59/) you will see this pie chart in Activity Charts:

![](https://raw.githubusercontent.com/chembl/GLaDOS-docs/master/.gitbook/assets/screen-shot-2018-06-21-at-13.55.55.png)

If you click on the section that represents "Potency" you will be directed to the \[activities\]\([https://www.ebi.ac.uk/chembl/beta/g/\#browse/activities/filter/molecule\_chembl\_id%3A\("CHEMBL59" OR "CHEMBL3247442" OR "CHEMBL1557"\) AND standard\_type%3A\("Potency"\)](https://www.ebi.ac.uk/chembl/beta/g/#browse/activities/filter/molecule_chembl_id%3A%28"CHEMBL59"%20OR%20"CHEMBL3247442"%20OR%20"CHEMBL1557"%29%20AND%20standard_type%3A%28"Potency"%29)\) of type "Potency" for compound CHEMBL59.

In the results pages, you can also select several items and then click on "Browse Activities", you will be directed to a list of the \[activities\]\([https://www.ebi.ac.uk/chembl/beta/g/\#browse/activities/filter/molecule\_chembl\_id%3A\("CHEMBL59" OR "CHEMBL3247442" OR "CHEMBL1557"\) AND standard\_type%3A\("Potency"\)](https://www.ebi.ac.uk/chembl/beta/g/#browse/activities/filter/molecule_chembl_id%3A%28"CHEMBL59"%20OR%20"CHEMBL3247442"%20OR%20"CHEMBL1557"%29%20AND%20standard_type%3A%28"Potency"%29)\) for the items that you selected:

![](.gitbook/assets/screen-shot-2018-06-21-at-14.13.02.png)

### Data Visualisations

In order to show in a better way what is inside [ChEMBL](https://www.ebi.ac.uk/chembl/beta/) we have created some data visualisations. You can see them in the main page, or by visiting [https://www.ebi.ac.uk/chembl/beta/visualise/](https://www.ebi.ac.uk/chembl/beta/visualise/).

### Descriptive URLs

The urls in the new interface are intended to always describe the data that is being shown. For example, when you search targets using the term 'Liver', the url is:

```text
https://www.ebi.ac.uk/chembl/beta/g/#search_results/targets/query=Liver
```

You should be able to copy any url in the page and send it to another person, so the receiver can see the same data. You can also get a shortened version of the url by clicking on the "share" icon of the breadcrumbs:

![](.gitbook/assets/screen-shot-2018-06-26-at-16.35.15.png)

