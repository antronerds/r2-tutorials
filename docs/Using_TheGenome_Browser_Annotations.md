# R2 Genome Browser — Annotation Track Reference

**!! Verify tracks (SuperEnhancers NB, MACS AMC/DKFZ) !!**

This document lists many of the annotation tracks available in the R2 genome browser, with a description of each resource and a numbered reference to the original publication. The tracks are grouped by their biological category.

---

## Contents

**[Genome Structure & Sequence Features](#genome-structure--sequence-features)**

- [Giemsa / Cytoband](#giemsa--cytoband)
- [CpG Islands](#cpg-islands)
- [Repeats (RepeatMasker)](#repeats-repeatmasker)
- [Conservation (PlacMammal)](#conservation-placmammal)
- [BlackListed (Consensus)](#blacklisted-consensus)
- [LaminB1 Boundaries](#laminb1-boundaries)
- [NAD Domains — Németh 2010](#nad-domains-németh-2010)
- [R-loop Forming Sequences](#r-loop-forming-sequences)
- [Sequence & GC Windows / GC Percentage](#sequence--gc-windows--gc-percentage)

**[Gene Annotation](#gene-annotation)**

- [RefSeq (R2) / RefSeq (CDS) / RefSeq features](#refseq-r2--refseq-cds--refseq-features)
- [Ensembl Gene (e75)](#ensembl-gene-e75)
- [Gencode](#gencode)
- [lincRNA from LNCipedia](#lincrna-from-lncipedia)
- [Neogenes — Vibert 2022 Mol. Cell](#neogenes--vibert-2022-mol-cell)

**[Regulatory Elements & Chromatin Accessibility](#regulatory-elements--chromatin-accessibility)**

- [SuperEnhancers (dbSUPER)](#superenhancers-dbsuper)
- [Deepmind AlphaMissense](#deepmind-alphamissense)
- [Encode TF Clustered V3 (161 TFs)](#encode-tf-clustered-v3-161-tfs)
- [Encode TF Clustered (~340 TFs)](#encode-tf-clustered-340-tfs)
- [ENCODE cCREs combined](#encode-ccres-combined)
- [NIH Epigenome Roadmap](#nih-epigenome-roadmap)
- [FANTOM5 Enhancers (permissive / robust / Gex FDR)](#fantom5-enhancers-permissive--robust--gex-fdr)
- [CAGE FANTOM5 Phase1 2 tpm Summary](#cage-fantom5-phase1-2-tpm-summary)
- [G4-quadruplex HEK293T (G4-seq, Marsico 2019)](#g4-quadruplex-hek293t-g4-seq-marsico-2019)
- [GVATdb — measured 83 T2D loci](#gvatdb--measured-83-t2d-loci)
- [GVATdb DeltaSVM 1k genomes (94 TFs)](#gvatdb-deltasvm-1k-genomes-94-tfs)
- [Hi-C Domains (Literature)](#hi-c-domains-literature)
- [Homer Known Motifs (Genome)](#homer-known-motifs-genome)
- [Liver Enhancers (Cell 2015, Villar)](#liver-enhancers-cell-2015-villar)
- [SuperEnhancers NB (George)](#superenhancers-nb-george)
- [Vista Enhancers](#vista-enhancers)

**[ChIP-seq & Chromatin State](#chip-seq--chromatin-state)**

- [ChromHMM (18-state models: ucle_18 / 18)](#chromhmm-18-state-models-ucle_18--18)
- [DiffBind](#diffbind)
- [ENCODE bed v1 / ENCODE bed v1 Ext](#encode-bed-v1--encode-bed-v1-ext)
- [MACS 1.4 (AMC / DKFZ / Public)](#macs-14-amc--dkfz--public)
- [MACS2 (Narrow) / MACS2 (Broad) 2](#macs2-narrow--macs2-broad-2)

**[References](#references)**

---

## Genome Structure & Sequence Features

### Giemsa / Cytoband
**Description:** Cytogenetic band locations derived from Giemsa staining of chromosomes, used to define the chromosomal banding pattern (p and q arms, centromeres, heterochromatic regions). Standard reference for cytogenetic coordinates. [1]

---

### CpG Islands
**Description:** "CpG islands are regions where CpGs are present at significantly higher levels than is typical for the genome as a whole. CpG islands are associated with genes, particularly housekeeping genes, in vertebrates, and are typically common near transcription start sites and may be associated with promoter regions." Predicted using criteria: length ≥200 bp, GC content ≥50%, observed/expected CpG ratio ≥0.6. [1]

---

### Repeats (RepeatMasker)
**Description:** "This track was created using Arian Smit's RepeatMasker program, which screens DNA sequences for interspersed repeats and low complexity DNA sequences. The program outputs a detailed annotation of the repeats that are present in the query sequence, as well as a modified version of the query sequence in which all the annotated repeats have been masked." Uses the Repbase Update library from the Genetic Information Research Institute (GIRI). [1, 2]

---

### Conservation (PlacMammal)
**Description:** PhastCons conservation scores across placental mammals, derived from multiz alignments of 46 vertebrate genomes. Measures the probability that each base belongs to a conserved element, useful for identifying functionally constrained regions across evolution. [1, 3]

---

### BlackListed (Consensus)
**Description:** Consensus blacklist regions representing genomic areas with anomalously high signal in functional genomics assays (ChIP-seq, ATAC-seq, DNase-seq) independent of cell type or experimental conditions. These regions arise from structural artifacts, satellite repeats, or repetitive elements and should be excluded from genomic analyses. [4]

---

### LaminB1 Boundaries
**Description:** Boundaries of lamina-associated domains (LADs) as determined by LAMIN B1 ChIP-seq or DamID. LADs are genomic regions in contact with the nuclear lamina — typically heterochromatic, late-replicating, and transcriptionally repressed. The boundaries mark transitions between lamina-associated and non-lamina-associated chromatin and are associated with CTCF binding and TAD boundaries. [5]

*(!!! Verify the exact source dataset)*

---

### NAD Domains Németh 2010
**Description:** Nucleolus-associated domains (NADs) represent genomic regions in close contact with the nucleolus. "NADs represent several megabases of the human genome from all 23 chromosomes, typically regions displaying silent chromatin signatures." NADs overlap extensively with LADs and are enriched for heterochromatic marks (H3K9me3), low gene density, and low expression levels. [6]

---

### R-loop Forming Sequences
**Description:** An R-loop is a three-stranded nucleic acid structure comprising nascent RNA hybridized with its corresponding DNA template strand while leaving the non-template DNA single-stranded. This track displays computationally predicted R-loop forming sequences (RLFS) across the genome, based on sequence features favoring RNA:DNA hybrid formation. [7]

---

### Sequence & GC Windows / GC Percentage
**Description:** GC content calculated in sliding windows across the genome. Used to assess local sequence composition. Regions of high GC content often correspond to CpG islands and gene-rich regions; regions of very low GC often correspond to gene-poor, repeat-dense areas. [1]

---

## Gene Annotation

### RefSeq (R2) / RefSeq (CDS) / RefSeq features
**Description:** "The Reference Sequence (RefSeq) collection provides a comprehensive, integrated, non-redundant, well-annotated set of sequences, including genomic DNA, transcripts, and proteins." RefSeq is the primary curated gene annotation resource used in R2. The CDS track specifically marks coding sequence exons; RefSeq features includes additional annotations such as UTRs and non-coding transcripts. [8]

---

### Ensembl Gene (e75)
**Description:** Ensembl provides automated genome annotation of gene structures, transcripts, and regulatory features. Release 75 (GRCh37/hg19, February 2014) is shown here for compatibility with the hg19 genome build. Ensembl annotation integrates ab initio gene predictions, EST alignments, and manually curated Havana annotations. [9]

---

### Gencode
**Description:** "The GENCODE project produces high quality reference gene annotation and experimental validation for human and mouse genomes." GENCODE integrates both automated Ensembl annotation and manual HAVANA curation, and is the standard gene annotation used by ENCODE and many large-scale genomics projects. [10]

---

### lincRNA from LNCipedia
**Description:** A comprehensive, publicly available database of human long non-coding RNA (lncRNA) sequences and annotation. LNCipedia integrates lncRNA annotations from multiple sources, including GENCODE, RefSeq, and literature-based annotations, with an emphasis on large intergenic non-coding RNAs (lincRNAs). Annotation includes transcript sequences, secondary structure, protein-coding potential, and links to expression data. [11]

---

### Neogenes — Vibert 2022 Mol. Cell
**Description:** "EWS::FLI1 induces the robust expression of a specific set of novel spliced and polyadenylated transcripts within otherwise transcriptionally silent regions of the genome. These neogenes are virtually undetectable in large collections of normal tissues or non-EwS tumors." The Vibert 2022 track marks genomic coordinates of neogenes identified across oncogenic transcription factor fusion proteins — tumor-specific transcriptional outputs from otherwise silent regions, representing potential immunotherapy targets. [12]

---

## Regulatory Elements & Chromatin Accessibility

### SuperEnhancers (dbSUPER)
**Description:** "dbSUPER is the first integrated and interactive database of super-enhancers, which contains 82,234 super-enhancers in 102 human and 25 mouse tissue/cell types." Super-enhancers are clusters of transcriptional enhancers that drive cell-type-specific gene expression and are crucial to cell identity. Many disease-associated sequence variations are enriched in super-enhancer regions of disease-relevant cell types. [13]

---

### Deepmind AlphaMissense
**Description:** AlphaMissense is an adaptation of AlphaFold fine-tuned on human and primate variant population frequency databases to predict missense variant pathogenicity. By combining structural context and evolutionary conservation, the model achieves state-of-the-art predictions. AlphaMissense classified 89% of all 71 million possible human missense variants as likely pathogenic or likely benign. This track overlays AlphaMissense scores at genomic positions, enabling rapid assessment of the likely functional impact of missense variants. [14]

---

### Encode TF Clustered V3 (161 TFs)
**Description:** "This track shows regions of transcription factor binding derived from a large collection of ChIP-seq experiments performed by the ENCODE project, together with DNA binding motifs identified within these regions by the ENCODE Factorbook repository." Clusters are derived from 161 transcription factors assayed across multiple cell types. [15]

---

### Encode TF Clustered (~340 TFs)
**Description:** An expanded version of the ENCODE transcription factor ChIP-seq clustering track, covering approximately 340 transcription factors. Derived from ENCODE Phase 3 and 4 data using a unified peak calling and clustering pipeline across hundreds of cell types and conditions. [15]

---

### ENCODE cCREs combined
**Description:** "The Registry of cCREs pipeline integrates DNase-seq datasets to generate a set of representative DNase hypersensitive sites (rDHSs). It then classifies a subset of rDHSs with supporting histone or CTCF ChIP-seq as candidate cis-regulatory elements (cCREs)." cCREs are classified as promoter-like (PLS), enhancer-like (ELS), or CTCF-only elements, providing a comprehensive catalogue of potential regulatory sequences across hundreds of human cell types. [16]

---

### NIH Epigenome Roadmap
**Description:** "The NIH Roadmap Epigenomics Mapping Consortium was launched with the goal of producing a public resource of human epigenomic data to catalyze basic biology and disease-oriented research. The project has generated high-quality, genome-wide maps of several key histone modifications, chromatin accessibility, DNA methylation and mRNA expression across hundreds of human cell types and tissues." This track displays reference epigenome data from 111 consolidated epigenomes. [17]

---

### FANTOM5 Enhancers (permissive / robust / Gex FDR)
**Description:** "Using the FANTOM5 CAGE expression atlas, bidirectional capped RNAs are a signature feature of active enhancers. Over 40,000 enhancer candidates were identified from over 800 human cell and tissue samples across the whole human body." The permissive set includes all identified enhancers; the robust set applies stricter thresholds; the Gex FDR set contains enhancers correlated with nearby gene expression at a defined false discovery rate. [18]

---

### CAGE FANTOM5 Phase1 2 tpm Summary
**Description:** A summary track of CAGE (Cap Analysis of Gene Expression) transcription start sites from FANTOM5 Phase 1, filtered at a minimum expression threshold of 2 tags per million (tpm). CAGE measures transcription initiation at single-nucleotide resolution across a diverse panel of human primary cells and tissues, providing an atlas of active promoters and enhancers. [18]

---

### G4-quadruplex HEK293T (G4-seq, Marsico 2019)
**Description:** Genome-wide map of experimentally observed G-quadruplex (G4) structures in HEK293T cells, generated using G4-seq — a high-throughput sequencing method for mapping DNA regions capable of forming G-quadruplex structures under physiological potassium conditions. G4 structures are enriched at gene promoters and are implicated in transcriptional regulation, DNA replication, and genome stability. [19]

---

### GVATdb — measured 83 T2D loci
**Description:** "This database characterizes the allelic binding of 95,886 common human single nucleotide polymorphisms (SNPs, MAF >1%) to 270 distinct transcription factors. The SNPs were chosen from neighboring regions (≤500 kb) of 83 risk loci of type 2 diabetes identified in several genome-wide association studies. The data were generated using SNP-SELEX." This track displays the genomic locations of the measured T2D risk locus variants. [20]

---

### GVATdb DeltaSVM 1k genomes (94 TFs)
**Description:** Predicted allelic transcription factor binding effects for variants from the 1000 Genomes Project, computed using deltaSVM models trained on SNP-SELEX data from 94 transcription factors. DeltaSVM scores quantify the predicted change in TF binding affinity resulting from each SNP allele, enabling genome-wide prediction of regulatory variant effects beyond the directly measured T2D loci. [20]

---

### Hi-C Domains (Literature)
**Description:** Topologically associating domains (TADs) identified from Hi-C chromosome conformation capture experiments, as reported across multiple publications. TADs are megabase-scale regions of preferential self-interaction that compartmentalize the genome into structural and regulatory units. TAD boundaries are enriched for CTCF binding sites and often coincide with housekeeping genes and tRNA genes. [21]

---

### Homer Known Motifs (Genome)
**Description:** "These tracks display motif positions genome-wide for human and mouse. They are based on HOMER-motifs, and certainly miss many 'weak' binding sites and incorrectly predict others. However, the predictions can still serve as a useful guide to where factors are likely to bind." HOMER (Hypergeometric Optimization of Motif EnRichment) is a suite of tools for motif discovery and ChIP-seq analysis. This track shows predicted genome-wide binding locations for known transcription factor motifs. [22]

---

### Liver Enhancers (Cell 2015, Villar)
**Description:** "We track the evolution of promoters and enhancers active in liver across 20 mammalian species from six diverse orders by profiling genomic enrichment of H3K27 acetylation and H3K4 trimethylation. We report that rapid evolution of enhancers is a universal feature of mammalian genomes." This track displays the human liver enhancers identified in this study, defined as regions enriched for H3K27ac but not H3K4me3. [23]

---

### SuperEnhancers NB (George)
**Description:** Super-enhancer regions identified in neuroblastoma cell lines and tumor samples, as generated by the George lab. Super-enhancers in neuroblastoma are often associated with key oncogenes such as MYCN and ALK, and mark cell-type-specific transcriptional programs relevant to neuroblastoma biology.

*(!!! Verify publication)*

---

### Vista Enhancers
**Description:** "The VISTA Enhancer Browser is a central resource for experimentally validated human noncoding fragments with gene enhancer activity as assessed in transgenic mice. The core dataset consists of experimental in vivo data of tissue-specific enhancers identified by their conservation between human and non-mammalian vertebrates across long evolutionary distances or by their unusually high conservation among mammals." Elements are tested by cloning upstream of a reporter gene and assaying tissue-specific expression in transgenic mouse embryos. [24]

---

## ChIP-seq & Chromatin State

### ChromHMM (18-state models: ucle_18 / 18)
**Description:** "ChromHMM displays a chromatin state segmentation derived by computationally integrating ChIP-seq data for multiple histone marks using a Hidden Markov Model. States were learned across multiple cell types and represent combinations of histone modifications associated with distinct functional elements such as active promoters, enhancers, transcribed regions, heterochromatin, and repressed regions." The 18-state models here were derived from ENCODE data. [25]

---

### DiffBind
**Description:** DiffBind is an R/Bioconductor package for identifying differentially bound ChIP-seq peaks between sample groups. The DiffBind track in R2 displays regions showing statistically significant differential binding between conditions or groups, as computed from aligned ChIP-seq datasets processed through the DiffBind analysis pipeline. [26]

---

### ENCODE bed v1 / ENCODE bed v1 Ext
**Description:** BED-format peak files from ENCODE ChIP-seq experiments, representing transcription factor binding sites or histone modification peaks from Version 1 of the ENCODE data release. The "Ext" (extended) version includes a broader set of experiments or extended peak regions. [15]

---

### MACS 1.4 (AMC / DKFZ / Public)
**Description:** Peak calls generated using MACS (Model-based Analysis of ChIP-Seq) version 1.4, a widely used algorithm for identifying enriched regions in ChIP-seq data. [27]

---

### MACS2 (Narrow) / MACS2 (Broad) 2
**Description:** Peak calls generated using MACS2, the successor to MACS 1.4, with improved statistical modeling. Narrow peaks are used for transcription factor ChIP-seq and ATAC-seq (sharp, punctate signals); broad peaks are used for histone modifications that span large genomic regions (e.g. H3K27me3, H3K9me3).  [27]

---

## References

1. UCSC Genome Browser. University of California Santa Cruz. https://genome.ucsc.edu
2. Smit AFA, Hubley R, Green P. RepeatMasker Open-4.0. 2013–2015. http://www.repeatmasker.org
3. Siepel A, et al. Evolutionarily conserved elements in vertebrate, insect, worm, and yeast genomes. *Genome Research* 2005; 15(8):1034–1050. https://doi.org/10.1101/gr.3715005
4. Amemiya HM, Kundaje A, Boyle AP. The ENCODE Blacklist: Identification of Problematic Regions of the Genome. *Scientific Reports* 2019; 9:9354. https://doi.org/10.1038/s41598-019-45839-z
5. Chen Y, et al. An atlas of lamina-associated chromatin across twelve human cell types reveals an intermediate chromatin subtype. *Genome Biology* 2023; 24:1. https://doi.org/10.1186/s13059-022-02849-5
6. Németh A, et al. Initial genomics of the human nucleolus. *PLOS Genetics* 2010; 6(3):e1000889. https://doi.org/10.1371/journal.pgen.1000889
7. Jenjaroenpun P, et al. R-loopDB: a database for R-loop forming sequences (RLFS) and R-loops. *Nucleic Acids Research* 2017; 45(D1):D119–D127. https://doi.org/10.1093/nar/gkw1054
8. O'Leary NA, et al. Reference sequence (RefSeq) database at NCBI: current status, taxonomic expansion, and functional annotation. *Nucleic Acids Research* 2016; 44(D1):D733–D745. https://doi.org/10.1093/nar/gkv1189
9. Cunningham F, et al. Ensembl 2022. *Nucleic Acids Research* 2022; 50(D1):D988–D995. https://doi.org/10.1093/nar/gkab1049
10. Frankish A, et al. GENCODE reference annotation for the human and mouse genomes. *Nucleic Acids Research* 2019; 47(D1):D766–D773. https://doi.org/10.1093/nar/gky955
11. Volders PJ, et al. LNCipedia 5: towards a reference set of human long non-coding RNAs. *Nucleic Acids Research* 2019; 47(D1):D135–D139. https://doi.org/10.1093/nar/gky1031
12. Vibert J, et al. Oncogenic fusion proteins and their role in three-dimensional chromatin structure, phase separation, and cancer. *Molecular Cell* 2022; 82(18):3484–3498. https://doi.org/10.1016/j.molcel.2022.04.022
13. Khan A, Zhang X. dbSUPER: a database of super-enhancers in mouse and human genome. *Nucleic Acids Research* 2016; 44(D1):D164–D171. https://doi.org/10.1093/nar/gkv1002
14. Cheng J, et al. Accurate proteome-wide missense variant effect prediction with AlphaMissense. *Science* 2023; 381(6664):eadg7492. https://doi.org/10.1126/science.adg7492
15. ENCODE Project Consortium. An integrated encyclopedia of DNA elements in the human genome. *Nature* 2012; 489:57–74. https://doi.org/10.1038/nature11247
16. Moore JE, et al. Expanded encyclopaedias of DNA elements in the human and mouse genomes. *Nature* 2020; 583:699–710. https://doi.org/10.1038/s41586-020-2493-4
17. Kundaje A, et al. Integrative analysis of 111 reference human epigenomes. *Nature* 2015; 518:317–330. https://doi.org/10.1038/nature14248
18. Andersson R, et al. An atlas of active enhancers across human cell types and tissues. *Nature* 2014; 507:455–461. https://doi.org/10.1038/nature12787
19. Marsico G, et al. Whole genome experimental maps of DNA G-quadruplexes in multiple species. *Nucleic Acids Research* 2019; 47(8):3862–3874. https://doi.org/10.1093/nar/gkz179
20. Yan J, et al. Systematic analysis of binding of transcription factors to noncoding variants. *Nature* 2021; 591:147–151. https://doi.org/10.1038/s41586-021-03211-0
21. Dixon JR, et al. Topological domains in mammalian genomes identified by analysis of chromatin interactions. *Nature* 2012; 485:376–380. https://doi.org/10.1038/nature11222
22. Heinz S, et al. Simple combinations of lineage-determining transcription factors prime cis-regulatory elements required for macrophage and B cell identities. *Molecular Cell* 2010; 38(4):576–589. https://doi.org/10.1016/j.molcel.2010.05.004
23. Villar D, et al. Enhancer evolution across 20 mammalian species. *Cell* 2015; 160(3):554–566. https://doi.org/10.1016/j.cell.2015.01.006
24. Visel A, Minovitsky S, Dubchak I, Pennacchio LA. VISTA Enhancer Browser — a database of tissue-specific human enhancers. *Nucleic Acids Research* 2007; 35(Database issue):D88–D92. https://doi.org/10.1093/nar/gkl822
25. Ernst J, Kellis M. ChromHMM: automating chromatin-state discovery and characterization. *Nature Methods* 2012; 9:215–216. https://doi.org/10.1038/nmeth.1906
26. Ross-Innes CS, et al. Differential oestrogen receptor binding is associated with clinical outcome in breast cancer. *Nature* 2012; 481:389–393. https://doi.org/10.1038/nature10730
27. Zhang Y, et al. Model-based analysis of ChIP-Seq (MACS). *Genome Biology* 2008; 9:R137. https://doi.org/10.1186/gb-2008-9-9-r137

---

 
