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
	
3. Here we entered the detailed view of the circos plot section. On the right side you can open different tabs with informatio
	1.	Sample annotation.
	2.	Somatic structural variants.
	3.	Somatic structural variants of a limited size inside or close to genes that could be affected by them.
	4.	Hight quality non structural somatic variants.
	5.	A link out to the genome browsers showing a cgh-like plot of the sequencing data of a region of interest.

	![Figure 1: Choose the ChIPSeq module](_static/images/IntAnalysis_WGS_CircosDetailView.png)
	
	[**Figure 1: Choose the ChIPSeq module**](_static/images/IntAnalysis_WGS_CircosDetailView.png)
	
	