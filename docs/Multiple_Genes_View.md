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

1.  Use "single dataset" in field 1 and select the "Tumor
    Medulloblastoma PLoS One - Kool - 62 - MAS5.0 - u133p2" dataset in
    field 2.
2.  Choose "View multiple genes " in field 3 and Click Next
3.  To illustrate the possibilities of the multiple gene view, genes
    identified as classifiers for Medulloblastoma subtypes (Kool et al,
    Plos one) will be used. In the GENE/reporter textbox type or copy
    the following genes: AXIN2,BOC,dkk2,GABRA5,PTCH1,SMARCD3,WIF1
    and click next.
    
	![](_static/images/MultipleGenesView_Default.png "Figure    1: Default multiple geneview.")
	
	[**Figure    1: Default multiple genes view.**](_static/images/MultipleGenesView_Default.png)
	
4.  Under the graph many settings can be adjusted in the Adjustable settings box. For instance,
    you can choose a different type of graph. Next to the option to influence the space between the genes, the height of the plot etc, you can add one or more extra spaces between genes of choice by adding one or more extra delimiters. 
    In the GENE/reporter textbox add 2 extra comma's behind dkk2 (AXIN2,BOC,dkk2,,,GABRA5,PTCH1,SMARCD3,WIF1); 
    in the field 'Plot type' select "Average with stderr", set 'Transform' to  and click next. This enables the creation of visual subgroups in the gene representation. 
    ![](_static/images/MultipleGenesView_ExtraSpacer.png "Figure    2: Add a spacer between genes")
    	
    [**Figure    2: Add a spacer between genes**](_static/images/MultipleGenesView_ExtraSpacer.png)
    	

Step 2: Viewing multiple genes through track annotation
---------------

1.  In Figure 1 a selection of gene expression profiles is depicted in
    one picture in contrast to the one gene view. Figure 2 shows the possibility to make gene subgroups by adding extra spacers to the plot.  
    Now we will look at the option to represent the gene expression separately for
    each subgroup of a categorical track. In this manner potential relations between subgroups and
    gene expression can be visualized.
2.  The dataset we are using is described in
    [PLoS One.](http://www.ncbi.nlm.nih.gov/pubmed/18769486)"2008
    Aug 28;3(8), Kool M et al. Here the classification of 5
    medulloblastoma subgroups are reported and annotated as such:
    A,B,C,D and E. To investigate the expression levels of a small group
    of genes per subgroup of the categorical track "subtypes" of medullablastoma cells, select in the Adjustable settings box
    "subtype (5 cat)" at 'use track', "lump by group plot gene" at 'handle
    groups by' and "Track" at 'color by track'. Further set 'Transform' to
    "none", select "boxplot" at 'Plot type' and click NEXT.

	![](_static/images/MultipleGenesView_perTrack.png "Figure    3: Multiple gene view per subgroup")
	
	[**Figure    3: Multiple gene view per subgroup**](_static/images/MultipleGenesView_perTrack.png)
	


3.  Most of the overexpressed genes are part of the WNT (subgroup A) and de SHH
    (subgroup B) signaling pathway as shown by Kool et al.  
    In Figure 3, the gene names and the subtype labels a,b,c,d and e are concatenated on the x-axis. 
    The Medulloblastoma molecular subtypes clearly show different expression profiles, with an overexpression of genes 
    in subgroup a and b. 
4.  Also try the "lump by gene plot group" which will produce an image
    where the genes are shown, separated by the subtypes. The "group by panel" option under 'handle groups by'
    will display the same information in a multifaceted graph with separate panels for each sub-group of the chosen track. 
    
	![](_static/images/MultipleGenesView_perTrack_v1.png "Figure    4: Multiple gene view, panel per subgroup")
	
	[**Figure    4: Multiple gene view, panel per subgroup**](_static/images/MultipleGenesView_perTrack_v1.png)
	


5. The sample filter option allows you to generate a multiple gene view representation, that can also depict parts of the data set using subsets, as is available throughout R2. For example you could choose to exclude one or more of the subgroups, or use another track to make any intersection you would like to use.

6. In some situation, you may want to highlight one or more samples or patients from a data set in the multiple gene view. This is easily achieved, if you use the r2 samplename. Lets try it with one of the patients within this medulloblastoma cohort ('itcc0334'). To mark this sample, we simply paste the samplename in the 'samples to mark' field and update the plot. Using the options provided by the settings you can tweak the result to your personal taste.

   ![](_static/images/MultipleGenesView_mark.png "Figure    4: Multiple gene view, mark a sample")

   [**Figure    5: Multiple gene view, mark a sample**](_static/images/MultipleGenesView_mark.png)

7. To use the generated image in programs like Powerpoint, you can 'right-click' on the image and 'copy' it to the clipboard. A simple paste will then put the figure in your presentation. You can also store the file as a 'svg' vector file on your computer. Using this reoute, you are also able to adapt the figure in a program like Adobe Illustrator, or Inkscape.



Step 3: View multiple genes (Bubble plot)
---------------

1. Up to now, we have used the more classical graphs to look at more than 1 gene at once within a data set. Within R2, you can also depict multiple genes in a graphical format that is often used within single cell analyses, called 'bubble plot'. The concept here shows the average expression of genes (optionally within different groups contained in a track) as a color representation in a grid. Every cel in this grid is then drawn as a circle, such that the surface area reflects the ratio of the samples within such a group that is considered to be expressed ( having a Present call within R2). 

   So let's have a look and explore this feature in a scRNA dataset first. From the main page, we first select a data set called : '**Cell line Neuroblastoma 13 cell lines - Chapple - 35323 - seurat_cp10k - ensh38e98**'. This resource contains 13 neuroblastoma cell lines, measured by 10x Genomics technology. 

2.  From the option box 3 we then select 'view multiple genes (bubble plot)' and progress to the next page. Since we will work with a large resource, it may take a few seconds for the page to finish loading the 1st time that you use it within your current session. 

    At first nothing much is shown. Now paste a few genes in the 'genes' box "PHOX2A,DBH,ALK,CD24,PRRX1,CD44" and press 'next'.  We now see 1 row of circles, showing the expression of the different genes in the color representation, and the ratio of cell showing expression as the size of the circles
    ![](_static/images/VMGB_bubble_1.png "Figure    4: Multiple gene view (bubble), 1")

    [**Figure    6: Multiple gene view (bubble), 1**](_static/images/VMGB_bubble_1.png)

3. We can also use a track, to segregate the cells (or samples in case a bulk data set is used). Let's use the 'cell_line' track and press 'next' again. We can now see 13 rows of the circles, one row for every cell line. This starts to look more interesting, as not every gene seems to be equally expressed in the different cell lines.

   ![](_static/images/VMGB_bubble_2.png "Figure    4: Multiple gene view (bubble), 2")

   [**Figure    7: Multiple gene view (bubble), 2**](_static/images/VMGB_bubble_2.png)

4. We can also reorganize the genes, by putting them in another order. It is also possible to 'group' the genes, by adding an additional ','. Let's try the following order "PHOX2A,CD24,DBH,ALK,,PRRX1,CD44" and press 'next' again. The image looks more organized now. 

   ![](_static/images/VMGB_bubble_3.png "Figure    4: Multiple gene view (bubble), 3")

   [**Figure    8: Multiple gene view (bubble), 3**](_static/images/VMGB_bubble_3.png)

5. By default the circle areas are represented as proportion of the complete data set. To not end up with very small circles, the largest identified proportion is chosen as the maximal bubble width, and all the others are scaled proportionally. This allows you to see the expression in those cells that have a signal, but also that not every cell line has equal numbers of cells. If you are not so much interested in the relative numbers between the different cell lines. then we use the 'scale bubble by' drop down and use 'group size proportion'. Press 'next' again. The image now reflects how the different genes are proportionally expressed by row. 

   ![](_static/images/VMGB_bubble_4.png "Figure    4: Multiple gene view (bubble), 4")

   [**Figure    9: Multiple gene view (bubble), 4**](_static/images/VMGB_bubble_4.png)

6. As with many plots in R2, you can also use different transformations, use other color schemas or make the circles bigger etc. Hovering over the circles will also show you the statistics for a circle, that may be helpful when exploring the data.

   ![](_static/images/VMGB_bubble_5.png "Figure    4: Multiple gene view (bubble), 5")

   [**Figure    10: Multiple gene view (bubble), 5**](_static/images/VMGB_bubble_5.png)

7. As will also be explained in the dimensionality reduction tutorial of the tutorials book, single cell data is often explored in so called 'UMAP' plots as well. These are also available in R2 via the 'menu' at the left side named 'sample maps'. Using that route, you can also explore the expression of a gene, or annotation features in our interactive plots. Combining some of these functions will enable you to test hypotheses, and produce images for your next publication ;)

   ![](_static/images/VMGB_bubble_6.png "Figure    4: Multiple gene view (bubble), 6")

   [**Figure    11: Multiple gene view (bubble), 6**](_static/images/VMGB_bubble_6.png)



Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amsterdamumc.nl).



Everything described in this chapter can be performed in the R2: genomics analysis and visualization platform (http://r2platform.com / https://r2.amc.nl).



We hope that this tutorial has been helpful,  
the R2 support team.

