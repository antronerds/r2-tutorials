
<a id="tSNE_dimensionality_reduction"></a>

t-SNE: high dimensionality reduction in R2
========================================


*How to find groups in your dataset using t-SNE.*


Scope
-----

-  In this tutorial several expression datasets will be used.
-  t-SNE will be used to find sub groups in datasets.
-  t-SNE maps will be annotated with tracks and the expression of genes



t-SNE 

A clustering tool which gaining more and more popularity in biomedical research, is the so called t-SNE algorithm.  t-SNE stands for t-Distributed Stochastic Neighbor EMbedding and is a machine learning dimensionality reduction algorithm that is well suited for the reduction of high dimensional datasets to 2 or three dimensions. 

Most researchers are already familiar with another dimensionality reduction algorithm  called PCA also supported by R2 and explained  in more detail in this tutorial. Both PCA and the t-SNE both reduces the dimension and captures the structure of high dimensional data. However,  PCA can only captures linear structures where the t-SNE algorithm captures non-linear relations and preserves local distances in high dimensions while reducing the information to 2 dimensions (an XY plot).

Another feature of  t-SNE is the so called perplexity which is a tunable parameter. This parameter is in a sense,  an estimation how many neighbors each point has. The robustness of the found clusters with the t-SNE algorithm can be validated to view the clusters for a number of perplexities. Typical values for perplexity are between 5-50. Once you have selected a dataset and applied the t-SNE algorithm, R2 will calculate the t-SNE clusters for 5 to 50 perplexities. Which perplexity is the best one depends on the structure of the dataset, and is also a matter of taste (how the samples are placed). Before you start analyzing and interpreting these very nice visualizations, it is highly recommended to read about the power and pitfalls of t-SNE in a blog-post that is also linked to from within the R2 interface.

Since running t-SNE  algorithm is  a time consuming task and can take up to hours of processing time for large datasets, R2 stores the results for every dataset where the t-SNE has been completed. All users of R2, can explore generated t-SNE maps, by coloring for tracks or expression values of a particular gene. Furthermore, the perplexity sweeps can be visualized. These options can be accessed via the left menu structure in R2. Users with collaborator, or higher access, are also able to initiate the generation of maps for datasets, or subsets within a dataset. These additional options will be available via ‘box 3’ on the main page of R2.

Step 1: Selecting t-SNE maps
----------------------------

Let’s have a look at a t-SNE result to see what we can learn from this dimensionality reduction algorithm. The analysis is most informative with the larger datasets, and actually requires more than 16 samples as an absolute minimum (in R2). We will first have a look at the CCLE (cancer cell line encyclopedia) dataset which is comprised of more than 900 cell lines from various cancers.

1.  In the left menu click on t-SNE maps and select in the pull down menu , ‘Cellline Cancer Encyclopedia - Broad - 917 - MAS5.0 - u133p2
2. R2 will assess will collect the result and provide a button to start exploring the result. Click on the button

	![Figure    1: t-SNE preprocessed t-SNE maps](_static/images/Tsne_select_preprocessed.png "Figure 1:Selecting t-SNE maps")
  
	[**Figure    1: t-SNE preprocessed t-SNE maps**](_static/images/Tsne_select_preprocessed)
	
4.  Click "next"


Step 2: Annotating t-SNE maps
----------------------------

In this screen the t-SNE result is plotted with the highest perplexity, or a preset value that has been selected upon manual curation. There is no strict rule to select the ‘best’ perplexity. In most cases the highest perplexity is not the best choice to investigate the cluster further.  If the perplexity result is something other than 23, then select this perplexity value. We can see structure in the location of the various cell lines. We would like to look at the annotations that are available for the cell lines. 


1. In the 'adjustable settinsg box' set "perplexity' to the value of 23
2. Select ‘color by track’ from the ‘colormode’ and choose ‘primary ite’. Press ‘next to redraw the image.’

	![Figure    2: t-SNE preprocessed t-SNE maps](_static/images/Tsne_cellbroad_primsite.png "Figure 2:Coloring by Track")
  
	[**Figure 2: t-SNE preprocessed t-SNE maps**](_static/images/Tsne_cellbroad_primsite.png)


Another feature that may be informative in the context of a t-SNE map is to ‘overlay’ the expression of a particular gene on the map by coloring the cell lines by the expression values of a dataset, in this case mRNA gene expression. We can have a look at this by changing the ‘colormode’ to ‘color by expression’.

1. In the 'adjustable settings box'  select 'Color by Gene'  at Color mode and subsequently type 'CLDN3' as Gene for color ,  corresponding reporter will automatically pop-up (Figure 3 ).It can take a little bit of time before the gene selection box appears. 

	![Figure    3: t-SNE_select_probeset](_static/images/Tsne_select_probeset.png "Figure 3: Select  A probeset")

	[**Figure 3: t-SNE_select_probeset**](_static/images/Tsne_select_probeset.png)

	
2. Again click ‘next’ to refresh the view.’  In this view the samples are not colored by a group annotation (track) but by their gene expression using a color gradient.  In this sample you can observe  a subgroup of the carcinoma samples which have higher level in contrast to the (carcinoma) samples. 

	![Figure    4: t-SNE_Color by Gene ](_static/images/Tsne_cellbroad_colorbygeneCLDN3.png "Figure 4: Select  A probeset")

	[**Figure 4: t-SNE_Color by Gene **](_static/images/Tsne_cellbroad_colorbygeneCLDN3.png)

3. Use  the track histology_subtype1 to generate a new t-SNE plot in the 'Adjustable settings' menu.  It appears that the subgroup which was striking by the color gradient are mostly adenocarcinoma' another gene which emphasizes the observation in the previous example is the NR3c1 gene showing an inverse gradient pattern for this subgroup.

	![Figure    5: t-SNE_Color by Gene ](_static/images/Tsne_cellbroad_colorbygeneNR3C1.png "Figure 4: Select  A probeset")
	
	[**Figure 5: t-SNE_Color by Gene **](_static/images/Tsne_cellbroad_colorbygeneNR3C1.png)


Step 3: Perplexity sweeps for t-SNE maps
----------------------------

Which perplexity value is the best option for your dataset of interest depends on the embedded structure (the subgroups), and even a bit on taste (the way the samples are layed out). To assess the robustness of the layout as well as the effect that the perplexity parameter has, the R2 platform performs a perplexity sweep. The analysis will be ran repeatedly, starting with a value of 5, and stopping at a perplexity value of 50 if the size of the dataset permits (n/3-1). 


1. In order to generate an overview of all possible perplexities  set in the "Adjustable Settings" the number of perplexities to "ALL" and for a  more clear  set the color by track modus to eg: histology.

	![Figure   6: t-SNE: all perplexities ](_static/images/Tnse_cellbroad_allperplexity.png "Figure 6: All perplexities")
	
	[**Figure 6: t-SNE: all perplexities **](_static/images/Tnse_cellbroad_allperplexity.png)
	

	
By choosing the perplexity values 'All', miniature tiles will be generated for all perplexities (5-50), where it is still possible to use the color by track mode.



Step 4: Creating t-SNE maps
----------------------------

Depending on your access level in R2, you are also able to create t-SNE maps from any dataset that is represented in R2 (with at least 16 or more samples). The t-SNE module will be located in 'box 3' at the main page of R2. You can either run the algorithm on the complete dataset, or focus on a particular sub-section of the samples using the 'subset' function. 

Lets take a look at some other nice examples of R2 generated t-SNE maps. Such as very large dataset of normal tissue expression profiles

1. In main menu select  Normal tissues - GTEX - 2921 - RPKM - ensgtexv4 en box2 and select T-SNE. If the 'default' map has already been calculated, a shortcut button will also appear as shown by the dashed box in figure 7. In the 'Adjustable settings' you can adjust severall settings such as sample filtering ,specific gene categories and expression level restrictions.  

	![Figure   7: t-SNE: Menu ](_static/images/Tnse_shortcutPlot.png "Figure 7: All perplexities")
	
	[**Figure 7: t-SNE: Menu **](_static/images/Tnse_shortcutPlot.png)

Keep in mind that when adjusting input settings the t-SNE algorithm will be runned again in case  a t-SNE map has been generated with default settings. A note on the execution times of t-SNE. The generation of the maps will take a substantial amount of time to generate, especially for larger datasets (up to a number of hours for datasets >600 samples). Once initiated (showing the message that t-SNE is being calculated), you can close that window and return to the analysis at a later time. The process will keep on running in the background. 

2. click Next

3. In the Adjusting settings set the color by track om Tissue and click next.

	![Figure   8: t-SNE: Colored by track ](_static/images/Tsne_normaltissuetrackcolored.png "Figure 8:  Colored by track")
	
	[**Figure 8: t-SNE: Colored by track **](_static/images/Tsne_normaltissuetrackcolored.png)



Final remarks
----------------------------


We hope that this tutorial has been helpful,The R2 support team.



