# R2 Genome Browser - Annotation Track Reference

This document describes the annotation tracks available in the R2 genome browser. Where a track was taken from the UCSC Genome Browser, the reference is the UCSC track description page, since UCSC may have processed or lifted over the data; the papers UCSC itself cites are listed alongside. Tracks not sourced from UCSC cite their original publication.

UCSC track description pages follow the pattern `genome.ucsc.edu/cgi-bin/hgTrackUi?db=<assembly>&g=<track>`.

---

## Contents

**[Genome Structure & Sequence Features](#genome-structure-sequence-features)**

- [Giemsa / Cytoband](#giemsa-cytoband)
- [Sequence Bases (Sequence_b)](#sequence-bases-sequence-b)
- [CpG Islands](#cpg-islands)
- [Conservation (PlacMammal)](#conservation-placmammal)
- [Repeats (RepeatMasker)](#repeats-repeatmasker)
- [GC Percentage](#gc-percentage)
- [LaminB1_boundaries](#laminb1-boundaries)
- [R loop forming seq.](#r-loop-forming-seq)
- [NAD domains Nemeth 2010](#nad-domains-nemeth-2010)

**[Gene Annotation](#gene-annotation)**

- [RefSeq(R2) / RefSeq(CDS) / RefSeq_features](#refseq-r2-refseq-cds-refseq-features)
- [Ensembl Gene e75](#ensembl-gene-e75)
- [Gencode](#gencode)
- [Neogenes Vibert 2022 Mol. Cell](#neogenes-vibert-2022-mol-cell)

**[Regulatory Elements & Chromatin Accessibility](#regulatory-elements-chromatin-accessibility)**

- [Deepmind AlphaMissense](#deepmind-alphamissense)
- [Encode TF Clustered V3 (161 TFs)](#encode-tf-clustered-v3-161-tfs)
- [Encode TF Clustered (~340 TFs)](#encode-tf-clustered-340-tfs)
- [ENCODE cCREs combined](#encode-ccres-combined)
- [NIH Epigenome Roadmap](#nih-epigenome-roadmap)
- [G4_quadruplex HEK293T (G4-seq Marsico 2019)](#g4-quadruplex-hek293t-g4-seq-marsico-2019)
- [SuperEnhancers (dbsuper)](#superenhancers-dbsuper)
- [GVATdb (measured 83 T2D loci)](#gvatdb-measured-83-t2d-loci)
- [GVATdb DeltaSVM 1k genomes (94 TFs)](#gvatdb-deltasvm-1k-genomes-94-tfs)
- [Homer Known Motifs (Genome)](#homer-known-motifs-genome)
- [Liver Enhancers (Cell 2015, Villar)](#liver-enhancers-cell-2015-villar)
- [SuperEnhancers NB (George)](#superenhancers-nb-george)
- [Vista Enhancers](#vista-enhancers)

**[ChIP-seq & Chromatin State](#chip-seq-chromatin-state)**

- [DiffBind](#diffbind)
- [ENCODE bed v1 / ENCODE bed v1 Ext](#encode-bed-v1-encode-bed-v1-ext)
- [MACS 1.4 (AMC / DKFZ / Public)](#macs-1-4-amc-dkfz-public)
- [MACS2 (Narrow) / MACS2 (Broad) 2](#macs2-narrow-macs2-broad-2)

**[References](#references)**

---

## Genome Structure & Sequence Features

### Giemsa / Cytoband
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** Chromosome Bands Localized by FISH Mapping Clones (`cytoBand`, hg19)  
**Description:** The chromosome band track represents the approximate location of bands seen on Giemsa-stained chromosomes. Cytologically identified bands are numbered outward from the centromere on the short (p) and long (q) arms. Band information is downloaded from NCBI and transformed into the browser's visualisation format; band lengths are typically estimated from FISH or other molecular markers interpreted via microscopy. [1]

---

### Sequence Bases (Sequence_b)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25362797&end=25362893&a01giemsa=on&a10refseq=on&a02bsequence=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** The reference genome sequence itself, rather than an annotation derived from it. At sufficient zoom the individual nucleotides are displayed per genomic position. Hovering over a position reports the coordinate and the base at that position. [2]

---

### CpG Islands
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr9&start=21966750&end=21996323&a01giemsa=on&a10refseq=on&cpgisland=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** CpG Islands (`cpgIslandExt`, hg19)  
**Description:** CpG islands are regions where CpG dinucleotides are present at significantly higher levels than is typical for the genome as a whole. They are associated with genes, particularly housekeeping genes, in vertebrates, and are typically common near transcription start sites and promoter regions. Islands were predicted by scoring each dinucleotide and identifying maximally scoring segments, then requiring GC content of 50% or greater, length greater than 200 bp, and a ratio greater than 0.6 of observed to expected CpG dinucleotides. [3]

---

### Conservation (PlacMammal)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&a04cons=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** Conservation, phyloP placental mammal subset (`phyloP46wayPlacental`, hg19)  
**Description:** Per-base evolutionary conservation scores for the placental mammal subset of a 46-species vertebrate alignment, computed with phyloP. UCSC aligns vertebrate species and derives several score sets from that one alignment - all vertebrates, the primates subset and the placental mammal subset - so 'placental mammal' and 'vertebrate' are not in conflict. phyloP scores each site independently and detects both conservation and acceleration, reporting accelerated sites as negative values; this makes it more variable from base to base than the hidden Markov model-based phastCons, which measures conservation only and considers runs of conserved sites. R2 reads the table phylop46wayplacental. [26]

---

### Repeats (RepeatMasker)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&rmsk=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** Repeating Elements by RepeatMasker (`rmsk`, hg19)  
**Description:** Generated with the RepeatMasker program, which screens DNA sequences for interspersed repeats and low-complexity sequence, using the Repbase Update library from the Genetic Information Research Institute. [4]

---

### GC Percentage
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr9&start=21966750&end=21996323&a01giemsa=on&a10refseq=on&a03gc=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr9:21,966,750-21,996,323, the same window as the CpG Islands entry so the two can be compared.  
**UCSC track:** GC Percent (`gc5Base`, hg19)  
**Description:** The GC percent track shows the percentage of G (guanine) and C (cytosine) bases in 5-base windows. High GC content is typically associated with gene-rich areas. R2 draws the track as a grey ramp: 30% GC or below is white, 80% or above is black, and values in between are shaded proportionally. When zoomed out far enough that several windows share a pixel, their values are averaged rather than dropped, so the track stays informative at any scale. Hovering reports the coordinates and the GC percentage at that position. The track is off by default. [5]

---

### LaminB1_boundaries
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr5&start=139860000&end=140950000&a01giemsa=on&a10refseq=on&laminb_steensel=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr5:139,860,000-140,950,000, showing a 582 kb lamina-associated domain with both borders in view.  
**UCSC track:** NKI Nuclear Lamina Associated Domains (LaminB1 DamID) (`laminB1Super`, hg19)  
**Description:** A high-resolution map of genome interactions with the nuclear lamina in human Tig3 lung fibroblasts, determined by the DamID technique using a Dam-LaminB1 fusion protein. Genome-lamina interactions occur through more than 1,300 sharply defined domains of 0.1-10 megabases. These lamina associated domains (LADs) show low gene-expression levels, indicating a repressive chromatin environment, and their borders are demarcated by CTCF, by promoters oriented away from LADs, or by CpG islands. The hg19 coordinates were lifted over from hg18. In R2 the track renders as custom_laminb1_steensel and reports a sharp-boundary domain score per domain (LaminB1_domain_shrp_bndr). [6]

---

### R loop forming seq.
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&rloopdb_merged=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** An R-loop is a three-stranded nucleic acid structure comprising nascent RNA hybridized with its DNA template strand while leaving the non-template DNA single-stranded. This track displays computationally predicted R-loop forming sequences from R-loopDB, merged into non-redundant regions; R2 describes them as predicted rather than experimentally mapped. [27]

---

### NAD domains Nemeth 2010
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56400000&end=57600000&a01giemsa=on&a10refseq=on&nad_nemeth_2010=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr19:56,400,000-57,600,000, a NAD covering the 19q13.43 zinc-finger gene cluster.  
**Description:** Nucleolus-associated domains (NADs) are genomic regions in close contact with the nucleolus, mapped using 454 sequencing and microarray analysis. NADs make up roughly 4% of the human genome and are built largely from particular gene families and satellite repeats. NADs overlap extensively with LADs and are enriched for heterochromatic marks, low gene density and low expression. The study identified 97 NADs with a median size of 749 kb, covering roughly 4% of the genome, so most loci carry no annotation. Zinc-finger genes are 4-fold enriched in NADs relative to the genome; olfactory receptor and defensin genes are enriched in both NADs and LADs, far more strongly in NADs. In R2 the track renders as bed_nad_hela_nemeth and reports a per-domain score (hela_nad_nemeth_s1_2010); these are the HeLa NADs, and nucleolar association is cell-type dependent. [7]

---

## Gene Annotation

### RefSeq(R2) / RefSeq(CDS) / RefSeq_features
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a10refseq=on&tview_drawmode=off)  
**UCSC track:** NCBI RefSeq Genes (`refGene`, hg19). R2 loads this as the UCSC refFlat track, held internally in the tables `gb_refflat` and `gb_reflink`.  
**Description:** Known protein-coding and non-protein-coding genes taken from the NCBI RNA reference sequences collection (RefSeq). Colour shading indicates the level of review the RefSeq record has undergone: predicted (light), provisional (medium), reviewed (dark). [8]

---

### Ensembl Gene e75
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&a15ensgene=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** Ensembl Genes (`ensGene`, hg19)  
**Description:** Gene predictions generated by Ensembl. Release 75 is built on the GRCh37/hg19 assembly. [9]

---

### Gencode
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gencode=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** GENCODE Genes V19 (`wgEncodeGencodeV19`, hg19)  
**Description:** The GENCODE reference human genome annotation produced for the ENCODE Project, covering protein-coding and non-coding loci including alternatively spliced isoforms and pseudogenes, combining automated Ensembl annotation with manual HAVANA curation. [10]

---

### Neogenes Vibert 2022 Mol. Cell
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&neogenes_vibert_2022=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** "EWS::FLI1 induces the robust expression of a specific set of novel spliced and polyadenylated transcripts within otherwise transcriptionally silent regions of the genome. These neogenes are virtually undetectable in large collections of normal tissues or non-EwS tumors." The study reports neogenes driven by EWS::FLI1 and by 22 further chimeric transcription factors across 17 cancer types. [11]

---

## Regulatory Elements & Chromatin Accessibility

### Deepmind AlphaMissense
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25362797&end=25362893&a01giemsa=on&a10refseq=on&deepmind_alpha_missense=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** AlphaMissense (`alphaMissense`, hg38)  
**Description:** AlphaMissense predictions for all possible single amino acid substitutions in the human proteome. AlphaMissense is a deep learning method for predicting the pathogenicity of missense variants, classifying 32% of all missense variants as likely pathogenic and 57% as likely benign at a cutoff yielding 90% precision on ClinVar. Four lettered subtracks show scores for mutation from the reference to each nucleotide. [12]

---

### Encode TF Clustered V3 (161 TFs)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_tf_v1=on&pluginopt%3Aencode_tf_v1%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) with transcription factor names switched on.  
**UCSC track:** Transcription Factor ChIP-seq Clusters (V3) (`wgEncodeRegTfbsClusteredV3`, hg19)  
**Description:** Regions of transcription factor binding derived from a large collection of ChIP-seq experiments performed by the ENCODE project, together with DNA binding motifs identified within these regions by the ENCODE Factorbook repository. Clusters are derived from 161 transcription factors assayed across multiple cell types. In R2 the track renders with the row label wgencoderegtfbsclusteredv3, matching the UCSC table name. Each cluster is labelled with the transcription factor bound there, so at gene-scale zoom the dense binding at an active promoter is visible against the sparse gene body. [13]

---

### Encode TF Clustered (~340 TFs)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_tf_v2=on&pluginopt%3Aencode_tf_v2%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) with transcription factor names switched on.  
**UCSC track:** Transcription Factor ChIP-seq Clusters (`encRegTfbsClustered`, hg38)  
**Description:** An ENCODE transcription factor ChIP-seq clustering track covering approximately 340 transcription factors, larger than the V3 clustering track. [14]

---

### ENCODE cCREs combined
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encodeccrecombined=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** ENCODE cCREs (`encodeCcreCombined`, hg38)  
**Description:** The Registry of candidate cis-regulatory elements, built by integrating DNase-seq data into representative DNase hypersensitive sites, then classifying the subset with supporting histone or CTCF ChIP-seq signal as cCREs. Elements are classified as promoter-like (PLS), enhancer-like (ELS), or CTCF-only. [15]

---

### NIH Epigenome Roadmap
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&epi_roadmap=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** The NIH Roadmap Epigenomics Mapping Consortium produced a public resource of human epigenomic data, generating genome-wide maps of key histone modifications, chromatin accessibility, DNA methylation and mRNA expression across a large panel of human cell types and tissues. This track displays reference epigenome data from 111 consolidated epigenomes. In R2 it is a 15-state hidden Markov model segmentation based on five marks: H3K4me3, H3K4me1, H3K36me3, H3K27me3 and H3K9me3. A separate 25-state track built on 12 marks is also available. [16]

---

### G4_quadruplex HEK293T (G4-seq Marsico 2019)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&g4_quadruplex_hek293t=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Genome-wide map of experimentally observed G-quadruplex (G4) structures in HEK293T cells, generated using G4-seq, a high-throughput sequencing method for mapping DNA regions capable of forming G-quadruplex structures under physiological potassium conditions. G4 structures are enriched at gene promoters and are implicated in transcriptional regulation, DNA replication and genome stability. [17]

---

### SuperEnhancers (dbsuper)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&dbsuper=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** "dbSUPER is the first integrated and interactive database of super-enhancers, which contains 82,234 super-enhancers in 102 human and 25 mouse tissue/cell types." Super-enhancers are clusters of transcriptional enhancers that drive cell-type-specific gene expression and are crucial to cell identity. [18]

---

### GVATdb (measured 83 T2D loci)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gvatdb_b1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Binding of 270 human transcription factors to 95,886 common noncoding variants, measured using SNP-SELEX, a high-throughput multiplex protein-DNA binding assay yielding 828 million transcription factor-DNA interaction measurements. The variants were drawn from regions surrounding 83 type 2 diabetes risk loci identified in genome-wide association studies. [19]

---

### GVATdb DeltaSVM 1k genomes (94 TFs)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gvatdb_deltasvm=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Predicted allelic transcription factor binding effects for variants from the 1000 Genomes Project, computed using deltaSVM models trained on SNP-SELEX data from 94 transcription factors. DeltaSVM scores quantify the predicted change in TF binding affinity resulting from each SNP allele. [19]

---

### Homer Known Motifs (Genome)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&homer_known_motifs=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Genome-wide positions of known transcription factor binding motifs, predicted with HOMER. Motif-based predictions will miss weaker binding sites and produce some false positives, so the track is best used as a guide to where a factor is likely to bind rather than as a definitive binding map. [20]

---

### Liver Enhancers (Cell 2015, Villar)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&liver_enhancer_cell201501=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** "We track the evolution of promoters and enhancers active in liver across 20 mammalian species from six diverse orders by profiling genomic enrichment of H3K27 acetylation and H3K4 trimethylation. We report that rapid evolution of enhancers is a universal feature of mammalian genomes." This track displays the human liver enhancers identified in that study, defined as regions enriched for H3K27ac but not H3K4me3. [21]

---

### SuperEnhancers NB (George)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&superenhancer_nb_george=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Super-enhancer regions in neuroblastoma, defined from H3K27ac signal. Super-enhancers are clusters of transcriptional enhancers that mark cell-type-specific transcriptional programs; in MYCN-amplified neuroblastoma they are associated with MYCN itself and with other oncogenic drivers. [28]

---

### Vista Enhancers
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&vista_enhancers=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**UCSC track:** VISTA Enhancers (`vistaEnhancers`, hg19)  
**Description:** The VISTA Enhancer Browser identifies distant-acting transcriptional enhancers in the human genome by coupling the identification of evolutionarily conserved non-coding sequences with a moderate-throughput mouse transgenesis enhancer assay. Conserved non-coding elements are cloned upstream of a minimal promoter fused to LacZ, injected into a fertilised mouse egg, and the 11.5 day embryo assayed with lacZ stain. An element is defined as a positive enhancer when it shows reproducible expression in the same structure in at least three independent transgenic embryos. [22]

---

## ChIP-seq & Chromatin State

### DiffBind
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&diffbind_v1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** DiffBind is an R/Bioconductor package for identifying differentially bound ChIP-seq peaks between sample groups. The track displays regions showing statistically significant differential binding between conditions or groups. [23]

---

### ENCODE bed v1 / ENCODE bed v1 Ext
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_bed_data_v1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Peak files downloaded directly from the ENCODE portal, holding transcription factor binding sites and histone modification peaks. R2 provides two of these tracks drawn from separate tables: the plain track and an Ext version whose sample annotation carries an extra peak-type field, which also appears in the by_line and by_factor groupings - so Ext means extended annotation rather than extended regions or a larger set of experiments. Both are sample-based, using the same custom plus custom_id mechanism as the MACS tracks. Peaks are drawn in blue, brightened in proportion to their signal value, and hovering reports the coordinates, the sample label, the description and the signal value. Beyond 5000 bases per pixel the display switches from individual peaks to a grey histogram of peak counts per bin, and both tracks can also be shown genome-wide in karyotype view. [25]

---

### MACS 1.4 (AMC / DKFZ / Public)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr2&start=15640000&end=15750000&a01giemsa=on&a10refseq=on&macs14_geo_og_v1=custom&custom_id=GSM2113521%2CGSM2113517%2CGSM2113523&pluginopt%3Amacs14_geo_og_v1%3Amodus=by_line&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr2:15,640,000-15,750,000, three transcription factors in the BE2C neuroblastoma line sharing a binding site at the DDX1 promoter.  
**Description:** Peak calls generated using MACS (Model-based Analysis of ChIP-Seq) version 1.4, an algorithm for identifying enriched regions in ChIP-seq data. Like the MACS2 tracks these are sample-based, using the same custom plus custom_id mechanism. R2 describes them as MACS 1.4 analysis with default parameters on experiment versus input, generated at AMC OncoGenomics, so peaks are control-corrected and were called in-house whatever the origin of the data. The AMC, DKFZ and Public suffixes refer to where the ChIP-seq data came from, with Public denoting datasets taken from GEO. The samples in these tracks are predominantly transcription factors rather than histone marks, and peaks are narrow, on the order of one to two kilobases. Hovering a peak reports a MACS score and the summit position; note this is a different measure from the -10log p-value reported by the MACS2 tracks, so the two are not directly comparable. [24]

---

### MACS2 (Narrow) / MACS2 (Broad) 2
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56200000&end=57700000&a01giemsa=on&a10refseq=on&macs2_broad_og2_v1=custom&custom_id=GSM4105311atr-et200%2CGSM4105308atr-et200%2CGSM4105309atr-et200&pluginopt%3Amacs2_broad_og2_v1%3Amodus=by_line&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr19:56,200,000-57,700,000 with three histone marks from one cell line on separate rows.  
**Description:** Peak calls generated using MACS2, the successor to MACS 1.4, with improved statistical modelling. Narrow peaks are used for transcription factor ChIP-seq and ATAC-seq; broad peaks are used for histone modifications that span large genomic regions, such as H3K27me3, H3K9me3 or H3K36me3. These are sample-based tracks: peaks are drawn per sample from a selected ChIP-seq dataset, so no peaks appear until a dataset is loaded. R2 offers several of these tracks, all described as MACS2 analysis with extended reads of 200 bp on experiment versus input, but attributed to different groups and batches: two broad tracks from AMC OncoGenomics, a third from AUMC CEMM, and the narrow track from AMC CEMM. They are batches of one pipeline split by contributing group rather than different methods, so the choice of track determines which samples are available rather than how the peaks were called. Peaks are control-corrected, and the -et200 suffix on the sample identifiers refers to the 200 bp read extension. To display samples, set the track to custom and pass a comma-separated list of sample identifiers in the custom_id parameter; pluginopt:<track>:modus=by_line then places each sample on its own labelled row. Hovering a peak reports its MACS2 -10log p-value, pileup and enrichment, and the track can be filtered on a minimum -10log p-value. Peak strength differs greatly between datasets - values range from around 4 in weak samples to over 70 in strong ones - so a filter that cleans up one dataset can remove another entirely. It also differs systematically between marks: because broad marks spread their signal over tens of kilobases, they score lower per peak than sharp promoter marks, and a threshold suited to H3K4me3 will remove most, though not all, H3K27me3. The colour scale rescales to whatever is loaded. [24]

---

## References

1. UCSC Genome Browser, hg19, track `cytoBand` - Chromosome Bands Localized by FISH Mapping Clones. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=cytoBand`. UCSC cites: Cheung VG, et al. Integration of cytogenetic landmarks into the draft sequence of the human genome. *Nature* 2001;409(6822):953-8. PMID 11237021. Furey TS, Haussler D. Integration of the cytogenetic map with the draft human genome sequence. *Hum Mol Genet* 2003;12(9):1037-44. PMID 12700172.

2. UCSC Genome Browser, hg19, reference genome sequence (Base Position). `genome.ucsc.edu`. Kent WJ, et al. The human genome browser at UCSC. *Genome Research* 2002;12(6):996-1006. PMID 12045153.

3. UCSC Genome Browser, hg19, track `cpgIslandExt` - CpG Islands. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=cpgIslandExt`. UCSC cites: Gardiner-Garden M, Frommer M. CpG islands in vertebrate genomes. *J Mol Biol* 1987;196(2):261-82. PMID 3656447.

4. UCSC Genome Browser, hg19, track `rmsk` - Repeating Elements by RepeatMasker. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=rmsk`. UCSC cites: Smit AFA, Hubley R, Green P. RepeatMasker Open-3.0, 1996-2010. Jurka J. Repbase Update: a database and an electronic journal of repetitive elements. *Trends Genet* 2000;16(9):418-420. PMID 10973072.

5. UCSC Genome Browser, hg19, track `gc5Base` - GC Percent. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=gc5Base`. Data and presentation prepared by Hiram Clawson, UCSC. No primary publication is listed by UCSC for this track.

6. UCSC Genome Browser, hg19, track `laminB1Super` - NKI Nuclear Lamina Associated Domains (LaminB1 DamID). Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=laminB1Super`. Data generated by Guelen L, Pagie L and van Steensel B at the Netherlands Cancer Institute; GEO accession GSE8854. UCSC cites: Guelen L, et al. Domain organization of human chromosomes revealed by mapping of nuclear lamina interactions. *Nature* 2008;453(7197):948-51. PMID 18463634.

7. Nemeth A, et al. Initial genomics of the human nucleolus. *PLOS Genetics* 2010;6(3):e1000889. doi:10.1371/journal.pgen.1000889

8. UCSC Genome Browser, hg19, track `refGene` - NCBI RefSeq Genes. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=refGene`. UCSC cites: Kent WJ. BLAT - the BLAST-like alignment tool. *Genome Res* 2002;12(4):656-64. PMID 11932250. Pruitt KD, et al. RefSeq: an update on mammalian reference sequences. *Nucleic Acids Res* 2014;42(Database issue):D756-63. PMID 24259432.

9. UCSC Genome Browser, hg19, track `ensGene` - Ensembl Genes. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=ensGene`. UCSC cites: Hubbard T, et al. The Ensembl genome database project. *Nucleic Acids Res* 2002;30(1):38-41. PMID 11752248.

10. UCSC Genome Browser, hg19, track `wgEncodeGencodeV19` - GENCODE Genes V19. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=wgEncodeGencodeV19`. UCSC cites: Harrow J, et al. GENCODE: the reference human genome annotation for The ENCODE Project. *Genome Res* 2012;22(9):1760-74. PMID 22955987.

11. Vibert J, Saulnier O, Collin C, et al. Oncogenic chimeric transcription factors drive tumor-specific transcription, processing, and translation of silent genomic regions. *Molecular Cell* 2022;82(13):2458-2471.e9. doi:10.1016/j.molcel.2022.04.019

12. UCSC Genome Browser, hg38, track `alphaMissense` - AlphaMissense. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg38&g=alphaMissense`. UCSC cites: Cheng J, et al. Accurate proteome-wide missense variant effect prediction with AlphaMissense. *Science* 2023;381(6664):eadg7492. PMID 37733863.

13. UCSC Genome Browser, hg19, track `wgEncodeRegTfbsClusteredV3` - Transcription Factor ChIP-seq Clusters (V3). Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=wgEncodeRegTfbsClusteredV3`. UCSC cites: Gerstein MB, et al. Architecture of the human regulatory network derived from ENCODE data. *Nature* 2012;489(7414):91-100. PMID 22955619. Wang J, et al. Sequence features and chromatin structure around the genomic regions bound by 119 human transcription factors. *Genome Res* 2012;22(9):1798-812. PMID 22955990.

14. UCSC Genome Browser, hg38, track `encRegTfbsClustered` - Transcription Factor ChIP-seq Clusters. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg38&g=encRegTfbsClustered`. UCSC cites: ENCODE Project Consortium. An integrated encyclopedia of DNA elements in the human genome. *Nature* 2012;489(7414):57-74. PMID 22955616. Sloan CA, et al. ENCODE data at the ENCODE portal. *Nucleic Acids Res* 2016;44(D1):D726-32. PMID 26527727.

15. UCSC Genome Browser, hg38, track `encodeCcreCombined` - ENCODE cCREs. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg38&g=encodeCcreCombined`. UCSC cites: ENCODE Project Consortium. Expanded Encyclopedias of DNA Elements in the Human and Mouse Genomes. *Nature* 2020;583(7818):699-710.

16. Kundaje A, et al. Integrative analysis of 111 reference human epigenomes. *Nature* 2015;518:317-330. doi:10.1038/nature14248

17. Marsico G, et al. Whole genome experimental maps of DNA G-quadruplexes in multiple species. *Nucleic Acids Research* 2019;47(8):3862-3874. doi:10.1093/nar/gkz179

18. Khan A, Zhang X. dbSUPER: a database of super-enhancers in mouse and human genome. *Nucleic Acids Research* 2016;44(D1):D164-D171. doi:10.1093/nar/gkv1002

19. Yan J, et al. Systematic analysis of binding of transcription factors to noncoding variants. *Nature* 2021;591:147-151. doi:10.1038/s41586-021-03211-0

20. Heinz S, et al. Simple combinations of lineage-determining transcription factors prime cis-regulatory elements required for macrophage and B cell identities. *Molecular Cell* 2010;38(4):576-589. doi:10.1016/j.molcel.2010.05.004

21. Villar D, et al. Enhancer evolution across 20 mammalian species. *Cell* 2015;160(3):554-566. doi:10.1016/j.cell.2015.01.006

22. UCSC Genome Browser, hg19, track `vistaEnhancers` - VISTA Enhancers. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=vistaEnhancers`. Description excerpted by UCSC from the VISTA Enhancer Handbook and Methods page at Lawrence Berkeley National Laboratory. UCSC cites: Pennacchio LA, et al. In vivo enhancer analysis of human conserved non-coding sequences. *Nature* 2006;444(7118):499-502. PMID 17086198.

23. Ross-Innes CS, et al. Differential oestrogen receptor binding is associated with clinical outcome in breast cancer. *Nature* 2012;481:389-393. doi:10.1038/nature10730

24. Zhang Y, et al. Model-based analysis of ChIP-Seq (MACS). *Genome Biology* 2008;9:R137. doi:10.1186/gb-2008-9-9-r137

25. ENCODE Project Consortium. An integrated encyclopedia of DNA elements in the human genome. *Nature* 2012;489(7414):57-74. PMID 22955616. Peaks for these tracks were downloaded from the ENCODE portal, `www.encodeproject.org`.

26. UCSC Genome Browser, hg19, Conservation track, phyloP placental mammal subset. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=cons46way`. Method: Pollard KS, Hubisz MJ, Rosenbloom KR, Siepel A. Detection of nonneutral substitution rates on mammalian phylogenies. *Genome Research* 2010;20(1):110-121. PMID 19858363.

27. Jenjaroenpun P, et al. R-loopDB: a database for R-loop forming sequences (RLFS) and R-loops. *Nucleic Acids Research* 2017;45(D1):D119-D127. `doi.org/10.1093/nar/gkw1054`

28. Chipumuro E, Marco E, Christensen CL, et al. CDK7 inhibition suppresses super-enhancer-linked oncogenic transcription in MYCN-driven cancer. *Cell* 2014;159(5):1126-1139. PMID 25416950.
