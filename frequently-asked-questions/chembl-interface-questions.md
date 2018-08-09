# ChEMBL Interface Questions

## Browsing Related Entities

### After doing a search I obtain X compounds, how can I get counts for the total number of bioactivities?

After doing a search by a term, for example [Taxol](https://www.ebi.ac.uk/chembl/beta/g/#search_results/all/query=Taxol), you will a header like the following in every result per entity:

![](../.gitbook/assets/screen-shot-2018-08-01-at-09.54.16%20%281%29.png)

This means that we found 206 compounds for your search. If you click on the link "Browse Activities":

![](../.gitbook/assets/screen-shot-2018-08-01-at-10.22.22%20%281%29.png)

A new page will open with all the [activities related](https://www.ebi.ac.uk/chembl/beta/g/tiny/xB1NBZge73NTMiwKxpvQXQ==) to the 206 compounds that you obtained:

![](../.gitbook/assets/screen-shot-2018-08-01-at-10.26.46%20%285%29.png)

Here you can see that there are 7807 activities related to the 206 compounds that you found. 

### After doing a search I obtain X compounds, how can I get information about the related targets?

Similarly to the previous answer, lets assume that you searched for [Taxol](https://www.ebi.ac.uk/chembl/beta/g/#search_results/all/query=Taxol), you can click on the "Heatmap" button of the "Compound Results" header:

![](../.gitbook/assets/screen-shot-2018-08-01-at-10.33.04%20%281%29.png)

You will see a heatmap like the following:

![](../.gitbook/assets/screen-shot-2018-08-01-at-10.40.51.png)

* **Orange rectangle:** You can see that there are [1043 targets related](https://www.ebi.ac.uk/chembl/beta/g/tiny/YYX2P/h/OrOYL9ZGFzzkiA==) to the 206 compounds that you obtained. If you click on the text a new page will open with the targets that are related to these compounds.
* **Blue rectangle:** Hover to see a mini report card of each of the compounds, click to go to the report card page. 
* **Red rectangle:** Hover to see a mini report card of each of the targets, click to go to the report card page. 
* **Green rectangle:** Click on a square to open a tooltip with a link to see all the activities between the compound and target related by that square. For example, If you click on the square relating the compound CHEMBL3545252 and the target Tubulin, you will see all the [activities](https://www.ebi.ac.uk/chembl/beta/g/tiny/oW+U32lw6/IMI6N+ldRS5Q==) relating that compound with that target.

### What does the 'Bioactivities' filter mean?

When you are browsing a set of compounds, targets, assays, documents, cell lines or tissues, in the filters on the left you will see a filter like this one:

![](../.gitbook/assets/screen-shot-2018-08-01-at-11.16.56%20%282%29.png)

You can see an example [here](https://www.ebi.ac.uk/chembl/beta/g#browse/compounds/filter/Taxol). This example shows 206 compounds:

![](../.gitbook/assets/screen-shot-2018-08-01-at-11.15.21%20%281%29.png)

The filter means:

* 27 out of the 206 compounds have 1 related bioactivity. 
* 65 out of the 206 compounds have 2 related bioactivities.
* etc...
* 26 out of the 206 compounds have between 12 to 4989 related bioactivities. 







