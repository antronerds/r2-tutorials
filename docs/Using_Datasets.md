<a id="using_datasets"> </a>

Using Datasets
==============

*Selecting or searching datasets in R2*

Scope
-----

- Working with datasets.
- R2 allows you to perform all kinds of analyses based on a well
    annotated single dataset or a selection of datasets at the
    same time. Different analyses are available based on the selection
    of one of these options in field 1.
- R2 contains omic profiles such as expression and methylation profiles for more than ~2.500.000 unique
    individual samples. The samples are grouped in so-called datasets. Each dataset has its own characteristics, 
    such as tissue type, tumor/disease type, or from cell-line experiments. Frequently, new datasets are added the platform.
- The *Tumor Neuroblastoma public - Versteeg - 88 - MAS5.0 -
    u133p2* dataset will be used as an example dataset to guide you
    through most of the tutorial but other datasets will be used as examples. Later on, working with multiple datasets will be discussed.

   ![](_static/images/Usingdatasets/Usingdatasets_type1a.png "Figure 1: Change Dataset on the main page")

   [**Figure 1: Select types of datasets**](_static/images/Usingdatasets/Usingdatasets_type1a.png)



Step 1: Selecting a dataset
---------------

1. R2 offers a large number of datasets ready for analysis and visualization.
    The numbered boxes on the main page will guide you through all the steps necessary to perform a task, starting
    with the selection of a dataset. In field 1 select **Single Dataset**, in field 2 click on the name of the dataset.
	
    ![](_static/images/Usingdatasets/UsingDataset_selectv1a.png "Figure 2: Change Dataset on the main page")
	
    [**Figure 2: Change Dataset on the main page**](_static/images/Usingdatasets/UsingDataset_selectv1a.png)

	
2. A popup window appears that shows all the currently available datasets in a grid: each row represents one dataset, with its main descriptive details split up in the columns. You can simply scroll through the list and get more information about a dataset by clicking on the row of any dataset in this list and extra information about a dataset will appear in an information panel below the grid box. Possible adjustments of the original data by the R2 team, such as data transformations or annotation changes, can be found in the Adjustments section of the information panel. At the bottom you will see links to the original data source and Pubmed resources, if available.

   ![](_static/images/Usingdatasets/UsingDataset_select_by_row.png "Figure 3: Select a dataset or read more in-depth information")

   [**Figure 3: Select a dataset by clicking on a row**](_static/images/Usingdatasets/UsingDataset_select_selectbutton.png)  


3. Every column header provides options to filter the database, e.g. in the Tissue/Tumor text field a keyword such as **medull** can be written to filter for medulloblastoma datasets or, with the Select Filter dropdown under the Data type header you can requests an overview of for instance methylation datasets. If you know specific details, other columns can be of help as well: e.g. you can search for an author, or use the N column to search for a datasets of which you know the number of samples. The grid box will display all the datasets that fulfill the (combined) filter requirements. In the bottom right corner you find the number of (filtered) datasets that are available to you. 

   ![](_static/images/Usingdatasets/UsingDataset_select_autofill_text.png "Figure 4: Use the search bar to filter the list of datasets with a keyword")
		 

[**Figure 4: Use the search bar to textually filter the list of datasets with a keyword**](_static/images/Usingdatasets/UsingDataset_select_autofill_text.png)  



4. Click on the table row of the dataset of your choice and click the blue colored button **Confirm selection** in order to use a dataset in field 2 of the main page for further analysis.



----------

  ![](_static/images/R2d2_logo.png)**Did you know that datasets have an informative naming?**   Datasets have a structured naming in R2, using the following rules: type_of_dataset - author - number_of_samples - normalization - chiptype. The dataset selection grid consists of these informative parts as columns, each with filter options to perform an advanced search through the dataset.

  ![](_static/images/Usingdatasets/UsingDataset_understanding_dataset_names.png "The information parts of a dataset name")
	
  [**Figure 5: The informative parts of a dataset name correspond to the columns of the dataset selection grid.**](_static/images/Usingdatasets/UsingDataset_understanding_dataset_names.png) 

----------


Step 2: Advanced selection of datasets
---------------

1. The grid itself enables the user to search through datasets using keywords and other filter options as well. 
   The column dropdown functions and textboxes can filter the datasets for specific characteristics, e.g. datasets 
   with a minimal number of samples, a specific author, platform or publication date. You can easily combine the search functions of the different columns.  
  
   As an example, we want to see which large sets sets are available. First we write part of the word 
   Neuroblastoma in the search box of the Tissue/Tumor column. Next, we use the pull down of the N (sample number) column to order the datasets in descending order. 
	
    ![](_static/images/Usingdatasets/UsingDataset_combine_grid_filters_v1.png "Figure 7: Combine search filters in the grid")
	
    [**Figure 6: Combine search filters in the grid**](_static/images/Usingdatasets/UsingDataset_combine_grid_filters.png)
	
2. Again we use the **Confirm Selection** button if we want to continue our analysis with a specific dataset of the grid. 
	
3. Select “Across Datasets” in field **1**. Note that in field 2
    different options become available compared to the “single
    dataset” option.
   
    ![](_static/images/Usingdatasets/UsingDatasets_SelectAcrossDatasetsInR2v1.png "Figure 8: Selecting across datasets")
	
    [**Figure 7: Selecting across datasets**](_static/images/Usingdatasets/UsingDatasets_SelectAcrossDatasetsInR2v1.png)
	
    Analysis methods following selecting the “Across Datasets” option in field **1** will be discussed in Chapter 10 “Working with multiple datasets”.  



Step 3: Using Dataset favorites
---------------

Since R2 is hosting hundreds of datasets, it could be convenient to store the datasets you often use in a preselection that 
is easily accessible. In order to maintain favorites, you need to be a registered user. If you did not yet register; 
an account can easily be created via 'Login/Register' which is absolutely free. Clicking on the dataset name will open the dataset selection grid, where resources can be searched and selected.

![](_static/images/Usingdatasets/UsingDataset_selectv1b.png  "Figure 8: Change Dataset, to access favorites")
	
[**Figure 8: Change Dataset to access favorites**](_static/images/Usingdatasets/UsingDataset_selectv1b.png)

Within the dataset selection table, you can select and deselect cohorts to add or remove them from your selection of
preferred sets. This is done by using the favorite select boxes in the last column on the right side. Favorite 
datasets will always be represented at the top of your selection table and will be marked with a green background 
color in the selection column. This makes it very convenient to quickly access them.  

![](_static/images/Usingdatasets/UsingDataset_selectfav_v1.png "Figure 09: Managing favorites")
	
[**Figure 09: Managing favorites**](_static/images/Usingdatasets/UsingDataset_selectfav_v1.png)


Step 4: Data Scopes
---------------

1. R2 can be forced to only display a sub-selection of all the datasets that are available (e.g. only neuroblastoma datasets). 
    These are called data scopes and can be selected from within R2 by the left-hand menu item 'Change Data Scope'. 
    From here you can use one of the pre-set scopes. 
    This is also the section where you can remove a scope that has been set. 
    An obvious reason why scopes can be convenient, is the focussed view on the available data, 
    to restrict data to a particular subject or as a landing page for a specific publication/subject.
    Datascopes as dedicated landing pages can also be configured to expose additional functionalities and quick jumps to sections in the platform. 
    Just have a look at which ones are already accessible.  
2. Data scopes can be used directly from the internet address line, which can be handy when a referral needs to be made to R2 from a manuscript. For now, you do need to provide a link directly to the server (usually hgserver1.amc.nl/cgi-bin/r2/main.cgi?&dscope=NRBL).  

Further details on the use of Datascopes can be found in Chapter 18 'Datascopes'.   

----------
 ![](_static/images/R2d2_logo.png)**Did you know that the R2-support team is scanning public repositories for interesting datasets to expand the R2-database on a regular basis**      

> *In case you want to see a dataset added to R2 please send an email to r2-support@amsterdamumc.nl  
> Such an email should contain a link to the publicly accessible files, such as a Gene Expression Omnibus number (GSE\*\*\*\*\*).* 
>
> *Your own private datasets can also be added to R2 with user/group restricted access. Please send us an email at* ***<r2-support@amsterdamumc.nl>*** *and inquire on the procedure to get your data available in R2 (see also Chapter 25).*

---------------



Final remarks / future directions
---------------------------------


All the procedures described in this chapter can be executed using the R2: genomics analysis and visualization platform (http://r2platform.com / http://r2.amc.nl).

If you encounter any quirks or issues, please do not hesitate to contact R2 support at r2-support@amsterdamumc.nl.

We hope that this tutorial has been useful.

Best regards,
The R2 support team.



