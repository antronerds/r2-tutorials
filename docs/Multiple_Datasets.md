<a id="multiple_datasets"> </a>


Multiple datasets overview with Megasampler
===========================================


*Create an overview of the expression level of a single gene in multiple
datasets*



Scope
-----

-   The megasampler is a R2 module to investigate the expression level
    of a gene in any number of the numerous datasets stored in the R2
    database
-   Use R2 to compose your selection of datasets to investigate the
    expression level of a gene
-   Use the megasampler "adjustable settings" to adapt the megasampler
    graphics
-   The megasampler allows you to quickly get an overview of the
    selected gene expression level for all the datasets available in the
    R2 database
-   Go directy from the overview to one-gene view to investigate in
    detail the expression level in a single dataset.


Step 1: Selecting multiple datasets
---------------

1.  Use "Across Datasets" in field 1 by default the "megasampler" option
    is selected in field 2 and click "next".
    
	![Figure 1: Using across datasets](_static/images/MultipleDatasets_across.png "Figure 1: Using across datasets")
	
	[**Figure 1: Using across datasets**](_static/images/MultipleDatasets_across.png)
	
2.  Leave "u133p2, mas5.0" at the "type of data" option and select " XPO
    sampler" at "use presets". The meaning of presets will be explained
    later on.

--------------------------------------------------------------------------
![](_static/images/R2d2_logo.png)**Did you know that R2 harbours different types of microarray platforms**

![Multiple dataset selectiong](_static/images/MultipleDatasets_Select.png)             
                                                                          
> *Megasampler only allows you to query multiple datasets if they are of the same chiptype and normalized by the same algorithm and of certain normalizations.*

--------------------------------------------------------------------------

1.  With the "selection preset" option a pre-stored dataset collection
    with associated settings can be selected. Select "XPO sampler"
    (Expression Project for Oncology (expO)) to pre-select a series of
    tumor datasets. Click "next".
    
	![Figure 2: Select a preset](_static/images/MultipleDatasets_Preset.png "Figure 2: Select a preset")
	
	[**Figure 2: Select a preset**](_static/images/MultipleDatasets_Preset.png)
	
2.  In the previous screen the preset "XPOsampler" is selected, a
    collection of datasets is already marked for the
    megasampler analyses. In Figure 3 clicking the small triangle
    unfolds the available dataset categories, notice that some of the
    datasets in the "tumor" section are already marked. In this way this
    you can adapt your pre-selection of datasets. Unfold the normal and
    tumor category and select the following datasets. Normal Adrenal
    gland - Various " 13, Normal Brain PFC - Harris " 44 and the " Tumor
    Neuroblastoma public - Versteeg " 88" . Enter MYCN and click "next".
    
	![Figure3: Megasampler adjustment selection](_static/images/Pathway_menu.png "Figure3: Megasampler adjustment selection")
	
	[**Figure 3: Megasampler adjustment selection**](_static/images/Pathway_menu.png)
	

--------------------------------------------------------------------------
![](_static/images/R2d2_logo.png)]**Did you know that private datasets linked to a specific user are indicated with a green background color**

![Add a private dataset](_static/images/MultipleDatasets_Didyou1.png)

> *Add a private dataset to the (pre) selected datasets.*

--------------------------------------------------------------------------


Step 2: Viewing a gene in multiple datasets
---------------



1.  In the "adjustable settings" panel there are several options to
    customize the megasampler graph. For every selected dataset, you can
    change the order in which they are drawn by adjusting the number in
    the selection boxes. These are processed first, followed by the
    dataset names in alphabetical order (so changing the order of 1 or 2
    datasets should be sufficient). The pull down next to "dataset
    ordering pull down menu" enables to split one or more dataset by
    selecting a track , in this manner the chosen dataset(s) will be
    split according to the numbers of groups of the selected track.
2.  For now change the color for the datasets as indicated in Figure 4
    and click "next".
    
	![Figure 4: Adjusting the megasampler graph.](_static/images/MultipleDatasets_AdjustGraph.png "Figure 4: Adjusting the megasampler graph.")
	
	[**Figure 4: Adjusting the megasampler graph.**](_static/images/MultipleDatasets_AdjustGraph.png)
	
3.  R2 now performs a one-way Anova statistical test on the fly. This
    **AN**alyis **O**f **VA**riance is a statistical test that
    calculates whether the means of the expression levels between the
    selected datasets are significant different.

	![Figure 5: Anova test for the selected datasets.](_static/images/MultipleDatasets_Anova.png "Figure 5: Anova test for the selected datasets.")
	
	[**Figure 5: Anova test for the selected datasets.**](_static/images/MultipleDatasets_Anova.png)
	

By default de megasampler graph is plotted in a so called Boxdotplot
representation. The Boxdotplot shows a combined boxplot, on top of which
the signals of the separate samples are plotted; a quickly interpretable
graph.


![Figure 6: MYCN expression levels in 15 datasets covering 2173 samples.](_static/images/MultipleDatasets_YCC-express.png "Figure 6: YCC expression levels in 15 datasets covering 2173 samples.")

[**Figure 6: MYCN expression levels in 15 datasets covering 2173 samples.**](_static/images/MultipleDatasets_YCC-express.png)


Additional insight can be obtained transforming the data, in this case
transform the data to logical values (none) set "graphtype" on barplot
and click on "redraw at the bottom of the screen.


![Figure 7: Different Megasampler graphical representations](_static/images/MultipleDatasets_Representations.png "Figure 7: Different Megasampler graphical representations")
	
[**Figure 7: Different Megasampler graphical representations**](_static/images/MultipleDatasets_Representations.png)
	

The plotted graphs for "MYCN" clearly show a high expression level
specifically in the Neuroblastoma data sets compared to Normal Tissue
and other Tumor datasets. At the bottom of the page it"s possible to
adapt dataset coloring, change the order and split datasets in tracks
directly.



--------------------------------------------------------------------------
![](_static/images/R2d2_logo.png)**Did you know that you can save your selection of datasets and select your stored dataset the next time you login to R2.**

![](_static/images/MultipleDatasets_Didyou2.png)

![](_static/images/UsingDatasets_LinksToRawDataInR2.png)
                         
> *Storing a preset not only stores the selection of datasets for future use, but will also remember all of the other settings such as order,
colors, plot type etc. In essence you can generate the same visual representation for any other gene in this way.*

--------------------------------------------------------------------------



You can can use the adjustable panel to adapt the megasampler graph. In
case you splitted one or more datasets according to a specific track in
the previous screen, it"s now possible to skip subgroups from your
dataset or more interesting, apply different colors for groups within a
dataset (see Figure 8).

![Figure8: Adjustable settings panel, color groups within adataset.](_static/images/MultipleDatasets_AdjustGroups.png "Figure8: Adjustable settings panel, color groups within adataset.")
	
[**Figure8: Adjustable settings panel, color groups within adataset.**](_static/images/MultipleDatasets_AdjustGroups.png)
	





Step 3: Expression distribution over many datasets
----------------



The red arrow in the "did you know box" indicates a handy module to
obtain a quick overview of the expression level patterns for most of the
datasets R2 contains (providing that the normalization allows
comparisons between datasets).



1.  Click "view Expression in many datasets" and a new screen (or Tab)
    appears depicting colored dots. The colored dots are representing
    the different dataset categories (cell line dataset, Tumor or Normal
    Tissue etcetera). Via this module (effectively the 2D distribution)
    you can easily detect in what way your probeset of interest is
    expressed in many other datasets. At the Y-axis the 2log transformed
    average expression level and the standard deviation is represented.
    The X-axis "overlap avoider" is simply a means to represent all
    datasets in the plot without overlap of the circles. Figure 9
    clearly shows that the MYCN expression is also high in other dataset
    which could be of interest and a second Neuroblastoma dataset. Next
    to the graphs 2 tables summarize dataset names and a R-value set
    to "1. The R-value comes of use with the 2D-distrubution module
    where you can quickly scan the correlation between two genes for all
    datasets of the same platform in R2. This module is discussed in the
    correlate genes tutorial.
    
	![Figure 9: MYCN expression level distribution for all u133-2 datasets in R2.](_static/images/MultipleDatasets_LevelDistribution.png "Figure 9: MYCN expression level distribution for all u133-2 datasets in R2.")
	
	[**Figure 9: MYCN expression level distribution for all u133-2 datasets in R2.**](_static/images/MultipleDatasets_LevelDistribution.png)
	
2.  Via the the probeset distribution view you can easily investigate a
    specific dataset in more detail.Click a preferred colored dataset
    dot and R2 will generate an one-gene-view graph. The one-gene-view
    representation is explained in more details in tutorial 2.
       
Step 4: Megasearch
----------------

We have already discussed the find differential expression module for a single dataset to find differentially expressed genes.
In the across dataset section  we can also apply a similar approach, not between groups within 
single dataset but for a user defined selection of multiple datasets. However, keep in mind that you can only
select datasets of the same platform,  the most abundant datasets are of the Affymetrix u133p2 platform. As explained
before not every platform can be used for the megasearch due to the normalisation procedure which has been used.

 ![Figure 10: Select the megasearch option.](_static/images/Megasampler_Select1.png "Figure 10: Megasearch select.")
	
 [**Figure 10: MYCN expression level distribution for all u133-2 datasets in R2.**](_static/images/Megasampler_Select1.png)
	
 
 
1. At step 1 select the platform you want to use the most common is the u133p2 platform and click next. 

2. Select type of platform and click next.

3. In the next step select the datasets of interest and click next.

4. Select the datasets you want to use  for the analyses in this example we selected  some \Normal brain , AML and Medulloblastoma datasets
, click next.

 ![Figure 11: Select the megasearch option.](_static/images/megasampler_selectsdatasets.png "Figure 11: Selecting datasets for analyses in R2.")

 [**Figure 11:  Dataset selection **](_static/images/megasampler_selectsdatasets.png)
5. For the megasearch two groups only can be applied to find the statistical difference between the groups.  In the settings box assign the proper group parameters (1 or 2) leave the pulldowen menu at their default settings for the datasets and click
next. 

 ![Figure 12: Select the megasearch option.](_static/images/megasampler_selectsdatasetsgroups.png "Figure 12: Assign the statistical group for testing.")

 [**Figure 12: Assign the statistical group for testing**](_static/images/megasampler_selectsdatasetsgroups.png)
 
6. In the next adjustable settings menu select at Genecategory 'transcription regulator Act' for filtering.  In the 'Hugoonce Dataset' the first selected dataset will be used as target dataset for probeset usage.
This needs some explanation, for the most platforms each gene has multiple probesets for many analysis in R2 the probeset with the highest average signal is used.  For the megasearch you can not use for
each dataset an different probeset for a particular gene. In the 'Hugooce Dataset' pulldown menu you can change the target dataset in case you already familar with one of the selected datasets
to make sure that probesets from single datasets analysis are used. In case of OTX2 which is a marker gene for Medulloblastoma two probesets are designed (242128_at and 231731_at) in
Medulloblastoma dataset 242128_at has the highest expression level and will be picked by R2 however in other type of cancers/tissues there is hardly any expression of the OTX2 gene
in that case the other probeset could easily be selected.










---------------
  ![](_static/images/R2d2_logo.png)**Did you know that the Megasampler can also be used to look through the methylation datasets**

---------------





Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.





