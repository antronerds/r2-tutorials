<style>
/* Page-local: inline code (track names, parameters) in body colour
   instead of the theme's red. Applies only to this page. */
.rst-content code.literal { color: #404040; background: #fbfbfb;
    border: 1px solid #e1e4e5; font-weight: normal; }
.rst-content a code.literal { color: #2980b9; }
</style>

# R2 Genome Browser - Annotation Track Reference

This document describes the annotation tracks available in the R2 genome browser. Each annotation description below includes a link to an example location in the R2 Genome Browser, with the corresponding track switched on.

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

- [RefSeq(R2)](#refseq-r2)
- [RefSeq(CDS)](#refseq-cds)
- [RefSeq_features](#refseq-features)
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
- [MACS 1.4 (AMC / Public)](#macs-1-4-amc-public)
- [MACS2 (Narrow) / MACS2 (Broad) 2](#macs2-narrow-macs2-broad-2)

**[References](#references)**

---

## Genome Structure & Sequence Features

### Giemsa / Cytoband
**View in R2:** [Giemsa / Cytoband](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Approximate locations of the cytogenetic bands seen on Giemsa-stained chromosomes, numbered outward from the centromere on the short (p) and long (q) arms. [1]

:::{dropdown} More...
**Background:** Band information is downloaded from NCBI and transformed into the browser's visualisation format; band lengths are typically estimated from FISH or other molecular markers interpreted via microscopy.

**In the R2 Genome Browser:**
- Hovering over a band shows its coordinates, band name and Giemsa stain; band names are also printed inside bands that are wide enough.
- Clicking a band zooms in to it.
- The `style` setting shows chromosomes in Giemsa colours, standard colours, or both.

**Source:** UCSC track: Chromosome Bands Localized by FISH Mapping Clones (`cytoBand`, hg19)
:::

---

### Sequence Bases (Sequence_b)
**View in R2:** [Sequence Bases (Sequence_b)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25362797&end=25362893&a01giemsa=on&a10refseq=on&a02bsequence=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** The reference genome sequence itself, shown as individual nucleotides when zoomed in. [2]

:::{dropdown} More...
**In the R2 Genome Browser:**
- The track is only drawn when zoomed in to 0.5 bp per pixel or less; the base letters appear from 0.1 bp per pixel.
- Hovering over a base shows its coordinate and the base.
:::

---

### CpG Islands
**View in R2:** [CpG Islands](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr9&start=21966750&end=21996323&a01giemsa=on&a10refseq=on&cpgisland=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Regions where CpG dinucleotides occur at much higher frequency than elsewhere in the genome; they are common near transcription start sites and promoters. [3]

:::{dropdown} More...
**Background:** CpG islands are associated with genes, particularly housekeeping genes, in vertebrates. Islands were predicted by scoring each dinucleotide and identifying maximally scoring segments, then requiring GC content of 50% or greater, length greater than 200 bp, and a ratio greater than 0.6 of observed to expected CpG dinucleotides.

**In the R2 Genome Browser:**
- Hovering over an island shows its position and name.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the islands are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).

**Source:** UCSC track: CpG Islands (`cpgIslandExt`, hg19)
:::

---

### Conservation (PlacMammal)
**View in R2:** [Conservation (PlacMammal)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&a04cons=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Per-base evolutionary conservation scores (phyloP) for the placental mammal subset of a 46-species vertebrate alignment; positive scores indicate conservation, negative scores accelerated evolution. [26]

:::{dropdown} More...
**Background:** UCSC aligns vertebrate species and derives several score sets from that one alignment - all vertebrates, the primates subset and the placental mammal subset - so 'placental mammal' and 'vertebrate' are not in conflict. phyloP scores each site independently and detects both conservation and acceleration, reporting accelerated sites as negative values; this makes it more variable from base to base than the hidden Markov model-based phastCons, which measures conservation only and considers runs of conserved sites.

**In the R2 Genome Browser:**
- Hovering shows the position and the phyloP score.
- The colour scale is capped at -2 and +2.
- Zoomed out beyond 1,024 bp per pixel, scores are averaged per pixel.

**Source:** UCSC track: Conservation, phyloP placental mammal subset (`phyloP46wayPlacental`, hg19)
:::

---

### Repeats (RepeatMasker)
**View in R2:** [Repeats (RepeatMasker)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&rmsk=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Interspersed repeats and low-complexity sequence identified with the RepeatMasker program, using the Repbase Update library. [4]

:::{dropdown} More...
**Background:** The Repbase Update library is maintained by the Genetic Information Research Institute.

**In the R2 Genome Browser:**
- Hovering over a repeat shows its position, repeat class, family and name.
- Clicking a feature zooms in to it.
- Individual repeats are drawn up to 1,000 bp per pixel; zoomed out further they are summarised as counts per bin.
- The `color_by` setting colours repeats by class (default, following the UCSC class colours) or by strand.
- The `modus` setting `by_class` groups the repeats by class.

**Source:** UCSC track: Repeating Elements by RepeatMasker (`rmsk`, hg19)
:::

---

### GC Percentage
**View in R2:** [GC Percentage](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr9&start=21966750&end=21996323&a01giemsa=on&a10refseq=on&a03gc=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr9:21,966,750-21,996,323, the same window as the CpG Islands entry so the two can be compared.  
**Description:** Percentage of G (guanine) and C (cytosine) bases in 5-base windows; high GC content is typically associated with gene-rich areas. [5]

:::{dropdown} More...
**In the R2 Genome Browser:**
- The track is drawn as a grey ramp: 30% GC or below is white, 80% or above is black, and values in between are shaded proportionally.
- Hovering shows the coordinates and the GC percentage.
- Zoomed out beyond 5,120 bp per pixel, windows sharing a pixel are averaged rather than dropped, so the track stays informative at any scale.

**Source:** UCSC track: GC Percent (`gc5Base`, hg19)
:::

---

### LaminB1_boundaries
**View in R2:** [LaminB1_boundaries](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr5&start=139860000&end=140950000&a01giemsa=on&a10refseq=on&laminb_steensel=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr5:139,860,000-140,950,000, showing a 582 kb lamina-associated domain with both borders in view.  
**Description:** Lamina-associated domains (LADs): genome regions that interact with the nuclear lamina in human Tig3 lung fibroblasts, mapped by DamID with a Dam-LaminB1 fusion protein. [6]

:::{dropdown} More...
**Background:** Genome-lamina interactions occur through more than 1,300 sharply defined domains of 0.1-10 megabases. These lamina associated domains (LADs) show low gene-expression levels, indicating a repressive chromatin environment, and their borders are demarcated by CTCF, by promoters oriented away from LADs, or by CpG islands. The hg19 coordinates were lifted over from hg18.

**In the R2 Genome Browser:**
- Hovering over a domain shows its position and name; the track reports a sharp-boundary domain score per domain (LaminB1_domain_shrp_bndr).
- Clicking a feature zooms in to it.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).

**Source:** UCSC track: NKI Nuclear Lamina Associated Domains (LaminB1 DamID) (`laminB1Super`, hg19)
:::

---

### R loop forming seq.
**View in R2:** [R loop forming seq.](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&rloopdb_merged=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Computationally predicted R-loop forming sequences from R-loopDB, merged into non-redundant regions. [27]

:::{dropdown} More...
**Background:** An R-loop is a three-stranded nucleic acid structure comprising nascent RNA hybridized with its DNA template strand while leaving the non-template DNA single-stranded. The regions in this track are predicted, not experimentally mapped.

**In the R2 Genome Browser:**
- Hovering over a region shows its position, strand and name.
- Clicking a feature zooms in to it.
- Zoomed out beyond 30,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count).
:::

---

### NAD domains Nemeth 2010
**View in R2:** [NAD domains Nemeth 2010](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56400000&end=57600000&a01giemsa=on&a10refseq=on&nad_nemeth_2010=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr19:56,400,000-57,600,000, a NAD covering the 19q13.43 zinc-finger gene cluster.  
**Description:** Nucleolus-associated domains (NADs) in HeLa cells: genomic regions in close contact with the nucleolus, together covering about 4% of the genome. [7]

:::{dropdown} More...
**Background:** NADs were mapped using 454 sequencing and microarray analysis and are built largely from particular gene families and satellite repeats. They overlap extensively with LADs and are enriched for heterochromatic marks, low gene density and low expression. The study identified 97 NADs with a median size of 749 kb, so most loci carry no annotation. Zinc-finger genes are 4-fold enriched in NADs relative to the genome; olfactory receptor and defensin genes are enriched in both NADs and LADs, far more strongly in NADs. Nucleolar association is cell-type dependent, so these HeLa domains may differ in other cells.

**In the R2 Genome Browser:**
- Domains are drawn in blue. Hovering over a domain shows its position and name; the track reports a per-domain score (hela_nad_nemeth_s1_2010).
- Clicking a feature zooms in to it.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

## Gene Annotation

### RefSeq(R2)
**View in R2:** [RefSeq(R2)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a10refseq=on&tview_drawmode=off)  
**Description:** Known protein-coding (NM_) and non-coding (NR_) genes from the NCBI RNA reference sequences collection (RefSeq). [8]

:::{dropdown} More...
**In the R2 Genome Browser:**
- Transcripts are coloured by strand: green for the plus strand, red for the minus strand. Exons and gene symbols appear when zoomed in.
- Hovering over a transcript shows its position, RefSeq accession, gene symbol and product description; hovering over an exon shows the exon position.
- Clicking a transcript or exon zooms in to it.
- Track settings let you show only protein-coding or non-coding transcripts (`class`), merge transcript variants into one representation per gene symbol (`represent` = `merge_by_symbol`), and highlight genes by name (`hilite`, separated by `;`).

**Source:** UCSC track: NCBI RefSeq Genes, loaded from the UCSC refFlat table (`refFlat`, hg19)
:::

---

### RefSeq(CDS)
**View in R2:** [RefSeq(CDS)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25362797&end=25362893&a01giemsa=on&a10refseq=on&a10refseq_cds=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Coding sequences of the RefSeq transcripts, shown codon by codon with the encoded amino acids. [8]

:::{dropdown} More...
**In the R2 Genome Browser:**
- The track is only drawn when zoomed in to 3 bp per pixel or less.
- Each codon is drawn as a block coloured by the amino acid it encodes; the amino-acid letter appears from 0.34 bp per pixel. A second row shows the coding-strand nucleotides (from 1 bp per pixel, letters from 0.1 bp per pixel).
- The `mode` setting emphasises one amino acid (for example stop codons) and fades the others; the `types` setting shows amino acids only.
- The tracks RefSeq(CDS) -1 and RefSeq(CDS) +1 show the translation in the reading frame shifted by one base.
:::

---

### RefSeq_features
**View in R2:** [RefSeq_features](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&a10refseq_features=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Features annotated in the NCBI RefSeq flat-file records, mapped to genome coordinates. [8]

:::{dropdown} More...
**In the R2 Genome Browser:**
- Hovering over a feature shows its position and the feature description from the RefSeq record.
- Clicking a feature zooms in to it.
:::

---

### Ensembl Gene e75
**View in R2:** [Ensembl Gene e75](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&a15ensgene=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Gene annotation from Ensembl release 75, built on the GRCh37/hg19 assembly. [9]

:::{dropdown} More...
**In the R2 Genome Browser:**
- Genes are drawn as footprints (their full extent, without exon structure).
- Hovering over a gene shows its position, gene name, biotype and description.

**Source:** UCSC track: Ensembl Genes (`ensGene`, hg19)
:::

---

### Gencode
**View in R2:** [Gencode](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gencode=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** The GENCODE reference annotation of the human genome: protein-coding and non-coding loci, including alternatively spliced isoforms and pseudogenes. [10]

:::{dropdown} More...
**Background:** GENCODE was produced for the ENCODE Project and combines automated Ensembl annotation with manual HAVANA curation.

**In the R2 Genome Browser:**
- The track dropdown lists the GENCODE versions available for the genome build; select the version to show. Hovering over a transcript also shows the GENCODE versions it occurs in.
- Transcripts are drawn as footprints when zoomed out; exons and labels appear when zoomed in.
- Hovering over a transcript shows its position, gene symbol and transcript accession, plus extra annotation where available. Hovering over an exon shows the exon; with `merge_by_symbol` it shows in how many of the gene's transcripts the exon occurs.
- Clicking a transcript or exon zooms in to it.
- Track settings: `class` (all, protein_coding, non_coding), `represent` (`merge_by_symbol` merges a gene's transcripts into one), `label` (symbol, transcript, both, off), `strand_show` (both, plus or minus strand) and `hilite` (gene names to highlight, separated by `;`).

**Source:** UCSC track: GENCODE Genes V19 (`wgEncodeGencodeV19`, hg19)
:::

---

### Neogenes Vibert 2022 Mol. Cell
**View in R2:** [Neogenes Vibert 2022 Mol. Cell](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&neogenes_vibert_2022=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Neogenes: novel spliced and polyadenylated transcripts induced by EWS::FLI1 and other chimeric transcription factors in otherwise transcriptionally silent regions of the genome. [11]

:::{dropdown} More...
**Background:** "EWS::FLI1 induces the robust expression of a specific set of novel spliced and polyadenylated transcripts within otherwise transcriptionally silent regions of the genome. These neogenes are virtually undetectable in large collections of normal tissues or non-EwS tumors." The study reports neogenes driven by EWS::FLI1 and by 22 further chimeric transcription factors across 17 cancer types.

**In the R2 Genome Browser:**
- Transcripts are drawn as footprints when zoomed out; exons and labels appear when zoomed in.
- Hovering over a transcript shows its position, gene symbol and transcript accession, plus extra annotation where available. Hovering over an exon shows the exon; with `merge_by_symbol` it shows in how many of the gene's transcripts the exon occurs.
- Clicking a transcript or exon zooms in to it.
- Track settings: `class` (all, protein_coding, non_coding), `represent` (`merge_by_symbol` merges a gene's transcripts into one), `label` (symbol, transcript, both, off), `strand_show` (both, plus or minus strand) and `hilite` (gene names to highlight, separated by `;`).
:::

---

## Regulatory Elements & Chromatin Accessibility

### Deepmind AlphaMissense
**View in R2:** [Deepmind AlphaMissense](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25362797&end=25362893&a01giemsa=on&a10refseq=on&deepmind_alpha_missense=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** AlphaMissense pathogenicity predictions for all possible single amino-acid substitutions in the human proteome. [12]

:::{dropdown} More...
**Background:** AlphaMissense is a deep learning method for predicting the pathogenicity of missense variants, classifying 32% of all missense variants as likely pathogenic and 57% as likely benign at a cutoff yielding 90% precision on ClinVar.

**In the R2 Genome Browser:**
- Each possible substitution is drawn as a dot whose height is its AlphaMissense pathogenicity score.
- Hovering over a dot shows the pathogenicity score, the nucleotide change and the amino-acid change.
- The `color_mode` setting colours dots by the resulting amino acid (default), by predicted effect (blue below 0.34, red above 0.564, grey in between), or all grey. `dotsize` and `height_histo` change the dot size and track height.

**Source:** UCSC track: AlphaMissense (`alphaMissense`, hg38)
:::

---

### Encode TF Clustered V3 (161 TFs)
**View in R2:** [Encode TF Clustered V3 (161 TFs)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_tf_v1=on&pluginopt%3Aencode_tf_v1%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) with transcription factor names switched on.  
**Description:** Transcription factor binding regions from ENCODE ChIP-seq experiments for 161 transcription factors, clustered across multiple cell types. [13]

:::{dropdown} More...
**Background:** The clusters are derived from a large collection of ChIP-seq experiments performed by the ENCODE project, together with DNA binding motifs identified within these regions by the ENCODE Factorbook repository.

**In the R2 Genome Browser:**
- Clusters are coloured by score, from blue (0) to red (1000).
- Hovering over a cluster shows its position and the transcription factor.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the clusters are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).

**Source:** UCSC track: Transcription Factor ChIP-seq Clusters (V3) (`wgEncodeRegTfbsClusteredV3`, hg19)
:::

---

### Encode TF Clustered (~340 TFs)
**View in R2:** [Encode TF Clustered (~340 TFs)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_tf_v2=on&pluginopt%3Aencode_tf_v2%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) with transcription factor names switched on.  
**Description:** ENCODE transcription factor ChIP-seq clusters covering approximately 340 transcription factors, a larger set than the V3 clustering track. [14]

:::{dropdown} More...
**In the R2 Genome Browser:**
- Clusters are coloured by score, from blue (0) to red (1000).
- Hovering over a cluster shows its position and the transcription factor.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the clusters are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).

**Source:** UCSC track: Transcription Factor ChIP-seq Clusters (`encRegTfbsClustered`, hg38)
:::

---

### ENCODE cCREs combined
**View in R2:** [ENCODE cCREs combined](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encodeccrecombined=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** ENCODE registry of candidate cis-regulatory elements (cCREs), classified as promoter-like (PLS), enhancer-like (ELS) or CTCF-only. [15]

:::{dropdown} More...
**Background:** The registry was built by integrating DNase-seq data into representative DNase hypersensitive sites, then classifying the subset with supporting histone or CTCF ChIP-seq signal as cCREs.

**In the R2 Genome Browser:**
- Hovering over an element shows its position, strand and cCRE label.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the elements are summarised as a histogram of counts per bin (hover shows the count).
- The `names` setting (`yes`) prints the cCRE labels in the image.

**Source:** UCSC track: ENCODE cCREs (`encodeCcreCombined`, hg38)
:::

---

### NIH Epigenome Roadmap
**View in R2:** [NIH Epigenome Roadmap](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&epi_roadmap=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Chromatin states of 111 reference epigenomes from the NIH Roadmap Epigenomics project: a 15-state hidden Markov model segmentation based on H3K4me3, H3K4me1, H3K36me3, H3K27me3 and H3K9me3. [16]

:::{dropdown} More...
**Background:** The NIH Roadmap Epigenomics Mapping Consortium produced a public resource of human epigenomic data, generating genome-wide maps of key histone modifications, chromatin accessibility, DNA methylation and mRNA expression across a large panel of human cell types and tissues. A separate 25-state track built on 12 marks is also available.

**In the R2 Genome Browser:**
- The track is only drawn when zoomed in to 200 bp per pixel or less.
- Each of the 15 states has its own colour, for example red for active TSS, yellow for enhancers and white for quiescent.
- Choose `all` epigenomes, a single epigenome, or `custom` with a list of samples. The `modus` setting switches between an `overview` (default), a grouped overview (`grp_overview`) and `detail`, which shows one row per epigenome.
- In `detail` mode, zoomed in to 100 bp per pixel or less, hovering shows the sample, chromatin state and sample label, and clicking zooms in to the segment.
:::

---

### G4_quadruplex HEK293T (G4-seq Marsico 2019)
**View in R2:** [G4_quadruplex HEK293T (G4-seq Marsico 2019)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&g4_quadruplex_hek293t=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** G-quadruplex (G4) structures in HEK293T cells, mapped experimentally with G4-seq under physiological potassium conditions. [17]

:::{dropdown} More...
**Background:** G4-seq is a high-throughput sequencing method for mapping DNA regions capable of forming G-quadruplex structures. G4 structures are enriched at gene promoters and are implicated in transcriptional regulation, DNA replication and genome stability.

**In the R2 Genome Browser:**
- Regions are coloured by score, from blue (-100) to red (100).
- Hovering over a region shows its position, name and score.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### SuperEnhancers (dbsuper)
**View in R2:** [SuperEnhancers (dbsuper)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&dbsuper=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Super-enhancers from the dbSUPER database, defined by H3K27ac signal across human tissues and cell types. [18]

:::{dropdown} More...
**Background:** "dbSUPER is the first integrated and interactive database of super-enhancers, which contains 82,234 super-enhancers in 102 human and 25 mouse tissue/cell types." Super-enhancers are clusters of transcriptional enhancers that drive cell-type-specific gene expression and are crucial to cell identity.

**In the R2 Genome Browser:**
- Hovering over a region shows its position, name and description.
- Clicking a feature zooms in to it.
- Zoomed out beyond 300,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### GVATdb (measured 83 T2D loci)
**View in R2:** [GVATdb (measured 83 T2D loci)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gvatdb_b1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Allelic transcription factor binding measured with SNP-SELEX for 95,886 common noncoding variants around 83 type 2 diabetes risk loci. [19]

:::{dropdown} More...
**Background:** Binding of 270 human transcription factors to the variants was measured using SNP-SELEX, a high-throughput multiplex protein-DNA binding assay yielding 828 million transcription factor-DNA interaction measurements. The variants were drawn from regions surrounding risk loci identified in genome-wide association studies.

**In the R2 Genome Browser:**
- Each entry is a variant-transcription factor pair, coloured from grey (0) to red (2) by the difference in log p-value between the alleles.
- Hovering shows the position, the transcription factor and a description of the measurement.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the entries are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### GVATdb DeltaSVM 1k genomes (94 TFs)
**View in R2:** [GVATdb DeltaSVM 1k genomes (94 TFs)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&gvatdb_deltasvm=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Predicted effects of 1000 Genomes variants on transcription factor binding, computed with deltaSVM models for 94 transcription factors. [19]

:::{dropdown} More...
**Background:** The deltaSVM models were trained on SNP-SELEX data. DeltaSVM scores quantify the predicted change in TF binding affinity resulting from each SNP allele.

**In the R2 Genome Browser:**
- Each entry is a variant-transcription factor pair, coloured by deltaSVM score from blue (-20) to red (+20).
- Hovering shows the position, the transcription factor and a description of the prediction.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the entries are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### Homer Known Motifs (Genome)
**View in R2:** [Homer Known Motifs (Genome)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&homer_known_motifs=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Genome-wide positions of known transcription factor binding motifs, predicted with HOMER. [20]

:::{dropdown} More...
**Background:** Motif-based predictions will miss weaker binding sites and produce some false positives, so the track is best used as a guide to where a factor is likely to bind rather than as a definitive binding map.

**In the R2 Genome Browser:**
- Hovering over a motif shows its position, strand, motif name and score.
- Clicking a motif zooms in to it.
:::

---

### Liver Enhancers (Cell 2015, Villar)
**View in R2:** [Liver Enhancers (Cell 2015, Villar)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&liver_enhancer_cell201501=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Human liver enhancers and active promoters, identified from H3K27ac and H3K4me3 profiling. [21]

:::{dropdown} More...
**Background:** "We track the evolution of promoters and enhancers active in liver across 20 mammalian species from six diverse orders by profiling genomic enrichment of H3K27 acetylation and H3K4 trimethylation. We report that rapid evolution of enhancers is a universal feature of mammalian genomes." Regions with H3K27ac only are enhancers; regions with H3K27ac combined with H3K4me3 are active promoters.

**In the R2 Genome Browser:**
- Hovering over a region shows its position, name and description.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### SuperEnhancers NB (George)
**View in R2:** [SuperEnhancers NB (George)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&superenhancer_nb_george=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Super-enhancer regions in neuroblastoma, defined from H3K27ac signal. [28]

:::{dropdown} More...
**Background:** Super-enhancers are clusters of transcriptional enhancers that mark cell-type-specific transcriptional programs; in MYCN-amplified neuroblastoma they are associated with MYCN itself and with other oncogenic drivers.

**In the R2 Genome Browser:**
- Hovering over a region shows its position, name and description.
- Clicking a feature zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).
:::

---

### Vista Enhancers
**View in R2:** [Vista Enhancers](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&vista_enhancers=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Human non-coding elements tested for enhancer activity in transgenic mouse embryos, from the VISTA Enhancer Browser. [22]

:::{dropdown} More...
**Background:** The VISTA Enhancer Browser identifies distant-acting transcriptional enhancers by coupling the identification of evolutionarily conserved non-coding sequences with a moderate-throughput mouse transgenesis enhancer assay. Conserved non-coding elements are cloned upstream of a minimal promoter fused to LacZ, injected into a fertilised mouse egg, and the 11.5 day embryo assayed with lacZ stain. An element is defined as a positive enhancer when it shows reproducible expression in the same structure in at least three independent transgenic embryos.

**In the R2 Genome Browser:**
- Hovering over an element shows its position, name and description.
- Clicking an element opens its page in the VISTA Enhancer Browser.
- Zoomed out beyond 50,000 bp per pixel, the elements are summarised as a histogram of counts per bin (hover shows the count). The threshold can be changed with the `xfactor_count_switch` setting.
- The `names` setting prints labels in the image: the name (`yes`), name and description (`ext`) or description only (`descr`).

**Source:** UCSC track: VISTA Enhancers (`vistaEnhancers`, hg19)
:::

---

## ChIP-seq & Chromatin State

### DiffBind
**View in R2:** [DiffBind](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&diffbind_v1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Regions with statistically significant differential ChIP-seq binding between sample groups, identified with the DiffBind R/Bioconductor package. [23]

:::{dropdown} More...
**In the R2 Genome Browser:**
- This is a sample-based track: select `all` samples, or `custom` and list the samples in the `custom_id` field.
- Hovering over a region shows its position, name, -10log p-value, concentrations (target and control) and fold change.
- Clicking a region zooms in to it; zoomed out far, regions are summarised as counts per bin.
- Settings: `logpval` sets the minimal -10log p-value (default 2); `modus` (`by_line`, `by_factor`) places samples on separate lines.
:::

---

### ENCODE bed v1 / ENCODE bed v1 Ext
**View in R2:** [ENCODE bed v1 / ENCODE bed v1 Ext](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&encode_bed_data_v1=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Transcription factor binding and histone modification peaks downloaded directly from the ENCODE portal. [25]

:::{dropdown} More...
**Background:** R2 provides two of these tracks drawn from separate tables: the plain track and an Ext version whose sample annotation carries an extra peak-type field, which also appears in the by_line and by_factor groupings - so Ext means extended annotation rather than extended regions or a larger set of experiments.

**In the R2 Genome Browser:**
- This is a sample-based track: select `all` samples, or `custom` and list the samples in the `custom_id` field.
- Peaks are drawn in blue, brightened in proportion to their signal value.
- Hovering over a peak shows the coordinates, the sample label, the description and the signal value. Clicking a peak zooms in to it.
- Beyond 5,000 bases per pixel the display switches from individual peaks to a grey histogram of peak counts per bin (`xfactor_count_switch`).
- The `modus` setting (`by_line`, `by_factor`) places samples on separate lines; both tracks can also be shown genome-wide in karyotype view.
:::

---

### MACS 1.4 (AMC / Public)
**View in R2:** [MACS 1.4 (AMC / Public)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr2&start=15640000&end=15750000&a01giemsa=on&a10refseq=on&macs14_geo_og_v1=custom&custom_id=GSM2113521%2CGSM2113517%2CGSM2113523&pluginopt%3Amacs14_geo_og_v1%3Amodus=by_line&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr2:15,640,000-15,750,000, three transcription factors in the BE2C neuroblastoma line sharing a binding site at the DDX1 promoter.  
**Description:** ChIP-seq peaks called with MACS 1.4 (default parameters, experiment versus input) at AMC OncoGenomics. [24]

:::{dropdown} More...
**Background:** MACS (Model-based Analysis of ChIP-Seq) identifies enriched regions in ChIP-seq data. Peaks are control-corrected and were called in-house whatever the origin of the data. The AMC and Public suffixes refer to where the ChIP-seq data came from, with Public denoting datasets taken from GEO. The samples in these tracks are predominantly transcription factors rather than histone marks, and peaks are narrow, on the order of one to two kilobases.

**In the R2 Genome Browser:**
- This is a sample-based track: select `all` samples, or `custom` and list the samples in the `custom_id` field.
- Hovering over a peak shows its position, sample, MACS score and summit position (with summit height). The MACS score is a different measure from the -10log p-value of the MACS2 tracks, so the two are not directly comparable.
- Clicking a peak zooms in to it; zoomed out far, peaks are summarised as counts per bin.
- The `macs_score` setting sets the minimal MACS score.
:::

---

### MACS2 (Narrow) / MACS2 (Broad) 2
**View in R2:** [MACS2 (Narrow) / MACS2 (Broad) 2](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56200000&end=57700000&a01giemsa=on&a10refseq=on&macs2_broad_og2_v1=custom&custom_id=GSM4105311atr-et200%2CGSM4105308atr-et200%2CGSM4105309atr-et200&pluginopt%3Amacs2_broad_og2_v1%3Amodus=by_line&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr19:56,200,000-57,700,000 with three histone marks from one cell line on separate rows.  
**Description:** ChIP-seq peaks called with MACS2 (200 bp read extension, experiment versus input): narrow peaks for transcription factors and ATAC-seq, broad peaks for histone marks such as H3K27me3, H3K9me3 or H3K36me3. [24]

:::{dropdown} More...
**Background:** MACS2 is the successor to MACS 1.4, with improved statistical modelling. R2 offers several of these tracks, attributed to different groups and batches: two broad tracks from AMC OncoGenomics, a third from AUMC CEMM, and the narrow track from AMC CEMM. They are batches of one pipeline split by contributing group rather than different methods, so the choice of track determines which samples are available rather than how the peaks were called. Peaks are control-corrected, and the -et200 suffix on the sample identifiers refers to the 200 bp read extension.

**In the R2 Genome Browser:**
- These are sample-based tracks: no peaks appear until samples are selected. Set the track to `custom` and list the sample identifiers, separated by commas, in the `custom_id` field; `modus` = `by_line` places each sample on its own labelled row.
- Hovering over a peak shows its position, sample, MACS2 -10log p-value, pileup and enrichment. Clicking a peak zooms in to it.
- Peaks are coloured by -10log p-value, up to the value set with `max_color_intensity` (default 40).
- The `macs2_logpval` setting filters on a minimal -10log p-value. Peak strength differs greatly between datasets - from around 4 in weak samples to over 70 in strong ones - so a filter that cleans up one dataset can remove another entirely. Broad marks spread their signal over tens of kilobases and score lower per peak than sharp promoter marks, so a threshold suited to H3K4me3 will remove most, though not all, H3K27me3.
:::

---

## References

Where a track was taken from the UCSC Genome Browser, the reference is the UCSC track description page, since UCSC may have processed or lifted over the data; the papers UCSC itself cites are listed alongside. Tracks not sourced from UCSC cite their original publication.

UCSC track description pages follow the pattern `genome.ucsc.edu/cgi-bin/hgTrackUi?db=<assembly>&g=<track>`.

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
