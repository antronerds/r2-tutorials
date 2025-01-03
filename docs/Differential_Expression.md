<a id="differential_expression"> </a>

Differential expression of genes in your dataset
=======================================




*Find out which genes make a difference between groups of samples in
your dataset*





Scope
-----

-   Use R2 to determine whether the expression of your gene of interest
    is significantly different between groups of samples (steps 1 to 5).
-   Use R2 to find all genes exhibiting differential expression between
    groups of samples in a dataset (step 6).
-   This is established by use of statistical tests. R2 will guide you
    through this process in a self-explanatory way.
-   In order to enable assignment of samples to groups, proper annotation of the dataset is required. In this tutorial a set of Neuroblastoma tumors is used that is annotated with several clinical parameters:
    survival, age of diagnosis, etc.
-   All (advanced) parameters can be adapted to your specific needs.
-   These settings will be elaborated upon in separate boxes.
-   The results of these analyses are presented in adaptable graphics.




Step 1: Selecting data and the type of analysis
---------------



1.  Log on to the R2 homepage using your credentials and make sure the
    **Single Dataset** field is selected in field 1.
2.  Make sure the **Tumor Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2** dataset is selected in
    field 2 (see chapter 1 of the tutorial for more information about the selection of a dataset).
3.	Choose **View a Gene in groups** in field 3 and click Submit.



Step 2: Choose the gene and the annotation track as grouping variable
---------------
In the next screen you will choose the gene of interest and decide which grouping variable to use to establish the differential expression of your gene of interest.


![](_static/images/FindDiff/DifferentialExpression_Genev1a.png "Figure 1: Step-by-step scenario to select 'View a gene in groups' on the main page of R2")

[**Figure 1: Step-by-step scenario to select 'View a gene in groups' on the main page of R2**](_static/images/FindDiff/DifferentialExpression_Genev1a.png)


1. Type **mycn** as gene (see Figure 1) in the first text field in the Adjustable settings box. Select with a mouse click the first reporter in the popup (the first row). The reporter textfield is automatically filled in.


To view the expression of this gene in groups, you can use dataset specific annotation, the so-called "tracks", as grouping variable in R2.

2. In the dropdown of the setting *Track* select the track called **Alive (2 cat)**. This track contains survival data of the patients from whom the tumor sample was taken.
3. Note that the other fields can be kept as is, the right choices are already provided. Click **Submit**.

The "one way
Anova"/"student T test" test will be performed for data on the selected
groups (see explanation in the next step).

----------------
![](_static/images/R2d2_logo.png)***Did you know that you can create your own tracks?***

*Many datasets in R2 contain annotations. You can use these annotation tracks as grouping variable. Another option is to create your own annotation track for any dataset in R2. This is explained in a separate tutorial [Adapting R2 to your needs](Adapting_R2.md).*

------------------



Step 3: Anova results / adapting plots
---------------

R2 now performs a one-way Anova statistical test on the fly. More information about which test to choose can be found here: [Statistical test: did you know..?](Did_You_Know.md).

1. Check the graph and the information that is displayed underneath the graph in the resulting window.

The actual result of the ANOVA calculations is shown in the table under the graph; the difference in average expression between the two groups is significant.


![](_static/images/FindDiff/DifferentialExpression_ResultViewInGroups.png "Figure 4: Result of the one-way Anova test for the Neuroblastoma 88 samples.")


[**Figure 4: Result of the one-way Anova test for the Neuroblastoma 88 samples.**](_static/images/FindDiff/DifferentialExpression_ResultViewInGroups.png)


2. For a nicely ordered graph, you can adjust the settings in the menu at the bottom. Set *Extra Graph Option*  to **Track and Gene Sort** (Do not forget to click on Submit afterwards!).  

R2 displays the mRNA expression of the samples in a splitted plot in which per group the samples are ordered with increasing expression (Figure 4). Note that the "alive" annotation is in the second row (track) beneath the graph.

   ![](_static/images/FindDiff/DifferentialExpress_Result.png "Figure 5: Order the samples per group with increasing expression.")


[**Figure 5a: Order the samples per group with increasing expression.**](_static/images/FindDiff/DifferentialExpress_Result.png)

These results can also be shown in different types of plots (Figure 5).
1. Scroll down the window to the Adjustable settings menu.
2. Adapt the selection in the dropdown box *Graph type* to another graph type, e.g. **Box plot**, and change *Color mode* to **Color by Track**. Also set  "Add scatter" to TRUE. 
3. Note that you can change the order of the groups with *Order Groups By*, let's take **median (numeric Y)** in our case.
4. Click **Submit**. The resulting graph is adapted accordingly.

![](_static/images/FindDiff/DifferentialExpression_AdaptGraphDotPlots1a.png "Figure 6: Adapting the Graph type to Dot plot, change order and set Color by Track")

[**Figure 5b: Adapting the Graph type to Box plot, Add scatter**](_static/images/FindDiff/DifferentialExpression_AdaptGraphDotPlots.png)


The difference in expression between the groups can be shown more dramatically by plotting the data without a log2 transformation. Make sure to use log2 transformation in scientific reports, though, as untransformed mRNA gene expression data is hardly ever normally distributed.

5. Clicking on the setting wheel on the left upper corner enables a popup settings window which allows you to choose file types for saving, numerous visualization settings and marking samples by entering the ID or click the sample in the interactive graph.

![](_static/images/FindDiff/DifferentialExpres_thewheel.png "Figure 6a: Adapting the visualisation settings and marking samples")

[**Figure 6: Adapting the Graph type to Dot plot, change order and set Color by Track**](_static/images/FindDiff/DifferentialExpression_AdaptGraphDotPlots.png)



6. In the 'Adjustable settings' menu, set the *Transformation* dropdown to **none** (Figure 7).

8. Click **Submit**.

The resulting 2 graphs also depicted in different types of plots in Figure 6 show the difference between the expression values in the two groups more dramatically.

![](_static/images/FindDiff/DifferentialExpression_Barplotv2.png "Figure 7a: The same data now represented without transformation in bar/box plots")

[**Figure  7a: The same data now represented without transformation in bar/box plots**](_static/images/FindDiff/DifferentialExpression_Barplotv1.png)

Figure 5 shows that you can add the sample dots after selecting "Add scatter = TRUE" when e.g. box plot is selected this allows you add a second level of coloring by using the group parameters or coloring by gene.

![](_static/images/FindDiff/DifferentialExpress_twolevelcolor.png "Figure 7b: Coloring the dots by track or gene expression")

[**Figure  7b: Coloring the dots by track or gene expression**](_static/images/DifferentialExpress_twolevelcolor.png)



------------------
![](_static/images/R2d2_logo.png)**Did you know that samples can be filtered and/or marked?**

*Under the sub-header "Sample Filter" you can select a specific subset of samples based on the annotation on track. First choose a track, then select the wanted subgroups in the track. The analysis will only be performed on the selected subset.*

![](_static/images/FindDiff/DifferentialExpress_SampleFilterDropdown.png)

[**Figure 8: Sample selection with the Sample Filter**](_static/images/FindDiff/DifferentialExpress_SampleFilterDropdown.png)



*Clicking the wheel icon will open a grid supporting all selection combinations of interest*

![](_static/images/FindDiff/DifferentialExpress_SampleFilterAdvanced.png)

[**Figure 9: Advanced sample selection**](_static/images/FindDiff/DifferentialExpress_SampleFilterAdvanced.png)

*In the samples to mark section, a sample name can be entered that will be highlighted in the resulting graph; ideal for publication purposes. Also note that in the interactive plot section you can mark samples by clicking on the dots.*

Clicking the dots in box plot with scatter = TRUE will open the plot optio box were all kinds of settings can be adapted for the selected dots also a sample ID can be entered for selection.


![](_static/images/FindDiff/DifferentialExpress_SampleFilterMarkedSample1a.png)

[**Figure 10: Graph with sample selection INSS 3 and 4 and a marked sample**](_static/images/FindDiff/DifferentialExpress_SampleFilterMarkedSample1a.png)


--------
Step 4: Finding differentially expressed genes in two groups
---------------
It would be a pretty tedious job to look for all genes whether they are differentially expressed between groups. Why not let R2 do the job for you? 
1. Go back to the Main screen, by clicking the link in the
   upper left corner of the screen.
2. In field 3 of the R2 step-by-step guide you find two options to find differential expressed gene lists: 'Find Differential expression between two groups' and  Differential expression between multiple groups (Figure 8). 
3. Both types of Differential expression modules harbor specific statistical tests. Depending on your chosen dataset, number of groups you want to test and the type of data (RNAseq,microarrays) you can choose from several statistical tests.

   ![](_static/images/FindDiff/DifferentialExpression_Selectgroups.png "Figure 11: Selecting Find Differential Expression.")

   [**Figure 11: Selecting Find Differential Expression.**](_static/images/FindDiff/DifferentialExpression_Selectgroups.png)

4. Select **"Differential expression between two groups"** and click **Next**.
  
5. In the next window you can select several types of statistical tests which are present in the selection menu. By default, the **T-test** is selected. We too will use this default test.  

Which test is suitable for a given dataset, depends on the normalization of selected dataset and on what kind of data the dataset is build of.  Most expression sets are continuous and normally distributed data so the T-test is the most applicable. In case of a dataset which contains categorical data the Mann-whitney test is more suitable.  

A special remark for the **DESeq2 algorithm** is at place here. This test is only available for RNAseq data where R2 also has access to the un-normalized counts. Most of the datasets that have 'DESeq2_rlog' or 'DESeq2_vst' in the name consist of multiple data parts. One or more normalised data parts are available in case you want to use the 'T-test', or 'limma' and in addition a data part with the raw non-normalized counts is available. If available, then making use of the DESeq2 algorithm is preferred (especially for smaller data sets). Note that in the case of DESeq2,  the counts are only used for the statistical tests, the values depicted in the graphs etc. are always normalized data.  
Using the DESEq2 algorithm in case of RNAseq is often preferred since this is a well-established statistical test package dedicated to data such as RNAseq data. In the dataset selection grid box you can search for datasets which have '**deseq2_rlog**' or **'deseq2_vst'** as normalization procedure. Data sets with this annotation have three slots, rlog/vst normalized data, deseq normalized data (normcounts) and a counts slot. This counts slot is used when you run the DESeq2 algorithm on the fly for two group comparisons.  


   ![](_static/images/FindDiff/DifferentialExpress_deseq2select.png "Figure 12: Selecting Find Differential Expression.")

   [**Figure 12: Selecting the DESEq2 test.**](_static/images/FindDiff/DifferentialExpress_deseq2select.png)



Step 5 Setting parameters
---------------

In our case we continue with the Tumor Neuroblastoma dataset and the Differential Expression between two groups analysis with the T-test. 

1. Now we also make the choice for the two groups. Select behind *Group by* the track **Alive (2cat)** again. Click **Submit**.  


   ![](_static/images/FindDiff/DifferentialExpress_AdaptParamv1.png "Figure 13: Differential expression parameters")

   [**Figure 13: Differential expression parameters**](_static/images/FindDiff/DifferentialExpress_AdaptParamv1.png)

3. An extra menu shows up with many options. For now we only adjust the required Group 1 and Group 2 setting: we choose the value **no (33)** for *Group 1* and **yes (55)** for *Group 2*.
4.  Click **Submit**.

![](_static/images//FindDiff/DifferentialExpress_Progress1a.png "Figure 14: Progress dialog during on the fly calculation")

   [**Figure 14: Progress dialog during on the fly calculation**](_static/images/DifferentialExpress_Progress.png)

The result is a list of genes that is ordered by the most significant differential expression between the groups that you chose (Figure 15). A short summary of the calculation is given above the table; ~ 2600 genes have met the criteria set by default; their expression exhibits a correlation with the separation in the two groups.  
The generated list can be sorted or filtered by any of the column headers in the grid, such as by the p-value (P) or the difference.  

In the right menu numerous modules can be selected to continue the analysis. Also, the generated list can be extracted to continue for further usage outside R2 and stored as temporary or permanent geneset in R2, as indicated in the right menu

   ![](_static/images/FindDiff/DifferentialExpress_Genelistv2a.png "Figure 15 Genes differentially expressed between groups")

   [**Figure 15: Genes differentially expressed between groups.**](_static/images/FindDiff/DifferentialExpress_Genelistv2a.png)


-----------------

Step 5: Correct for paired analysis
---------------

A paired analysis is often performed when observations are natural paired or matched such as in this example. 

1. Select in the main screen the following dataset. Exp Neuroblastoma Adrn Mes resistant - George - 12 - tpm - gse165748 and differential expression between two groups, select group by cell_lineage and click submit. Subsequently select adrenergic and mesenchymal for the groups and click the lower submit button.  Take a look at the number of found combinations and continue with adapting the settings in the adjustable settings box below the list of combinations.

   ![](_static/images/FindDiff/DifferentialExpres_nocorrectfor.png "Figure 16: Genes differentially expressed between groups")

   [**Figure 16: Genes differentially expressed between groups.**](_static/images/FindDiff/DifferentialExpres_nocorrectfor.png).

2. In the select a test box, select Limma and again for Group by: Cell_lineage and click submit. Select Adrenergic and mesenchymal for the groups and now you can select a track you want to correct for in this case, the  genomic_mycn_status, click the lower submit button.

   ![](_static/images/FindDiff/DifferentialExpres_withcorrectfor1a.png "Figure 17: Genes differentially expressed between groups")

   [**Figure 17: Genes differentially expressed between groups with correction.**](_static/images/FindDiff/DifferentialExpres_withcorrectfor1a.png)

3. After correction for the genomic_mycn status more genes are found to be significant differentially expressed between the two groups. For example also the PAX5 gene appears higher and more significant in the list which could be a candidate for further investigation.

   ![](_static/images/FindDiff/DifferentialExpres_withcorPAX5.png "Figure 18: Genes differentially expressed between groups")

   [**Figure 18: Genes differentially expressed between groups with correcttion.**](_static/images/FindDiff/DifferentialExpres_withcorPAX5.png)


​	
--------------------------------------------------------------------------
![](_static/images/R2d2_logo.png)***Did you know that...***

*Very useful background information for this tutorial can be found in Chapter 25 [Concepts of R2: did you know..?](Did_You_Know.md)*

*Check it out:*

>  **What were those R and p-values again?**:  R is the correlation coefficient; it ranges from -1 to +1, if R > 0 the value of two variables tends to increase or decrease together... Read all about R & p-values in [Chapter 25](Did_You_Know.md)
>
>  **You can specify the preferred statistical test and choose a subset of genes?**
> *Use any (combination) of the following parameters to adapt the analysis to your needs.*
> - **Hugo Once (Hugoonce)**: *For most analysis genes should only be reported once in a dataset. R2 uses an algorithm called Hugoonce to choose a single probe-set to represent a gene. Scroll down in [Chapter 25](Did_You_Know.md) to the Settings section about Hugo Once.*
> - **Statistics panel**: *R2 determines p-values for the differential expression of genes by performing either a one-way anova (default setting) or alternatively a brute-force t-test on any combination of groups when the data is untransformed or log2 transformed. For rank-transformed data, a Kruskal-Wallis test is performed. In addition to these statistical tests, users can also ask for genes with a certain fold change or obtain a top-X list of the genes which are ordered by a user-specified test.*
> - **Correction for multiple testing**: *We are testing a lot of genes here; so we have to correct for multiple testing. Why? Read on about multiple testing in [Chapter 25](Did_You_Know.md)*
> - **Gene Filters:** *As for many analyses in R2, the gene filters allow you to study a specific subset of genes for differential expression. There are several domains you can choose from. Learn more about gene filters in [Chapter 25](Did_You_Know.md)*

*Of course, to actually get familiar with these settings you should not only read about it, but also toy around with them!*



-----------------

Step 6: Find differential expression in multiple groups
---------------


As mentioned above, Find Differential Expression for multiple groups can also be applied with a slightly different "Adjustable settings menu" and including other types of statistical tests. Read further about which test to use in [Chapter 25](Did_You_Know.md).

1. Go back to the **Main** page by the link in the upper left corner and select again the Neuroblastoma 88 set.
2. Select **Differential expression between multiple groups** and click **Next**
3. Select for *Group by* the value **inss (5 cat)** and leave all the other settings at their default value. Click **Submit**.

![](_static/images/FindDiff/DifferentialExpress_AdaptParamv2.png "Figure 19: Genes differentially expressed between groups")

[**Figure 19: Genes differentially expressed between groups.**](_static/images/FindDiff/DifferentialExpress_AdaptParamv2.png)

4. A list of differentially expressed genes between the groups is generated. Of course, now that we have more than two groups, the table no longer contains the Difference column and group order column.


-----------------
Step 7: Inspecting single genes
---------------

1. Choose one of the genes in the table to inspect further.
2. Hover over the magnify symbol in the list next to the gene name to find a description of the gene. 
3. Now click on the magnify symbol. A similar graph is produced as for TF, the differential
    expression is more pronounced for this gene (Figure 18). In stage 4s, even indicating  based on the TF expression that there is possible subgroup within the INSS 4s stage.
4. In the
    generated picture the samples are not ordered by their gene
    expression. Go to the adjustable settings menu and select **Track and
    gene sort** in the *Extra Graph Option* pulldown menu. Click
    **Submit**.

![](_static/images/FindDiff/DifferentialExpress_TopGene.png "Figure 20: Hover over and click on any gene of interest")

[**Figure 20: Hover over and click on any gene of interest**](_static/images/FindDiff/DifferentialExpress_TopGene.png)


--------------
Step 8: Plot all genes and adapt visualization: Volcano plot etc
---------------

1. The tab with the list of differentially expressed genes (Figure 15) is still open or perform the analysis again. Click on this tab.

2. Most of the functionalities in the right panel of this window will be explored in more advanced tutorials (K-Means clustering etc.). We will explore one
   additional data visualization however to plot all genes of this analysis. In the 'Adjustable settings' form, open the pull down of 'Display' and select 'Volcano plot'. Then press 'submit'.

      ![](_static/images/FindDiff/DifferentiaExpression_display_dropdown.png "Figure  21: Display options for Differential Expression analysis")

      [**Figure  21 : Display options for Differential Expression analysis**](_static/images/FindDiff/DifferentiaExpression_display_dropdown.png)

3. The Analysis will now be initiated again, but since the result is kept for a little while, the analysis should not take more than a couple of seconds. The resulting plot shows all genes of the list in a so called volcano plot. Hovering over the points shows the gene symbol, left-clicking on the dots will annotate the dots with the gene name (or other markings, as you can adapt in the 'Marked' tab of the plot options). To speed up the
   graph generation, some adaptations may not update automatically. Click on the "redraw plot" button at the bottom of the plot options to add
   this information. 

4. In the adjustable settings menu you select gene sets to high light the genes and toggle on histograms along the X and Y axis.


   ![](_static/images/FindDiff/DifferentialExpress_vulconoplot1b.png "Figure 21: Different plots of all genes differentially expressed in the current track;")

   [**Figure 21: XY, MA , Volcano plot of all genes differentially expressed in the current    track;**](_static/images/DifferentialExpress_vulconoplot1b.png)

This example is from another differential analysis, right clicking on the datapoint in the plot opens a new window showing the expression
   of the gene in the two groups as a violin plot.

   ![](_static/images/FindDiff/DifferentialExpress_Violinplot.png "Figure  21: Differential expression of MYCN")

   [**Figure  21 : Differential expression of MYCN**](_static/images/FindDiff/DifferentialExpress_Violinplot.png)



6. The plot has been adapted to show the AKR1C1, PIRT etc
   gene symbols also  DNA-replication genes are highlighted in green. Fold
   change lines show the regions where differential expression is 1 and
   2 fold (Figure 16). Note that most genes of the DNA replication
   pathway seem to be located below the diagonal.

   ![](_static/images/FindDiff/DifferentialExpres_DNArepl1a.png "Figure 22: Adjusted visualization of gene expression,hovering over the dots    shows the    gene name.")

   [**Figure 22: Adjusted visualization of gene expression,hovering over the dots shows the    gene name.**](_static/images/FindDiff/DifferentialExpres_DNArepl1.png)

8. In another example in the selected Colon carcinoma TCGA set, some Ribosomal gene categories were selected in the gene filter. The KRT16-gene was selected and adapted in the Adjustable settings box.

    ![](_static/images/FindDiff/DifferentialExpression_vulcano_emphasize.png "Figure 22: Adjustable settings for the all genes plot")

 [**Figure 22 : Gene set(s) Emphasis on TCGA COAD samples**](_static/images/FindDiff/DifferentialExpression_vulcano_emphasize.png)

--------------
Step 9: Using the Enrichr
---------------

The right menu also allows you to take your result list of differentially expressed genes (DEG) outside R2 to the public available Enrichr platform. Enrichr (https://maayanlab.cloud/Enrichr/enrich) is a web-based platform designed for gene set enrichment analysis (GSEA) and functional annotation of gene lists. It allows you to gain insights into the biological processes, pathways, and functions associated with their gene sets of interest. The Enrichr performs an enrichment analysis by comparing the generated R2-list against a large collection of well curated databases such as Gene Ontology, KEGG pathways and disease-associated gene sets

![](_static/images/FindDiff/DifferentialExpres_enrichr.png "Figure    23 : Adjusted visualization of gene expression,hovering over the dots    shows the    gene name.")

[**Figure 23: Taking the result to the Enrichr platform.**](_static/images/FindDiff/DifferentialExpres_enrichr.png)

Figure 23 shows the Enrichr button you can click directly when the DEG list genes is ready, in the next screen you can select  just one group when coming from the two group analysis or you want to include and even add of delete genes from list. Hitting the submit button will direct lead to the Enrichr platform. 




-------------------------------------------
![](_static/images/R2d2_logo.png)**Did you know that you can tailor visualization of specific genes in one go?**

* You can annotate gene names (gene symbols) by providing them in the 'Mark genes' field of the Adjustable Settings panel. By default, these will appear in red, size=10, on your plot. You can change the size and/or color of these genes either individually, or in groups.
* Clicking on the dots will annotate the dots with the gene name.  
* Please take note of the following rules: to mark groups of genes for which the same criteria apply,
first type the genes (comma separated), followed by :s=size, followed by :c=r,g,b  
for single genes: gene1:s=25:c=0,0,255;gene2:s=20:c=200,0,0  
for groups of genes: (gene1,gene2,gene3):s=25:c=0,0,255;(gene4,gene5,gene6):s=20:c=200,0,0"*

-------------------------------




Final remarks / future directions
---------------------------------



This tutorial has shown you how to find genes that are differentially
expressed in your dataset of choice. Now go ahead and toy around with
selecting groups and tracks of choice and see what interesting
scientific discoveries might lie ahead!





We hope that this tutorial has been helpful, the R2 support team.

