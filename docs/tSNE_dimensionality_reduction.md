
<a id="tSNE_dimensionality_reduction"></a>

t-SNE: high dimensionality reduction in R2
========================================


*How to find grouos in your dataset using t-SNE.*


Scope
-----

-  In this tutorial several expression datasets will be used.
-  t-SNE will be used to find sub groups in several datasets.



TSNE 

A clustering tool which gaining more and more popularity in the research world is the so called t-SNE algorithm.  t-SNE stands for t-Distributed Stochastic Neighbor EMbedding and is  a machine learning dimensionality reduction algorithm that is well suited for the reduction of high dimensional datasets to 2 or three dimensions. 

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


Step 1: Selecting t-SNE maps
----------------------------

In this screen the t-SNE result is plotted with the highest perplexity, or a preset value that has been selected upon manual curation. There is no strict rule to select the ‘best’ perplexity. In most cases the highest perplexity is not the best choice to investigate the cluster further.  If the perplexity result is something other than 23, then select this perplexity value. We can see structure in the location of the various cell lines. We would like to look at the annotations that are available for the cell lines. 


1. In the 'adjustable settinsg box' set "perplexity' to the value of 23
2. Select ‘color by track’ from the ‘colormode’ and choose ‘primary ite’. Press ‘next to redraw the image.’

	![Figure    2: t-SNE preprocessed t-SNE maps](_static/images/Tsne_cellbroad_primsite.png "Figure 2:Coloring by Track")
  
	[**Figure 2: t-SNE preprocessed t-SNE maps**](_static/images/Tsne_cellbroad_primsite.png)


Another feature that may be informative in the context of a t-SNE map is to ‘overlay’ the expression of a particular gene on the map by coloring the cell lines by the expression values of a dataset, in this case mRNA gene expression. We can have a look at this by changing the ‘colormode’ to ‘color by expression’.

1. In the 'adjustable settings box'  select 'Color by Gene'  at Color mode and subsequently type 'CLDN3' at Gene for color ,  corresponding reporter will automatically pop-up (Figure 3 ) 

	![Figure    3: t-SNE_select_probeset](_static/images/Tsne_select_probeset.png "Figure 3: Select  A probeset")

	[**Figure 3: t-SNE_select_probeset**](_static/images/Tsne_select_probeset.png)

	
2. Again click ‘next’ to refresh the view.’  In this view the samples are not colored by a group annotation (track) but by their gene expression using a color gradient.  In this sample you can observe  a subgroup of the carcinoma samples which have higher level in contrast to the (carcinoma) samples. 

	![Figure    4: t-SNE_Color by Gene ](_static/images/Tsne_cellbroad_colorbygeneCLDN3.png "Figure 4: Select  A probeset")
	
	[**Figure 4: t-SNE_Color by Gene **](_static/images/Tsne_cellbroad_colorbygeneCLDN3.png)

3. Use  the track histology_subtype1 to generate a new t-SNE plot in the 'Adjustable settings' menu.  It appears that the subgroup which was striking by the color gradient are mostly adenocarcinoma' another gene which emphasizes the observation in the previoius example  is the NR3c1 gene showing an inverse gradient pattern for this subgroup.

	![Figure    4: t-SNE_Color by Gene ](_static/images/Tsne_cellbroad_colorbygeneNR3C1.png "Figure 4: Select  A probeset")
	
	[**Figure 4: t-SNE_Color by Gene **](_static/images/Tsne_cellbroad_colorbygeneNR3C1.png)














