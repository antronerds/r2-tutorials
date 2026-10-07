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

- [Fantom5 enhancers (permissive / robust / Gex FDR)](#fantom5-enhancers-permissive-robust-gex-fdr)
- [CAGE FANTOM5 Phase1 2 tpm Summary](#cage-fantom5-phase1-2-tpm-summary)
- [Hi-C domains (Literature)](#hi-c-domains-literature)

**[ChIP-seq & Chromatin State](#chip-seq-chromatin-state)**

**[References](#references)**

---

## Genome Structure & Sequence Features

### BlackListed (Consensus)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr21&start=9600000&end=11250000&a01giemsa=on&a10refseq=on&consensusblacklist=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr21:9,600,000-11,250,000, chosen because it holds ten blacklisted regions spanning five different label types.  
**UCSC track:** DAC Blacklisted Regions, a subtrack of Mapability (`wgEncodeMapability`, hg19)  
**Description:** The DAC Blacklisted Regions identify a comprehensive set of regions in the human genome that have anomalous, unstructured, high signal or read counts in next-generation sequencing experiments, independent of cell line and type of experiment. They were derived from 80 open chromatin tracks (DNase and FAIRE datasets) and 20 ChIP-seq input/control tracks spanning approximately 60 human tissue types and cell lines. These regions tend to have a very high ratio of multi-mapping to unique mapping reads and high variance in mappability. Some overlap pathological repeat elements such as satellite, centromeric and telomeric repeats, but simple mappability-based filters do not account for most of them, so UCSC recommends using this blacklist alongside mappability filters. Release 3, October 2011. Each region carries a label giving the reason for exclusion, shown on hover in R2: the most frequent are Low_mappability_island, BSR/Beta, centromeric_repeat, Satellite_repeat, LSU-rRNA_Hsa, ALR/Alpha and TAR1, alongside rarer labels such as High_Mappability_island, telomeric_repeat and chrM. [U1]

---

## Gene Annotation

### lincRNA from Lincipedia
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&lincipedia=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Description:** A publicly available database of human long non-coding RNA sequences and annotation, integrating lncRNA annotations from GENCODE, RefSeq and the literature, with an emphasis on large intergenic non-coding RNAs. [U2]

---

## Regulatory Elements & Chromatin Accessibility

### Fantom5 enhancers (permissive / robust / Gex FDR)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&fantom5_enhancer_premissive=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Candidate UCSC track:** FANTOM5 (`fantom5`, hg19)  
**Description:** Enhancer candidates identified from bidirectional capped RNAs in the FANTOM5 CAGE expression atlas, across over 800 human cell and tissue samples. The permissive set includes all identified enhancers; the robust set applies stricter thresholds. [U3]

---

### CAGE FANTOM5 Phase1 2 tpm Summary
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&gene_symbol=kras&a01giemsa=on&a10refseq=on&fantom5_phase1_2_tpm=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off)  
**Candidate UCSC track:** FANTOM5 (`fantom5`, hg19)  
**Description:** Mapped transcription start sites and their usage in primary cells, cell lines and tissues, profiled by HeliScopeCAGE, a variation of the CAGE protocol based on a single molecule sequencer. Filtered here at a minimum of 2 tags per million. [U3]

---

### Hi-C domains (Literature)
**View in R2:** [Open this annotation in the genome browser](https://hgserver1.amc.nl/cgi-bin/r2/main.cgi?option=gbv2_base&modus=complex%3Atview&genome_build=hg19&chrom=chr19&start=56400000&end=57600000&a01giemsa=on&a10refseq=on&hic_domains_lit=on&pluginopt%3Aa10refseq%3Arepresent=merge_by_symbol&tview_drawmode=off) - chr19:56,400,000-57,600,000, where the four dataset rows show both shared and cell-type-specific domain boundaries.  
**Description:** Topologically associating domains (TADs) identified from Hi-C chromosome conformation capture experiments. TADs are megabase-scale regions of preferential self-interaction; their boundaries are enriched for CTCF binding sites. [U4]

---

## ChIP-seq & Chromatin State

## References

U1. UCSC Genome Browser, hg19, track `wgEncodeMapability` - Mapability, subtrack DAC Blacklisted Regions (`wgEncodeDacMapabilityConsensusExcludable`). Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=wgEncodeMapability`. Created by Anshul Kundaje at Stanford University in the labs of Batzoglou and Sidow, in cooperation with Ewan Birney at EBI, for the ENCODE project. Release 3, October 2011. NOTE: this is the first-generation (v1) blacklist. Amemiya HM, Kundaje A, Boyle AP, *Sci Rep* 2019;9:9354 describes the later v2 blacklist and is NOT the source of this track. Check UCSC's References section on the track page for the citation attached specifically to the DAC subtrack rather than to the Mapability composite.

U2. Volders PJ, et al. LNCipedia 5: towards a reference set of human long non-coding RNAs. *Nucleic Acids Research* 2019;47(D1):D135-D139. doi:10.1093/nar/gky1031

U3. UCSC Genome Browser, hg19, track `fantom5` - FANTOM5. Track page: `genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=fantom5`. UCSC cites: Andersson R, et al. An atlas of active enhancers across human cell types and tissues. *Nature* 2014;507(7493):455-461. PMID 24670763. Arner E, et al. Transcribed enhancers lead waves of coordinated transcription in transitioning mammalian cells. *Science* 2015;347(6225):1010-4. PMID 25678556.

U4. Dixon JR, et al. Topological domains in mammalian genomes identified by analysis of chromatin interactions. *Nature* 2012;485:376-380. doi:10.1038/nature11222

