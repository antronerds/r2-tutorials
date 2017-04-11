
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
