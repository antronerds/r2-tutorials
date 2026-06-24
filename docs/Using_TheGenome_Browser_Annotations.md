# R2 Genome Browser — Annotation Track Reference

This document lists all annotation tracks available in the R2 genome browser, with a link to the original resource and a description from the primary source. The tracks are grouped by their biological category, which also serves as a proposal for reorganizing the panel headers in the browser.

---

## Genome Structure & Sequence Features

### Giemsa / Cytoband
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=cytoBand>

**Description:** Cytogenetic band locations derived from Giemsa staining of chromosomes, used to define the chromosomal banding pattern (p and q arms, centromeres, heterochromatic regions). Standard reference for cytogenetic coordinates.

---

### CpG Islands
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=cpgIslandExt>

**Description (UCSC):** "CpG islands are regions where CpGs are present at significantly higher levels than is typical for the genome as a whole. CpG islands are associated with genes, particularly housekeeping genes, in vertebrates, and are typically common near transcription start sites and may be associated with promoter regions." Predicted using criteria: length ≥200 bp, GC content ≥50%, observed/expected CpG ratio ≥0.6.

---

### Repeats (RepeatMasker)
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=rmsk>

**Description (UCSC/RepeatMasker):** "This track was created using Arian Smit's RepeatMasker program, which screens DNA sequences for interspersed repeats and low complexity DNA sequences. The program outputs a detailed annotation of the repeats that are present in the query sequence, as well as a modified version of the query sequence in which all the annotated repeats have been masked." Uses the Repbase Update library from the Genetic Information Research Institute (GIRI).

---

### Conservation (PlacMammal)
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=phastCons46way>

**Description (UCSC):** PhastCons conservation scores across placental mammals, derived from multiz alignments of 46 vertebrate genomes. Measures the probability that each base belongs to a conserved element, useful for identifying functionally constrained regions across evolution.

---

### BlackListed (Consensus)
**Link:** <https://github.com/Boyle-Lab/Blacklist>

**Description:** Consensus blacklist regions representing genomic areas with anomalously high signal in functional genomics assays (ChIP-seq, ATAC-seq, DNase-seq) independent of cell type or experimental conditions. These regions arise from structural artifacts, satellite repeats, or repetitive elements and should be excluded from genomic analyses.

---

### LaminB1 Boundaries
**Link:** <https://pmc.ncbi.nlm.nih.gov/articles/PMC9869549/>

**Description:** Boundaries of lamina-associated domains (LADs) as determined by LAMIN B1 ChIP-seq or DamID. LADs are genomic regions in contact with the nuclear lamina — typically heterochromatic, late-replicating, and transcriptionally repressed. The boundaries mark transitions between lamina-associated and non-lamina-associated chromatin and are associated with CTCF binding and TAD boundaries.

---

### NAD Domains — Németh 2010
**Link:** <https://pubmed.ncbi.nlm.nih.gov/20118936/>

**Description (Németh et al., 2010):** Nucleolus-associated domains (NADs) represent genomic regions in close contact with the nucleolus. "NADs represent several megabases of the human genome from all 23 chromosomes, typically regions displaying silent chromatin signatures." NADs overlap extensively with LADs and are enriched for heterochromatic marks (H3K9me3), low gene density, and low expression levels.

---

### R-loop Forming Sequences
**Link:** <http://rloop.bii.a-star.edu.sg> / <https://rlbase.uthscsa.edu>

**Description (R-loopDB):** "An R-loop is a three-stranded nucleic acid structure comprising nascent RNA hybridized with its corresponding DNA template strand while leaving the non-template DNA single-stranded. R-loops are often formed during transcription." This track displays computationally predicted R-loop forming sequences (RLFS) across the genome, based on sequence features favoring RNA:DNA hybrid formation.

---

### Sequence & GC Windows / GC Percentage
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=gc5Base>

**Description (UCSC):** GC content calculated in sliding windows across the genome. Used to assess local sequence composition. Regions of high GC content often correspond to CpG islands and gene-rich regions; regions of very low GC often correspond to gene-poor, repeat-dense areas.

---

## Gene Annotation

### RefSeq (R2) / RefSeq (CDS) / RefSeq features
**Link:** <https://www.ncbi.nlm.nih.gov/refseq/>

**Description (NCBI):** "The Reference Sequence (RefSeq) collection provides a comprehensive, integrated, non-redundant, well-annotated set of sequences, including genomic DNA, transcripts, and proteins." RefSeq is the primary curated gene annotation resource used in R2. The CDS track specifically marks coding sequence exons; RefSeq features includes additional annotations such as UTRs and non-coding transcripts.

---

### Ensembl Gene (e75)
**Link:** <https://www.ensembl.org>

**Description (Ensembl):** Ensembl provides automated genome annotation of gene structures, transcripts, and regulatory features. Release 75 (GRCh37/hg19, February 2014) is shown here for compatibility with the hg19 genome build. Ensembl annotation integrates ab initio gene predictions, EST alignments, and manually curated Havana annotations.

---

### Gencode
**Link:** <https://www.gencodegenes.org>

**Description (GENCODE):** "The GENCODE project produces high quality reference gene annotation and experimental validation for human and mouse genomes." GENCODE integrates both automated ENSEMBL annotation and manual HAVANA curation, and is the standard gene annotation used by ENCODE and many large-scale genomics projects.

---

### lincRNA from LNCipedia
**Link:** <https://lncipedia.org>

**Description (LNCipedia):** A comprehensive, publicly available database of human long non-coding RNA (lncRNA) sequences and annotation. LNCipedia integrates lncRNA annotations from multiple sources, including GENCODE, RefSeq, and literature-based annotations, with an emphasis on large intergenic non-coding RNAs (lincRNAs). Annotation includes transcript sequences, secondary structure, protein-coding potential, and links to expression data.

---

### Neogenes — Vibert 2022 Mol. Cell
**Link:** <https://doi.org/10.1016/j.molcel.2022.04.022>

**Description (Vibert et al., Molecular Cell 2022):** "EWS::FLI1 induces the robust expression of a specific set of novel spliced and polyadenylated transcripts within otherwise transcriptionally silent regions of the genome. These neogenes are virtually undetectable in large collections of normal tissues or non-EwS tumors." The Vibert 2022 track marks genomic coordinates of neogenes identified across 23 oncogenic transcription factor fusion proteins in 17 cancer types — tumor-specific transcriptional outputs from otherwise silent regions, representing potential immunotherapy targets.

---

## Regulatory Elements & Chromatin Accessibility

### SuperEnhancers (dbSUPER)
**Link:** <https://asntech.org/dbsuper/>

**Description (Khan & Zhang, NAR 2016):** "dbSUPER is the first integrated and interactive database of super-enhancers, which contains 82,234 super-enhancers in 102 human and 25 mouse tissue/cell types." Super-enhancers are clusters of transcriptional enhancers that drive cell-type-specific gene expression and are crucial to cell identity. Many disease-associated sequence variations are enriched in super-enhancer regions of disease-relevant cell types.

---

### Deepmind AlphaMissense
**Link:** <https://deepmind.google/blog/a-catalogue-of-genetic-mutations-to-help-pinpoint-the-cause-of-diseases/>

**Description (Cheng et al., Science 2023):** "AlphaMissense is an adaptation of AlphaFold fine-tuned on human and primate variant population frequency databases to predict missense variant pathogenicity. By combining structural context and evolutionary conservation, our model achieves state-of-the-art predictions." AlphaMissense classified 89% of all 71 million possible human missense variants as likely pathogenic or likely benign. This track overlays AlphaMissense scores at genomic positions, enabling rapid assessment of the likely functional impact of missense variants.

---

### Encode TF Clustered V3 (161 TFs)
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTables?db=hg19&hgta_group=regulation&hgta_track=wgEncodeRegTfbsClusteredV3&hgta_table=wgEncodeRegTfbsClusteredV3&hgta_doSchema=describe+table+schema>

**Description (UCSC/ENCODE):** "This track shows regions of transcription factor binding derived from a large collection of ChIP-seq experiments performed by the ENCODE project, together with DNA binding motifs identified within these regions by the ENCODE Factorbook repository." Clusters are derived from 161 transcription factors assayed across multiple cell types.

---

### Encode TF Clustered (~340 TFs)
**Link:** <https://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg38&g=encRegTfbsClustered>

**Description (UCSC/ENCODE):** An expanded version of the ENCODE transcription factor ChIP-seq clustering track, covering approximately 340 transcription factors. Derived from ENCODE Phase 3 and 4 data using a unified peak calling and clustering pipeline across hundreds of cell types and conditions.

---

### ENCODE cCREs combined
**Link:** <https://screen.wenglab.org>

**Description (ENCODE, Moore et al., Nature 2020):** "The Registry of cCREs pipeline integrates DNase-seq datasets to generate a set of representative DNase hypersensitive sites (rDHSs). It then classifies a subset of rDHSs with supporting histone or CTCF ChIP-seq as candidate cis-regulatory elements (cCREs)." cCREs are classified as promoter-like (PLS), enhancer-like (ELS), or CTCF-only elements, providing a comprehensive catalogue of potential regulatory sequences across hundreds of human cell types.

---

### NIH Epigenome Roadmap
**Link:** <https://egg2.wustl.edu/roadmap/web_portal/>

**Description (Kundaje et al., Nature 2015):** "The NIH Roadmap Epigenomics Mapping Consortium was launched with the goal of producing a public resource of human epigenomic data to catalyze basic biology and disease-oriented research. The project has generated high-quality, genome-wide maps of several key histone modifications, chromatin accessibility, DNA methylation and mRNA expression across hundreds of human cell types and tissues." This track displays reference epigenome data from 111 consolidated epigenomes.

---

### FANTOM5 Enhancers (permissive / robust / Gex FDR)
**Link:** <https://fantom.gsc.riken.jp/5/>

**Description (Andersson et al., Nature 2014):** "Using the FANTOM5 CAGE expression atlas, bidirectional capped RNAs are a signature feature of active enhancers. Over 40,000 enhancer candidates were identified from over 800 human cell and tissue samples across the whole human body." The permissive set includes all identified enhancers; the robust set applies stricter thresholds; the Gex FDR set contains enhancers correlated with nearby gene expression at a defined false discovery rate.

---

### CAGE FANTOM5 Phase1 2 tpm Summary
**Link:** <https://fantom.gsc.riken.jp/5/>

**Description:** A summary track of CAGE (Cap Analysis of Gene Expression) transcription start sites from FANTOM5 Phase 1, filtered at a minimum expression threshold of 2 tags per million (tpm). CAGE measures transcription initiation at single-nucleotide resolution across a diverse panel of human primary cells and tissues, providing an atlas of active promoters and enhancers.

---

### G4-quadruplex HEK293T (G4-seq, Marsico 2019)
**Link:** <https://doi.org/10.1093/nar/gkz179>

**Description (Marsico et al., NAR 2019):** Genome-wide map of experimentally observed G-quadruplex (G4) structures in HEK293T cells, generated using G4-seq — a high-throughput sequencing method for mapping DNA regions capable of forming G-quadruplex structures under physiological potassium conditions. G4 structures are enriched at gene promoters and are implicated in transcriptional regulation, DNA replication, and genome stability.

---

### GVATdb — measured 83 T2D loci
**Link:** <https://renlab.sdsc.edu/GVATdb/>

**Description (Yan et al., Nature 2021):** "This database characterizes the allelic binding of 95,886 common human single nucleotide polymorphisms (SNPs, MAF >1%) to 270 distinct transcription factors. The SNPs were chosen from neighboring regions (≤500 kb) of 83 risk loci of type 2 diabetes identified in several genome-wide association studies. The data were generated using SNP-SELEX." This track displays the genomic locations of the measured T2D risk locus variants.

---

### GVATdb DeltaSVM 1k genomes (94 TFs)
**Link:** <https://renlab.sdsc.edu/GVATdb/>

**Description (Yan et al., Nature 2021):** Predicted allelic transcription factor binding effects for variants from the 1000 Genomes Project, computed using deltaSVM models trained on SNP-SELEX data from 94 transcription factors. DeltaSVM scores quantify the predicted change in TF binding affinity resulting from each SNP allele, enabling genome-wide prediction of regulatory variant effects beyond the directly measured T2D loci.

---

### Hi-C Domains (Literature)
**Link:** <https://doi.org/10.1038/nature11222> (Dixon et al., 2012)

**Description (Dixon et al., Nature 2012):** Topologically associating domains (TADs) identified from Hi-C chromosome conformation capture experiments, as reported across multiple publications. TADs are megabase-scale regions of preferential self-interaction that compartmentalize the genome into structural and regulatory units. TAD boundaries are enriched for CTCF binding sites and often coincide with housekeeping genes and tRNA genes.

---

### Homer Known Motifs (Genome)
**Link:** <http://homer.ucsd.edu/homer/>

**Description (Heinz et al., Mol Cell 2010):** "These tracks display motif positions genome-wide for human and mouse. They are based on HOMER-motifs, and certainly miss many 'weak' binding sites and incorrectly predict others. However, the predictions can still serve as a useful guide to where factors are likely to bind." HOMER (Hypergeometric Optimization of Motif EnRichment) is a suite of tools for motif discovery and ChIP-seq analysis. This track shows predicted genome-wide binding locations for known transcription factor motifs.

---

### Liver Enhancers (Cell 2015, Villar)
**Link:** <https://doi.org/10.1016/j.cell.2015.01.006>

**Description (Villar et al., Cell 2015):** "We track the evolution of promoters and enhancers active in liver across 20 mammalian species from six diverse orders by profiling genomic enrichment of H3K27 acetylation and H3K4 trimethylation. We report that rapid evolution of enhancers is a universal feature of mammalian genomes." This track displays the human liver enhancers identified in this study, defined as regions enriched for H3K27ac but not H3K4me3.

---

### SuperEnhancers NB (George)

**Description:** Super-enhancer regions identified in neuroblastoma cell lines and tumor samples, as generated by the George lab (internal/unpublished or published in the context of neuroblastoma research). Super-enhancers in neuroblastoma are often associated with key oncogenes such as MYCN and ALK, and mark cell-type-specific transcriptional programs relevant to neuroblastoma biology.  
*(Note: verify primary publication with the R2 team.)*

---

### Vista Enhancers
**Link:** <https://enhancer.lbl.gov>

**Description (Visel et al., NAR 2007):** "The VISTA Enhancer Browser is a central resource for experimentally validated human noncoding fragments with gene enhancer activity as assessed in transgenic mice. The core dataset consists of experimental in vivo data of tissue-specific enhancers identified by their conservation between human and non-mammalian vertebrates across long evolutionary distances or by their unusually high conservation among mammals." Elements are tested by cloning upstream of a reporter gene and assaying tissue-specific expression in transgenic mouse embryos.

---

## ChIP-seq & Chromatin State

### ChromHMM (18-state models: ucle_18 / 18)
**Link:** <https://compbio.mit.edu/ChromHMM/> / <https://doi.org/10.1038/nmeth.1906>

**Description (Ernst & Kellis, Nature Methods 2012):** "ChromHMM displays a chromatin state segmentation derived by computationally integrating ChIP-seq data for multiple histone marks using a Hidden Markov Model. States were learned across multiple cell types and represent combinations of histone modifications associated with distinct functional elements such as active promoters, enhancers, transcribed regions, heterochromatin, and repressed regions." The 18-state models here were derived from ENCODE data.

---

### DiffBind
**Link:** <https://bioconductor.org/packages/DiffBind/>

**Description:** DiffBind is an R/Bioconductor package for identifying differentially bound ChIP-seq peaks between sample groups. The DiffBind track in R2 displays regions showing statistically significant differential binding between conditions or groups, as computed from aligned ChIP-seq datasets processed through the DiffBind analysis pipeline.

---

### ENCODE bed v1 / ENCODE bed v1 Ext
**Link:** <https://www.encodeproject.org>

**Description (ENCODE Consortium):** BED-format peak files from ENCODE ChIP-seq experiments, representing transcription factor binding sites or histone modification peaks from Version 1 of the ENCODE data release. The "Ext" (extended) version includes a broader set of experiments or extended peak regions.

---

### MACS 1.4 (AMC / DKFZ / Public)
**Link:** <https://pypi.org/project/MACS/>

**Description:** Peak calls generated using MACS (Model-based Analysis of ChIP-Seq) version 1.4, a widely used algorithm for identifying enriched regions in ChIP-seq data. The AMC, DKFZ, and Public suffixes indicate the origin of the ChIP-seq data: samples generated at Amsterdam UMC, at DKFZ (German Cancer Research Center), or from publicly available repositories, respectively.

---

### MACS2 (Narrow) / MACS2 (Broad) 2
**Link:** <https://github.com/macs3-project/MACS>

**Description:** Peak calls generated using MACS2, the successor to MACS 1.4, with improved statistical modeling. Narrow peaks are used for transcription factor ChIP-seq and ATAC-seq (sharp, punctate signals); broad peaks are used for histone modifications that span large genomic regions (e.g. H3K27me3, H3K9me3). The "2" suffix in the broad track name indicates a second batch or reprocessing of the data.

---

*Document last updated: June 2026. Please verify internal tracks (SuperEnhancers NB, MACS AMC/DKFZ) with the R2 support team for primary citations.*