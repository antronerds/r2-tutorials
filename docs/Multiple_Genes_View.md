<a id="multiple_genes_view"> </a>

Multiple Genes View
===================



*Analyze the expression levels of a group of genes within a dataset*



Scope
-----

-   Use R2 to investigate the expression levels of more than 1 gene
    within a specific dataset.
-   In this example the expression levels of small groups of genes
    listed from several pathways will be used showing which genes are
    differentially expressed per subgroup.
-   Adjust several parameters in the settings panel
-   In R2, the samples are annotated with e.g. clinical data. Each group
    of annotated data is called a "Track" in R2. These tracks can be
    used to split the group gene expression levels per track.




Step 1: Viewing multiple genes
---------------

1.  Use *Single Dataset* in field 1 and select the *Mixed Cholangiocarcinoma (2022-v32) - tcga - 44 - tpm - gencode36* dataset in field 2.
2.  Choose *View multiple Genes* in field 3 and Click 'Next'.
3.  To illustrate the possibilities of the multiple gene view, genes
    identified as classifiers for  Cholangiocarcinomea in literature 
    will be used. In the **Genes/Reporters** textbox type or copy
    the following genes: *S100P,KRT19,EPCAM,CEACAM5,GPC3*. Here, either use a comma to separate the genes without space between the comma and the next gene or type each gene on it own line to separate them and click 'Next'.
    
	![](_static/images/Multiplegeneview/MultipleGenesView_Default_1.png "Figure    1: Default multiple geneview.")
	
	[**Figure    1: Default multiple genes view.**](_static/images/Multiplegeneview/MultipleGenesView_Default_1.png)
	
4.  In the "Adjustable settings" panel below the graph **(Track Separations)** or in the "plot options" panel of the Gear-icon under the 'General' section **(Seperation track)**, you can select the grouping variable *sample_type* from the dropdown menu to separate your data into normal vs tumor tissue. When using the "plot options" panel, the 'Handle groups by' dropdown menu should be set to 'Separated by gene grouped by track'. Then, in the **Graph Type** dropdown menu of the "plot optoins" panel, choose *Average with stderr* and click Redraw Plot. This will generate visual subgroups in the gene representation.

    ![](_static/images/Multiplegeneview/MultipleGenesView_sepgene.png "Figure    2: Separated per group")
    	
    [**Figure    2: Adapted group padding**](_static/images/Multiplegeneview/MultipleGenesView_sepgene.png)
    	

Step 2: Viewing multiple genes through track annotation
---------------

1.  In Figure 1, a selection of gene expression profiles is depicted in
    one picture in contrast to the one gene view. Figure 2 shows the possibility to make gene subgroups. Adapting the **Box padding** makes the difference more clear, also the graph type is adapted. 
    Now we will look at the option to represent the gene expression separately for
    each subgroup of a categorical track. In this manner potential relations between subgroups and
    gene expression can be visualized.
2.  Here, we change to another dataset; *Mixed Colon Adenocarcinoma (v32) - tcga - 512 - tpm - gencode36* which contains a large collection of annotations including the CMS classification. Here, the classification of the dataset we are using is provided by R2 and is described in
    [Nat Med ](https://pubmed.ncbi.nlm.nih.gov/26457759/)2015 Nov;21(1) Guinney et al.. The classification of 4 molecular subtypes is described and annotated as such:
    CMS 1, 2, 3 and 4. To investigate the expression levels of a small group
    of genes, again *View multiple Genes* is chosen in field 3 and the following genes will be investigated; *BEST4,OTOP2,CDH3,BMP3*. Select the categorical track *cms_nearest_ssp* of the Colon cohort in the "Adjustable settings" panel at **Track separations** and click next. Use the "plot options" panel (opened by the Gear-icon) to adapt **Handle groups by**: *separated by gene grouped by track*, **Separation Track**: *cms_nearest_ssp*, tick *add scatter*, adapt **Dot size**: *0.5* and select at **color mode** & **color mode (groups)**; *color by track*. There is no need to click **redraw plot** in the "plot options" panel, the graph is adapted on the fly.

	![](_static/images/Multiplegeneview/MultipleGenesView_perTrack_v2.png "Figure    3: Multiple gene view per subgroup")
	
	[**Figure    3: Multiple gene view per subgroup**](_static/images/Multiplegeneview/MultipleGenesView_perTrack_v2.png)
	


3.  The genes used in this example are the result of a Differential Expressed Gene analysis comparing normal to tumor tissue in this cohort.
    In Figure 3, the gene names and the subgroup labels CMS1, CMS2, CMS3 and CMS4 are concatenated on the x-axis. The grouping per track gives more insight how the genes are expressed for each each subgroup.
4.  Also try *separated track grouped by gene* in the **Handle groups by**. This which will produce an image
    where the genes are shown, separated by the subtypes. By setting **Handle groups by** to *group by panel* in the "plot options" panel, the same information will be displayed in a multifaceted graph with separate panels for each sub-group of the chosen track (**Figure 4**). 
    
	![](_static/images/Multiplegeneview/MultipleGenesView_perpanel_v2.png "Figure    4: Multiple gene view, panel per subgroup")
	
	[**Figure    4: Multiple gene view, panel per subgroup**](_static/images/Multiplegeneview/MultipleGenesView_perpanel_v2.png)
	


5. The sample filter option in the "Adjustable settings" panel allows you to generate a multiple gene view representation, that can also depict parts of the data set using subsets, as is available throughout R2. For example you could choose to exclude one or more of the subgroups or use another track to make any intersection you would like to use.

6. In some situations, you may want to highlight one or more samples of patients from a dataset in the multiple gene view. This is easily achieved when using the R2 samplename. Let's try it with one of the patients within this tcga Colon cohort (*tcga-cm-6169-01a_v32*). If you know the samplename, go to the 'Marked' section in the "plot options" panel. To mark this sample, we simply paste the samplename (*tcga-cm-6169-01a_v32*) in the **id** field and the plot will be automatically updated. Note, that you can also click the dot in graph in case the scatter option is turned on to highlight the samples of interest. By using the options provided in the 'Marked' section you can tweak the result to your personal taste.

   ![](_static/images/Multiplegeneview/MultipleGenesView_mark_v1.png "Figure    5: Multiple gene view, mark a sample")

   [**Figure    5: Multiple gene view, mark a sample**](_static/images/Multiplegeneview/MultipleGenesView_mark_v1.png )

7. The graph can be stored as a png and/or svg output to use upon publication and adapt in vector supported programs as Adope illustrator or Incape by clicking the desired format in the 'Save" section of the "plot options" panel (**Figure 5a**).

![](_static/images/Multiplegeneview/MultipleGenesView_saveoptions.png "Figure 5a: Multiple gene view, mark a sample")

[**Figure    5a: Multiple gene view, save options**](_static/images/Multiplegeneview/MultipleGenesView_mark_v1.png )


Step 3: View multiple genes (Bubble plot)
---------------

1. Up to now, we have used the more classical graphs to look at more than 1 gene at once within a dataset. Within R2, you can also depict multiple genes in a graphical format that is often used within single cell analyses, called 'bubble plots'. A bubble plot shows the average expression of genes (optionally within different groups contained in a track) as a color representation in a grid. Every cel in this grid is then drawn as a circle, such that the surface area reflects the ratio of the samples within such a group that is considered to be expressed (having a Present call within R2). 

   So let's have a look and explore this feature in a scRNA dataset first. From the main page, we first select a data set in field 2 called : *Cell line Neuroblastoma 13 cell lines - Chapple - 35323 - seurat_cp10k - ensh38e98*. This resource contains 13 neuroblastoma cell lines, measured by 10x Genomics technology. 


2.  From field 3 we then select 'View multiple Genes (bubble plot)' and progress to the next page. Since we will work with a large resource, the first time loading this page might take a few seconds. 

    At first not much is shown. Now paste the following genes in the **Genes/Reporters** box *PHOX2A,DBH,ALK,CD24,PRRX1,CD44* and click 'next'.  We now see 1 row of circles, where the color represents the expression of the different genes, and the size of the circles displays the ratio of cell showing expression (**Figure 6**.
    ![](_static/images/VMGB_bubble_1.png "Figure    4: Multiple gene view (bubble), 1")

    [**Figure    6: Multiple gene view (bubble), 1**](_static/images/VMGB_bubble_1.png)

3. We can also use a track, to separate the cells (or samples in case of a bulk dataset). Let's adjust the **Track** in the "Adjustable settings" panel to *cell_line* and press 'next'. We can now see 13 rows of circles, one row for every cell line. This is starting to look more interesting, as not every gene seems to be equally expressed in the different cell lines (**Figure 7**).

   ![](_static/images/VMGB_bubble_2.png "Figure    4: Multiple gene view (bubble), 2")

   [**Figure    7: Multiple gene view (bubble), 2**](_static/images/VMGB_bubble_2.png)

4. We can also reorganize the genes, by putting them in a different order. It is  possible to group the genes, by adding an additional comma(,). Let's try the following order *PHOX2A,CD24,DBH,ALK,,PRRX1,CD44* in the **Genes/Reporters** box and press 'next'. The image looks more organized now (**Figure 8**). 

   ![](_static/images/VMGB_bubble_3.png "Figure    4: Multiple gene view (bubble), 3")

   [**Figure    8: Multiple gene view (bubble), 3**](_static/images/VMGB_bubble_3.png)

5. By default the circle areas are represented as a proportion of the complete dataset. To not end up with very small circles, the largest identified proportion is chosen as the maximal bubble width, and all the others are scaled proportionally. This allows you to see the expression in those cells that have a signal, but keeping in mind that not every cell line has equal numbers of cells. If you are not interested in the relative numbers between the different cell lines, then adjust the **Scale bubble by** drop down to *group size proportion* and press 'next'. The image now reflects how the different genes are proportionally expressed by row (**Figure 9**). 

   ![](_static/images/VMGB_bubble_4.png "Figure    4: Multiple gene view (bubble), 4")

   [**Figure    9: Multiple gene view (bubble), 4**](_static/images/VMGB_bubble_4.png)

6. As with many plots in R2, you can also use different transformations, color schemas or make the circles bigger etc. Hovering over the circles will show the statistics of the circle, which may be helpful when exploring the data.

   ![](_static/images/VMGB_bubble_5.png "Figure    4: Multiple gene view (bubble), 5")

   [**Figure    10: Multiple gene view (bubble), 5**](_static/images/VMGB_bubble_5.png)

7. As will be explained in Chapter 16 "Sample maps: t-SNE / UMAP, high dimensionality reduction in R2" of the tutorials book, single cell sequencing data is often explored in so called 'UMAP' plots. These are also available in R2 via the panel on the left side under 'Sample maps (UMAP/tSNE)'. Here, again *Cell line Neuroblastoma 13 cell lines - Chapple - 35323 - seurat_cp10k - ensh38e98* can be selected and the expression of a gene, or annotation features in our interactive plots can be explored. Combining some of these functions will enable you to test hypotheses, and produce images for your next publication ;)

   ![](_static/images/VMGB_bubble_6.png "Figure    4: Multiple gene view (bubble), 6")

   [**Figure    11: Multiple gene view (bubble), 6**](_static/images/VMGB_bubble_6.png)

Finally, we have now used these bubble plots in a single cell dataset, where they are very well suited to convey both expression level, as well as 'proportion expressed' information. These plots can be equally informative in many of the bulk expression data sets that are provided within the R2 platform. In many data sets a notion of 'is expressed' is also captured in the 'present call' variable. 

Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amsterdamumc.nl).



Everything described in this chapter can be performed in the R2: genomics analysis and visualization platform ([http://r2platform.com](http://r2platform.com) / [https://r2.amc.nl]( https://r2.amc.nl)).



We hope that this tutorial has been helpful,  
the R2 support team.

