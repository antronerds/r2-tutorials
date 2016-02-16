---
title: Preface
...

*Analyze the expression levels of a group of genes within a dataset*

*[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)*

-   Use R2 to investigate the expression levels of more than 1 gene
    within a specific dataset.

-   In this example the expression levels of small groups of genes
    listed from several pathways will be used showing which genes are
    differentially expressed per subgroup.

-   Adjust several parameters in the settings panel

-   In R2, the samples are annotated with e.g. clinical data. Each group
    of annotated data is called a â€œTrackâ€� in R2. These tracks can be
    used to split the group gene expression levels per track.

1.  Use â€œsingle datasetâ€� in field 1 and select the â€œTumor
    Medulloblastoma PLoS One - Kool - 62 - MAS5.0 - u133p2â€� dataset in
    field 2.

2.  Choose â€œView multiple genes â€� in field 3 and Click Next

3.  To illustrate the possibilities of the multiple gene view. Genes
    identified as classifiers for Medulloblastoma subtypes (Kool et al,
    Plos one) will be used. In the GENE/reporter textbox type or copy
    the following genes: AXIN2, BOC, dkk2, GABRA5, PTCH1, SMARCD3, WIF1
    and click next.

![ *Figure 1: Default multiple gene view.*
](https://raw.githubusercontent.com/antronerds/r2-tutorials/master/img/MultipleGenesView_perTrack.png)

1.  In Figure 1 a selection of gene expression profiles are depicted in
    one picture in contrast to the one gene view. The multiple gene view
    enables the option to represent the gene expression separately for
    each track. In this manner potential relations between subgroups and
    gene expression can be visualized.

2.  The dataset we are using is described in
    [PLoS One.](http://www.ncbi.nlm.nih.gov/pubmed/18769486)Â 2008 Aug
    28;3(8), Kool M et al. Here the classification of 5 medulloblastoma
    subgroups are reported and annotated as such: A,B,C,D and E. To
    investigate the expression levels of a small group of genes per
    sub-category select in the adjustable settings box â€œsubtype (cat)â€�
    at use track, â€œlump by group plot geneâ€� at handle groups by and
    â€œTrackâ€� at color by track. Further set transform tot â€œnoneâ€�, select
    â€œboxplotâ€� at Plot type and click NEXT.

![ *Figure 2: Multiple gene view per track*
](http://ogtoolbox/w/index.php?title=File:MultipleGenesView_perTrack.png)

1.  Most of the used genes are part of the WNT (subgroup A) and de SHH
    (subgroup B) signaling pathway overexpressed per subtype as shown by
    Kool et al. These genes are overexpressed in different
    Medulloblastoma molecular subtypes a,b,c,d and e are plotted
    together with the gene names. s

2.  Also try the â€œlump by gene plot groupâ€� which will produce an image
    where the genes are shown, separated by the subtypes.

3.  The sample filter option allows the user to generate a multiple gene
    view per track.

Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).

We hope that this tutorial has been helpful,The R2 support team.

*Why these tutorials?*

Even though many people like the concept of R2, getting started with the
platform as a new user can be a bit difficult or intimidating. With this
tutorial book, we hope to get new users started and at the same time
demonstrate the diverse set of functionalities to users which may
already have experience with R2, but want to get familiar with new
additions to the platform.

The setup of the wiki is as follows: We have divided the different
aspects of the R2 platform in a number of chapters which reflect tasks
that are often performed within R2. In each chapter, step by step
instructions guide you through an analysis, which you can perform online
within R2 yourself. During these steps, also features related to the
respective chapter, such as additional analyses or visualizations will
be introduced, thereby conveying the ease of using the interconnected R2
interface. Chapters 1-6 demonstrate a great number of core
functionalities, which you will encounter often and from different
angles when working within the platform. The next set of chapters (7-14)
dive more into specialized functions, that some of you may be interested
in. Chapter 15 demonstrates how users can adapt R2 to their needs by
explaining how you can generate your own grouping variables or store
personal lists of genes. This chapter also explains how you can start
your own user group and share information with specific other users for
collaborative work. The last two chapters further elaborate on this by
explaining how to add your own data and how to export data from R2 for
use in other tools.

By using the book creation tool you can select chapters and create your
own pdf suited to your specific needs.

We hope that these tutorials will be helpful. If you have any comments
or suggestions you're welcome to contact us through the [R2
website](http://r2.amc.nl).
