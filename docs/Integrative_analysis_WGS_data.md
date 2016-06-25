<a id="integrative_analysis_wgs_data"></a>

Integrative Analysis : WGS/NGS data
===========================================

*Datatypes: Whole Genome Sequencing data and expression data*

Scope
-----
- In this part R2 is used to provide information about how Whole Genome Sequencing (WGS) data can be viewed, shared and analysed.
  This is a specialized topic for with most likely close collaboration is needed to tailor your own data to your needs.
- ...



## Step 1: View circos files.

1. To view circos plots of the sequenced genomes in R2, select *Static circos files (v3)* in Box 3 (Fig 1).
	
	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_main_staticCircosFiles.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_main_staticCircosFiles.png)
	
2. Select a subset of samples by using the menu on the top.
	- Select *inss (cat 5)* from the select a track (subset) selection box.
	- Select *st2 (19)*, click <font color="red">confirm</font> and *update*.
	
	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_SelectSubset.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_SelectSubset.png)
	
2. In Neuroblatoma whole chromosome and partial gains and losses are frequent. Indicated by the red and green colouring of the cgh-like scatterplots.
	- One sample doesn't apears to have large structural defects (N482TL).
	- N482 indicates the sample_id, TL indecates that the circos plot shows data of the **T**umor compared to the **L**ymphosites DNA sequence data.
	- Click on the N482TL tile and go to the newly opened tab of your browser.

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_inssSt2Subset.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_inssSt2Subset.png)
	
3. Here we entered the detailed view of the circos plot section.
   On the right side you can open different information tabs.
	1.	Sample annotation.
	2.	Somatic structural variants.
	3.	Somatic structural variants of a limited size inside or close to genes that could be affected by them.
	4.	Hight quality non structural somatic variants.
	5.	A link out to the genome browsers showing a cgh-like plot of the sequencing data of a region of interest.

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_CircosDetailView.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_CircosDetailView.png)
	
	- When you open the *Gene Affecting Structural Variants (of limited size)* tab you can now see two variants listed and not one as shown in the circos plot.
	  For the cicos plot a higher threshold was used for the read pair mates. For the table we show more but less accurate data.
	- Click on *view* inside the *link* column.
	- This opens a double genomebrowser view showing both sides of the selected structural variation.

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_StucVarDuoPlot.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_StucVarDuoPlot.png)

4. When the link under a genomebrowser location view is clicked the same location is shown inside te full genomebrowser view.
   Here you will be able to use the zoom buttons and select extra data to plot with the cgh-like scatterplot and junction information.
   For this sample there is also affymetrix gene expression data available. Here the zscore is shown above the cgh-like plot.

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_StucVarGenomebrowser.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_StucVarGenomebrowser.png)
	
5. The *FOXR1* gene shows a high zscore and by clicking on the dot above this gene you wil be taken into the one gene view of r2 showing the expression of this gene inside a Neuroblastoma tumor series.
   

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_FoxM1oneGeneView.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_FoxM1oneGeneView.png)
	
	  
	