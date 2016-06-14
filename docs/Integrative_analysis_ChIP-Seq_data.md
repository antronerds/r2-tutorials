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

Given the advanced character of this type of data analysis, some introduction on the concepts and algorithms used is in place.

### What is ChIP-Seq
With **C**hromatine **I**mmuno **P**recipitation binding of elements to the genome can be studied. Transcription of DNA to RNA is regulated by the binding of these elements. These can be Transcription Factors, that bind temporarily to start transcription, but also chemical modification of the histones (molecular structures that coil the DNA) by methylation, acetylation, etc. These modifications change the accessibility of the DNA for transcription. 

When a specific antibody is used in the pulldown that recognizes these chemically modified regions, these specific regions can be studied. Regions with H3K27Ac acetylation mark active enhancers and active transcription, H3K4Me3 methylation marks active and poised transcription. Studying the relative contributions of both types of modifications allows a researcher to discern enhancer regions from active transcription sites.


![Figure 1: Specific chemical modifications mark specific states of cis-regulatory elements](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)

[**Figure 1: Specific chemical modifications mark specific states of cis-regulatory elements; taken from doi:10.1016/j.molcel.2013.01.038 **](_static/images/IntAnalysis_ChIPSeq_ModificationTypes.png)


The assembly of the billions of fragments that result from a ChIPSeq experiment is a challenge. Algorithms to combine and map the reads into a consistent representation are under development. R2 allows you to study the outcome of these computationally intensive calculations through an intuitive visualization. Most default settings are suitable for a first impression of your data, to adapt certain parameters requires some knowledge about the actual computation, so we'll explain some of the concepts used below.

- **Peak calling**: 

R2 provides two algorithms to assess significant enrichment ChIP between experiment and control.  
First is the MACS algorithm; this is often used in ChIP-seq data analyses and publications. In R2 it is used to study the binding of transcription factors. It's drawback is that it is not very suitable for broad signals.

The other is RSEG; an algorithm especially designed for histone modification detection. In R2 this used to analyse the histone modification patterns. To distinguish between specific histone modifications (e.g. acetylation vs methylation), R2 allows you to assess the same region in two profiles. Every sample has its own peaks and these have to be scaled properly. 
  
- **Super enhancers **
An *enhancer* is a short (50-1500 bp) region of DNA that can be bound by proteins (activators) to increase the likelihood transcription will occur at a gene. They can be located up to 1 Mbp (1,000,000 bp) away from the gene, either upstream or downstream from the start site, and either in the forward or backward direction.  A *super-enhancer* is a region of the mammalian genome comprising multiple of these enhancers, collectively bound by an array of transcription factor proteins to drive transcription of genes, often involved in regulation of cell identity. 


For identification of super enhancers R2 uses the *R*ank *O*rdering of *S*uper-*E*nhancers algorithm (ROSE; [more on the algorithm here](http://www.cell.com/abstract/S0092-8674(13)00392-9)). This takes the peaks called by RSEG for both acetylation and methylation and compares them. It can also be used with the MACS calculated data.

Now that these concepts have been explained we're going to see how the ChIPSeq data can be accessed through R2.

## Step 1: Choosing data and modules

1. Since the annotation for ChIPSeq experiments is based on the HG19 build of the genome, make sure you've selected HG19 under *Change species>Human(HG19)* 
2. To enter the ChIP-Seq analysis module in R2 select *ChIPSeq data* in Box 3 (Fig 3).
	
	![Figure 2: Choose the ChIPSeq module](_static/images/IntAnalysis_ChIPSeq_ChooseInMenu3.png)
	
	[**Figure 2: Choose the ChIPSeq module **](_static/images/IntAnalysis_ChIPSeq_ChooseInMenu3.png)
	
3. See fig4 Several analysis paths start here; we're first going to explore binding around the Transcription Start Sites (TSS) of lists of genes.   
	
	![Figure 3: ChIPSeq Menu in R2](_static/images/IntAnalysis_ChIPSeq_ChIPSeqMenu.png)
	
	[**Figure 3: ChIPSeq Menu in R2 **](_static/images/IntAnalysis_ChIPSeq_ChIPSeqMenu.png)
	

## Step 2: Exploring Acetylation and Methylation patterns around Transcription Start Sites

1.  

## Step 3: Finding active enhancers

1.

## Final remarks

In R2 the ChIP-Seq data visualization is under development, so any suggestions are welcome.
Mail us at r2-support@amc.nl , also if you have any questions or remarks.

