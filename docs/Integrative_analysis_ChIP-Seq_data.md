<a id="integrative_analysis_chip-seq_data"></a>

Integrative analysis: ChIP-Seq data
===================================

*ChIP data visualization can be combined with other types of data*

Scope
---
-	Provide an introduction to the concepts and algorithms used in ChIP-Seq data
-	Check the properties of binding sites based on methylation and acetylation data
-	Relate this to expression data
-	Investigate the location of super enhancers on the genome

Some concepts
---

Given the advanced character of this type of data some introduction on the concepts and algorithms used is in place.

###What is ChIP-Seq
With **C**hromatine **I**mmuno **P**recipitation binding of elements to the genome can be studied. Transcription of DNA to RNA is regulated by the binding of these elements. These can be Transcription Factors that bind temporarily to start transcription, but also chemical modification of the histones (molecular structures that coil the DNA) by methylation, acetylation, etc. These modifications change the accessibility of the DNA for transcription. 

When a specific antibody is used in the pulldown that recognizes these chemically modified regions, these specific regions can be studied. Regions with H3K27Ac acetylation mark active enhancers and active transcription, H3K4Me3 methylation marks active and poised transcription. Studying the relative contributions of both types of modifications allows a researcher to discern enhancer regions from active transcription sites.


![Figure 1: Specific chemical modifications mark specific states of cis-regulatory elements](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)

[**Figure 1: Specific chemical modifications mark specific states of cis-regulatory elements; taken from doi:10.1016/j.molcel.2013.01.038 **](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)


The assembly of the billions of fragments that result from a ChIPSeq experiment is a challenge. Algorithms to combine and map the reads into a consistent representation are under development. R2 allows you to study the outcome of these computationally intensive calculations through an intuitive visualization. Most default settings are suitable for a first impression of your data, to adapt certain parameters requires some knowledge about the actual computation, so we'll explain some of the concepts used below.

- **Peak calling**: To distinguish between chemical modifications R2 allows you to assess the same region in 2 profiles. The RSEG algorithm generates peaks on basis of the data. Every sample has its own peaks. This makes them hard to compare; the ROSE analysis can be tuned to generate results on fixed regions under specific conditions thereby enabling the distinction of active enhancers
  
- **Super enhancers **

Now that these concepts have been explained we're going to see how R2 actually represents the ChIPSeq data.

##Step 1: Choosing data and modules

1. In R2 the ChIP-Seq data visualization is under development, any suggestions are welcome. Since the annotation for ChIPSeq experiments is based on the HG19 build of the genome, make sure you've selected HG19 under *Change species>Human(HG19)* 
2. To enter the ChIP-Seq analysis module in R2 select *ChIPSeq data* in Box 3 (Fig 3).
	
	![Figure 2: Choose the ChIPSeq module](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)
	
	[**Figure 2: Choose the ChIPSeq module **](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)
	
3. See fig4 Several analysis paths start here; we're first going to explore binding around the Transcription Start Sites (TSS) of lists of genes. This  
	
	![Figure 3: ChIPSeq Menu in R2](_static/images/IntAnalysis_ChIPSeq_ChIPSeqMenu.png)
	
	[**Figure 3: ChIPSeq Menu in R2 **](_static/images/IntAnalysis_ChIPSeq_ChIPSeqMenu.png)
	

##Step 2: Exploring Acetylation and Methylation patterns around Transcription Start Sites

1.  

##Step 3: Finding active enhancers

