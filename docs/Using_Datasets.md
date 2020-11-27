<a id="using_datasets"> </a>

Using Datasets
==============

*Selecting or searching for datasets in R2*

Scope
-----

-   Working with datasets.
-   R2 allows you to perform all kinds of analyses based on a well
    annotated single dataset or a selection of datasets at the
    same time. Different analyses are available based on the selection
    of one of these options in field 1.
-   R2 contains mRNA gene expression profiles for more than 191.000
    individual human samples and more 12.000 individual mouse samples. The samples are grouped in so
    called datasets. Each dataset has its own characteristics, such as
    tissue type, tumor type or from cell-line experiments. Frequently new datasets are added the platform.
-   The *Tumor Neuroblastoma public - Versteeg - 88 - MAS5.0 -
    u133p2* dataset will be used as an example dataset to guide you
    through most of the tutorial. Later on, working with multiple
    datasets will be discussed.

Step 1: Selecting a dataset
---------------

1.  R2 offers a large amount of readily available datasets for analysis
    and visualization. The numbered boxes on the main page will guide
    you through all the steps necessary to perform a task, beginning with the selection of a dataset. In box 1 select **Single Dataset**, in field 2 choose **Change Dataset**.
	
	![](_static/images/UsingDataset_select.png "Figure 1: Change Dataset on the main page")
	
	[**Figure 1: Change Dataset on the main page**](_static/images/UsingDataset_select.png)
	
2.  A popup window appears that shows all the available datasets in a grid: each row represents one dataset, its main descriptive details split up in the columns. To use a dataset for further analysis, you click on the **Select** button in the first column.   
   If you prefer to first read extra information about the dataset of your interest, click on any other part of the specific row (dashed area).

![](_static/images/UsingDataset_select_selectbutton.png "Figure 2A: Select a dataset or read more in-depth information")

[**Figure 2A: Select a dataset with the select button or read more in-depth information (click in the dashed area)**](_static/images/UsingDataset_select_selectbutton.png)  

 When you click on any of the information cells of the dataset row (dashed area), an information panel below the grid shows background information about the data. Possible adjustments of the original data by the R2 team, such as data transformations or annotation changes, can be found in the Adjustments box of the information panel. At the bottom you will see links to the original data source and Pubmed resources, if available. 

![](_static/images/UsingDataset_click_information.png "Figure 2B: Read in-depth information about a dataset")
	
 [**Figure 2B:  Read in-depth information about a dataset**](_static/images/UsingDataset_click_information.png) 

3. A search bar is located on top of the page. It allows you to search for a dataset by (part of) a keyword, such as a tissue type, a disease or an author name.   
       When you start typing in the search bar, a list appears with datasets that correspond to your keyword. Also, the grid is adjusted to only show the datasets that fulfill your search requirement. 
   
    ![](_static/images/UsingDataset_select_dropdown_text.png "Figure 4: Use the search bar to filter the list of datasets with a keyword")
		
    [**Figure 4: Use the search bar to textually filter the list of datasets with a keyword**](_static/images/UsingDataset_select_dropdown_text.png)  
   
   You can simply scroll through the list with the mouse and get more information about a dataset with a click of the mouse on any dataset in this list.  
    This way you can quickly filter for a tissue type, a disease or an author name. In the picture above we type the letters "neurobl" to look for all Neuroblatoma datasets. 
   
4. You can use the buttons in the bottom right corner to scroll through the pages of the grid, to jump ahead to a specific page and to adapt the amount of dataset rows that are shown per page. 

    ![](_static/images/UsingDataset_scroll_through_grid.png "Figure 5: Adapt or scroll through the grid")
	
    [**Figure 5: Adapt or scroll through the grid**](_static/images/UsingDataset_scroll_through_grid.png) 
    
5. Click on the "Select" button in the grid to see the dataset of your choice appear on the main page in box 2 for further analysis.



----------

  ![](_static/images/R2d2_logo.png)**Did you know that datasets have an informative naming?**   Datasets have a structured naming in R2, using the following rules: type_of_dataset - author - number_of_samples - normalization - chiptype. The dataset selection grid consists of these informative parts as columns, each with filter options to perform an advanced search through the dataset.

  ![](_static/images/UsingDataset_understanding_dataset_names.png "The information parts of a dataset name")
	
  [**Figure 5: The informative parts of a dataset name correspond to the columns of the dataset selection grid.**](_static/images/UsingDataset_understanding_dataset_names.png) 

----------



Step 2: Advanced selection of datasets
---------------

1.  The grid itself enables the user to search through datasets using keywords and other filter options as well. The column dropdown functions and textboxes can filter the datasets for specific characteristics, e.g. datasets with a minimal amount of samples, or a specific author, platform or publication date. You can easily combine the search functions of the different columns.  
  
     As an example, we want to see which large neuroblastoma sets are available. First we write part of the word neuroblastoma in the search box of the Tissue/Tumor column. Then we use the pull down of the N (sample number) column to order the datasets in descending order. 
	
	![](_static/images/UsingDataset_combine_grid_filters.png "Figure 6: Combine search filters in the grid")
	
	[**Figure 6: Combine search filters in the grid**](_static/images/UsingDataset_combine_grid_filters.png)
	
2.  Again we use the **Select** button if we want to continue our analysis with a specific dataset of the grid. 
	
5.  Select “Across Datasets” in field **1**. Note that in field 2
    different options become available compared to the “single
    dataset” option.
   
	![](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png "Figure 6: Selecting across datasets")
	
	[**Figure 6: Selecting across datasets**](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png)
	
	Analysis methods following selecting the “Across Datasets” option in field **1** will be discussed in tutorial “Working with multiple datasets”.  


-------------
 ![](_static/images/R2d2_logo.png)**Did you know that clicking on an exclamation balloon provides additional info?**      

![](_static/images/UsingDatasets_information balloon.png)

-------------


Step 3: Using Dataset favorites
---------------

Since R2 is hosting hundreds of datasets, it could be handy to store the datasets you use often in a preselection that is easily accessible. In order for maintaining favorites, you need to be a registered user. If you did not yet register; Accounts can easily be created via "Login/Register"and are absolutely free. Clicking on the ''Change Dataset' will open the datasets page, where resources can be searched and selected.

![](_static/images/UsingDatasets_favorites.png "Figure 7: Change Dataset, to access favorites")
	
[**Figure 7: Change Dataset to access favorites**](_static/images/UsingDatasets_favorites.png)

Within the dataset selection table, you can select, deselect cohorts to add or remove them from your selection of preferred sets. This is done by using the favorites select boxes  in the last column on the right side. Favorite datasets will always be represented at the top of your selection table and will be marked with a green background color. This makes it very convenient to quickly have assess to those. 

![](_static/images/UsingDataset_selectfav.png "Figure 8: Managing favorites")
	
[**Figure 8: Managing favorites**](_static/images/UsingDataset_selectfav.png)


Step 4: Data Scopes
---------------

1.  R2 can also be forced to only display a sub-selection of all the datasets that are available (e.g. only neuroblastoma datasets). These are called data scopes and can be selected from within R2 by the left hand menu items 'Change Data Scope'. 
    From here you can use one of the preset scopes. 
    This is also the section where you can remove a scope that has been set. 
    One obvious reason why scopes can be handy, is the focussed view on the available data: 
    to restrict data to a particular subject or as a landing page for a specific publication/ subject.
    Datascopes as dedicated landing pages can also be configured to expose additional functionalities and quick jumps to sections in the platform. Just have a look at which ones are accessible given your access rights.  
2. Data scopes can be used directly from the internet address line, which can be handy when a referral needs to be made to R2 from a manuscript. For now, you do need to provide a link directly to the server (usually hgserver1.amc.nl/cgi-bin/r2/main.cgi?&dscope=NRBL).  

Further details on the use of Datascopes can be found in the tutorial Datascopes.   

----------
 ![](_static/images/R2d2_logo.png)**Did you know that the R2-support team is scanning public repositories for interesting datasets to expand the R2-database on a regular basis**      

> *In case you want to see a dataset added to R2 please send an email to r2-support@amc.nl  
> Such an email should contain a link to the publicly accessible files, such as a Gene Expression Omnibus number (GSE\*\*\*\*\*).* 
>
> *Your own private datasets can also be added to R2 with user/group restricted access. Please send us an email at* ***<r2-support@amc.nl>*** *and inquire on the procedure to get your data available in R2 (see also chapter 22).*

---------------



Final remarks / future directions
---------------------------------


Everything described in this chapter can be performed in the R2: genomics analysis and visualization platform (http://r2platform.com / http://r2.amc.nl) 


If you run into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).


We hope that this tutorial has been helpful, the R2 support team.



