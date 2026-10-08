<style>
/* Page-local: inline code (track names, parameters) in body colour
   instead of the theme's red. Applies only to this page. */
.rst-content code.literal { color: #404040; background: #fbfbfb;
    border: 1px solid #e1e4e5; font-weight: normal; }
.rst-content a code.literal { color: #2980b9; }
/* Page-local: compact "More..." dropdowns (sphinx-design) */
.rst-content details.sd-dropdown { border: none; box-shadow: none;
    background: transparent; margin: -1em 0 1.2em 0; }
.rst-content details.sd-dropdown > summary.sd-summary-title {
    display: inline-flex; align-items: center; width: auto;
    padding: 0; border: none; background: transparent;
    font-size: 90%; font-weight: normal; color: #2980b9; }
.rst-content details.sd-dropdown > summary .sd-summary-up,
.rst-content details.sd-dropdown > summary .sd-summary-down {
    position: static; margin-left: 0.2em; line-height: 0; }
.rst-content details.sd-dropdown > summary svg { width: 1em; height: 1em; }
.rst-content details.sd-dropdown > .sd-summary-content {
    padding: 0.4em 0 0.1em 1em; border-left: 3px solid #e1e4e5; }
</style>

# R2 Genome Browser - Annotation Tracks Pending Confirmation

Staging document. These tracks need their source confirmed before publication. Once confirmed, entries move into the main annotation reference and the U-prefixed reference numbers are renumbered into the main list.

See the accompanying notes table for the specific open question per track.

---

## Contents

**[Genome Structure & Sequence Features](#genome-structure-sequence-features)**

- [BlackListed (Consensus)](#blacklisted-consensus)

**[Gene Annotation](#gene-annotation)**

- [lincRNA from Lincipedia](#lincrna-from-lincipedia)

**[Regulatory Elements & Chromatin Accessibility](#regulatory-elements-chromatin-accessibility)**

- [Fantom5 enhancers (permissive / robust)](#fantom5-enhancers-permissive-robust)
- [Fantom5 enhancers Gex FDR](#fantom5-enhancers-gex-fdr)
- [CAGE FANTOM5 Phase1 2 tpm Summary](#cage-fantom5-phase1-2-tpm-summary)
- [Hi-C domains (Literature)](#hi-c-domains-literature)

**[ChIP-seq & Chromatin State](#chip-seq-chromatin-state)**

**[References](#references)**

---

## Genome Structure & Sequence Features

### BlackListed (Consensus)
**View in R2:** [BlackListed (Consensus)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr21&start=9600000&end=11250000&a01giemsa=on&a10refseq=on&consensusblacklist=on&rmsk=on&pluginopt%3Armsk%3Amodus=by_class&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Regions of the human genome with anomalous, very high signal in sequencing experiments, independent of cell line and type of experiment (ENCODE blacklist); commonly used to filter out artefactual peaks. [U1]

:::{dropdown} More...
**Background:** The regions were derived from 80 open chromatin tracks (DNase and FAIRE datasets) and 20 ChIP-seq input/control tracks spanning approximately 60 human tissue types and cell lines. They tend to have a very high ratio of multi-mapping to unique mapping reads and high variance in mappability. Some overlap pathological repeat elements such as satellite, centromeric and telomeric repeats, but simple mappability-based filters do not account for most of them, so UCSC recommends using this blacklist alongside mappability filters. Each region carries a label giving the reason for exclusion: the most frequent are Low_mappability_island, BSR/Beta, centromeric_repeat, Satellite_repeat, LSU-rRNA_Hsa, ALR/Alpha and TAR1, alongside rarer labels such as High_Mappability_island, telomeric_repeat and chrM. The example view shows ten blacklisted regions of five types on the short arm of chromosome 21, together with RepeatMasker, so the overlap with repeat-dense sequence is visible.

**In the R2 Genome Browser:**
- Hovering over a region shows its position and the reason for exclusion (for example centromeric_repeat).
- Clicking a region zooms in to it.
- Zoomed out beyond 30,000 bp per pixel, the regions are summarised as a histogram of counts per bin (hover shows the count).
:::

---

## Gene Annotation

### lincRNA from Lincipedia
**View in R2:** [lincRNA from Lincipedia](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=hotair&a01giemsa=on&a10refseq=on&lincipedia=on&pluginopt%3Alincipedia%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Human long non-coding RNA (lncRNA) transcripts from the LNCipedia database, which integrates lncRNA annotations from GENCODE, RefSeq and the literature. [U2]

:::{dropdown} More...
**Background:** R2 spells the track "Lincipedia"; the resource is LNCipedia (lncipedia.org). LNCipedia lists many transcript models per lncRNA: the example view shows the eleven transcripts of HOTAIR (HOTAIR:1 to HOTAIR:11) in the HOXC cluster.

**In the R2 Genome Browser:**
- Each transcript is drawn with its exons (black) and introns (grey line).
- Hovering over a transcript shows its position, strand and name.
- Clicking a transcript zooms in to it.
- Zoomed out beyond 50,000 bp per pixel, the transcripts are summarised as a histogram of counts per bin (hover shows the count).
- The `names` setting (`yes`) prints the transcript names in the image.
:::

---

## Regulatory Elements & Chromatin Accessibility

### Fantom5 enhancers (permissive / robust)
**View in R2:** [Fantom5 enhancers (permissive / robust)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr7&start=27120000&end=27260000&a01giemsa=on&a10refseq=on&fantom5_enhancer_premissive=on&fantom5_enhancer_robust=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Enhancer candidates from the FANTOM5 CAGE expression atlas, identified by bidirectional capped RNA transcription across over 800 human cell and tissue samples; the robust set applies stricter thresholds than the permissive set. [U3]

:::{dropdown} More...
**Background:** The example view shows the HOXA cluster on chromosome 7, where six enhancer candidates lie between the HOXA genes and are found in both the permissive and the robust set.

**In the R2 Genome Browser:**
- The two sets are separate tracks: Fantom5 enhancers permissive and Fantom5 enhancers robust.
- Hovering over an enhancer shows its position and name (its coordinates).
- Clicking an enhancer zooms in to it.
- Zoomed out beyond 50,000 bp per pixel, the enhancers are summarised as a histogram of counts per bin (hover shows the count).
- The `names` setting prints the enhancer coordinates in the image, so the example view leaves it off.
:::

---

### Fantom5 enhancers Gex FDR
**View in R2:** [Fantom5 enhancers Gex FDR](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr4&start=74090000&end=74480000&a01giemsa=on&a10refseq=on&fantom5_enhancer_tss_fdr=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Links between FANTOM5 enhancers and the genes whose expression correlates with the enhancer's activity, with the correlation (R) and its false discovery rate (FDR). [U3]

:::{dropdown} More...
**Background:** In the R2 track name, "Gex FDR" refers to these enhancer-gene expression correlations. The example view shows links in the albumin gene cluster on chromosome 4, for example between enhancers and the promoter of ANKRD17.

**In the R2 Genome Browser:**
- Each link is drawn as a line between two blocks: a green block at the gene's transcription start site and a red block at the enhancer.
- Hovering over a link shows its position, the enhancer coordinates, the RefSeq transcripts and gene it is linked to, the correlation (R) and the FDR.
- Clicking a link zooms in to it.
- Zoomed out beyond 50,000 bp per pixel, the links are summarised as a histogram of counts per bin (hover shows the count).
:::

---

### CAGE FANTOM5 Phase1 2 tpm Summary
**View in R2:** [CAGE FANTOM5 Phase1 2 tpm Summary](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr12&start=25402800&end=25404300&a01giemsa=on&a10refseq=on&fantom5_phase1_2_tpm=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Transcription start sites mapped by CAGE in up to 1,834 FANTOM5 samples, summarised per CAGE peak in tags per million (tpm). [U3]

:::{dropdown} More...
**Background:** The transcription start sites and their usage in primary cells, cell lines and tissues were profiled by HeliScopeCAGE, a variation of the CAGE protocol based on a single molecule sequencer, and filtered at a minimum of 2 tags per million. The example view shows two CAGE peaks at the 5' end of KRAS.

**In the R2 Genome Browser:**
- Hovering over a CAGE peak shows its position, strand and name (for example CAGE_peak_1_at_KRAS_5end), the signal count, the average with its standard error, and the median with the 25th and 75th percentiles.
- Clicking a peak zooms in to it.
- Zoomed out beyond 3,000 bp per pixel, the peaks are summarised as a histogram of counts per bin (hover shows the count).
:::

---

### Hi-C domains (Literature)
**View in R2:** [Hi-C domains (Literature)](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56400000&end=57600000&a01giemsa=on&a10refseq=on&hic_domains_lit=on&pluginopt%3Ahic_domains_lit%3Anames=yes&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** Topologically associating domains (TADs) from published Hi-C experiments: megabase-scale regions of preferential self-interaction, whose boundaries are enriched for CTCF binding sites. [U4, U5]

:::{dropdown} More...
**Background:** The example view shows chromosome 19q13.43 with domains from three datasets: SK-N-SH (blue, Guo et al. 2015), H1-hESC (red) and IMR90 (green; Dixon et al. 2012). Shared boundaries show conserved structure; staggered boundaries show cell-type-specific topology.

**In the R2 Genome Browser:**
- Colour shows the dataset. Rows do not correspond to datasets: overlapping domains are placed on separate rows, so one dataset can appear on more than one row.
- Hovering over a domain shows its position, the cell line and the publication.
- Clicking a domain zooms in to it.
- Zoomed out beyond 300,000 bp per pixel, the domains are summarised as a histogram of counts per bin (hover shows the count).
- The `names` setting prints the cell line (`yes`) or the publication (`descr`) in the image.
:::

---

## ChIP-seq & Chromatin State

## References

U1. UCSC Genome Browser, hg19, track `wgEncodeMapability` - Mapability, subtrack DAC Blacklisted Regions (`wgEncodeDacMapabilityConsensusExcludable`). Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=wgEncodeMapability`. Created by Anshul Kundaje at Stanford University in the labs of Batzoglou and Sidow, in cooperation with Ewan Birney at EBI, for the ENCODE project. Release 3, October 2011. NOTE: this is the first-generation (v1) blacklist. Amemiya HM, Kundaje A, Boyle AP, *Sci Rep* 2019;9:9354 describes the later v2 blacklist and is NOT the source of this track. Check UCSC's References section on the track page for the citation attached specifically to the DAC subtrack rather than to the Mapability composite.

U2. Volders PJ, et al. LNCipedia 5: towards a reference set of human long non-coding RNAs. *Nucleic Acids Research* 2019;47(D1):D135-D139. doi:10.1093/nar/gky1031

U3. UCSC Genome Browser, hg19, track `fantom5` - FANTOM5. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=fantom5`. UCSC cites: Andersson R, et al. An atlas of active enhancers across human cell types and tissues. *Nature* 2014;507(7493):455-461. PMID 24670763. Arner E, et al. Transcribed enhancers lead waves of coordinated transcription in transitioning mammalian cells. *Science* 2015;347(6225):1010-4. PMID 25678556.

U4. Dixon JR, et al. Topological domains in mammalian genomes identified by analysis of chromatin interactions. *Nature* 2012;485:376-380. doi:10.1038/nature11222

U5. Guo Y, Xu Q, Canzio D, et al. CRISPR Inversion of CTCF Sites Alters Genome Topology and Enhancer/Promoter Function. *Cell* 2015;162:900-910. doi:10.1016/j.cell.2015.07.038
