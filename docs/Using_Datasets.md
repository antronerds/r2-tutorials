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

1.  In R2 a large amount of datasets are available for analysis
    and visualization. The numbered items in the main window will guide
    you through all the steps necessary to perform a task. In field
    **1** select “single dataset”, in field **2** choose "change"
	
	![](_static/images/First_image_select_dataset.png "Figure 1: In the main screen: Change dataset")
	
	[**Figure 1: In the main screen: Change dataset**](_static/images/First_image_select_dataset.png)
	
2.  A pull-down menu appears containing a large collection of datasets
    available for all types of analyses R2 is offering
3.  Click on the desired dataset.



![](_static/images/UsingDatasets_SelectSpecificDatasetFromPullDownInR2.png "Figure 2: Selecting datasets from the pull down menu on the main screen")

[**Figure 2: Selecting datasets from the pull down menu on the main screen**](_static/images/UsingDatasets_SelectSpecificDatasetFromPullDownInR2.png)

----------
 ![](_static/images/R2d2_logo.png)**Did you know that datasets have an informative naming?**      

> *Datasets have a structured naming in R2, using the following rules: **type_of_dataset - author - number_of_samples - normalization - chiptype**. Datasets are listed alphabetically*

----------



Step 2: Advanced selection of datasets
---------------

1.  Next to the pull down menu you can also choose for the “advanced
    dataset selection” tool. The advanced dataset selection facilitates
    searching through datasets using keywords and other filter options
    such as the minimal size of a dataset, the date a certain dataset
    was published etc. An example search would be finding all colon
    samples which are part of a mixed dataset consisting of normal
    tissue and tumor samples.
	
	![](_static/images/UsingDatasets_AdvancedSelectionLink.png "Figure 3: Advanced selection of datasets")
	
	[**Figure 3: Advanced selection of datasets**](_static/images/UsingDatasets_AdvancedSelectionLink.png)
	
2.  Click on the “Advanced” link. A new screen shows a table where the
    headers can be filled with search entries to fine tune your search
    for a dataset meeting your search criteria. Enter ‘Neuro’ in the
    Tissue/Tumor column and’ 50’ in the ‘\#’ column and select ‘ greater than’
    from the pull down menu. This returns all the datasets containing
    the search term ‘Neuro’ and having more than 50 samples. To have a quick glance at all available datasets, 
    change the value for 'Show rows' to the maximum. 
	
	![](_static/images/UsingDatasets_AdvancedSelectionPanelInR2.png "Figure 4: Advanced selection panel")
	
	[**Figure 4: Advanced selection panel**](_static/images/UsingDatasets_AdvancedSelectionPanelInR2.png)
	
3.  Click on the tekst 'neuroblastoma' in the third column of the dataset containing 88
    samples. A detailed info box is displayed below the table that contains additional dataset
    information from the R2 database. When the dataset is publicly
    available, clicking on the GEO ID link redirects to the GEO
    repository database where RAW data files are available. A Pubmed
    link is listed in case the dataset is linked to a publication listed
    in PubMed.
    Note: Clicking on an exclamation mark also shows detailed
    dataset information.  
    
4.  Click on 'select' in the first column to select the specific dataset for analysis and to return to the main page of R2.
	
	![](_static/images/UsingDatasets_AdditinalDatasetInfoInR2.png "Figure 5: Additional Dataset Info")
	
	[**Figure 5: Additional Dataset Info**](_static/images/UsingDatasets_AdditinalDatasetInfoInR2.png)
	
5.  Select “Across Datasets” in field **1**. Note that in field 2
    different options become available compared to the “single
    dataset” option.
	
	![](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png "Figure 6: Selecting across datasets")
	
	[**Figure 6: Selecting across datasets**](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png)
	

	Analysis methods following selecting the “Across Datasets” option in
field **1** will be discussed in tutorial “Working with multiple
datasets”.

-------------
 ![](_static/images/R2d2_logo.png)**Did you know that clicking on an exclamation balloon provides additional info?**      

> *Clicking on the GEO ID link redirects to the GEO repository database  
where RAW data files are available. A Pubmed link is listed in case the
dataset is linked to a publication listed in PubMed.*

![](_static/images/UsingDatasets_LinksToRawDataInR2.png)

-------------


Step 3: Data Scopes
---------------

1.  R2 can also be forced to only display a sub selection of all the datasets that are available. These are called data scopes and can be selected from within R2 by the left hand menu items 'Change Data Scope'. From here you can use one of the preset scopes. This is also the place where you can remove a scope that has been set. One obvious reason why scopes can be handy, is the focussed view on the available data: to restrict data to a particular subject or as a landing page for a specific publication/ subject.  

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



