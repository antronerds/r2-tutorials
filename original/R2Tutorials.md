---
...





Preface
=======



*Why these tutorials?*





The R2 platform (<http://r2platform.com> / <http://r2.amc.nl)> is a
genomics analysis and visualization platform that tries to provide a
biologist friendly interface to high throughput data. It has been
developed within the department of Oncogenomics at the AMC in the
Netherlands, where it still serves as a primary entry point for all
types of high throughput data generated within the department. The R2
platform consists of 2 parts; a (publicly accessible) database, that
stores the data, coupled to a web-interface that provides a set of tools
and visualizations to mine the database.





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





We hope that these tutorials will be helpful. If you have any comments
or suggestions you're welcome to contact us through the [R2
website](http://r2.amc.nl).







Using Datasets
==============



*Selecting or searching for datasets in R2*








Scope
-----

-   Working with datasets.
-   R2 allows you to perform all kinds of analyses based on a well
    annotated single dataset or a selection of datasets at the
    same time. Different analyses are available based on the selection
    of one of these options in field 1.
-   R2 contains mRNA gene expression profiles for more than 70.000
    individual human samples. The samples are grouped in so
    called datasets. Each dataset has its own characteristics such
    tissue type, tumor type or from cell-line experiments.
-   The "**Tumor Neuroblastoma public - Versteeg - 88 - MAS5.0 -
    u133p2"** dataset will be used as an example dataset to guide you
    through most of the tutorial. Later on working with multiple
    datasets will be discussed.





Tutorial step 1
---------------

1.  In R2 a large amount of datasets are available for analysis
    and visualization. The numbered items in the main window will guide
    you through all the steps necessary to perform a task. In field
    **1** select "single dataset", in field **2** choose "change
    [![](_static/images/First_image_select_dataset.png)**Figure
    1: In the main screen
    "Change dataset".**](_static/images/First_image_select_dataset.png)
2.  A pull-down menu appears containing a large collection of datasets
    available for all types of analyses R2 is offering
3.  Click on the desired dataset.
    [![](_static/images/UsingDatasets_SelectSpecificDatasetFromPullDownInR2.png)**Figure
    2: Selecting datasets from the pull down menu on the main
    screen**](_static/images/UsingDatasets_SelectSpecificDatasetFromPullDownInR2.png)

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that datasets have an informative naming***

  Datasets have a structured naming in R2, using the following rules: *type\_of\_dataset - author - number\_of\_samples - normalization - chiptype*\
  Datasets are listed alphabetically
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 2
---------------

1.  Next to the pull down menu you can also choose for the "advanced
    dataset selection" tool. The advanced dataset selection facilitates
    searching through datasets using keywords and other filter options
    such as the minimal size of a dataset , the date a certain dataset
    was published etc. An example search would be finding all colon
    samples which are part of a mixed dataset consisting of normal
    tissue and tumor samples.
    [![](_static/images/UsingDatasets_AdvancedSelectionLink.png)**Figure
    3: Advanced selection of
    datasets**](_static/images/UsingDatasets_AdvancedSelectionLink.png)
2.  Click on the "Advanced" link. A new screen shows a table where the
    headers can be filled with search entries to fine tune your search
    for a dataset meeting your search criteria. Enter "Neuro" in the
    class column and" 50" in the "\#" column and select " greater than"
    from the pull down menu. This returns all the datasets containing
    the search term "Neuro" and having more than 50 samples.
    [![](_static/images/UsingDatasets_AdvancedSelectionPanelInR2.png)**Figure
    4: Advanced selection
    panel**](_static/images/UsingDatasets_AdvancedSelectionPanelInR2.png)
3.  Clicking on "Neuroblastoma" in the class 3 column containing 88
    samples reveals a detailed info box containing additional dataset
    information from the R2 database. When the dataset is publicly
    available clicking on the GEO ID link redirects to the GEO
    repository database where RAW data files are available. A Pubmed
    link is listed in case the dataset is linked to a publication listed
    in PubMed.
    Note: Clicking on an exclamation mark also shows detailed
    dataset information.
    [![](_static/images/UsingDatasets_AdditinalDatasetInfoInR2.png)**Figure
    5: Additional Dataset
    Info**](_static/images/UsingDatasets_AdditinalDatasetInfoInR2.png)
4.  Select "Across Datasets" in field **1**. Note that in field 2
    different options become available compared to the "single
    dataset" option.
    [![](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png)**Figure
    6: Selecting across
    datasets**](_static/images/UsingDatasets_SelectAcrossDatasetsInR2.png)



Analysis methods following selecting the "Across Datasets" option in
field **1** will be discussed in tutorial "Working with multiple
datasets".



+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that clicking on an exclamation balloon provides additional     |
| info***                                                                  |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=400){width="400"}](_static/images/U |
| singDatasets_ClickExclamationMarkForInfoInR2.png)       |
|                                               |
|                                                                          |
| \                                                                        |
|                                                                          |
|                                                                    |
|                                                                          |
| [![](http://ogtoolbox/w/index.php?oldid=400){width="400"}](_static/images/U |
| singDatasets_LinksToRawDataInR2.png)                    |
|                                               |
|                                                                          |
| \                                                                        |
| Clicking on the GEO ID link redirects to the GEO repository database     |
| where RAW data files are available. A Pubmed link is listed in case the  |
| dataset is linked to a publication listed in PubMed                      |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+



\



  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that the R2-support team is scanning public repositories for interesting datasets to expand the R2-database on a regular basis.In case you want to see a dataset added to R2 please send an email to r2-support@amc.nl***
  Such an email should contain a link to the publicly accessible files, such as a Gene Expression Omnibus number (GSE\*\*\*\*\*). Your own private datasets can also be added to R2 with user/group restricted access. please send an email to ***<r2-support@amc.nl>***
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,The R2 support team.









One Gene View
=============



*Analyze the expression levels of a single gene within a dataset*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Use R2 to investigate the expression levels of all samples from a
    specific dataset.
-   In this example the expression levels of the MYCN gene will be used.
-   Adjust several parameters in the advanced settings panel to get a
    better insight in the expressions levels or adapt your
    graphic layout.
-   In R2, the samples are annotated with e.g clinical data, each group
    of annotated data is called a "Track" in R2. These tracks can be
    used to filter data in all types of analyses R2 is offering.
-   A separated info panel in the one-gene expression level screen
    provides different types of analyses based on the expression level
    of the chosen gene.
-   Most of the mRNA expression datasets are generated with Affymetrix
    profiling arrays. In general these arrays use more than one so
    called probeset to measure the expression level of one single gene.
    With a separated module "Transcript view", the details of the
    probesets can be studied.





Tutorial step 1
---------------

1.  Use "Single Dataset" in field 1 and make sure that the "Tumor
    Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2" dataset is
    selected in field 2.
2.  Choose "View a gene" in field 3.
3.  Type MYCN and click "next".

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can find the latest R2 updates in the right panel in the R2 main screen***
  Click on "all news" to see previous R2 updates
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

[![](_static/images/OneGene_singleselect.png)**Figure
1: Single gene
selection**](_static/images/OneGene_singleselect.png)





Tutorial step 2
---------------

1.  In many cases more than one probeset is reported for each gene. In
    this example, there are 5 probesets annotated for the MYCN gene. By
    default, the probeset with the highest average present signal (APS)
    is selected. This APS signal is simply the average of all samples
    that are considered to express a selected gene (have a
    present call). Occasionally other probesets assigned to the same
    gene could be of interest depending on the structure of the gene
    (for example a potential splice variant). Also realize that the most
    informative probeset is re-determined in every dataset, sometimes
    resulting in a different probeset as the choice of R2. The
    expression levels are by default converted to log2 values.
    [![](_static/images/OneGene_Adjust.png)**Figure
    2: By default the probeset with the highest expression level is
    selected**](_static/images/OneGene_Adjust.png)
2.  It could be that for a specific graphical representation not all
    the (default) tracks need to be represented in a graph. To add or
    skip tracks, click on the Track Display section and select the
    appropriate tracks.
3.  In the adjustable settings screen use the pre-defined default
    settings and click "next".

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that a reporter with an exclamation marks is an indication      |
| there may be something wrong with the reporter (e.g. bad design)***      |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=250){width="250"}](_static/images/O |
| neGene_Probeset.png)                                    |
|                                               |
|                                                                          |
| \                                                                        |
| Hovering over the exclamation mark will inform you on what may be the    |
| issue with a specific reporter (probeset).Reportes with an issue will    |
| not be used to represent a gene in searches where hugoonce is used.\     |
| Hovering over the name of a gene will display concise gene information,  |
| such as alternative names for the current gene. In case you are not      |
| searching with an official NCBI genesymbol, R2 will also search the      |
| alternative names to find your gene of interest.                         |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+





Tutorial step 3
---------------

1.  R2 generates a YY-graph Figure 3 from the MYCN expression levels of
    all samples with expression levels ordered from left (low) to
    right (high). Hovering over the dots reveals additional annotation
    that R2 has stored for the focused sample.
2.  Underneath the X-axis, colored boxes are depicted, representing
    clinical information of the samples in so called "tracks". Again,
    hovering over them will reveal underlying data. For MYCN there is a
    clear relation between the expression levels and the tracks for
    "MYCN amplification" and "INSS-stage". So these tracks underneath
    the image give a quick glance at some of the clinical parameters,
    defined for the dataset. It is also possible to define your own
    custom made tracks, or disable/adapt the settings for default tracks
    (further explained in "Adapting R2 to your needs").
    [![](_static/images/OneGene_MYCN.png)**'Figure
    3: YY plot MYCN
    expression**](_static/images/OneGene_MYCN.png)
3.  Sometimes you get more insight by reviewing the expression levels
    with other transformations. Scroll down and transform the data
    (Figure 4), choosing "none", in the "transformation" pulldown menu
    and click adjust settings. In the "adjustable settings" panel, there
    are several other settings to adapt the graph R2 generates (like
    changing font sizes, or adding labels to the datapoints). To mark
    specific samples in the graph you can enter the sample ID"s in the
    "adjustable settings" field, several marking options can be selected
    (e.g: "epicenter" and "arrow"). To generate a graph of a subgroup of
    samples use the subset Select pulldown to select a specific group.
    Click "**confirm"** and the redraw button.

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that the Adjustable Settings panel is also available in the previous screen***
  Just scroll down
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.  [![](_static/images/OneGene_Marksample.png)**Figure
    4: Adjusting the graph
    settings**](_static/images/OneGene_Marksample.png)

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that converting expression levels using the "transform" option  |
| can help you to gain additional insight.***                              |
+--------------------------------------------------------------------------+
| There are several data transformations available                         |
| -   "none": Raw untransformed expression values, as they are represented |
|     in the R2 database.                                                  |
| -   "2log": logarithmic values with base of 2. Every increment           |
|     constitutes twice the amount.                                        |
| -   "rank": Data transformation in which numerical or ordinal values are |
|     replaced by their rank when the data are sorted by expression. This  |
|     transformation is useful for non-parametric statistical tests.       |
| -   "zscore": 2log transformed data, centered around the average and     |
|     expressed as the number of standard deviations from the average.     |
| -   "zscore\_nonlog": raw intensity values, centered around the average  |
|     and expressed as the number of standard deviations from the average. |
|     This transformation is useful when the intensities in R2 are not     |
|     raw, but for example logfolds as is often the case for aCGH data.    |
| -   "mad/mad2log": Median absolute deviation (on raw values, or log2     |
|     transformed values).                                                 |
| -   "center/log2center": Expression values centered around 0 (on raw     |
|     values, or log2 transformed values).                                 |
| -   "zcore\_group": Coverts the expression levels from the zscore within |
|     a group (track). Applicable when e.g technical variation in          |
|     expression levels is expected. A possible reason could be when       |
|     samples from the same dataset originate from different centers.      |
+--------------------------------------------------------------------------+





Tutorial step 4
---------------



Figure 5 lists for the various reporters of MYCN whether they are in
agreement with the genome position of MYCN reference sequence (RefSeq).
If all are stating "YES" then everything appears alright (from the
perspective of an automated assessment). For the MYCN reporters "NO"
indications indicate there may be an issue with it. Scroll down the page
and click on the "Tview" link in the reporter table.



[![](_static/images/OneGene_Probesettable.png)**Figure
5: Probeset verification
table**](_static/images/OneGene_Probesettable.png)
1.  A new screen (or TAB in the browser) appears with TranscriptView.
    The Transcript view application depicts the alignment of expressed
    sequence tags (EST) and mRNA sequences to the human reference genome
    sequence (Fig 5). The strand orientation of these sequences are
    indicated by a color (green = positive strand, red = negative
    strand, blue = strand information is missing). The structure of the
    reference sequence has also been indicated. Furtermore, it has also
    aligned the sequences used to generate the reporters on the array
    (in the case of Affymetrix microarrays). This view can be used to
    inspect the quality of a reporter. Note that the reporter
    "242046\_at" is aligned to the genomic region of the MYCN reference
    sequence, but that it"s color is different from the rest (colored
    in red). In addition in this particular case the reporter is also
    located in the intronic (light shaded color) region which is also a
    reason not to pick a certain probeset. Indeed, if we compare the
    gene expression values of this reporter, then its expression is 60
    fold lower than R2's standard pick (22 vs 1,369). Below the ESTs the
    average gene expression of the individual probesets is illustrating
    that for this example the correct probeset is selected for analysis.
    NB: Currently probeset verification is only provided for various
    human Affymetrix array types.

[![](_static/images/OneGene_Colorlegend.png)**Figure
6: Color
legend**](_static/images/OneGene_Colorlegend.png)[![](_static/images/OneGene_Tview.png)**Figure
7: MYCN reporters in Transcript
view**](_static/images/OneGene_Tview.png)
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can browse the gene expression values along the genome***

  Once you have entered the genome browser with an attached dataset (like above), you can also navigate to / zoom out any other region in the genome. This allows you to look at the neighboring genes in a single go.\
  What can also be informative is the ability to separate the expression on the basis of a track. This can be achieved by selecting 'dataset\_track' from the sample dropdown in the middle panel. Finally, within the genome browser, the contents for a panel on the left side can be hidden from a view by setting the height to 0.
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 5.
----------------

1.  Close the TranscriptView TAB or go back to the MYCN 1-gene-view
    expression screen.

[![](_static/images/OneGene_menupanel.png)**Figure
8:Left menu panel providing additional info (including link-out) and
analyses options**](_static/images/OneGene_menupanel.png)


In the left upper menu-panel several options are available to provide
you with additional information sources of the MYCN gene and additional
analyses. KaplanScan and Time Series analyses will be discussed in
separate tutorials. GeneCards will redirect you to an overview on your
gene of interest composed of many different resources. ProbePlus, will
provide the sequences probed by the U133 Affymetrix platforms (Will not
be shown in other platforms).\
Across datasets will generate an overview showing the average expression
of the gene of interest within all datasets of the same
platform/normalization scheme (provided that the normalization supports
dataset additions).



  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that the CliniSnitch reveals possible clinical relevance with a chosen gene***

  The CliniSnitch module assesses whether your gene of interest displays differential expression in any of the annotated parameters provided for a dataset.\
  To determine the best association, brute force T-testing is employed between every possible subset which can be defined in a track. Ps. When you add tracks of your own, then these are also tested.
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



Clicking on pubsniffer opens a new screen showing a list of how times
your gene of interest is found within the NCBI Pubmed database in
combination with dataset keywords. Clicking on "outlink" redirects you
**to Pubmed Pub-reminer** which is a tool for PubMed query building and
literature mining.



  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that the [Pub-reminer](http://hgserver2.amc.nl/cgi-bin/miner/miner2.cgi) is a helpful tool for literature mining***

  In the large amounts of medical literature, finding information tailored to your needs and interest is becoming more and more complex. Using the right keywords is essential for effective searches, but which ones should you use?\
  Pub re-miner is a web-based tool that allows simple text-based query building and information gathering (mining) of the NCBI literature search engine PubMed.\
  Pub re-miner presents its results, gathered from abstracts, in frequency tables of journals, authors and words, which can be included / excluded in an iterative fashion.\
  Next to building efficient queries, Pub re-miner can also be helpful in other areas: selecting a journal for your current work (by scanning the most often used journals of similar research) Finding experts in a research area (by viewing the authors associated with your query) Determine the research interest of an author (by viewing the keywords associated with an author
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 6
---------------



To investigate the values R2 uses for graph generation click on
"Datatable" to unfold a table with the expression levels for all
samples.



[![](_static/images/OneGene_Datatable.png)**Figure
9: Unfold the
datatable**](_static/images/OneGene_Datatable.png)


The "track display selection" section can be opened by clicking on it.
In here, you are able to toggle which tracks to display and/or hide
within the YY-plots. Do note that these selections are non-persistent
and will be forgotten as soon as you leave the xgeneview. Persistent,
changes to the tracks can be made via the "my settings" menu item, which
is present in the main screen. Note that the adjustable settings panel
including the customize track parameters are available throughout R2.



[![](_static/images/OneGene_trackdisplay.png)**Figure
10: Tick and drag
tracks**](_static/images/OneGene_trackdisplay.png)


Other convenient options are revealed by clicking the "more settings"
section. An extra panel unfolds which allows you to adapt your graph to
meet for example the requirements of a journal. The appearance of this
section will change depending on the kind of graph that you are
selecting.



[![](_static/images/OneGene_Adapting.png)**Figure
11: the extra settings
Panel**](_static/images/OneGene_Adapting.png)[![](_static/images/OneGene_Extrasettings.png)**Figure
12: Adapting a
graph**](_static/images/OneGene_Extrasettings.png)


In Figure 12 sample annotation ("Annot Graph") and legend ("Draw
Legend") were added. The "Annot Graph" option, adds the information of a
selected track to the YY-plot. This can be helpful for the addition of
Sample labels, or cell line names etc. Annotations can be shown in 3
ways; just below/on top of the expression value, as a series below the
annotation tracks or at the values for those samples that haven been
marked. The size of the annotation scales with the setting of the
dotsize.The adjustable settings menu is available in most of the R2
modules where a one-or two gene view is generated.



[![](_static/images/OneGene_Adapting.png)**Figure
13: Legend
added**](_static/images/OneGene_Adapting.png)[![](_static/images/OneGene_Adapting2.png)**Figure
14: Adapting annotation
size**](_static/images/OneGene_Adapting2.png)





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,The R2 support team.









Multiple Genes View
===================



*Analyze the expression levels of a group of genes within a dataset*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Use R2 to investigate the expression levels of more than 1 gene
    within a specific dataset.
-   In this example the expression levels of small groups of genes
    listed from several pathways will be used showing which genes are
    differentially expressed per subgroup.
-   Adjust several parameters in the settings panel
-   In R2, the samples are annotated with e.g. clinical data. Each group
    of annotated data is called a "Track" in R2. These tracks can be
    used to split the group gene expression levels per track.





Tutorial step 1
---------------

1.  Use "single dataset" in field 1 and select the "Tumor
    Medulloblastoma PLoS One - Kool - 62 - MAS5.0 - u133p2" dataset in
    field 2.
2.  Choose "View multiple genes " in field 3 and Click Next
3.  To illustrate the possibilities of the multiple gene view. Genes
    identified as classifiers for Medulloblastoma subtypes (Kool et al,
    Plos one) will be used. In the GENE/reporter textbox type or copy
    the following genes: AXIN2, BOC, dkk2, GABRA5, PTCH1, SMARCD3, WIF1
    and click next.



Test regular image



[![](_static/images/MultipleGenesView_Default.png)**Figure
1: Default multiple gene
view.**](Image:File:MultipleGenesView_Default.png)


Test with template



[![](_static/images/MultipleGenesView_Default.png)**Figure
1: Default multiple gene
view.**](_static/images/MultipleGenesView_Default.png)





Tutorial step 2
---------------

1.  In Figure 1 a selection of gene expression profiles are depicted in
    one picture in contrast to the one gene view. The multiple gene view
    enables the option to represent the gene expression separately for
    each track. In this manner potential relations between subgroups and
    gene expression can be visualized.
2.  The dataset we are using is described in
    [PLoS One.](http://www.ncbi.nlm.nih.gov/pubmed/18769486)"2008
    Aug 28;3(8), Kool M et al. Here the classification of 5
    medulloblastoma subgroups are reported and annotated as such:
    A,B,C,D and E. To investigate the expression levels of a small group
    of genes per sub-category select in the adjustable settings box
    "subtype (cat)" at use track, "lump by group plot gene" at handle
    groups by and "Track" at color by track. Further set transform tot
    "none", select "boxplot" at Plot type and click NEXT.

[![](_static/images/MultipleGenesView_perTrack.png)**Figure
2: Multiple gene view per
track**](_static/images/MultipleGenesView_perTrack.png)
1.  Most of the used genes are part of the WNT (subgroup A) and de SHH
    (subgroup B) signaling pathway overexpressed per subtype as shown by
    Kool et al. These genes are overexpressed in different
    Medulloblastoma molecular subtypes a,b,c,d and e are plotted
    together with the gene names. s
2.  Also try the "lump by gene plot group" which will produce an image
    where the genes are shown, separated by the subtypes.
3.  The sample filter option allows the user to generate a multiple gene
    view per track.





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,The R2 support team.









Annotation analyses
===================



*Using (custom) annotation tracks as input for analyses*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----



As you know by now, annotation of your data is stored in R2 as "tracks".
Within R2, one can easily create new annotation tracks. This can be done
either based on results generated within analyses, or completely
independent by uploading of tracks. In some cases it is of interest to
start comparing one track with another. The type of statistics used to
compare the tracks depends on the type of data; either categorical or
numerical. One may wonder if there are significant overlaps between 2
tracks (with categorical variables), based on Fisher"s exact test.
Alternatively, if there are multiple numerical tracks available; one may
wonder if there is a significant correlation between 2 tracks. For these
cases, R2 contains the Annotation modules; "relate 2 tracks" and
"annotation plotter".



-   Relate 2 tracks (categorical), test significant overlap and view as
    honeycomb-plot
-   Relate 2 tracks (numerical), assess significance of correlation and
    view as XY-plot
-   Relate 2 tracks (Categorical vs numerical), assess differential
    values between groups
-   Annotation plotter. Visualize tracks within sample cohort





Tutorial step 1: Relating 2 (categorical) tracks
------------------------------------------------

1.  Make sure that you are on the "main" page of R2, and that the
    selected dataset is "Tumor Neuroblastoma public - Versteeg - 88 -
    MAS5.0 - u133p2". From the "type of analysis" dropdown select
    "relate 2 tracks", which can be found in the annotation subsection
    and press next.
    [![](_static/images/AnnotationAnalyses_relate.png)**Figure
    1: Figure 1: Select "relate
    two tracks".**](_static/images/AnnotationAnalyses_relate.png)
2.  For the different tracks, make sure that you select a categorical
    one (which can be recognized by (cat)). Let"s investigate whether
    there is a relation between the neuroblastoma age-group
    (track=agegroup, flip point being 18 months at diagnosis) and the
    survival status (track=alive). Then press next to generate
    the result.
    [![](_static/images/AnnotationAnalyses_adjust.png)**Figure
    2: Select "Selecting categorical
    tracks**](_static/images/AnnotationAnalyses_adjust.png)
3.  The generated result is now displayed on the screen. As we are
    testing 2 categorical variables, R2 has tested the relation between
    the 2 tracks and finds a highly significant Fisher"s exact p-value,
    indicating that there is a relation between the agegroup and vital
    status of the patients. The result is also shown in a honeycomb
    image, where every individual patient is represented as a separate
    circle, with the annotation as a hover box.
4.  One can add more visual information to the plot, by coloring the
    patients on the basis of a track. From the adjustable settings at
    the bottom of the page, set the "colormode" to "color by track" and
    select the "inss\_stage" as track. Press the adapt settings to
    create an updated image. Now we can clearly see that there is a
    great over-representation of stage 4 patients in the group of
    diseased patients who are older than 18 months.

[![](_static/images/AnnotationAnalyses_colorsamples.png)**Figure
3: "Color samples by
track**](_static/images/AnnotationAnalyses_colorsamples.png)





Tutorial step 2: Relating 2 (numerical) tracks
----------------------------------------------

1.  Just as in the previous example, we select the "relate 2 tracks"
    option from the main R2 screen and press enter. Now this time, we
    select 2 numerical tracks, which can be recognized by the (\#) sign
    at the end of a track. Within the Neuroblastoma dataset our options
    are limited for this example, so we select the "age in years" track
    vs the "nti\_surv\_overall" track and proceed to the next screen.
2.  In the result page, R2 has detected that 2 numerical tracks were
    selected, so the correlation between the different tracks is being
    displayed and tested for statistical significance. Just as in the
    previous example, we could color the patients by a track if that
    would be appropriate.

[![](_static/images/AnnotationAnalyse_relatetracks.png)**Figure
4: "Output of relating numerical
tracks**](_static/images/AnnotationAnalyse_relatetracks.png)





Tutorial step 3: Relating a categorical track to a numerical track
------------------------------------------------------------------

1.  The last example for relating 2 tracks, involves the combination of
    a numerical one to a categorical track. Essentially, this option
    allows you to test meta-gene data (such as combined expression
    values of multiple genes expressed as a single value) as well, where
    you could create a track containing only value information for the
    patients, and test this track to clinical parameters. We again
    select "Relate 2 tracks" from the main menu and navigate to the
    next page.
2.  From the track options, we choose a categorical track for X (inss
    stage), and a numerical one for Y (nti\_surv\_overall) and navigate
    to the next page.
3.  The result page will now start to look like view a gene in groups,
    only this time using the data contained in your track. Via the
    adjustable settings, you can change the representation to another
    plot type, such as a boxplot, change the colormode to color by
    track, and you have a nice result here, showing that the survival
    rate is significantly lower in patients of INSS stage 4.

[![](_static/images/AnnotationAnalyse_relationnumcat.png)**Figure
5: Representing the relation between categorical and numerical
tracks**](_static/images/AnnotationAnalyse_relationnumcat.png)


As a recap for the last 3 tutorial steps, you have used the "relate 2
tracks" option from the annotation methods in R2 and represented
different types of tracks with each other to gain new insights from
combining 2 tracks. Below the 3-different representations are depicted
side by side. Do remember, that this module allows you to use "meta
data" tracks that you can assemble either within, but also outside of R2
via the uploading of a track option that will be shown in the "adapting
r2 to your needs" chapter.



[![](_static/images/AnnotationAnalyse_representation.png)**Figure
6: "Representations of relations between different types of tracks in
R2**](_static/images/AnnotationAnalyse_representation.png)





Tutorial step 4: Annotation plotter
-----------------------------------

1.  In some publications, patient data is represented in slick looking
    annotation plots, showing the patient characteristics in rectangles.
    In a sense, these are just like the tracks that are represented
    underneath YY-plots in R2. To allow users to create these "track"
    figures, ordered in a user provided order, we have implemented the
    annotation plotter in R2.
2.  Make sure that you are on the "main" page of R2, and that the
    selected dataset is "Tumor Neuroblastoma public - Versteeg - 88 -
    MAS5.0 - u133p2". From the "type of analysis" dropdown select
    "Annotation plotter", which can be found in the annotation
    subsection and press next.
3.  The default view for the dataset will be plotted. Now one can change
    the tracks to display (with track display selection), as well as the
    order in which the samples should be ordered (track sort order). The
    order in which tracks are selected for ordering will also dictate
    the final sort. For some complicated sorts, it may be necessary to
    create a numeric track that puts the sample in the intended order.

[![](_static/images/AnnotationAnalyse_plotting.png)**Figure
7: Plotting the annotation
tracks**](_static/images/AnnotationAnalyse_plotting.png)





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,





The R2 support team.









Differential expression of genes in your dataset
================================================



*Find out which genes make a difference between groups of samples in
your dataset*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Use R2 to find which genes exhibit differential expression between
    groups of samples in a dataset.
-   Use R2 to determine whether the expression of your gene of interest
    is significantly different between groups of samples
-   This is established by use of statistical tests. R2 will guide you
    through this process in a self-explanatory way
-   This requires proper annotation of the dataset to enable assignment
    of samples to groups. In this tutorial a set of neuroblastoma tumors
    is used that is annotated with several clinical parameters:
    survival, age of diagnosis, etc.
-   All (advanced) parameters can be adapted to your specific needs
-   In separate boxes these settings will be elaborated upon
-   The results of these analyses are presented in adaptable graphics





Tutorial step 1
---------------

1.  Logon to the R2 homepage using your credentials and make sure the
    "Single Dataset" field is selected in field 1 of the R2
    step-by-step guide.
2.  Make sure the Tumor Neuroblastoma public dataset is selected in
    field 2 (For additional information on these first two steps,
    consult tutorial 1: Choose "View a gene in groups" in field 3.
3.  Type MYCN as gene (see Figure 1) in field 4.
4.  Click "next" in field 5.

[![](_static/images/DiffentialExpression_Gene.png)**Figure
1: Step-by-step scenario: selecting to 'View a gene in groups' on the
main page of
R2**](_static/images/DiffentialExpression_Gene.png)





Tutorial step 2
---------------

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can create your own tracks?***

  This is explained in a separate tutorial "Adapting R2 to your needs"\
  Datasets are listed alphabetically
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.  In the next screen you will decide which grouping variable to use to
    establish the differential expression of your gene of interest. In
    R2 the so called "tracks" contain this annotation. For the current
    dataset there is a track called "alive" containing survival data of
    the patients from whom the tumor sample was taken. Select this
    (Figure 2). Note that the other fields can be kept as is, the right
    choices are already provided. Note also that the proper reporter
    probeset is already selected.
2.  Click "next"

[![](_static/images/DiffentialExpression_Select.png)**'Figure
2: Selecting the proper annotation track to differentiate expression
data**](_static/images/DiffentialExpression%20Select.png)
+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that samples can be filtered and/or marked?***                  |
+--------------------------------------------------------------------------+
|                                               |
|                                                                          |
| Under the sub-header "Sample Filter" you can select a specific subset of |
| samples based on the annotation (track).\                                |
| The analysis will only be performed on the selected subset. In Fig 2a    |
| the track gender was selected that enables filtering on gender.\         |
| Be sure to click the red confirm link to set the filter, or make further |
| selections. Filtering and marking samples Keep in mind that you can      |
| repeat the filter procedure on top of the previous one.\                 |
| Don"t forget the red "confirm" link before switching tracks. The extra   |
| graph option allows the users to select different graphical              |
| representations.\                                                        |
| In the samples to mark section, a sample name can be entered that will   |
| be highlighted resulting graph; ideal for publication purposes.          |
|                                                                          |
|                                                                    |
|                                                                          |
| [![](http://ogtoolbox/w/index.php?oldid=250){width="250"}](_static/images/D |
| iffentialExpress_Adjust.png)                            |
+--------------------------------------------------------------------------+





Tutorial step 3
---------------

1.  In the next window a selection of the groups can be made. Only the
    selected group will be displayed in the graph; the "one way
    Anova"/"student T test" test will be performed for data on both
    groups (of course, see explanation in step 4). In this case this we
    want to see both groups so keep the selection as is.
    [![](_static/images/DiffentialExpression_Selectgroup.png)**Figure
    3: Selecting groups for the
    graph**](_static/images/DiffentialExpression_Selectgroup.png)
2.  Click "next"





Tutorial step 4
---------------

1.  R2 now performs a one-way Anova statistical test on the fly. This
    **AN**alyis **O**f **VA**riance is a statistical test that
    calculates whether the means of variables differ between two or
    more groups. In the case of 2 groups, this is identical to the
    student T-test. ANOVA can be concerned a sound test when the
    variables are normally distributed and samples are independent. More
    information here:
    [](http://en.wikipedia.org/wiki/One-way_ANOVA)<http://en.wikipedia.org/wiki/One-way_ANOVA>.
    A simple example calculation can be found here:
    [](http://en.wikipedia.org/wiki/F_test#One-way_ANOVA_example)<http://en.wikipedia.org/wiki/F_test#One-way_ANOVA_example>.
    R2 shows the result by default as a graph where the mRNA expression
    of the samples is plotted over the two groups with increasing
    expression (Figure 3Figure 4). Note that the "alive" annotation is
    in the second row (track) beneath the graph. The actual result of
    the calculations is shown above the graph; the difference in average
    expression between the two groups is significant. These results can
    also be shown in a more conventional bar-plot by adapting the
    settings and redrawing the graph.
    [![](_static/images/DiffentialExpress_Result.png)**Figure
    4: Result of the one-way Anova test for the Neuroblastoma
    88 samples.**](_static/images/DiffentialExpress_Result.png)
2.  Scroll down the window
3.  Adapt the selection in the dropdown box 'Graphtype' to 'Barplot' and
    'ColorMode' to 'Color by Track'
4.  Click 'Adjust Settings' (Figure 5)

[![](_static/images/DiffentialExpression_AdaptGraph.png)**Figure
5: Adapting the Graphtype to BarPlot and set Color by
Track**](_static/images/DiffentialExpression_AdaptGraph.png)





Tutorial step 5
---------------

1.  The resulting graph is adapted accordingly (Figure 5)
    [![](_static/images/DiffentialExpression_Barplot.png)**Figure
    6: The same data as a
    Barplot**](_static/images/DiffentialExpression_Barplot.png)
2.  The difference can be shown more dramatically by plotting the data
    without a log2 transformation, scroll down again. Do report the test
    results based on the log transformed data though, as
    none-transformed mRNA gene expression data is hardly ever
    normally distributed.
3.  In the 'Adjustable settings' dialog, set the 'Transform' dropdown to
    'none' (Figure 7)
4.  Click 'Adjust Settings'
    [![](_static/images/DiffentialExpress_BarplotAdjust.png)**Figure
    7: Adjusting data
    transformation**](_static/images/DiffentialExpress_BarplotAdjust.png)
5.  The resulting graph in Figure 8 shows the difference
    more dramatically.
    [![](_static/images/DiffentialExpress_BarplotNotransform.png)**Figure
    8: Bar plot without
    transformation**](_static/images/DiffentialExpress%20BarplotNotransform.png)
6.  Note furthermore the menu items to the right and left of the graph.
    The left panel contains hyperlinks that provide further information
    about this gene and additional analysis options. The KaplanScanner
    will be explained in a separate tutorial. The right panel allows you
    to change your gene of interest immediately, while keeping all the
    changes that you have made to the graphical representation; just
    type a gene name and click 'Change Gene'. The "sample overview"
    shows the clinical data associated with the samples. Click the view
    button for the first sample.
7.  Figure 9 shows the clinical data associated with that
    particular sample.
    [![](_static/images/DiffentialExpress_ClinAnno.png)**Figure
    9: Clinical annotation of a
    sample**](_static/images/DiffentialExpress%20ClinAnno.png)





Tutorial step 6
---------------

1.  It would be a pretty tedious job to look for all genes whether they
    are differentially expressed between groups. Why not let R2 do the
    job for you? Go back to the Main screen, by clicking the link in the
    upper left corner of the screen
2.  In field 3 of the R2 step-by-step guide select 'Find Differential
    expression between groups' (Figure 10)
    [![](_static/images/DiffentialExpress_FindDiff.png)**Figure
    10: Selecting Find
    Differential Expression.**](_static/images/DiffentialExpress%20FindDiff.png)
3.  Click 'Next'





Tutorial step 7
---------------

1.  In the next window there appear quite a few choices for setting the
    statistical parameters for this analysis. Luckily only one is of
    real immediate importance; selecting the track of choice (shown
    in red). Select the 'Alive' track again.
    [![](_static/images/DiffentialExpress_AdaptParam.png)**'Figure
    11: Differential expression
    parameters**](_static/images/DiffentialExpress_AdaptParam.png)
2.  Click "next"
3.  In the next screen click next also; R2 now calculates for all genes
    (under the parameters set) a one way anova test and also corrects
    this for multiple testing! (Figure 12). An amazing amount of
    calculations! R2 performs this on the fly.

[![](_static/images/DiffentialExpress_Progress.png)**Figure
12: Progress dialog during on the fly
calculation**](_static/images/DiffentialExpress%20Progress.png)
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that all other parameters have a meaning?***

  **HugoOnce**:For most analysis genes should only be reported once in a dataset. R2 uses an algorithm called HugoOnce to choose a single probe-set to represent a gene. For each probe set of a gene, the average expression over all samples with a present call (from the MAS5.0 normalization) is calculated (average present signal APS). The probe set with the highest signal is chosen to represent this gene in the analyzed dataset. For every dataset this procedure is repeated, thereby allowing tissue specific selection for probesets to represent a gene. When no call information is available, the average expression of a probeset is used.\
  **Differential Expression**: R2 determines p-values for the differential expression of genes by performing either a one-way anova (default setting) or alternatively a brute-force t-test on any combination of groups when the data is untransformed or log2 transformed. For rank-transformed data, a Kruskal Wallis test is performed. Besides these statistical tests, users can also ask for genes with a certain fold change or obtain a top-X list of the genes which are ordered by a user-specified test.\
  **Multiple Testing:** We are testing a lot of genes here; so we have to correct for Multiple testing. For example, one might declare that a coin was biased if in 10 flips it landed heads at least 9 times. Indeed, if one assumes as a;null hypothesis ;that the coin is fair, then the probability that a fair coin would come up heads at least 9 out of 10 times is (10 + 1) " (1/2)10 = 0.0107This is relatively unlikely, and under"statistical criteria;such as ;p-value;&lt; 0.05, one would declare that the null hypothesis should be rejected " i.e., the coin is unfair. A multiple-comparisons problem arises if one wanted to use this test (which is appropriate for testing the fairness of a single coin), to test the fairness of many coins. Imagine if one was to test 100 fair coins by this method. Given that the probability of a fair coin coming up 9 or 10 heads in 10 flips is 0.0107, one would expect that in flipping 100 fair coins ten times each, to see ;*a particular*;(i.e., pre-selected) coin come up heads 9 or 10 times would still be very unlikely, but seeing any coin behave that way, without concern for which one, would be more likely than not. Precisely, the likelihood that all 100 fair coins are identified as fair by this criterion is (1 - 0.0107)100 \~ 0.34.. Therefore the application of our single-test coin-fairness criterion to multiple comparisons would be more likely to falsely identify at least one fair coin as unfair. This occurs in a similar way if we are testing multiple genes in one experiment; we have to correct for this. There are several ways to do so; a conservative approach is the Bonferroni correction. The correction is based on the idea that if an experimenter is testing n dependent or independent hypotheses on a set of data, then one way of maintaining the familywise error rate is to test each individual hypothesis at a statistical significance level of 1/n times what it would be if only one hypothesis were tested. So, if it is desired that the significance level for the whole family of tests should be (at most) a, then the Bonferroni correction would be to test each of the individual tests at a significance level of a/n. The more sophisticated False Discovery Rate controls the expected proportion of false positives. A FDR threshold is determined from the observed p-value distribution, and hence is adaptive to the amount of signal in your data.\
  **Gene Filters:** The gene filters allow you to study a specific subset of genes only. There are several domains you can choose from. A specific chromosome can be chosen, note when a chromosome is chosen a specific position range can be defined also. Under GeneCategory some predefined categories can be selected, some examples are known transcription factors or drugtargets Here you'll find the categories you've defined yourself also. \#\# Kegg pathway selects a set of genes present in the KEGG pathway database ( [](http://www.genome.jp/kegg/pathway.html)<http://www.genome.jp/kegg/pathway.html>). Gene ontology select a group of genes belonging to a specific Gene Ontology category (www.geneontology.org). Note that if you click a category, further choices deeper down the ontology tree are enabled \#\# Genesets are publicly defined sets or sets you've constructed yourself yourself (see also: tutorial adapting R2 to your needs). A convenient search functionality is available to find what you're looking for. Combinations are also possible; this enables you for example to find the developmental genes on chromosome 1.\
  \
  Of course: to really get familiar with these settings you have to toy around with them!
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 8
---------------

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that what those R and p-values were again?***
  R is the correlation coefficient; it ranges from -1 to +1, if R &gt; 0 the value of two variables tends to increase or decrease together. If R &lt; 0 the value of X increases if that of Y decreases, if R\~0 there is no relation. Perhaps the best way to interpret the value of R is to square it. This is the fraction of the variance in the two variables that is shared. For example, if R^2^=0.59 then 59% of the variance in Y can be explained by (or goes along with) variation in X. The p-value for this calculation estimates the probability that this is an observation by pure chance; a p-value of 0.01 you can be 99% sure that this is not the case.
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1.  The result is a list of genes that is ordered for having the most
    significant differential expression between the groups you chose
    (Figure 13). A short summary of the calculation is given above the
    table; \~ 2600 genes have met the criteria set by default; their
    expression exhibits a correlation with the separation in two groups.
    [![](_static/images/DiffentialExpress_Genelist.png)**Figure
    13: Genes differentially expressed
    between groups.**](_static/images/DiffentialExpress%20Genelist.png)
2.  Click on the hyperlinked top gene in the list
3.  A similar graph as produced for MYCN appears, the differential
    expression is more pronounced for this gene (Figure 14). In the
    generated picture the genes are not ordered for their gene
    expression go to the adjustable settings menu and select "Track and
    gene sort" in the "Extra Graph Option" pulldown menu. Click
    "adjust settings".
4.  The functionality in the right panel of Figure 15 will be explored
    in more advanced tutorials (K-Means clustering). We'll explore one
    add**i**tional data visualization however; that of all genes I this
    dataset; in the right menu click 'Plot all genes (xy,
    volcano, etc)'.

[![](_static/images/DiffentialExpress_TopGene.png)**Figure
14: In the main screen "Change
dataset".**](_static/images/DiffentialExpress_TopGene.png)[![](_static/images/DiffentialExpress_RightMenu.png)**Figure
15: Right menu in genelist windos; choosing plot all
genes**](_static/images/DiffentialExpress_RightMenu.png)





Tutorial step 9
---------------

1.  The resulting plot shows all genes in the list in a XY-plot;
    datapoints above and below the diagonal are
    differentially expressed. Hovering over the points shows the
    genesymbol, in this case the NTRK1 gene (Figure 16). To speed up the
    graph generation this information is not automatically loaded: click
    on the "add hovering" button below the graph to add
    this information. Note: every plot in R2 with larger amounts of
    datapoints (&gt;5000) will have this "add hovering" button.
    [![](_static/images/DiffentialExpress_XYplot.png)**Figure
    16: XY plot of all genes differentially expressed in the current
    track;**](_static/images/DiffentialExpress%20XYplot.png)
2.  Clicking on the symbol opens up a new window showing the expression
    of the gene in the two groups as a box plot.
    [![](_static/images/DiffentialExpress_BoxdotplotCircle.png)**Figure
    17: Differential expression of
    NTRK1**](_static/images/DiffentialExpress_BoxdotplotCircle.png)
3.  R2 allows further annotation of the XY plot of all genes; in the XY
    plot window (still open in your browser) scroll down and adapt the
    settings; add a genesymbol to mark, eg AKR1C1; choose a KEGG pathway
    to emphasize, eg DNA replication and set the 'Draw fold lines'
    option to 'yes'.
    [![](_static/images/DiffentialExpress_AdjustAllgenes.png)**Figure
    18: Adjustable settings for the all genes
    plot**](_static/images/DiffentialExpress_AdjustAllgenes.png)
4.  Click redraw image. The plot has been adapted to show the AKR1C1
    genesymbol, DNA-replication genes are highlighted in red. Fold
    change lines show the regions where differential expression is 1 and
    2 fold (Figure 19). Note that most genes of the DNA replication
    pathway seem to be located below the diagonal.
    [![](_static/images/DiffentialExpress_AdjustVisual.png)**Figure
    19: Adjusted visualization of gene expression,hovering over the dots
    shows the
    gene name.**](_static/images/DiffentialExpress_AdjustVisual.png)
5.  R2 can visualize the same data also as a Volcano plot or a MA plot.
    In the Adjustable Settings dialog change the Plot type to Volcano
    (Figure 20) or MA (Figure 21). Note that the distinct
    characteristics of the AKR1C1 gene and the DNA replication are more
    obvious in the Volcano plot. The DNA replication pathway statistics
    will be explored in more detail in the 'Find genes correlating with
    your gene of interest'-tutorial

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can tailor visualization of specific genes in one go?***
  You can annotate genenames by providing them in this box. By default, these will appear in red, size=10, on your plot. You can change the size and/or color of these genes either individually, or in groups. Please take note of the following rules: \# \#\* mark groups of genes for which the same criteria apply. First type the genes (comma separated), followed by :s=size, followed by :c=r,g,b \#\* for single genes: gene1:s=25:c=0,0,255;gene2:s=20:c=200,0,0 \#\* for groups of genes: (gene1,gene2,gene3):s=25:c=0,0,255;(gene4,gene5,gene6):s=20:c=200,0,0"
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

[![](_static/images/DiffentialExpress_Volcano.png)**Figure
20:Volcano
plot**](_static/images/DiffentialExpress_Volcano.png)[![](_static/images/DiffentialExpress_MAplot.png)**Figure
21: MA
plot**](_static/images/DiffentialExpress_MAplot.png)





Final remarks / future directions
---------------------------------



This tutorial has shown you how to find genes that are differentially
expressed in your dataset of choice. Now go ahead and toy around with
selecting groups and tracks of choice and see what interesting
scientific discoveries might lie ahead!





We hope that this tutorial has been helpful,The R2 support team.









Find genes correlating with your gene of interest
=================================================



*Or how you can find genes that have similar or opposite expression
patterns in your dataset of choice*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   R2 allows you to explore the relations your gene exhibits with other
    genes in your dataset of choice; correlation statistics is used to
    calculate this.
-   The expression of a set of genes correlating with the expression of
    MYCN in a series of Neuroblastoma tumors is used to demonstrate that
    in this tutorial
-   The results can be further explored in one-on-one graphs or as a
    heatmap
-   The set of genes can be further explored statistically in several
    domains as will be shown in this tutorial:
    -   In a gene ontology analysis
    -   On pathway maps
    -   On a chromosome map
-   Using this exploratory analysis, new biologically relevant
    hypotheses can be generated as will be shown in this tutorial by an
    example concerning MYCN and MCM genes.
-   The data can be saved and used in other tools
-   Further advanced analysis based on the use of sets of genes can be
    found in the Kaplan scanner and GeneSets tutorials.





Tutorial step 1
---------------

1.  Logon to the R2 homepage using your credentials and make sure the
    "Single Dataset" field is selected in field 1 of the R2 step-by-step
    guide
2.  Make sure the "Tumor Neuroblastoma public dataset" is selected in
    field 2 (For additional information on these first two steps,
    consult tutorial : Working with datasets
3.  In field 3 select 'Find Correlated genes with a single gene'
    (Figure 1).
4.  In field 4 type 'MYCN' as gene name
5.  Click 'Next'

[![](_static/images/FindGenes_Choiceof.png)**Figure
1: Choice of correlation
analysis.**](_static/images/FindGenes%20Choiceof.png)





Tutorial step 2
---------------

1.  Further information on the statistics choices and the meaning of the
    HugoOnce mode you can find in the 'Differential
    Expression' tutorial.
2.  Further information on the statistics choices and the meaning of the
    HugoOnce mode you can find in the 'Differential
    Expression' tutorial.
    [![](_static/images/FindGenes_OptionPage.png)**Figure
    2: Options page for correlation
    calculation**](_static/images/FindGenes%20OptionPage.png)
3.  Scroll down the screen and click 'Next'

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can find the correlation between two genes directly?***
  Just choose 'Correlate 2 genes' in field 3 if you have a specific gene you want to correlate with your gene of interest. Of course this method would be rather tedious if you want to find new genes, hence we're exploring exactly this scenario in this tutorial. Another possibility is to correlate your gene with a track (containing numerical data). This essentially tests whether the expression of your gene of interest correlates with the numerical order described in the track. This scenario is further explored in the 'Differential Expression' tutorial.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 3
---------------





1.  R2 calculates the correlation of the expression of MYCN with the
    expression of every other single gene in the current dataset. A lot
    of calculations! The result is presented as two tables (Figure 3 )
    In the header a summary is given: \~ 2200 combinations of MYCN and
    another gene met the criteria, i.e. having a significant correlation
    (p &lt; 0.01) with the expression of MYCN, \~ 15000 genes did not
    obey these criteria. The left table represents the genes whose
    expression correlates positively, or is similar, with that of MYCN
    in this dataset. Of course MYCN has a perfect correlation
    with itself. Some characteristics of the genes are already described
    in red. R and p-values are given in separate columns (for a short
    description of their meaning, consult the 'Differential
    Expression' tutorial).
    [![](_static/images/FindGenes_GeneList.png)**Figure
    3: Genes whose expression is correlating with that of the MYCN gene
    in 88 Neuroblastoma
    tumors**](_static/images/FindGenes%20GeneList.png)



Exact (gene-) numbers listed in the tutorial Figures such as in this
example "2208 combinations"" can vary. This could be caused by database
updates upon a new genebuild release or an affymetrix annotation update.



1.  The right table summarizes the genes that show a negative
    correlation; the expression of MYCN behaves oppositely to that of
    these genes.
2.  A little table to the right summarizes the results of a limited
    Ontology analysis. More about that in subsequent steps where we also
    explore the menu items to the right. All gene names are clickable to
    explore the specifics of the correlation in a separate graph; try
    and click the APEX1 gene in the left column.
3.  In the left upper corner the filter icon is located , this links
    directly to the "adjustable settings panel " where you adapt the
    filtering conditions . The filter button is accessible in many
    analysis modules of R2.





[![](_static/images/FindGenes_GotoMain.png)**Figure
4: Filter
button**](_static/images/FindGenes%20GotoMain.png)





Tutorial step 4
---------------





1.  The resulting graph depicts the expression of both genes in this
    tumor series in a graph. The tumor samples are ordered by increasing
    MYCN expression. Note that the expression of APEX1 follows the
    expression of MYCN quite good! This is reflected in the R and
    p-values that are quite significant.
    [![](_static/images/FindGenes_ExpressionPos.png)**Figure
    5: The expression of the MYCN gene correlates with the expression of
    the
    APEX1 gene.**](_static/images/FindGenes_ExpressionPos.png)
2.  For an opposite example, click on one of the the top genes in the
    right column; MEAF6. This produces Figure 6. The original list of
    results is still open in another tab in your browser, return there.
    [![](_static/images/FindGenes_ExpressionNeg.png)**Figure
    6: The expression of MYCN has a negative correlation with that of
    the MEAf6
    gene**](_static/images/FindGenes_ExpressionNeg.png)



To generate a correlation plot where the negative relation between MYCN
and MEAF6 gene is more clearly visualized select "XY-plot" as graph type
in the graphics section in the Adjustable Settings box and click the
Adjust Settings button. In this correlation plot it"s also still
possible to show expression levels for the samples are distributed. In
order to do so click on more settings in the Adjustable Settings box and
set Histogram to yes, click Adjust Settings button. Now the histogram
boxes in the x and y axes show expression levels are distributed for the
samples in the selected dataset see Figure 7



1.  [![](_static/images/FindGenes_ExpressionHis.png)**Figure
    7: Toggle Histogram
    on/off**](_static/images/FindGenes%20ExpressionHis.png)
2.  Through the menu to the right several additional dataviews and
    analyses are available. Let's start with different overviews; R2 is
    able to produce heatmaps of this analysis. Click on the 'Heatmap
    (zscore)' menu item Figure 8. The gene names are on the y-axis,
    sample names on the x-axis. Return to the genelist view (Figure 3)





[![](_static/images/FindGenes_ExpressionHeat.png)**Figure
8: Heatmap view of the expression of all genes correlating with the
expression of MYCN in 88 Neuroblastoma
samples.**](_static/images/FindGenes%20ExpressionHeat.png)





Tutorial step 5
---------------



Another view is the mapping of these genes on all chromosomes. Click on
the 'Chromosome Map' menu item. In Figure 9 this mapping is depicted in
an overview. Sometimes, eyeballing already suggests that some regions
seem to be affected. R2 provides a table where the statistics behind
this analysis are given: Figure 10. The overrepresentation of genes that
correlate with MYCN expression with respect to all genes present on (an
arm of) a chromosome is calculated.



  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that over-representation is explained here?***
  Over-representation quantifies the notion that a subset of genes from a larger set can harbor more genes that have a certain characteristic than you would expect by chance. On the p-arm of chromosome 1 for example, there are 1157 genes located of the grand total of 21300 known genes. From our set of 2229 genes (only slightly more than 10% of the total number) some 210 are present on this arm. This is 18.2% ,an enrichment above what you would expect by chance. This can be quantified using a 2X2 contingency table with a chi-squared test that produces a p-value to establish whether this difference is significant
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

[![](_static/images/FindGenes_Chromosome.png)**Figure
9: Mapping of the genes correlating with MYCN on all
chromosomes**](_static/images/FindGenes_Chromosome.png)[![](_static/images/FindGenes_ChromeTable.png)**Figure
10: Statistics of overrepresentation of genes that have a correlation
with MYCN on different
chromosomes**](_static/images/FindGenes_ChromeTable.png)
1.  To further explore this set of genes return to the list: Figure 3





Tutorial step 6
---------------

1.  Further overrepresentation analyses in other domains can give a
    first clue for processes that are of importance in this set
    of genes. A domain is the [Gene
    Ontology](http://geneontology.org/); a
    controlled vocabulary that systematically describes processes,
    locations and functions in biology. Click 'Gene Ontology analysis'
2.  The resulting categories are presented in a sortable table (Figure
    11), sort on p-value by clicking on the column header.
    [![](_static/images/FindGenes_GeneOnto.png)**Figure
    11: Gene Ontology categories that are overrepresented in the set of
    genes that correlates with MYCN expression in the current dataset,
    sorted by increasing p-value
    of overrepresentation.**](_static/images/FindGenes%20GeneOnto.png)
3.  One of the categories where genes of our current set are
    overrepresented is 'DNA-strand elongation'; and what is also obvious
    that all genes in this process have a consistent positive
    correlation (as can be seen by the green color). Let's take a look
    if we can corroborate this observation in another domain.
4.  The adjustable panel settings menu allows you to redo the
    gene-ontology analysis with the up or down regulated genes only.

[![](_static/images/FindGenes_Adjust.png)**'Figure
12: Re-do analysis with genes that are either positively or negatively
correlated with
MYCN.**](_static/images/FindGenes_Adjust.png)





Tutorial step 7
---------------

1.  Return to the gene list Figure 3 and click 'Map on pathway image'
2.  In the next screen a choice can be made for other datasets; we use
    the KEGG database. Click next.
    [![](_static/images/First_image_select_dataset.png)**Figure
    13: Choice panel for other
    datasets**](_static/images/First_image_select_dataset.png)
3.  A similar overrepresentation analysis is performed on all gene
    members of the pathways in the KEGG database. Click on the p-value
    column header again to find the most significant ones: Figure 14
    [![](_static/images/FindGenes_KeggPath.png)**Figure
    14: KEGG pathways exhibiting an overrepresentation of genes of the
    current dataset, ordered
    by significance.**](_static/images/FindGenes_KeggPath.png)
4.  The DNA-replication pathway pops up as most significant. Note that
    most genes are similar to the GO process found in the
    former analysis. The pathway will be shown when the blue A in front
    of the pathway name is clicked.
5.  A hyperlinked KEGG pathway appears: Figure 15

[![](_static/images/FindGenes_Pathway.png)**Figure
15: Mapping of the overrepresented genes (darker green) in the MYCN
correlating set on the DNA-replication pathway\
from the KEGG database. Hovering over the gene shows additional
information.**](_static/images/FindGenes%20Pathway.png)


MCM-genes seem to play a role. Go back to list (Figure 3) to show their
individual relation with MYCN.







Tutorial step 8
---------------

1.  Scroll down and look for the MCM2 gene, click on the link to show
    their relationship: Figure 16
    [![](_static/images/FindGenes_MYCNMCM2.png)**Figure
    16: MCM2 expression correlates with
    MYCN expression.**](_static/images/FindGenes%20MYCNMCM2.png)
2.  The correlation is significant. In the left upper table there is a
    link to the Pubsniffer tool within R2. This tool performs a live
    search in the Pubmed literature database for (co-)occurrences of
    MYCN and MCM2 (and some other keywords). Click the link: Figure 17
    [![](_static/images/FindGenes_Pubsniffer.png)**Figure
    17: Pubsniffer results for gene symbols MYCN and
    MCM2**](_static/images/FindGenes%20Pubsniffer.png)
3.  Apparently there are some abstracts where the two genes are
    mentioned together, you can view this article directly by clicking
    the hyperlinked number in the Articles column. The outlink
    Pubreminer column directs to the PubReminer tool: Figure 18
    [![](_static/images/FindGenes_Reminer.png)**Figure
    18: The PubReminer tool web interface; the genes MCM2 and MYCN
    co-occur in one article. This versatile webtool allows you to build
    very specific
    literature queries.**](_static/images/FindGenes_Reminer.png)
4.  This versatile tool offers quite some functionality to build a
    literature search query tailored to your needs. That being slightly
    out of scope of this tutorial, click the "Goto Pubmed with query"
    button to find the article.
5.  This article is actually published work by our group where the
    relation between the MCM genes and MYCN was proven experimentally.

[![](_static/images/FindGenes_PubReminerresult.png)**Figure
19: The correlation between MCM genes and MYCN was proven experimentally
in this
article.**](_static/images/FindGenes_PubReminerresult.png)





Tutorial step 9
---------------

1.  The genelist produced in the beginning of this tutorial (Figure 3)
    can be stored for use in later analyses in R2, or for use in
    other applications. Return to the page containing the list, this is
    still open in another tab in your browser.
2.  The menu to the right gives several possibilities (Figure 53). Some
    of these have been explored already; we'll touch shortly on the rest
    of them.

-   "Gene set analysis": use public genesets; this is further explored
    in the advanced Correlate with DataSet tutorial.
-   "Map on pathway image", "Chromosome map", "Gene Ontology analysis",
    "Heatmap" have been explored in this tutorial.
-   "MakeMeATable" produces a txt file that is formatted for direct
    input into the data analysis tool TM4
    (<http://www.tm4.org/mev.html)>
-   "Save current selection as TXT file" produces a tab separated file
    containing the current analysis. In the header of such file all
    information is stored to be able to redo the analyses in the future.
-   Reference for current selection produces a list of probesets and
    genenames that are considered to be expressed in the
    current dataset. This is a suitable background set for eg. the DAVID
    tool
    ([](http://david.abcc.ncifcrf.gov/)<http://david.abcc.ncifcrf.gov/>)
-   Last but not least the data can be stored as a personal
    genecategory; this is further explored in the advanced tutorial
    "Adapting R2 to your own needs".

[![](_static/images/FindGenes_DatasetOptions.png)**Figure
20: Menu choices for
Dataset**](_static/images/FindGenes%20DatasetOptions.png)





Final remarks / future directions
---------------------------------



Based on this tutorial you can further explore R2 in the set of advanced
tutorials.





We hope that this tutorial has been helpful,The R2 support team.









Working with Kaplan Meier
=========================



*Investigate the prognostic value of a gene or a group of genes*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Use R2 to generate a Kaplan graph by "annotated parameter". Use
    tracks or combine two tracks to assign the group separation of a
    specific dataset.

<!-- -->

-   R2 supports any type of survival data, such as overall survival and
    relapse free survival.

<!-- -->

-   An often used feature of R2 is the Kaplan Scan, where an optimum
    survival cut-off is established based on statistical testing instead
    of for example just taking the average of median. The Kaplan scanner
    separates the samples of a dataset into two groups based on the gene
    expression of one gene. In the order of expression, it will use
    every increasing expression value as a cutoff to create 2 groups and
    test the p-value in a logrank test. The highest value is then
    reported, accompanied by a kaplan meier picture. So in short, it
    will find the most significant expression cutoff for
    survival analysis. The best possible Kaplan Meier curve is based on
    the logrank test. However, R2 does also allow you to use median,
    average and more as a cutoff in assessing whether a gene of interest
    has the potential to separate patient survival.Of course, such
    analysis id only possible for datasets where survival data
    is present.

<!-- -->

-   Use the Kaplan Scan for a group of genes.





Tutorial step 1
---------------





1.  Logon the R2 homepage and select Kaplan Meier " By
    Annotated parameter. You can find this option either in the left
    menu panel on the main screen or in field 3 at the type of analysis
    pull down menu. Using the Kaplan Meier module via the left menu
    directly shows from which datasets survival data is available.
    [![](_static/images/WorkingWithKaplan_menu.png)**Figure
    1: Select a Kaplan
    Meier option.**](_static/images/WorkingWithKaplan_menu.png)
2.  In the adjustable settings menu choose "overall survival" , select
    "track" at Separate by and select "inss-cat" stage in use track pull
    down menu . Click "next" .
    [![](_static/images/WorkingWithKaplan_Kaplan.png)**Figure
    2: Kaplan Meier by
    "Annotated parameter.**](_static/images/WorkingWithKaplan%20Kaplan.png)



Note that stage st4s en st1 survival curves are overlapping which is in
agreement with the clinical outcome of the INSS stages.



1.  A handy feature of the R2 kaplan module is the option to combine two
    tracks to generate subgroups for the Kaplan meier analyses. Use the
    back-button from the browser and select at " separate by " , "
    combination of two tracks". Choose for example for the first track "
    agegroup (cat) " and for the second track "mycn\_amp (cat) ". And
    click next.
    [![](_static/images/WorkingWithKaplan_Combined.png)**Figure
    3: Kaplan Meier graph with
    combined tracks.**](_static/images/WorkingWithKaplan%20Combined.png)



The combined track agegroup ( &gt;=1 year) and no mycn application
results in intermediate survival probability. Note that there are 3
groups instead of "expected" 4 since there are no patients &lt; 1 year
and a mycn amplification, in this cohort.



+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that you can apply a filter to analyze a subgroup. In addition  |
| you can also adapt the graphical representation***                       |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=250){width="250"}](_static/images/W |
| orkingWithKaplan_Adjust.png)                            |
|                                               |
|                                                                          |
| \                                                                        |
| When you are defining a subsection of the samples, you can execute       |
| multiple selections after each other. To use the selection (subset), you |
| need to click on **confirm** to finalize it. A successful subset         |
| selection will be shown as a small message indicating the used           |
| trackname, groups and the final number of samples between brackets.\     |
| Nb. If you use the 'back' button in your webbroswer, then this selection |
| will be lost and needs to be defined again.                              |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+





Tutorial step 2
---------------





1.  Select from the main screen either the left menu or in field 3,
    Kaplan Meier " By gene expression. Make sure that "Tumor
    Neuroblastoma public " Versteeg " 88" is selected, for analyses
    choose "Kaplan Scan a single gene" fill in MYCN and use as cut-off
    method " scan " and click "next".
2.  In the next screen use the prefilled settings and click "next".
3.  The Kaplan scan generates a Kaplan Meier Plot based on the most
    optimal mRNA cut-off expression level to discriminate between a good
    and bad prognosis cohort.
4.  The determined separation in groups can be stored in a track and
    used in other analyes, click the "store as track" button
    [![](_static/images/WorkingWithKaplan_GroupPvalue.png)**Figure
    5: Kaplan plot with multiple cutoffs: A) Scan B) Quartile C)
    Median D)
    Average**](_static/images/WorkingWithKaplan_GroupPvalue.png)
5.  To illustrate that with the Kaplan scan more significant biological
    subgroups can be found, adjust the cut-off mode to "median" in the
    settings menu and click "redraw"graph.
    [![](_static/images/WorkingWithKaplan_Multiple.png)**Figure
    6:Kaplan plot with multiple cutoffs: A) Scan B) Quartile C)
    Median D)
    Average**](_static/images/WorkingWithKaplan_Multiple.png)



It"s obvious that with the Kaplan Meier scan the group separation is
much more significant compared to the median cut-off modus. Try to find
out whether this is also the case with other cut-off modi.



1.  Next to the Kaplan plot Figure 4, a small sub-plot is
    generated (underlined) which represents a graphical representation
    of the p-value plotted against the mRNA expression level values. In
    some cases it could be useful to change the p-value cut-off level
    and for this reason this graphical p-value plot (which is clickable)
    could be of help. Alternatively, you could use the "cutoff" field to
    regenerate a Kaplan curve with that separation.





[![](_static/images/WorkingWithKaplan_ChangePvalue.png)**Figure
7: Adjustable settings menu: change p-vale
cutoff.**](_static/images/WorkingWithKaplan_ChangePvalue.png)





Tutorial step 3
---------------

1.  Instead of using the Kaplan Scan for a single gene you can also
    analyse a group of genes at the same time. Go to Kaplan Meier " by
    gene expression, select at analysis "Kaplan Scan a group of
    genes"and click "next"
2.  In this example select the apoptosis route at the Kegg path way
    pulldown menu. Leave the "type of survival" at overall survival. In
    the statistics panel there are several filtering options possible
    leave these options unchanged
3.  In the graphics section select "yes" at "Draw heatmap and
    click next.
4.  In the next screen R2 had generated a list of the genes within the
    apoptosis pathway which have significant prognostic value. A heatmap
    for this list of genes is generated as well.

[![](_static/images/WorkingWithKaplan_Kaplanlist.png)**Figure
7: A list of Kaplan Meier for a group of
genes**](_static/images/WorkingWithKaplan%20Kaplanlist.png)


In Figure 7, clicking on each gene name in the hugo column will result
in a new screen or tab with the corresponding Kaplan plot.
WorkingWithKaplan Heatmap.png



[![](_static/images/WorkingWithKaplan_Heatmap.png)**Figure
8: Heatmap of the significant prognostic list of
genes.**](_static/images/WorkingWithKaplan_Heatmap.png)


The heatmap shows in this case that 2 or 3 possible biological relevant
clusters based on this set of genes. Clicking a spot in the heatmap will
show directly the gene expression level for all samples via a new
one-gene-view screen.







Tutorial step 4
---------------

1.  It may happen that you would like to use the KaplanScan method on a
    dataset that is not available in R2. Especially for this reason we
    have made a user defined version within R2, where you can paste your
    cohort into R2 and run the procedure. To initiate such a user
    defined kaplanscan, select the "Kaplan Meier" &gt; "Kaplan Meier by
    user provide data" option from the left hand menu.
    [![](_static/images/Kaplanscan_userdefined_1a.png)**Figure
    9: Kaplanscan with user defined
    data**](_static/images/kaplanscan_userdefined_1a.png)
2.  For the remaining to work as intended, we need to take into account
    a couple of things. You should prepare your data in the following
    four tab- or semicolon(;) separated columns.
    -   Column1 contains a sample identifiers (without spaces)
    -   Column2 contains the survival time in days (R2 will convert
        these )
    -   Column3 contains the censoring information (Event) and can be
        yes/no or 1/0
    -   Column4 contains the expression value of the gene of interest
        for the kaplanscan

3.  One can easily prepare this information in Excel and paste the
    selected columns into the large white paste box. Do take care that
    we use "." for decimal signs. After you pasted the dataset
    information, you make the selection for the cutoff option and
    subsequently press next. R2 will now calculate the kaplan method
    that you selected and display the result in an interactive image.
    [![](_static/images/Kaplanscan_userdefined_2a.png)**Figure
    10: Kaplanscan with user defined data
    result**](_static/images/kaplanscan_userdefined_2a.png)
4.  Once the image has been created, you are able to adapt various
    parameters to optimize appearance of your result.

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that The survival data used in your scan produces a unique signature***
  R2 will indicate within the image a checksum (MD5 sum) of all the survival information, which can be used to identify whether the same cohort information has been used in different scans that you may perform (this code should remain idenitical).
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







Pathway Finder
==============



*Which known pathways play a role in your data?*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   In molecular biology the concept of pathways is important; small
    molecules, proteins, genes, etc. interact, resulting in specific
    phenotypic outcomes at all levels in biology.
-   Quite a lot of this knowledge is stored as pathways in databases. An
    extensive resource can be found here
    [](http://www.pathguide.org/)<http://www.pathguide.org/> .
    To name a few:
    -   KEGG Pathway database
        ([](http://www.genome.jp/kegg/pathway.html)<http://www.genome.jp/kegg/pathway.html>)
    -   WikiPathways
        ([](http://wikipathways.org/)<http://wikipathways.org>)
    -   PantherDB
        ([](http://www.pantherdb.org)<http://www.pantherdb.org>)
-   R2 allows you to see whether biological pathways might play a role
    in your dataset of choice.
-   In this tutorial we'll use array data of a set of 62
    Medulloblastoma tumors. In some Medulloblastoma tumors the gene
    beta-catenin is mutated. This specific dataset has clinical
    annotation for beta catenin mutations. We're going to investigate
    this in a pathway context.





Tutorial step 1
---------------

1.  Make sure that the Single Dataset option is selected in field 1 of
    the step by step guide.
2.  In field 2 locate and select the 'Tumor Medulloblastoma PLoS One-
    Kool - 62 MAS5.0 -u133p2' dataset by clicking 'Change Dataset'
3.  In field 3 select 'KEGG PathwayFinder by Gene correlation'
4.  You might not know the exact gene symbol for beta catenin. R2 can
    find the gene symbol by alternative name also, we'll try 'catenin';
    Figure 1.
5.  Click 'Next'

[![](_static/images/Pathway_menu.png)**Figure
1: Selecting KEGG pathwayfinder by gene correlation for
catenin**](_static/images/Pathway_menu.png)





Tutorial step 2
---------------

1.  R2 has found several suggestions with the word catenin, hovering
    over the gene symbols gives additional information. Based on that
    information choose CTNNB1, take the probeset with the highest
    average expression, this is most likely the probeset that best
    represents mRNA concentration.
    [![](_static/images/Pathway_list.png)**Figure
    2: Options for alternative name catenin: choose
    CTNNB1**](_static/images/Pathway_list.png)
2.  Scroll down, leave the other options as they are, and
    click 'Submit'.





Tutorial step 3
---------------

1.  R2 calculates for all genes in the KEGG pathways whether their
    expression correlates with that of CTNNB1. Next it calculates for
    all pathways whether they contain a significant number of
    correlating genes; if the genes correlating with CTNNB1 are
    overrepresented in that pathway (For an in depth discussion see R2
    Tutorial; Find genes correlating with your gene of interest. The
    result is returned as a list of pathways; Figure 3.
    [![](_static/images/Pathway_Kegg.png)**Figure
    3: KEGG pathways that have an overrepresentation of genes that
    correlate with CTNNB1 in this
    dataset**](_static/images/Pathway_Kegg.png)
2.  An overall explanation is printed above the list; of all genes
    present in all KEGG pathways, \~ 540 correlate with CTNNB1 with a p
    value &lt; 0.05. In the table the KEGG pathways are listed ranked by
    their p-value for overrepresentation (background in red) or
    under-representation (in green) of these genes. The brightly colored
    letters in front of the pathway-name are hyperlinked. **R** links to
    a list of the genes, **K** leads to the original KEGG pathway on the
    Japanese servers, **A** links to an image of the KEGG pathway that
    is provided with hover-over information for all genes in
    the pathway. We'll discuss the first two later, now click on the A
    in front of the 'SNARE interactions in vesicular transport'-pathway.
    [![](_static/images/Pathway_SNARE.png)**Figure
    4: The SNARE pathway; darker green and red are genes correlating
    with CTNNB1**](_static/images/Pathway_SNARE.png)
3.  R2 opens a new window in your browser (Figure 4). In darker green
    the genes that have a positive correlation with CTNNB1 and in red
    those having a negative correlation. Hovering over the genes with
    the mouse pointer presents additional information; some of the
    gene-boxes represent multiple genes: Figure 5 Although not in this
    example, it may happen that multiple genes within a box show both
    positive, as well a s negative correlations. In such case the box is
    proportionally filled with red and green.
4.  The result however, is not quite convincing, apparently CTNNB1
    expression does not correlate with pathways. We're going to try it
    the other way around; which pathways correlate with a catenin
    mutation
5.  Return to list view (still open in another tab of your browser) and
    go to the R2 main page by clicking the link in the upper left corner
    of the screen.

[![](_static/images/Pathway_Zoom.png)**Figure
5: : Hovering over the Stx1-4 box shows that this actually represents 5
genes; only one of them is correlating with
CTNBB1.**](_static/images/Pathway_Zoom.png)





Tutorial step 4
---------------

1.  In field 3 on the R2 start page select 'KEGG PathwayFinder by
    Groups';
    [![](_static/images/Pathway_Finder.png)**Figure
    6: Selecting PathwayFinder by
    Groups**](_static/images/Pathway_Finder.png)
2.  Click "Next"





Tutorial step 5
---------------

1.  This set of tumors is annotated with several clinical and molecular
    biology parameters in so called tracks. One of them is the presence
    of a beta catenin mutation; bcat mutation. Select this; Figure 7.
    Pathway\_Select
    [![](_static/images/Pathway_Select.png)**'Figure
    7: Selecting the bcat
    mutation track.**](_static/images/Pathway_Select.png)
2.  Click "Submit"





Tutorial step 6
---------------

1.  R2 calculates for all genes in the KEGG pathways whether they are
    differentially expressed between the groups of tumors having a
    mutation and those that do not have one. In a subsequent calculation
    the overrepresentation of these genes in the individual pathways
    is determined. From the resulting list it is obvious that the Wnt
    pathway has a strong overrepresentation of genes that are
    differentially expressed between the two groups. \[\[Image:\]\]
2.  Click on the R link to let R2 create a list of these genes.

[![](_static/images/Pathway_Wnt.png)**Figure
8:The Wnt pathway has a strong overrepresentation of genes that are
differentially expressed between the groups of tumors that have and
don't have a beta catenin
mutation.**](_static/images/Pathway_Wnt.png)





Tutorial step 7
---------------

1.  A list of hyperlinked genes is returned, sort them by descending
    R-value by clicking on the R-column-header twice;
    [![](_static/images/Pathway_correlate.png)**Figure
    9: Wnt pathway genes correlating with Beta Catenin mutation as
    a list.**](_static/images/Pathway_correlate.png)
2.  Each gene-symbol is hyperlinked to a graph representing the specific
    results; click the top gene in the list: AXIN2.





Tutorial step 8
---------------

1.  The graph shows an excellent correlation of the expression of the
    Wnt pathway gene AXIN2 with tumors having a Beta Catenin mutation.
    The same goes for a significantly overrepresented set of genes in
    this pathway. This specific group of tumors is also known as the
    Wnt-subtype in the Medulloblastoma field.

[![](_static/images/Pathway_Axin.png)**Figure
10:AXIN2 expression correlates with Beta Catenin
mutations**](_static/images/Pathway_Axin.png)





Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







Multiple datasets overview with Megasampler
===========================================



*Create an overview of the expression level of a single gene in multiple
datasets*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   The megasampler is a R2 module to investigate the expression level
    of a gene in any number of the numerous datasets stored in the R2
    database
-   Use R2 to compose your selection of datasets to investigate the
    expression level of a gene
-   Use the megasampler "adjustable settings" to adapt the megasampler
    graphics
-   The megasampler allows you to quickly get an overview of the
    selected gene expression level for all the datasets available in the
    R2 database
-   Go directy from the overview to one-gene view to investigate in
    detail the expression level in a single dataset.





Tutorial step 1
---------------

1.  Use "Across Datasets" in field 1 by default the "megasampler" option
    is selected in field 2 and click "next".
    [![](_static/images/MultipleDatasets_across.png)**Figure
    1: Using across
    datasets**](_static/images/MultipleDatasets_across.png)
2.  Leave "u133p2, mas5.0" at the "type of data" option and select " XPO
    sampler" at "use presets". The meaning of presets will be explained
    later on.

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that R2 harbours different types of microarray platforms***     |
+--------------------------------------------------------------------------+
| [![](_static/images/MultipleDatasets_Select.png |
| )](_static/images/MultipleDatasets_Select.png)             |
|                                               |
|                                                                          |
| Megasampler only allows you to query multiple datasets if they are of    |
| the same chiptype and normalized by the same algorithm and of certain    |
| normalizations.                                                          |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+

1.  With the "selection preset" option a pre-stored dataset collection
    with associated settings can be selected. Select "XPO sampler"
    (Expression Project for Oncology (expO)) to pre-select a series of
    tumor datasets. Click "next".
    [![](_static/images/MultipleDatasets_Preset.png)**Figure
    2: Select a
    preset**](_static/images/MultipleDatasets_Preset.png)
2.  In the previous screen the preset "XPOsampler" is selected, a
    collection of datasets is already marked for the
    megasampler analyses. In Figure 3 clicking the small triangle
    unfolds the available dataset categories, notice that some of the
    datasets in the "tumor" section are already marked. In this way this
    you can adapt your pre-selection of datasets. Unfold the normal and
    tumor category and select the following datasets. Normal Adrenal
    gland - Various " 13, Normal Brain PFC - Harris " 44 and the " Tumor
    Neuroblastoma public - Versteeg " 88" . Enter MYCN and click "next".
    [![](_static/images/Pathway_menu.png)**Figure
    3: Megasampler adjustment
    selection**](_static/images/Pathway_menu.png)

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that private datasets linked to a specific user are indicated   |
| with a green background color***                                         |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=400){width="400"}](_static/images/M |
| ultipleDatasets_Didyou1.png)                            |
|                                               |
|                                                                          |
| Add a private dataset to the (pre) selected datasets.                    |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+





Tutorial step 2
---------------





1.  In the "adjustable settings" panel there are several options to
    customize the megasampler graph. For every selected dataset, you can
    change the order in which they are drawn by adjusting the number in
    the selection boxes. These are processed first, followed by the
    dataset names in alphabetical order (so changing the order of 1 or 2
    datasets should be sufficient). The pull down next to "dataset
    ordering pull down menu" enables to split one or more dataset by
    selecting a track , in this manner the chosen dataset(s) will be
    split according to the numbers of groups of the selected track.
2.  For now change the color for the datasets as indicated in Figure 4
    and click "next".
    [![](_static/images/MultipleDatasets_AdjustGraph.png)**Figure
    4: Adjusting the
    megasampler graph.**](_static/images/MultipleDatasets_AdjustGraph.png)
3.  R2 now performs a one-way Anova statistical test on the fly. This
    **AN**alyis **O**f **VA**riance is a statistical test that
    calculates whether the means of the expression levels between the
    selected datasets are significant different.
4.  [![](_static/images/MultipleDatasets_Anova.png)**Figure
    5: Anova test for the
    selected datasets.**](_static/images/MultipleDatasets_Anova.png)



By default de megasampler graph is plotted in a so called Boxdotplot
representation. The Boxdotplot shows a combined boxplot, on top of which
the signals of the separate samples are plotted; a quickly interpretable
graph.



1.  [![](_static/images/MultipleDatasets_YCC-express.png)**Figure
    6: YCC expression levels in 15 datasets covering
    2173 samples.**](_static/images/MultipleDatasets_YCC-express.png)



Additional insight can be obtained transforming the data, in this case
transform the data to logical values (none) set "graphtype" on barplot
and click on "redraw at the bottom of the screen.



1.  [![](_static/images/MultipleDatasets_Representations.png)**Figure
    7: Different Megasampler graphical
    representations**](_static/images/MultipleDatasets_Representations.png)



The plotted graphs for "MYCN" clearly show a high expression level
specifically in the Neuroblastoma data sets compared to Normal Tissue
and other Tumor datasets. At the bottom of the page it"s possible to
adapt dataset coloring, change the order and split datasets in tracks
directly.



+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that you can save your selection of datasets and select your    |
| stored dataset the next time you login to R2.***                         |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=400){width="400"}](_static/images/M |
| ultipleDatasets_Didyou2.png)                            |
|                                               |
|                                                                          |
| \                                                                        |
|                                                                          |
|                                                                    |
|                                                                          |
| [![](_static/images/UsingDatasets_LinksToRawDat |
| aInR2.png)](_static/images/UsingDatasets_LinksToRawDataInR2.png){.mwx.link. |
| image}                                                                   |
|                                               |
|                                                                          |
| \                                                                        |
| Storing a preset not only stores the selection of datasets for future    |
| use, but will also remember all of the other settings such as order,     |
| colors, plot type etc. In essence you can generate the same visual       |
| representation for any other gene in this way.                           |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+



You can can use the adjustable panel to adapt the megasampler graph. In
case you splitted one or more datasets according to a specific track in
the previous screen, it"s now possible to skip subgroups from your
dataset or more interesting, apply different colors for groups within a
dataset (see Figure 8).



[![](_static/images/MultipleDatasets_AdjustGroups.png)**Figure
8: Adjustable settings panel, color groups within a
dataset.**](_static/images/MultipleDatasets_AdjustGroups.png)





Tutorial step 3:
----------------



The red arrow in the "did you know box" indicates a handy module to
obtain a quick overview of the expression level patterns for most of the
datasets R2 contains (providing that the normalization allows
comparisons between datasets).



1.  Click "view Expression in many datasets" and a new screen (or Tab)
    appears depicting colored dots. The colored dots are representing
    the different dataset categories (cell line dataset, Tumor or Normal
    Tissue etcetera). Via this module (effectively the 2D distribution)
    you can easily detect in what way your probeset of interest is
    expressed in many other datasets. At the Y-axis the 2log transformed
    average expression level and the standard deviation is represented.
    The X-axis "overlap avoider" is simply a means to represent all
    datasets in the plot without overlap of the circles. Figure 9
    clearly shows that the MYCN expression is also high in other dataset
    which could be of interest and a second Neuroblastoma dataset. Next
    to the graphs 2 tables summarize dataset names and a R-value set
    to "1. The R-value comes of use with the 2D-distrubution module
    where you can quickly scan the correlation between two genes for all
    datasets of the same platform in R2. This module is discussed in the
    correlate genes tutorial.
    [![](_static/images/MultipleDatasets_LevelDistribution.png)**Figure
    9: MYCN expression level distribution for all u133-2 datasets
    in R2.**](_static/images/MultipleDatasets_LevelDistribution.png)
2.  Via the the probeset distribution view you can easily investigate a
    specific dataset in more detail.Click a preferred colored dataset
    dot and R2 will generate an one-gene-view graph. The one-gene-view
    representation is explained in more details in tutorial 2.









Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







K-means clustering in R2
========================



*How to discover novel groups or subtypes in your dataset using k-means
clustering*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   In this tutorial expression data of a set of Medulloblastoma tumors
    will be investigated for the occurrence of groups that have similar
    expression patterns.
-   Affymetrix data will be used in a k-means clustering analysis.





Tutorial step 1
---------------

1.  Make sure that the Single Dataset option is selected in field 1 of
    the step by step guide.
2.  In field 2 locate and select the 'Tumor Medulloblastoma PLoS One-
    Kool - 62 MAS5.0 -u133p2' dataset by clicking 'Change Dataset'
3.  In field 3 choose the 'K-means' option (Figure 1)
    [![](_static/images/Kmeans_selecting.png)**Figure
    1: Selecting K-means clustering on the R2 main
    page**](_static/images/Kmeans_selecting.png)
4.  Click "next"





Tutorial step 2
---------------

1.  The next window presents a set of fields where specific settings of
    the clustering algorithm used can be set. There are only a few
    settings immediately relevant, the others are appropriate for
    most analyses. For the k-means clustering these are the number of
    groups and the number of draws. We'll explain these shortly; for
    other settings refer to the boxed items.
2.  K-means clustering requires a number of groups beforehand, we start
    with two. To see whether the outcome of the clustering is stable
    (see boxed text on K-means clustering) we set the number of draws
    (performing of the calculation) to 10x10.
    [![](_static/images/Kmeans_clustersettings.png)**Figure
    2: K-means clustering
    settings**](_static/images/Kmeans_clustersettings.png)
3.  Dependending on the size of your dataset or geneset you can enlarge
    of minimize your K-means plot by adapting te size of the retangles
    at heatmap option. click "next"

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that K-means is a method of cluster analysis?***                |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=400){width="400"}](_static/images/K |
| means_didyouknow.png)                                   |
|                                               |
|                                                                          |
| \                                                                        |
| In data mining, k-means clustering is a method of cluster analysis which |
| aims to partition n observations into k clusters in which each           |
| observation belongs to the cluster with the nearest mean. This might     |
| sound complicated but is easily illustrated: suppose we have a set of 12 |
| patients where we observe the expression of two genes; expression of     |
| gene 1 along the x-axis, gene 2 on the y-axis (in our situation we have  |
| much more genes; the calculation will then be done in more dimensions).  |
| We're now going to try to cluster this set of n patients observed in     |
| three groups; k = 3. The following steps illustrate the algorithm (1-4   |
| from left to right) \# k = 3 initial "means" are randomly selected in    |
| the data set (shown in color) \# k clusters are created by associating   |
| every observation with the nearest mean. This partitions 2-D plane (the  |
| so called dataspace) in three areas. \# The initial means are moved to   |
| the centers of the three areas; the centroids. \# Steps 2 and 3 are      |
| repeated until convergence has been reached. As is obvious from the end  |
| point from this calculation this is a heuristic algorithm, there is no   |
| guarantee that it will converge to the global optimum, and the result    |
| may depend on the initial, randomly assigned clusters. As the algorithm  |
| is usually very fast, it is common to run it multiple times with         |
| different starting conditions and compare the outcome. R2 visualizes     |
| this in the end result of the calculation.                               |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+





Tutorial step 3
---------------

1.  R2 clusters the samples using the expression of 1500 genes
    exhibiting the highest standard deviation in this set. The result of
    10 sets of 10 calculations each, is shown as colored bars
    (Figure 3). Below the bars a heatmap is shown of the expression of
    the genes involved. It is obvious that two consistent clusters are
    formed; the assignment of the samples to a respective cluster is
    always the same. Note that figures reproduced by yourself might
    differ slightly when weaker associations are investigated; k-means
    is non-deterministic (random initiation).
    [![](_static/images/Kmeans_cluster.png)**Figure
    3: Results for the 10x10 k-means clustering in two groups; two
    consistent clusters
    are formed.**](_static/images/Kmeans_cluster.png)
2.  For visualization of k-means clusters, R2 performs hierarchical
    clustering on the samples for every group of k. Finally a
    hierarchical clustering is performed on the genes, making use of the
    information present in all samples. Because this is a large set only
    part of the map is shown in Figure 4
3.  This dataset has a clinical annotation for BCAT mutations; the upper
    bar or track in Figure 3. The subgroup having this annotation seems
    to cluster together in one of the two groups; this is however a
    subset of one of the two current clusters; more groups are expected.
    We're going to use a larger value for k to investigate this. In your
    browser click the back button and change the number of groups to 8.
4.  Click "next".
    [![](_static/images/Kmeans_heatmap.png)**Figure
    4: The heatmap for the k-means clustering in 2 groups; it is obvious
    that the data is represented in
    the clusters.**](_static/images/Kmeans_heatmap.png)

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that 'the \# highest SD genes is the number of genes with highest Standard Deviation?***
  Most of the other options (Sample/Gene filters etc) are explained in former tutorials. The "\# highest SD genes" is the number of genes with highest Standard Deviation (genes that 'make a difference' in this set) that is used for the K-means analysis. By default this value is 1500.
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



\



  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)**'Did you know that** ***some virus scanners slow drawing of these graphs??***
  If R2 takes a long time to draw images like these this might have to do with your virus scanner. The graphs are interactive and contain a lot of scripts that are usually scanned by a virus-scanner like McAffee. You can avoid this by disabling Script scanning.
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 4
---------------

1.  The resulting clustering in 8 groups is depicted in Figure 5
    [![](_static/images/Kmeans_track1.png)**Figure
    5: Clustering in 8 groups produces no
    consistent outcome.**](_static/images/Kmeans_track1.png)
2.  The outcome is not consistent (except for the cluster of samples
    having a bcat mutation)
3.  Repeat the procedure for 4 groups.
4.  In Figure 6 a clear and almost perfect clustering in 4 groups
    is established. Kool e.a. (2008) identified 5 subtypes in
    Medulloblastoma; this set is annotated in the lower track above the
    k-means tracks; they neatly follow 3 out of 4 clusters; the
    remaining two subtypes are less clear as is also clear when we try
    to separate the data in 5 clusters (Figure 7). By choosing
    subsets (categories) of genes before clustering you might be able to
    determine more precisely defined groups. An example of this method
    can be found in the Adapting R2 tutorial.

[![](_static/images/Kmeans_track2.png)**Figure
6: Consistent clustering for 4
groups.**](_static/images/Kmeans_track2.png)[![](_static/images/Kmeans_track3.png)**Figure
7: Clustering in 5
groups**](_static/images/Kmeans_track3.png)





Final remarks / future directions
---------------------------------



The identification of medulloblastoma subtypes has been published here:
Kool M, Koster J, Bunt J, Hasselt NE, Lakeman A, van Sluis P, Troost D,
Meeteren NS, Caron HN, Cloos J, Mrsic A, Ylstra B, Grajkowska W,
Hartmann W, Pietsch T, Ellison D, Clifford SC, Versteeg R.; Integrated
genomics identifies five medulloblastoma subtypes with distinct genetic
profiles, pathway signatures and clinicopathological features. PLoS One.
2008 Aug 28;3(8):e3088.





We hope that this tutorial has been helpful,The R2 support team.









Using signatures
================



*Find related gene signatures with a specified genelist or novel
correlating gene signatures*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----



Within the current context, we define a signature as a collection of
genes that are defined on a particular basis. This can be the presence
within a gene-ontology class, the genomic location of a gene, or perhaps
something potentially more meaningful like a functional pathway
signature. Functional pathway signatures are mRNA proxies for a
particular perturbation, such as the response to the downregulation of a
gene, or the consequence of a targeted compound (drug). Especially in
this context, the collection of genes may have predictive power for the
activity of a process. Of course it becomes cumbersome to assess the
activity on a gene-by-gene basis. It would be very handy if we could
express the behavior of all the genes in a single value. Within R2, we
can convert the behavior of a list of genes into a signature score that
can be calculated for all samples within a particular dataset. This
signature score is simply defined as the average zscore of a zscore
transformed dataset (the standard way of visualizing a heatmap) (Figure
1). In R2, such scores are automatically generated when one generates
heatmaps via the "view a geneset" function. With the exception of some
exceptional cases, most functional signatures will be composed of both
upregulated genes as well as downregulated ones. Using both as a single
list may then become problematic, as downregulated genes may counteract
the effects of upregulated genes, effectively leveling each other out.
To circumvent this problem, we can create 2 separate gene categories,
one containing only the upregulated genes, and one containing only the
downregulated genes. R2 will recognize couples of gene categories if
they follow a specific convention (fixed prefix, followed by \_up and
\_down; e.g. mycn\_up and mycn\_down).



[![](_static/images/Genesetcorrelation_sig_score_explained_v0.png)**Figure
1: Signature score: one category vs up/down
category**](_static/images/Genesetcorrelation_sig_score_explained_v0.png)
-   What is a genesignature
-   Create a track using the weight scores of a genesignature
-   Relate a weighed genesignature track to a single gene
-   Find correlating genesignatures with a track

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can create gene category couples***
  R2 can treat particular gene categories in a special way if you follow a simple naming convention. Especially helpful for signature scores are up/down regulated gene couples. Within the "view a geneset" function, you can select multiple gene categories to be used in for the heatmap. If you select 2 categories that contain a fixed prefix, coupled to \_up and \_down (or \_dn), then R2 will treat them as a couple, and will subtract the downregulated signals from the upregulated ones (effectively creating a signature score). We can weigh the 2 separate lists of genes either equally, or weighted as a percentage of the number of genes (the weighted\_match / \_wm signatures).
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 1
---------------



As a start, let"s create the signature scores for a pair of gene
categories. In this tutorial, we will make use of a published functional
MYCN pathway activity signature that was created on the Neuroblastoma 88
dataset (Valentijn et al 2012). This signature is provided within R2.



1.  We start at "Main". Make sure that the "Single dataset" option is
    selected in "box 1".
2.  In "box 2" verify that the current dataset is "Neuroblastoma
    public - Versteeg - 88 - MAS5.0 - u133p2".
3.  In "box 3" we select "View geneset (Heatmap)".
4.  Click "Next" (Figure 2.1).
5.  In the following screen we select the
    "geneset\_\_r2provided\_genesets" Gene set collection and click
    "Next" (Figure 2.2).
6.  In the following screen we select the "functional genesignature"
    subselection and click "Next" (Figure 2.3).
7.  We can now see the lists of genes that are represented in
    this collection. While holding the CTRL key pressed, we can select
    the following 2 gene categories "r2\_imr32mycn\_dn"
    and "r2\_imr32mycn\_up". Then click "Next" (Figure 2.4).
8.  R2 will now produce a hierarchical clustered heatmap image of the
    selected gene categories (Figure 2.5). Note that at the right end of
    the image the red boxes indicate in which category a particular gene
    was represented. In the bottom part of the heatmap, a blue-white-red
    colorscale is depicted for both gene categories. We can clearly see
    the opposing effects of the 2 signatures.
9.  Scrolling down on this page, we will encounter a heading "Gene set
    values", which presents a small table. The links within this table
    point to the numerical values of the geneset scores. For the 2 gene
    categories, R2 will create the scores of the 2 separate categories,
    a matched score (where up and down regulated genes are treated
    equally (50/50)), and a weighted\_matched score (where up and
    downregulated genes are treated on their contribution (percentage
    for number of genes)). Click on "store" for the "weighted\_matched"
    signature, so that we can perform additional analyses on it
    (Figure 2.6).
10. R2 has now assembled the information into a prescription to generate
    a track. By default R2 will store the track for 24 hours, which is
    fine for the current tutorial. Click on "Build set" to store the new
    track (Figure 2.7).

[![](_static/images/Genesetcorrelation_mycn_signature_v1.png)**Figure
2: Generate
genesignature**](_static/images/Genesetcorrelation%20mycn%20signature%20v1.png)





Tutorial step 2
---------------



Now that we have created a signature from our 2 lists of genes, we can
start using it as if it was a gene itself. For example we can inspect
how the MYCN pathway activity signature correlates to the MYCN gene at
the mRNA level.



1.  Go back to the "main" page and select "correlate gene with track"
    from "box 3". In "box 4" we provide "MYCN" and click "Next"
    (Figure 3.1).
2.  On the following page, we select our newly created track in the
    "select a track" dropdown box and click "Next"(Figure 3.2).
3.  R2 will now produce a plot where the signature score for every
    patient is related to the MYCN mRNA expression value (Figure 3.3).
4.  We can make this look a bit prettier by adapting the color for
    patients on the basis of e.g. MYCN amplification status. To achieve
    this, we go to the "adjustable settings" at the bottom of the page
    and select "Color by track" from the "ColorMode" and select
    "mycn\_amp" from the "Track for color" option. Click "Adjust
    Settings" to redraw (Figure 3.4).
5.  We can now clearly see that MYCN amplified patients have a higher
    MYCN activity score. The possibilities for numerical tracks are
    endless with some smart questions (Figure 3.5).





[![](_static/images/Genesetcorrelation_mycn_signature_group_v0.png)**Figure
3: Add group
colouring**](_static/images/Genesetcorrelation_mycn_signature_group_v0.png)





Tutorial step 3
---------------



Now that we have related the signature to a particular gene, it is easy
to envision that this can be done as an analysis as well, where the
signature is correlated to all genes in the genome ("correlate with a
track " in "box3"). A lot of signatures have been designed and published
in literature over the past years. We can convert all of these into
signature scores and start searching for relations of these meta-genes
with our signature of interest.



1.  Go back to the "main" page and select "Geneset vs Geneset
    correlation" from "box 3" and click "Next" (Figure 4.1).
2.  On the next page, select at the input Geneset -&gt; Gene set
    Collection (source): "geneset\_\_r2provided\_genelists". In the
    Genesets to Scan (target): select 'geneset\_broad\_2012\_oncogenic'
    (Figure 4.2). Then click "next".
3.  In the next screen select in the source pull downmenu "functional
    genesignature" and "ALL" in the target pulldown menu leave the
    remanining settings to their default and click 'next'(Figure 4.3).
4.  The gene signature consists of two parts. one set of genes which are
    up regulated by MYCN and one set of down regulated genes. In the
    next screen select both presented gene lists by holding the Ctrl-
    button (see Figure 4.4) and click "next."
5.  R2 has now generated all the possible correlations for the selected
    MYCN signature against all the gene lists within the broad
    oncogene category. This results in a table of geneset versus geneset
    correlations sorted by the p-value. The "venn source/ same / target"
    column provides insight in overlapping genes between two gene lists.
    Another informative parameter in the table is the range parameter in
    the last column. This value indicates the range of geneset scores in
    gene target signature (see Figure 4.5).
6.  To inspect the correlation in more detail, we can click on the
    "XY-plot" link.
7.  Now R2 has generated an XY-plot of all samples in the dataset. The
    XY values represent the signature scores for the 2 signatures for
    every sample. Below the image the overlapping genes in the 2
    signatures are listed (see Figure 4.6).
8.  We can also inspect the target signature as a heatmap by clicking on
    the "View heatmap of "", providing gene-by-gene information (see
    Figure 4.7).

[![](_static/images/Fig4_mycn_signature_vs_sign_v1.png)**Figure
4: Find
genesignatures**](_static/images/Fig4%20mycn%20signature%20vs%20sign%20v1.png)







Analysing Time Series
=====================



*Search for up and-down regulated genes in a time series experiment*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Time series experiments, where a cell line is manipulated and
    followed over time, are analyzed and visualized in a separate
    section in R2. The actual analysis of any time series in R2 has been
    pre-calculated by the Affymetrix GCOS program. Within GCOS, every
    timepoint in a series has been compared to time-point zero. GCOS,
    makes use of the fact that every probe-set of an Affymetrix array is
    actually a measurement performed 11-16 times. These measurements are
    used as "independent" inputs to calculate a p-value. Due to the use
    of GCOS, the time series functionality is only available for the
    U133 type Affymetrix platforms. Of course, our advice would be to
    use biological replicates of all experiments.
-   In most cases, time series experiments are performed by specific
    usergroups, whose data is often shielded from public assess. There
    are however also a few publicly available sets, to illustrate what
    this part of R2 can do. All the experiments performed on the same
    platform will most often be stored within a single set.
-   Single gene expression levels can be visualized and list of
    regulated genes can be generated via a range of filtering methods.
    Please be aware that GCOS uses the probe information (contained
    within a probe set) from a single array to calculate p-values on.
    This is a controversial approach, but for many of the performed
    experiments the only way to obtain statistical values. If a
    timeseries experiment has been performed 3 or more times, then
    perhaps a better alternative would be to make use of the
    functionalities that are available for regular datasets.

<!-- -->

-   Use the time series module to investigate the expression level of a
    single gene.
-   Use the time series module to generate a list of regulated genes.

<!-- -->

-   Use a list of regulated genes to analyze a dataset by using the
    geneset view.

<!-- -->

-   Use correlate with dataset to optimize your genecategory.





Tutorial step 1
---------------





1.  To view the expression pattern of a single gene from a time series
    experiment we make use of the "Time-series" module. Logon to R2 and
    select Time series in left menu panel of R2.
    [![](_static/images/AnalysingTime_Select.png)**Figure
    1: Single selection in the Time-series
    module**](_static/images/AnalysingTime_Select.png)
2.  In field 1, select at collection "u133p2 (public)". Here
    "collection" is indicated as a category of Time series experiments.
    For time series the analysis is limited to the Affymetrix Hu133A or
    Hu133plus arrays. The "Collection" field not only implies the
    platform type but may also include another subgroup , in this a case
    a publically available Times series data. Select "View a gene; in
    field 2, type *HMOX1* in field 3*,* and click "next".
3.  In the next screen all the public available time series for the
    u133p platform R2 is hosting, is listed. In our example we make use
    of a Time series experiment published in
    [Bioinformatics.](http://www.ncbi.nlm.nih.gov/pubmed/20007254)"2010
    Feb 15;26(4):456-63. In this Time series, the experiments are
    performed in triplo . The A549 Adenocarcinoma cellline is treated
    with TGF-beta and the expression levels where measured at
    several timepoints. In Figure 2 click on the (+) sign to unfold the
    Time-course experiments belonging to the A549 cellline and
    click "next". In the adjustable settings menu, leave all the default
    settings and click "GO".
    [![](_static/images/AnalysingTime_SelectSeries.png)**'Figure
    2: Timeseries
    selection screen.**](_static/images/AnalysingTime_SelectSeries.png)
    In Figure 3 the expression levels of the HMOX1 gene are represented
    in a triplicate Time course experiment after stimulation
    with TGF-beta. Clearly the HMOX1 gene is an early responder and is
    upregulated with a maximum at 4 hours. The HMOX1 gene is presented
    by the authors of the corresponding publication as one the
    upregulated genes after TGF-beta stimulation. It"s should be noted
    that a control experiment is missing in this experimental design.
    Hovering over the individual timepoint reveals
    additional information.
    [![](_static/images/AnalysingTime_HMOX1.png)**Figure
    3: Expression levels of the HMOX1 gene during a time course
    experiment**](_static/images/AnalysingTime_HMOX1.png)
4.  Another gene the authors claim to be upregulated by TGF-beta is the
    BCL6 gene. In the same screen you can quickly generate a time series
    graph by providing the BCL6 gene in the right upper corner and click
    "Search Gene".
    [![](_static/images/AnalysingTime_Probeset.png)**Figure
    4: Probeset verification and
    Adjustable Settings.**](_static/images/AnalysingTime_Probeset.png)



The probeset verification table lists in the case of BCL6 the 3
probesets designed for the BCL6 gene. By default R2 will select the
probeset with the highest average expression level. Clicking on the
Tview link opens a separate application "Transcript view" to investigate
the reporters in more detail. The Transcript view application is
explained in tutorial 2 "one-gene-view".





In the adjustable settings menu you can customize the Time series graph
to your personal needs. Such as fontsize , Line width etc.



  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can contact the R2-support team to add your Time-series experiments***
  Your Time series experiments will be listed as a separate collection and for private analyses only. The R2-support team requires the CEL datafiles provided by your Microarray facility, to generate the result files.
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 2
---------------

1.  Instead of looking at one single gene, you may most likely want to
    find novel up and-down regulated genes in your cell-line experiment.
    Go to the main screen and select in field 2 "Select type of
    analysis, "create a list of genes" and click "next".
2.  In the next screen select again all the A549 timeseries experiment
    and click "next".
3.  In following screen you can use the table builder to apply all kind
    of filtering options to find the novel regulated genes. Some of the
    options are already set.
    [![](_static/images/AnalysingTime_Tablebuild.png)**Figure
    5: The time series
    table builder.**](_static/images/AnalysingTime_Tablebuild.png)
    An explanation of some of the options follows below:
    ***Min \#experiments***: Depending on your experimental design
    select in how many experiments your gene should be regulated
    according to your filter.
    ***Min highest expression in series***: Set the minimal highest
    expression in at least one of the samples in your Time
    Series experiment. In this way the genes which are not expressed
    above a certain level (eg background) \#:will be skipped.
    ***Min\# present calls in series***: The affymetrix MAS5.0 algorithm
    detects whether a gene is significantly detected and receive a
    "present call".
    ***Min \#significant change in series***: Whenever the expression in
    a time series is significantly altered compared to time point 0, a
    "change" call is elevated. At least one change in expression level
    should be \#:significant (meaning that you also would like to see
    those results where only in 1 time point a change is observed).
    ***Fold orientation***: determine the orientation here. Up / Down /
    Both
    ***Minimal best fold in a series***: Set a minimal logfold that has
    to occur within the series.
    ***Min lowest change pvalue in series***: The MAS5 algorithm
    provides a p-value of the fold change, before a probeset is
    considered changed a minimal pvalue of 0.00025 should be met. Here
    you can set the pvalue to a more \#:strict level.
    ***Force single reporter for hugo***: It"s possible to analyse all
    probesets representing a single gene. As explained in another
    tutorial by default R2 will select the probeset with the highest
    average expression level.
    Select and set the options as depicted in Figure 5 and click "next".
    [![](_static/images/AnalysingTime_SortedTable.png)**Figure
    6: Up and down regulated genes table sorted on best fold
    change**](_static/images/AnalysingTime_SortedTable.png)
4.  In Figure 6 a part of the up and down regulated genes are shown,
    listing the fold change and highest expression level for each Time
    series experiment. Clicking on a probeset link generates a single
    gene time series plot as shown in Figure 7.
    [![](_static/images/AnalysingTime_RegulatedGene.png)**Figure
    7:
    regulated gene.**](_static/images/AnalysingTime_RegulatedGene.png)
5.  Clicking on the filter button will open the "adjustable settings"
    panel to re-adjust the selection options. Clicking on the Venn
    "diagram button re-direct to the automatically generated Venn
    Diagram representing the intersection of the genesets.
    [![](_static/images/AnalysingTime_Button.png)**Figure
    8: Top
    buttons**](_static/images/AnalysingTime_Button.png)
    [![](_static/images/AnalysingTime_Venn.png)**Figure
    9: Time series Venn
    diagram**](_static/images/AnalysingTime_Venn.png)

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that Venn diagrams can be created directly from your genecategories of choice?***
  In the My Settings section you can upload text files containing your lists of genes and store them as genecaterory. Repeating the procedure described above will produce the desired Venn diagrams.
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 3.
----------------

1.  One of the strong points of R2 is that it supports directly further
    analyses with other modules and datasets stored in the database. Use
    the table of up and down-regulated genes of step2 to investigate if
    this list of genes can be of relevance in other datasets. In the
    left panel click "store results as gene category". A new screen
    appears where you can enter an informative name for your
    genecategory and add a short description. The genecategory can be
    stored for 24 hours or stored permanently in your account, after
    which it is available each time you log in to R2. For now choose the
    Temporary option at "Where" and remember the name of the stored
    genecategory for the next step.
    [![](_static/images/AnalysingTime_CustomCat.png)**Figure
    10: : Store a gene
    category**](_static/images/AnalysingTime_CustomCat.png)
2.  It has been published that the timecourse expression data from the
    cell experiment used in this example is linked to
    epithelial-mesenchymal transition (EMT) by TGF-beta induction. It"s
    also known that this process plays an important role in
    Breast cancer. We can use this generated genecategory to investigate
    whether this of any relevance or not.
3.  Go the the main screen of R2 and select at "change dataset" the
    following dataset . Tumor Breast - Iglehart - 123 - MAS5.0 -
    u133p2 . In field 3 select "View Geneset" at "Select type of
    analyses" and click "next".
    [![](_static/images/AnalysingTime_Geneview.png)**'Figure
    11: Geneview
    adjustable settings.**](_static/images/AnalysingTime_Geneview.png)
4.  At "Gene set Collection" choose " My 24h geneCategories" and select
    the generated "genecategory" from step 1. Instead of an unsupervised
    sample clustering you can also cluster samples within a track.
    Select at "Order samples" by " ordering by track and click next.
5.  Click next again.
6.  Choose the temporary Genecategory generated via the Timeserie
    experiments, the track b-r\_grade and click "next".
    [![](_static/images/AnalysingTime_Heatmap.png)**Figure
    12: Heatmap of unsupervised clustering within a track of a
    selected geneset.**](_static/images/AnalysingTime_Heatmap.png)
7.  The samples are unsupervised hierarchically clustered within each
    group of the selected track and presented in a heatmap. The selected
    genecategory resulting from the timeserie experiment could be of
    clinical relevance since the clustering correlates with the
    Oestrogen Recepter track. At the bottom of the heatmap the z-scores
    of the selected genecategory is represented./

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that clicking a spot in the heatmap reveals more info***
  Clicking on a spot generates a one-gene-view for the chosen gene in the dataset only supported for a genecollection consisting &lt; \~400 genes.
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



\



  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that with "sample ordering" (Figure 11) you can manage the way the samples are clustered.***
  By choosing "sample ordering " by "track" , the unsupervised clustering of the samples is applied within the groups of a track. It is even possible to customize the way the samples are ordered by yourself (user defined order).
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial step 4
---------------





1.  Instead view a " geneset, you can also choose perform a "K-means"
    clustering based on your stored genecategory described in the steps
    " above". Go to the main menu, select "K-means" at " Select type of
    analysis" and click "next".
2.  In the "Adjustable settings" panel leave most of the default
    settings but make sure that you select the already stored
    "Genecategory" at the clustering section select '10x10" at "numbers
    of draw" and click "next".
    [![](_static/images/AnalysingTime_heatmap2.png)**Figure
    13: 10x10 Heatmap with the same dataset and gene category as
    depicted in
    Figure 9.**](_static/images/AnalysingTime_heatmap2.png)



Performing a 10x10 K-means clustering via de main menu supports the
potential clinical relevance of the genecategory extracted from the
timeserie experiment. The K-means cluster module is discussed in more
detail in tutorial 10.



  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can store the K-means generated track and use this track every time you log in to R2.***
  You can use this track for further analysis with a custom made track for example by using the "find differential expression between groups". This approach explained in more detail in tutorials : Differential Expression Of Gene Between Groups and "Adapting R2 to your needs" .
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





Tutorial Step 5
---------------

1.  The module "correlate" the results with dataset compares the
    resulting genelist with a dataset of interest. Clicking the
    correlate with dataset button in the left menu redirects to a
    new screen. Choose the Igleheart " Breast in field 2, in field 3 ,
    choose "relate to differential expression" and click next.
2.  Choose "er" at select a track and click "next".
3.  In de background R2 generates a list of genes based on the module
    "Find differential expression between groups" and presents the
    overlay of the results with the list generated in the " time
    series module".
    [![](_static/images/AnalysingTime_TableCorrelate.png)**Figure
    14: Part of correlate with
    dataset genelist.**](_static/images/AnalysingTime_TableCorrelate.png)
4.  In *Figure 14* the overlap is presented between the result from the
    " time series" module and the " relate to differential
    expression" option. The list of genes is sub-divided in a positive
    and a negative correlation list of genes. Clicking the "2-view" link
    opens a new screen with a combined graph of a one-geneview and the
    time series experiment.





Final remarks / future directions
---------------------------------



Final remarks / future directions if applicable





We hope that this tutorial has been helpful,The R2 support team.









Using / Creating genesets in R2
===============================



*Or how you can achieve clear, presentation ready heatmaps of your
dataset*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   In this tutorial the visualization of a set of genes will be
    explored
-   R2 provides a conventional heatmap view""
-   This heatmap view can be adapted to your needs by sorting the data
    along the axes according to your wishes.
-   Generating your own genelists to analyze using the
    Toplister function.





Tutorial step 1
---------------

1.  On the main page of R2 select View Geneset (Heatmap) (Figure 1).
    Click 'Next'.
    [![](_static/images/UsingGenesets_Select.png)**Figure
    1: Select View a
    Geneset**](_static/images/UsingGenesets%20Select.png)
2.  In the subsequent window three choices are available to customize
    the way the GeneSet data will be presented (Figure 2). The first
    field asks for a collection of genesets (Figure 3); R2 harbors
    hundreds of publicly available genesets, KEGG pathways being one
    of them. The second field is a filter for selecting the samples. The
    third field is the order by which the resulting heatmap will be
    drawn (Figure 4). By default R2 presents the data in a heatmap where
    a hierarchical clustering is performed on the genes, making use of
    the information present in all samples to order the data. We'll show
    first what this ordering by clustering looks like. Keep all settings
    as they are and click next. The search fields below the Adjustable
    Settings dialog provide a shortcut for finding a GeneSet of choice,
    we're going to use this now. Suppose we want to find a geneset
    containing Cell Cycle genes. Type Cell Cycle in the 'Search a
    geneset' box and click 'Search'.
    [![](_static/images/UsingGenesets_Settings.png)**Figure
    2: The R2 Gene Set view settings; A set can be selected, filtered
    for subsets and the clustering results will be ordered according to
    the selection. We're now going to search for Cell Cycle gene
    sets**](_static/images/UsingGenesets%20Settings.png)
    [![](_static/images/UsingGenesets_Collections.png)**Figure
    3: Available collections of Genesets in
    R2**](_static/images/UsingGenesets_Collections.png)
    [![](_static/images/UsingGenesets_Ordering.png)**Figure
    4: Available ordering domains for
    samples**](_static/images/UsingGenesets_Ordering.png)
3.  In the next window all genesets containing the words Cell Cycle in
    their description are shown. Choose the KEGG Cell Cycle (in the
    collection of Cellular Processes) by clicking the 'View' hyperlink.
    [![](_static/images/UsingGenesets_Selecting.png)**Figure
    5: Selecting a geneset out of the large collection of available sets
    in R2; Cell Cycle was used as a
    search term.**](_static/images/UsingGenesets_Selecting.png)
4.  The Affymetrix data for the Neuroblastoma 88 dataset is shown for
    the genes in the Cell Cycle as a clustered heatmap. Hovering over
    the heatmap rectangles reveals the sample information stored in the
    R2 database. Keep in mind that the hovering option is limited to
    10000 cells otherwise the graph generation consumes too much time.
    This limitation can be adapted in the \`my settings\`.

[![](_static/images/UsingGenesets_Heatmap.png)**Heatmap
view of the Kegg Cell Cycle geneset for the Neuroblastoma 88 dataset;
genes and samples are sorted according to the
clustering.**](_static/images/UsingGenesets_Heatmap.png)





Tutorial step 2
---------------

1.  R2 also allows for multiple genesets to be shown at once; return to
    the main page; select View Geneset (Figure 1: Select View
    a Geneset). We're not going to search for a geneset but look for
    multiple sets at once in the KEGG collection. In the next window
    (Figure 2) leave the default collection to KEGG. Click "next" in the
    'Adjustable Settings' box.
2.  In the next screen a subcollection within the current collection of
    genesets has to be defined; Select 'Cellular Processes' and click
    "next" (Figure 7).
    [![](_static/images/UsingGenesets_Subcollection.png)**Figure
    7: Selection a subcollection from the large collection of Kegg
    pathways**](_static/images/UsingGenesets_Subcollection.png)
3.  R2 allows selection of multiple genesets at the same time; CTRL+
    select Cell Cycle and Apoptosis and click 'Next'.
    [![](_static/images/UsingGenesets_Doubleselect.png)**'Figure
    8: Selecting multiple
    genesets**](_static/images/UsingGenesets_Doubleselect.png)
4.  The resulting heatmap (Figure 9) has the samples ordered by the
    result of the clustering of the dataset. On the y-axis the genes are
    annotated with their membership to both pathways; the upper bar is
    the Cell Cycle. It is obvious that part of the Cell Cycle member
    genes are clustering together.

[![](_static/images/UsingGenesets_Heatmap2.png)**Figure
9: Heatmap view of the Cell Cycle and Apoptosis genesets for the
Neuroblastoma 88
dataset.**](_static/images/UsingGenesets_Heatmap2.png)





Tutorial step 3
---------------

1.  We're going to explore that in further detail by sorting the dataset
    according to the staging. Return to the former choice page
    (Figure 2) by clicking the back button in your browser. Choose
    'Order samples by a track' and click "next" (Figure 10). In the next
    subcollection selection window choose Cellular Processes again
    (Figure 7) and click "next".
    [![](_static/images/UsingGenesets_SelectDomain.png)**Figure
    10: Selecting the domain to order samples by: Order by a
    track**](_static/images/UsingGenesets_SelectDomain.png)
2.  Now select only the Cell cycle subset as GeneSet. Choose the
    Neuroblastoma staging INSS as track to order samples by and click
    "next" (Figure 11)
    [![](_static/images/UsingGenesets_CellCycle.png)**Figure
    11: Selecting Cell Cycle only, order samples by Neuroblastoma
    staging
    track**](_static/images/UsingGenesets_CellCycle.png)
3.  In the resulting heatmap it is clear that there is a segment of
    genes in the Cell Cycle pathway cluster that is consistently
    upregulated in the stage 4 Neuroblastoma samples (in red in the
    INSS track).
    [![](_static/images/UsingGenesets_HeatmapSorted.png)**Figure
    12: Heatmap sorted by INSS stage, there is a clear relation between
    the stage 4 tumors (in red in the INSS track) and up-regulation of a
    subset of genes \#:of the Cell
    Cycle**](_static/images/UsingGenesets%20HeatmapSorted.png)
4.  In the previous example R2 offers the possibility to set a fixed
    ordering of samples by track. It"s also possible to perform a
    clustering and set a fixed ordering of genes. In the "adjustable
    settings" panel, select user defined order in the geneselection
    pulldown menu and click next two times. Here you can paste a list of
    genes sorted according to your needs.
5.  Ifyou want to perform hierarchical clustering with a fixed
    sample order. From the main menu select View a Geneset (Heatmap) ,
    in the sample order section, select user defined order and click
    next, select a geneset sub collection and click next. Copy and paste
    your sample order and click next. The export track function see
    chapter Error: Reference source not found can be handy for
    this issue.





Tutorial step 4
---------------



It could be that for a given dataset there is no annotation to apply the
analysys tools R2 is offering or your"re lacking a starting point to
further investigated a dataset. A good starting point could be to do is
to do a simple hierarchicl clustering



1.  In chapter " Error: Reference source not found" is explained how to
    generate genesets describing the difference between tracks (groups)
    from an annotated dataset. Researchers often want to investigate the
    presence of subgroups without using annotation information in their
    dataset or just find a list of genes with the highest variation in
    gene expression. In case your dataset of interest lack annotation
    you are still able via the Toplister tool to investigate datasets
    for biological relevance.
2.  For this purpose R2 is hosting a convenient tool to generated lists
    of genes using a filter. By using this filter you can select groups
    of genes with the highest, lowest or most variable genes etc etc.
3.  To use the toplister tool go to the main menu and select
    tools&gt;small tools &gt; Toplister. Make sure Data Type is set to
    Expression data and select Tumor Medulloblastoma PLoS One - Kool -
    62 - MAS5.0 - u133p2 and click next. In the adjustable settings
    screen all kinds of settings and filtering options can be adapted.
    We want to know which 100 genes have the highest variation in this
    case leave " which set" at standard deviation (SD) which is the
    default settings. Click next.
4.  R2 has generated a list of 100 genes showing the highest variation
    in gene expression.
5.  Scrolling down to the bottom of the page shows possibilities to save
    or export the genelist to use for other analyses and/or usage in
    other datasets. Clicking on the Heatmap (Zscore) will perform an
    unsupervised hierarchical clustering and plots a heatmap . In this
    heatmap the subgroups are clearly clustered together as shown by
    Kool e.a. (2008).

[![](_static/images/UsingGenesets_Unsupervised.png)**'Figure
13: Unsupervised hierarchical clustering revealing subgroups in a
Medulloblastoma
dataset.**](_static/images/UsingGenesets_Unsupervised.png)





Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







Principle Component Analysis in R2
==================================



*How to identify patterns or groups in your dataset using Principle
Component Analysis.*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   In this tutorial expression data of a set of Medulloblastoma tumors
    will be investigated for the existence of subgroups.
-   Principle Component Analysis (PCA) will be used to analyze the
    tumor samples.





Tutorial step 1
---------------

1.  Make sure that the Single Dataset option is selected in field 1 of
    the step by step guide.
2.  In field 2 locate and select the 'Tumor Medulloblastoma PLoS One-
    Kool - 62 MAS5.0 -u133p2' dataset by clicking 'Change Dataset'
3.  In field 3 choose the 'Principle Component Option' option (Error:
    Reference source not found)
    [![](_static/images/PrincipleComponent_Select.png)**Figure
    1: Selecting Principe Component
    Analysis**](_static/images/PrincipleComponent_Select.png)
4.  Click "next"





Tutorial step 2
---------------

1.  The next window presents a set of fields where specific settings of
    the clustering algorithm used can be set. Leave all the settings at
    their default and click "next".
2.  Click to plot the PCA result.
3.  You now see a plot of the of the first 2 principle components. In
    the adjustable settings box, al the combinations principle
    components can be selected. R2 enables visualization of the first
    three principle components (PC1,2,3) in 2D or 3D graphs.
4.  In the adjustable setting box select the all PCA-components option
    to the several principle components combinations to investigate
    whether you can distinguish subgroups in your dataset.
    [![](_static/images/PrincipleComponent_Adjust.png)**Figure
    2: Adjusting PCA
    settings**](_static/images/PrincipleComponent_Adjust.png)
    [![](_static/images/PrincipleComponent_SelectTracks.png)**'Figure
    3: Selecting
    tracks**](_static/images/PrincipleComponent_SelectTracks.png)
    [![](_static/images/PrincipleComponent_Combinations.png)**Figure
    4: All 3 PCA-component combinations plotted in
    2-dimensional space.**](_static/images/PrincipleComponent_Combinations.png)
    In this example the samples are colored by known groups and fitted
    with the PCA result. In Figure 4 a clear subgroup, the yellow wnt
    subgroup is revealed. Hovering over the data points provides the
    principle component vector \#:values which are depicted, as well as
    additional sample information. This example illustrated that PCA is
    powerful tool aiding to find possible subgroups in your dataset
    of interest.
5.  Select in the adjustable settings box "Label by Track" at LabelMode.
    A "Track for Label" pulldown menu unfolds, here select your option
    of interest e.g "Samplenames" and click next.

[![](_static/images/PrincipleComponent_Label.png)**'Figure
5: Samples are in annotated by track by using
LabelMode.**](_static/images/PrincipleComponent_Label.png)
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that PCA clustering is a method that reduces data dimensionality?***
  \[Principle Component Analysis is a method that reduces data dimensionality by performing co-variance analysis between factors. PCA is especially suitable for datasets with many dimensions, such as a microarray experiment where the measurement of every single gene in a dataset can be considered a dimension. It is impossible to make a visual representation of the relation between genes and their conditions in multi-dimensional matrix. One way to make sense of data is to reduce dimensionality. Several techniques can be used for this purpose and PCA is one of them. The reduction of dimensions is archived by plotting points in a multidimensional space onto a space with fewer dimensions. The reduction is accomplished by identifying directions, so called *principle components*, that describe maximal variation in the data. These principle components can then be used as surrogates to represent each sample, making it possible to visually assess similarities and differences between samples and determine whether samples can be grouped. As the principle components are uncorrelated, they may represent different aspects of the samples and is therefore a powerful tool to identify subgroups in you dataset.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



\
Each datapoint in the graph is now provided with a label annotation.







Tutorial step 3:
----------------



A very nice feature of the R2 PCA module is the possibility to
investigate your data in an interactive 3D-plotted graph. Most recent
internet browsers support the 3D visualization.



+--------------------------------------------------------------------------+
|                                               |
|                                                                          |
| With Firefox in some cases it"s not possible to rotate the 3D graph in   |
| that case adjusts the following setting in firefox. : type about         |
| "about:config" in the URL box, search for webgl and Enable               |
| "webgl.force-enabled": TRUE. The 3-D module is also working with Chrome  |
| but not with Internet Explorer.                                          |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+

1.  In the adjustable settings menu select the "3d" option and
    click "next".
2.  Click the cube and hold the left mouse button and rotate the picture
    in order to investigate whether there are any (more)
    subgroups visible.
    [![](_static/images/PrincipleComponent_3D.png)**'Figure
    6: Showing a 3D PCA graph from
    different angles.**](_static/images/PrincipleComponent_3D.png)
3.  By rotating the graph more subgroups could be revealed as clearly
    shown in Figure 6.





Final remarks / future directions
---------------------------------



The identification of medulloblastoma subtypes has been published here:
Kool M, Koster J, Bunt J, Hasselt NE, Lakeman A, van Sluis P, Troost D,
Meeteren NS, Caron HN, Cloos J, Mrsic A, Ylstra B, Grajkowska W,
Hartmann W, Pietsch T, Ellison D, Clifford SC, Versteeg R.; Integrated
genomics identifies five medulloblastoma subtypes with distinct genetic
profiles, pathway signatures and clinicopathological features. PLoS One.
2008 Aug 28;3(8):e3088.





We hope that this tutorial has been helpful,The R2 support team.









Using the R2-Genome browser
===========================



*Use the Genome browser to verify reporters*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   In this tutorial investigate reporters and reveal information R2 is
    providing based on the genome location.
-   Explore reporters in the genome browser in combination with gene
    expression profiles (from the one-gene-view).





Tutorial step 1
---------------

1.  In the main menu select in field 2 the default dataset "Tumor
    Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2". In Field 3
    choose "View a gene" at "type of analysis". In field 4: type "MYCN"
    and click "next".
2.  Leave all the settings at their default and click "next". You have
    now arrived at the "One Gene View". In this tutorial the main focus
    is the evaluation of the reporters designed by manufactures such as
    Affymetrix represented in the R2 Genome browser and to a lesser
    extent the gene expression. When you slide down on the "One gene
    view" page of the MYCN expression, you encounter the "Probeset
    verification" table. The Probeset verification table, displays an
    automated analysis for U133 based Affymetrix platforms, where the
    reporter-gene relation validity has been verified by their genomic
    location (also described in more detail in the
    tutorial one-gene-view). Click on the "R2 Tview" link of the upper
    probeset and The embedded R2 genomebrowser will open in a
    new screen. The genome browser shows the Genomic span where the MYCN
    gene is located together with the 5 MYCN probesets mapped to their
    genomic position.
    [![](_static/images/UsingR2genome_probesettable.png)**Figure
    1: Genome browser and Transcript
    view**](_static/images/UsingR2genome_probesettable.png)
    [![](_static/images/UsingR2genome_Genomebrowser.png)**Figure
    2: The probeset verification
    table**](_static/images/UsingR2genome_Genomebrowser.png)
    When we access the genome browser via the one-gene-view, then by
    default it has enabled a number of annotations (Tracks). At the top
    of the image,R2 is depicting all known EST and mRNA sequences
    aligned to the genome ( \#: synchronized with the USCS
    database regularly). These mappings serve as evidence for the
    existence of a gene, and are individually hyperlinked to the
    Genbank database. The EST and mRNA sequences are colored by the
    orientation \#: of alignments, as determined by exon-intron
    junctions and poly-A signals to the genome. Here, green alignments
    indicate a 5\`-&gt; 3\` mapping on the positive strand of the
    genome, while a red mapping represents a \#: 5\`-&gt;3\`mapping on
    the negative strand of the genome (reverse complement orientation).
    In sequences where no information on the orientation is encountered,
    the alignment becomes blue. In this MYCN example, the gene, as \#:
    represented by the refseq \#: track, is green. This tells us that
    the MYCN gene maps to the positive strand of the genome, and should
    be read 5\`-&gt;3\`from left to right. The shadings in green, for
    the separate EST and mRNA \#: mappings, indicate exon (darker) and
    intronic (lighter) regions (Figure 3 shows a legend to all the
    different color shades). If we look at the reporters underneath the
    refseq track, then we see that most of them are green \#: as well
    (thus mapping to the same strand as the MYCN gene). However, the
    242026\_at reporter appears in red (thus mapping to the negative
    strand), and thus cannot measure MYCN expression. Furthermore, this
    reporter also maps \#: at the intronic region, another reason why
    you should not use this reporter to represent MYCN. Still, this
    reporter is annotated to measure MYCN by the Affymetrix company.
    Below the EST and mRNA mappings, you can see the average gene
    expression for the reporters in the neuroblastoma dataset, which we
    are investigating. This panel can be handy, to see which reporter
    shows the highest
    expression (and often is the preferred reporter to use). Since the
    U133 platforms of Affymetrix are 3\`based, you can nicely see that
    the reporter signals are higher as the 3\`end of the gene. The
    209757\_at reporter is the
    most informative here, and was also picked by the hugoonce
    algorithm, embedded in R2.
    For Affymetrix arrays a probeset by itself is a collection of
    separate 25-bp reporters. For Affymetrix arrays other then the
    Hu133-2 and Hu133-a platforms the reporters may vary in the number
    of basepairs. These measured
    regions are indicated in the reporter track by very dark shades.
    ****
    [![](_static/images/UsingR2genome_legend1.png)**Figure
    3: Legend of the color
    usage**](_static/images/UsingR2genome_legend1.png)
    [![](_static/images/UsingR2genome_tracks.png)**Figure
    4: Second half of the genome browser with
    default tracks.**](_static/images/UsingR2genome_tracks.png)
    With the default settings the genome browser shows the average
    expression signal per probeset for a chosen dataset with their
    genomic location.
3.  The properties and adjustable settings panel allows users to
    configure the graph display in various ways.. In the left properties
    panel set in the transcriptview section "draw mode to count and in
    the expression section "draw mode" to bars. The expression level can
    also be investigated per sample. The one-gene-view plot shows that
    ITCC0030 has no MYCN amplification resulting in low MYCN expression
    levels to illustrate this in the genome browser select in the
    "Adjustable Settings panel", ITCC0030. Click redraw.
4.  The picture now shows for one sample the expression levels for all
    MYCN probe sets in a more simplified fashion with barplots. Note the
    extra annotation tracks which were selected and hover over the
    tracks to reveal extra information.

[![](_static/images/UsingR2genome_settingspanel.png)**Figure
5: Adjustable settings
panel.**](_static/images/UsingR2genome_settingspanel.png)[![](_static/images/UsingR2genome_tracksadded.png)**Figure
6: Annotation tracks
added.**](_static/images/UsingR2genome_tracksadded.png)





Tutorial step 2
---------------

1.  The R2 Genome browser is a highly interactive application offering
    several ways to zoom and scroll the genome display. In the right
    upper corner of the screen search for the GTPBP8 gene click go and
    in the next screen choose "GTP-binding protein 8 isoform 1" by
    clicking on "VIEW".
2.  At some time it could be usefull to zoom into a location such as an
    aligned probeset. To quickly zoom into a specific region of interest
    user the browsers "drag and zoom" feature. At a desired position
    click and hold the left mouse button and drag the highlighted window
    to a second position and release the mouse button. The selected
    "white" region, can be repositioned (cross mouse indicator). A
    selection can be cancelled by clicking in the dark regions (Do note
    however that the positions of the selection were already adapted
    though ). Also in the track panel set "sequence and GC" windows
    to on. Click redraw in the middle panel.
    [![](_static/images/UsingR2genome_zoomcontrols.png)**Figure
    7: Zoom
    controls**](_static/images/UsingR2genome_zoomcontrols.png)
3.  At a larger magnification certain features such basepair pair
    coloring at the sequence annotation track may become visible. Note
    the black rectangles in the dark green exon region a collection of
    the probes which form together a probeset . Repeat the same drag and
    zoom procedure for one probe and click redraw.
    [![](_static/images/UsingR2genome_zoomgraph.png)**Figure
    8: Zoom-in
    graph**](_static/images/UsingR2genome_zoomgraph.png)
    [![](_static/images/UsingR2genome_basepair.png)**Figure
    9: Zoom revealing basepair
    sequence**](_static/images/UsingR2genome_basepair.png)
    Now the actual sequence is revealed a single affymetrix probe
    is matching. Clicking on the refseq bar will automatically zoom out
    to the genome browser representing the complete gene.
4.  Click on the "GET DNA" button to retrieve the DNA sequence directly
    from the UCSC database (keep in mind this option is available until
    the region of interest reaches a certain size)

+--------------------------------------------------------------------------+
| [![](_static/images/R2d2_logo.png)](Image:Image |
| :R2d2%20logo.png)***Did                                 |
| you know that the additional settings can be changed in "Tracks          |
| Panel".***                                                               |
+--------------------------------------------------------------------------+
| [![](http://ogtoolbox/w/index.php?oldid=150){width="150"}](_static/images/U |
| singR2genome_toolicon.png)                              |
|                                               |
|                                                                          |
| . Clicking on the tool icon unfolds extra options to configure your      |
| graph                                                                    |
|                                                                          |
|                                                                    |
+--------------------------------------------------------------------------+





Tutorial step 3
---------------



The Genome browser offers various options to zoom into a certain region.
In case there is an interest in gene expression levels of a certain
region on the chromosome. This can be quickly done by clicking on the
chromosome at a certain location.



1.  Click at a certain region on the chromosome and a new graph will be
    generated with average gene expression levels for the selected
    dataset in that region.
    [![](_static/images/UsingR2genome_Clicking.png)**Figure
    10: Chromosomal
    clicking**](_static/images/UsingR2genome_Clicking.png)
2.  Furthermore it"s worth mentioning that in order to use the genome
    browser it"s not necessary to do so via first selecting a dataset.
    The genome browser can directly be accessed from the main menu
    including many basic functionalities.





Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







Integrative Analyses I
======================



For some patients, R2 may have multiple types of measurements within the
platform. Provided that you have access to more than one datatype (for
public data, or when you are part of an r2 usergroup with restricted
data), then you are able to combine these directly from within the R2
platform. From R2"s perspective, an analysis where multiple datatypes
will be combined is an "across datasets" analysis, so we need to select
this from the main page in box 1. The easiest example of a combined
analysis would be to simply plot the contents of 2 different types
within a single plot. To do this, we select "view a gene in 2 datatypes"
and press "next". Since R2 needs to be instructed that overlapping
samples may be identified, we create so called collections, which list
datasets with overlapping patients. In this tutorial, we will make use
of a public cohort where both mRNA gene expression as well as Illumina
450k methylation bead chip data is available. Select "" from the
collection and click "next". Within the current screen you are able to
select 2 dataypes to plot against each other. In the current example,
only mRNA and Methylation data is available, and within these only 1
option can be selected. Please select the 2 datasets to combine,
indicate the gene or reporter that you would like to view for the 2
datasets separately (behind the dataset name) and press "next". We have
now selected the 2 datasets to combine. R2 will automatically identify
overlapping samples within the current selection and create "subsets"
for both datasets to only allow the overlapping samples for the plot.
Did you know that R2 will determine the overlap between datasets
automatically? R2 will scan for overlapping samples on the basis of the
r2\_samplename. Overlap is automatically determined and therefore can
also use cohorts that are not completely overlapping. R2 will simply
exclude samples that are only found in 1 of the datasets. In addition,
the order in which samples are represented is also accounted for. From
the perspective of both datasets we can now select the reporter to
represent the gene(s) that we indicated on the previous page.
Furthermore, we can select the transformation for both datasets and
continue to the actual plot. Press "next" to advance to the image. Did
you know that the annotation from both datasets is combined Within the
resulting image, annotation from both datasets is also combined.
Annotation is being merged on the basis of the name of a track. In a
perfect setting this would never result in conflicting data, however
sometimes it may happen that the different datasets contain a different
annotation. In that situation, R2 will concatenate both values by a
semicolon and thus create a new group identifier. If there is an obvious
mistake in one of the datasets, then we appreciate a message on this, so
that we can correct it accordingly. The image displays the correlation
between the 2 datatypes for those patients that were represented in both
data sets. From within this view we can adapt the visualization in a
couple of ways. When we look at the XY plot, we can annotate the graph
with a track distinction and color all of the circles accordingly. To
achieve this, simply select "color by track" and select the annotation
source to be used for the coloring. Once redrawn, this will also add
"boxplot" representations on the sides of the image to represent the
signals from both dataset perspectives. Alternatively, we can also
represent the image as a "YY" plot, where multiple annotations will be
represented underneath the imag. We can adapt this via the "graphtype"
selection. Next to simply "looking" at reporters from the different
datasets, we can also correlate 2 data types with each other. To achieve
this, we first go back to the "main" page by clicking on the upper left
link. We would now like to identify which gene has the best association
with its methylation status. Wherefore we need to correlate every gene
with the methylation probes that are in the annotated to belong to a
gene.



    Just like the previous example, we select "across datasets" in box 1 and now select "dataset extender (within genes)" in box 2. This will allow us to identify the best possible combinations where the expression of a gene correlates with the methylation status for the same gene.
    Again, we need to identify the collection within which R2 will look for the overlapping samples. Select "" and press "next".



On the current page, you can now select the parameters for the current
search. You can leave all as specified and advance to the next page. R2
will now perform the search for you. Do keep in mind that the across
dataset searches can be quite intensive as all genes are being
correlated to all methylation probes. For a simple setup like the
current one, more than 2 minutes will be needed to obtain the result. To
reduce the strain on the servers and speed up the serving of results, R2
will store the results of an analysis for a couple of days. If you are
lucky that someone else has performed the exact analysis that you are
interested in in the past few days, then R2 will serve those for you
(which reduces the search from 2 min to a mere couple of seconds). This
routine is used at multiple places within the platform.







Adapting R2 to your needs
=========================



*Or how you can optimize R2 for your specific data analysis*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   This tutorial describes the adaptable settings within R2. These are
    basically all items under the My Settings menu-item. Through these
    you can personalize the use of R2
-   First a couple of regular settings will be treated: changing colors,
    setting parameters
-   Next we'll delve into the practical adaptation of R2; uploading your
    dataset, adding your personal genesets (categories),
    creating/exporting /uploading your own tracks and maintaining a user
    community





Tutorial step 1
---------------

1.  Personalizing R2 starts with selecting the My Settings menu item
    (Figure 1). First item under there is the general 'My Settings';
    choose that.
    [![](_static/images/AdaptingR2_Mysettings.png)**Figure
    1: Personalizing R2: the My Settings
    menu-item**](_static/images/AdaptingR2_Mysettings.png)
2.  In the User Defined Settings window several parameters for analyses
    in R2 can be adapted to your preferences. For most analyses these
    are set to appropriate values, but of course you want to set your
    favorite dataset here!
    [![](_static/images/AdaptingR2_Userdefined.png)**Figure
    2: The User Defined Settings window; most parameters are
    appropriate; you want to change your preferential
    dataset however.**](_static/images/AdaptingR2_Userdefined.png)
3.  Next item in the My Settings submenu are the 'Megasampler Presets'
    (Figure 1), these are of relevance when you've built a specific
    Preset in an analysis Across Datasets. ( (chapter: Multiple datasets
    overview with Megasampler).
4.  The 'Upload New Dataset'-, 'Categories'-, 'Tracks'- and
    'Communities'-menu-items will be elaborated further upon later in
    this tutorial. The 'Timeseries colors' allows you to set the colors
    for the graphs of specific experiments in a series (Figure 3).

[![](_static/images/AdaptingR2_SettingsTime.png)**Figure
3: Setting time series
colors**](_static/images/AdaptingR2_SettingsTime.png)





Tutorial step 2
---------------

1.  The extensive functionality of R2 can be best experienced when you
    have your own data available. In order to do so it first has to be
    uploaded and processed. Click the Upload New Dataset (Figure 1), the
    upload form appears (Figure 4). This has to be filled out according
    to MIAME guidelines as (amongst others) used at the gene expression
    database GEO
    ([](http://www.ncbi.nlm.nih.gov/geo/info/MIAME.html)<http://www.ncbi.nlm.nih.gov/geo/info/MIAME.html>).
    If you have any specific annotations or wishes or microarray samples
    other than Affymetrix you'd best contact r2 support directly
    (<r2-support@amc.nl>). If you would like to see a publicly
    accessible dataset in R2, then send an email to <r2-support@amc.nl>
    with a link to the microarray data, or in the case of a Gene
    Expression Omnibus dataset, the GSE\*\*\*\* identifier, and we will
    take care of the rest and send a notification email.

[![](_static/images/AdaptingR2_DatasetUpload.png)**Figure
4: Dataset upload form in R2; fill out the form in a MIAME GEO compliant
way.**](_static/images/AdaptingR2_DatasetUpload.png)





Tutorial step 3
---------------

1.  Another way in which R2 can be adapted to your specific needs is by
    introducing your own set of genes, which are called categories in
    R2; hover over the 'Category'-item and select 'Build Category'
    (Figure 5)
    [![](_static/images/AdaptingR2_Categories.png)**Figure
    5: Categories related menu-items; select Build Category to make
    your own.**](_static/images/AdaptingR2_Categories.png)
2.  The 'Custom Category' window pops up (Figure 6). Default this is set
    to upload from a text file formatted as a single column of official
    gene symbols (obtained from NCBI gene). The uploaded data can be
    stored temporary (24 hrs) or in your personal tracks database. We're
    now going to use the input text field for data upload. Select the
    'Input Box' option in the 'how' dropdown box and select 'personal
    track' in the 'Where' dropdown.
    [![](_static/images/AdaptingR2_BuildingCategory.png)**Figure
    6: Building a Custom Category: Uploading
    a file.**](_static/images/AdaptingR2_BuildingCategory.png)
3.  The input box allows you to paste a bunch of genes to upload as a
    category for use in analyses in R2. In the example a set of genes,
    mutated in tumors are pasted. Selecting the 'personal track' option
    guarantees that this
    set will remain available for you (for people in your community, see
    later in this tutorial). Click "next" to upload the set (Figure 7),
    you'll receive a message when everything has succeeded. Your set of
    genes is now
    available as a Category for all analyses within R2. Go back to the
    main page to see where you can use this set.
    [![](_static/images/AdaptingR2_Inputbox.png)**Figure
    7: Using the Input Box to upload your category
    of genes.**](_static/images/AdaptingR2_Inputbox.png)
4.  We're going to lookup your category, an example is available in the
    GeneSet view. In the main menu in Field 3 select 'View a Geneset'
    and click "next"( Figure 8)
    [![](_static/images/AdaptingR2_Viewset.png)**Figure
    8: Using a category; select View
    Geneset**](_static/images/AdaptingR2_Viewset.png)
5.  In the GeneSetView your Category is privately available for yourself
    for similar analyses as with any other public geneset present in R2.
    Select My GeneCategories to choose from your categories (currently
    only one of course) \#: and click Next (Figure 9).
    [![](_static/images/AdaptingR2_Selectgeneset.png)**Figure
    9: Selecting your
    genecategories**](_static/images/AdaptingR2_Selectgeneset.png)
6.  In the next window you can specify which geneset you want to view.
    The Category 'Changed Genes' we just made above is now available
    (Figure 10). For now we end here, later on we'll see the category
    again in the context of \#:Tracks.
    [![](_static/images/AdaptingR2_YourGeneset.png)**Figure
    10: Your geneset is available
    as category.**](_static/images/AdaptingR2_YourGeneset.png)
7.  We now return to the My Settings menu to find out how we can manage
    the categories we just build. From the My Settings menu hover over
    'Categories' and click 'Manage Categories'.
    [![](_static/images/AdaptingR2_CategoryManager.png)**Figure
    11: The Category
    Manager**](_static/images/AdaptingR2_CategoryManager.png)
8.  The Category Manager (Figure 11) allows you to keep track of the
    categories; sets of genes you've stored within R2. Existing
    Categories can be adapted or deleted. New Categories can be based on
    existing ones, and to keep
    track of large amounts of categories these can be stored
    in collections. As an example we're going to update the Category we
    just made. Click the 'Copy/Delete/Rename/Edit Categories' button.
    [![](_static/images/AdaptingR2_Selectprocedure.png)**Figure
    12: Select the procedure for a Category; in this case
    'update**](_static/images/AdaptingR2_Selectprocedure.png)
9.  In the next screen you'll be asked what type of procedure is needed
    for your category of choice; in our case we want to keep the
    category and update it. Select it and click 'Execute'.
    [![](_static/images/AdaptingR2_AdaptCategory.png)**Figure
    13: The Category we just built can be adapted in
    all details.**](_static/images/AdaptingR2_AdaptCategory.png)
10. The details of the Category we built in the former steps are
    available for adaptation. In this way you can keep track and adapt
    the sets you use for your analyses





Tutorial step 4
---------------

1.  Another important feature in R2 that can be adapted to your needs is
    the Tracks feature. Tracks in R2 give you the opportunity to divide
    your samples in groups for further analysis. They can be created as
    a result of analyses within R2 and stored, or you can create them
    yourself based on sample characteristics. We'll first start with a
    K-means analysis that results in a division of the samples in two
    groups, for more about this analysis see the available tutorials on
    this subject) . On the main page of R2 select the K-means analysis
    in Field 3 (Figure 14)
    [![](_static/images/AdaptingR2_SelectKmeans.png)**Figure
    14: Selecting a K-means
    analysis**](_static/images/AdaptingR2_SelectKmeans.png)
2.  In the settings window for the K-means analysis (Figure 15) you can
    choose the Category created above to cluster the current set
    of samples. In our case this is called stud06-ChangedGenes. Set the
    number of draws to 10x10, click 'next'
    [![](_static/images/AdaptingR2_SelectOwnCat.png)**Figure
    15: Settings for K-means; the Category built above is available for
    clustering**](_static/images/AdaptingR2_SelectOwnCat.png)
3.  The resulting clustering in two groups might not be ultimately
    convincing (Figure 16), but for our testing purposes this
    is alright. What is important is that the resulting groups can be
    stored as a track; click the button 'store as a track'.
    [![](_static/images/AdaptingR2_UsestoredTrack.png)**Figure
    16: Clustering result of the Neuroblastoma dataset with the Category
    built in the former
    steps**](_static/images/AdaptingR2_UsestoredTrack.png)
4.  R2 now shows all samples as a long table with radio buttons
    indicating which group each sample belongs to. These can be adapted
    if you want to. Scroll down the window to find the fields that have
    to be set in order to store this as a track (Figure 17). You may
    want to change the group names into something more informative, and
    potentially also change the name to something you could easily
    relate to.
    [![](_static/images/AdaptingR2_DefineGroups.png)**Figure
    17: Storing the current groups as Track; Track name has been
    adapted, the track will be stored in our personal
    track database.**](_static/images/AdaptingR2_DefineGroups.png)
5.  Clicking the Build set button will store this as a track. In the
    custom tracks manager we can adapt this track again. From the My
    Settings menu select 'Manage Custom Tracks' (Figure 18).
    [![](_static/images/AdaptingR2_ManageCustomTracks.png)**Figure
    18: Selecting the Manage Custom
    Tracks**](_static/images/AdaptingR2_ManageCustomTracks.png)
6.  In the next screen keep the default selection; your current dataset.
    Tracks are, of course, defined based on a specific dataset; for each
    dataset you can store your own tracks. Click 'Continue'.
    [![](_static/images/AdaptingR2_DatasetTracks.png)**Figure
    19: Tracks are defined per dataset; keep the
    current selection.**](_static/images/AdaptingR2_DatasetTracks.png)
7.  In the next screen you're able to adapt the Track we just generated.
    Of interest in here is the option "drawtrack", which will result in
    the display of the information underneath the YY-plots. The tracks
    can also be assigned to collections to make large sets of
    tracks manageable. We leave the deletion of the track to the
    imagination of the reader. Now we'll pay attention to the default
    tracks for this dataset.
    [![](_static/images/AdaptingR2_AdaptTrack.png)**Figure
    20: The track we just generated can be adapted from here. For a
    start set the Drawtrack propery to 'yes'; we want to see this track
    in the graphs we
    create!**](_static/images/AdaptingR2_AdaptTrack.png)
8.  Select Manage Default Tracks from the My Settings menu (Figure 21)
    [![](_static/images/AdaptingR2_ManageDefaultTracks.png)**Figure
    21: Selecting the Default Tracks
    Manager**](_static/images/AdaptingR2_ManageDefaultTracks.png)
9.  In the next screen the dataset has to be defined; keep the defaults
    and click Continue. You'll end up in the Default Tracks Manager
    (Figure 22). Basically all annotation provided with this dataset is
    available as a track, we'll select the additional annotations of
    gender and recurrence as visible, they'll show up in
    further analyses. Be sure to click the 'Update Tracks' button for
    these changes to take effect. When collections of tracks are used
    these we'll show up conveniently as separate groups of tracks under
    the graph.
    [![](_static/images/AdaptingR2_SelectDefault.png)**Figure
    22: Selecting the default tracks for this
    dataset**](_static/images/AdaptingR2_SelectDefault.png)





Tutorial step 5
---------------

1.  R2 also allows you to build your own tracks from scratch. You'll be
    able to assign each sample to a group of your choice. To illustrate
    this select 'Build Custom Track' in 'My Settings' (Figure 21). The
    Custom Track window appears. R2 also provides the possibility to
    upload a custom track from a prefab text file; we'll shortly show
    this; click 'Upload a Track' (Figure 23).
    [![](_static/images/AdaptingR2_UploadTrack.png)**Figure
    23: The Custom Track dataset
    choice window.**](_static/images/AdaptingR2_UploadTrack.png)
2.  In the Upload Custom Track window you can either select a tab
    delimited txt file built with a tool like Excel, or alternatively
    paste tab or semicolon delimited text in the paste-box; that
    provides R2 with the proper assignment of each sample to a
    specific value. Based on that, R2 creates the groups for you. Using
    this procedure you can create tracks with as many groups as
    you like. If you intend to create a track with a limited number of
    groups, then an easier way is provided through the user interface,
    which we will now try. Click back button in your browser to return
    to Figure 23
    [![](_static/images/AdaptingR2_Trackdescribed.png)**Figure
    24: Uploading a track described in a text file; for each sample a
    description has to
    be provided.**](_static/images/AdaptingR2_Trackdescribed.png)
3.  In the Custom Track window(Figure 23) the number of groups desired
    has to be given in advance. We try 3. The Gene/PS option allows you
    to order the samples based on the expression of a gene, and make
    sub-groups that range in expression. Leave that field open and click
    Submit
4.  In the next window a convenient grouping of all annotation
    parameters and there values is available to create groups. In this
    example we select the low grade(1,2,3) vs high grade(4) vs
    special (4s) tumor types in the Neuroblastoma dataset as known from
    the INSS classification. Tick the appropriate boxes in the
    appropriate group columns. It is also convenient to recapitulate the
    resulting groups in a separate column so tick that box also
    (Figure 25).
    [![](_static/images/AdaptingR2_DefineGroupsSpecs.png)**Figure
    25: In the inss row the stage 1-2-3 tumors are selected to form
    group 1, stage 4 forms group 2 and stage 4s group 3 in a
    new track.**](_static/images/AdaptingR2_DefineGroupsSpecs.png)
5.  Click "next", all samples appear in a table with check boxes to
    assign them to the appropriate group. Scroll down to create the
    annotation for these groups (). Names have been adapted, show track
    is set to yes, the track is set to be stored a personal track and
    colors per group have been adapted. Click 'Build set' to store the
    set, you'll receive a message accordingly in the next window. Of
    course you now finally want to see all our track manipulation in an
    actual graph. Go to the R2 main page again to see how the data of a
    gene will be plotted using the new tracks.
    [![](_static/images/AdaptingR2_Trackproperties.png)**Figure
    26: Setting the custom
    track properties.**](_static/images/AdaptingR2_Trackproperties.png)
6.  Select View a gene in groups in Field 3 of the main page, type MYCN
    as gene name in Field 4 (Figure 27). Click 'next'.
    [![](_static/images/AdaptingR2_ViewTrack.png)**Figure
    27: Selecting a gene to view in the newly
    created tracks.**](_static/images/AdaptingR2_ViewTrack.png)
7.  The track created in the Custom Track manager is available for
    selection: u-lowgradvs4vs4s. Note that the other Track created in
    the K-means analysis, is also available here. Choose it and
    click 'Next'.
    [![](_static/images/AdaptingR2_Selectowntrack.png)**Figure
    28: Select the Track created in the Custom track manager;
    u-lowgradvs4vs4s**](_static/images/AdaptingR2_Selectowntrack.png)
8.  The different groups we created as part of our track in the previous
    steps are available for selection. We want to see them all, keep the
    settings and click 'Next'.
    [![](_static/images/AdaptingR2_Trackgroups.png)**Figure
    29: The groups created in the track are available for
    selection**](_static/images/AdaptingR2_Trackgroups.png)
9.  The expression of MYCN is plotted in the different groups of the
    track that was created (Figure 30). Note that the other track of
    mutated genes has a large overlap with the stage 4 group. There is
    also overlap with the "recurrence\_or\_progression" Default Track
    that we set to visible.
    [![](_static/images/AdaptingR2_VisualizeTracks.png)**Figure
    30: Tracks created are visualized underneath the
    graph**](_static/images/AdaptingR2_VisualizeTracks.png)
10. Another convenient option from the "custom track manager" is the
    export function which enables you to manipulate your tracks manually
    outside R2. This could be of use when your want to share tracks with
    other users or create new custom tracks. One reason you want to use
    the export function is to fix the ordering of your sample when
    generating a heatmap (see Error: Reference source not found) . Make
    sure you already have a personal custom track (Not a temporary
    track, 24h ). Select Manage default Tracks from the My Settings menu
    (Figure 21) and click next. Here select the dataset of interest ,
    only datasets which have a corresponding personalized track are
    represented in the pulldown menu. Click the
    "Copy/delete/rename/export Tracks" button. Here select the personal
    track , "export" operation and r2\_track at "export as" . Click
    execute" and download link with the track name can be loaded by
    clicking the right mouse button.





Tutorial step 6
---------------

1.  Cooperation is of great importance in scientific research. You
    probably want to share the tracks created above with other people in
    your group. For this reason R2 features the Communities. Creating a
    community is done by clicking 'Community' in the 'My Settings' menu
    (Figure 31).
    [![](_static/images/AdaptingR2_Community.png)**Figure
    31: Community in the My Settings
    menu**](_static/images/AdaptingR2_Community.png)
2.  Since this will be the first time in the community section, there
    are no communities yet; click the 'Start a new Community' link
    (Figure 32).
    [![](_static/images/AdaptingR2_StartCommunity.png)**Figure
    32: Starting a
    community**](_static/images/AdaptingR2_StartCommunity.png)
3.  In the Community window a name has to be set and a short description
    for people invited as members for this group (Figure 33). Through a
    community you can share GeneCategories, Tracks and Settings.
    [![](_static/images/AdaptingR2_SettingCommunitygroup.png)**Figure
    33: Setting the Community group name
    and description.**](_static/images/AdaptingR2_SettingCommunitygroup.png)
4.  Click 'Next'; you'll be notified that the group has been created;
    return to the Communities Center by clicking the Community link
    again in the My Settings menu (Figure 31). The TestGroup has been
    created (next to the already existing MyTestGroup for this user).
    Click the link to start adding users (Figure 34).
    [![](_static/images/AdaptingR2_Availablegroups.png)*Figure
    34: The available Communities for
    this user.*'](_static/images/AdaptingR2_Availablegroups.png)
5.  You have to add users by their R2 username; we'll add
    user "pietmolenaar". He'll receive a message in the R2 startup page
    as soon as he logs on the next time. Click "next" to add the user.
    [![](_static/images/AdaptingR2_GroupManager.png)**'Figure
    35: Add a user by their R2 user
    name**](_static/images/AdaptingR2_GroupManager.png)
6.  R2 returns with a message that the user has been invited, he or she
    has to accept your invitation first before he will see what you
    are sharing.
    [![](_static/images/AdaptingR2_Managegroups.png)**Figure
    36: R2 return message; user is invited; but not yet
    visible**](_static/images/AdaptingR2_Managegroups.png)
7.  The perspective of the invited user after logon; he or she can
    accept the invitation (Figure 37).
    [![](_static/images/AdaptingR2_GroupInvitation.png)**'Figure
    37: The invited user receives a notification on the main page where
    he or she can accept the membership of the
    group**](_static/images/AdaptingR2_GroupInvitation.png)
8.  When the invitation has been accepted the user is available in
    this community. When we add a category, track or preset the next
    time, it is possible to make this available to this community.
    [![](_static/images/AdaptingR2_CommunityUsers.png)**Figure
    38: The user is available in
    the TestGroup.**](_static/images/AdaptingR2_CommunityUsers.png)
9.  When a Category is created there is now a possibility to make it
    available to a Community (Figure 39)
10. Managing the tracks, gene categories and megasampler presets is done
    in a similar way as has been shown in the user tracks and user
    categories at the beginning of this tutorial. pietmolenaar, as a
    member of this group, can manage the tracks that have been shared
    with him via his default track manager
    [![](_static/images/AdaptingR2_CommunityCategory.png)**Figure
    39: As an example here the creation of a category and the assignment
    to
    a Community.**](_static/images/AdaptingR2_CommunityCategory.png)





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,The R2 support team.









Exporting data
==============



*Export (filtered) normalized data for additional analysis outside of
R2*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Export expression data with the "Data Grabber" functionality
    directly from the main menu
-   Export expression data in R2 after an analysis.





Tutorial step 1
---------------





1.  In the main menu select "Tools" &gt; "Data Grabber". A dropdown menu
    appears from where you can select the dataset of interest and
    click "next".
    [![](_static/images/ExportData_datagrabber.png)**Figure
    1: In the main menu "Data
    Grabber**](_static/images/ExportData_datagrabber.png)
2.  A settings menu appears where several filter options can be applied
    to the data you want to export. You may optionally select a
    track (subset) to filter the samples by the annotated groups; in
    this example select "inss (cat)" and select one or more stage(s). Be
    sure to click the red "**confirm"** link to enforce your selection
    before proceeding.
3.  In the "reporters" section, by default, a specific set of reporters
    (either reporter names or genesymbols) can be selected via
    copy/paste a set of genes in the "input\_identifiers" box. Another
    option for the reporter selection would be the "HugoOnce", where
    only a single reporter is chosen for all of the genes annotated
    within the dataset, and where orphan reporters are omitted. In this
    example we are interested to perform an additional analysis outside
    R2 with all reporters for several stages. In the menu select
    "HugoOnce" and click "next".
    [![](_static/images/ExportData_filter.png)**Figure
    2: Filter options for
    exporting data.**](_static/images/ExportData_filter.png)



A "datagrabber.txt" hyperlink is generated on the fly and appears on
your screen. Right-click the link and store the tab delimited file with
expression data on your hard drive. In case a dataset contains more than
60.000 reporters, then R2 only allows up to 60.000 reporters to be
exported, due to the large file-sizes which would have to be created.
You may always drop r2-support a note, if you require these large
amounts, and we will dispatch those via other means.







Tutorial step 2.
----------------



The example listed above shows that R2 facilitates the export of data
without performing any analysis. Of course you may want to do the same
after analyzing data in R2. In most of the analyses options you can
export the data via the right menu.



1.  To illustrate this option. Select in the main screen in box 3 "Find
    Correlated genes with a single gene".
2.  Type "MYCN" in box and click "next", in the next screen leave all
    the selection criteria at their default settings and click "next".
3.  A list of genes significantly correlating (up and down) with the
    MYCN gene is generated. The right menu provides you with a set of
    options to continue your analysis including exporting data.
    [![](_static/images/ExportData_menu.png)**Figure
    3: Continuing
    your analysis.**](_static/images/ExportData_menu.png)
4.  Click on "MakeMeATable (TMEV) ready" in a new (tab) screen you can
    download the table matrix with the corresponding annotation by using
    the right click of your mouse. The generated table can be used
    directly in external programs such as the commonly used clustering
    program as the TIGR Multi experiment viewer (TMEV) which is
    freely available.
5.  Try also the other options listed in this menu, "save current ".",
    "reference for "" and "Store results ". These are all different
    formats to export your results for use outside R2 or store in R2 to
    continue your analyses at a later time-point.

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can export data from different types of modules?***
  Using a different module such as "Time Series" also provides the option to export the results of use outside R2 or at a later time point within R2.
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



Note: If the requested file size exceeds \~200MB, R2 will terminate the
request because of the system load. Or course there is a workaround by
mailing the r2-support@amc.nl and request for the dataset expression
values of interest.







Final remarks / future directions
---------------------------------

We hope that this tutorial has been helpful,The R2 support team.







R2 Dataset Addition
===================



*How to add your own or publicly available datasets for analysis in R2*





**[Back to the list of
tutorials](http://ogtoolbox/w/index.php?title=R2_Wiki_Tutorials)**





Scope
-----

-   Learn how to add your own datasets to R2
-   Have datasets added that are published in literature.





What to prepare when you would like to have a dataset added
-----------------------------------------------------------



R2 allows users / groups to have their own (private) human / mouse
datasets added to the platform, which enable them to analyze their own
data from anywhere in the world, as long as they have access to the
internet. Such datasets can be added with various access policies,
ranging from public to restricted to a single user. The current document
describes all that you need to know about the addition of datasets in
R2, and will also show you how files should be prepared.







Who can add datasets to R2
--------------------------



Most often, users would like to analyze their data, in combination with
datasets already present in the R2 database. For example, one would like
to compare the extend of expression, compared to other tissues (the so
called MegaSampler). One can imagine that such analyses require
identical processing for all datasets of the same platform (provided
that the normalization scheme supports this). For that reason, we have
decided that only administrators of the R2 platform can add new
datasets, since they understand the R2 platform architecture and can
supervise / guide the upload procedure.







Addition of a public dataset from the GEO database
--------------------------------------------------



Having a public dataset added to R2 from the NCBI GEO database is by far
the easiest. Depending a bit on whether the array platform is already
used within R2, such datasets can be added fairly quickly. In most cases
you only have to send an email to <r2-support@amc.uva.nl> stating the
GEO series identifier GSE\*\*\*\*\* and one of the administrators will
take care of the rest. One note for your consideration though. Since the
R2 platform has initially been designed to work with Affymetrix
microarrays, it works best with single channel platforms. We do also
incorporate dual channel datasets, but always warn for potentially
unwanted behavior. For the addition of Affymetrix datasets, we
preferably would like to be able to work with the raw data (CEL files),
so please make sure that those are attached in the GEO series.





The GEO database can be browsed from
[](http://www.ncbi.nlm.nih.gov/geo/browse/?view=series)<http://www.ncbi.nlm.nih.gov/geo/browse/?view=series>







Addition of personal datasets
-----------------------------



Within R2, we also house datasets that are provided by authors which are
not (yet) available in the public domain. In some cases these are made
publicly available, but most often, some form of restricted access in
enforced on them.







Access levels
-------------



R2 can provide access to datasets on a number of levels. The default
access model provides public access to a dataset to anybody using R2.
Within R2, datasets can also be made accessible to a group of users.
Such a construction is ideal for departments where more people want to
make use of the information. Also consortia can make use of this access
model. Finally, datasets can also be made accessible to single users. In
all of the cases where restricted access is involved, users should
create a (free) personal account for R2, and be granted access by an R2
administrator. Requests for access to a group should be send by the
owner of a group, or such an owner should at least be cc-ed in the email
correspondence. Additional owners of a group or transfer of the
ownership to another person can be done achieved by email to
<r2-support@amc.uva.nl> from the current owner. If your research group
already has data in R2, then you should already know the name of your
user-group.







Preparing the expression data
-----------------------------



When the data to be uploaded originates from Affymetrix gene expression
platforms, and you would like to have the data added in the standard
way, then we prefer to have the original CEL files send to us by
[www.wetransfer.com](http://www.wetransfer.com) or a
similar service. We can then add the dataset in such a way that it can
be used in conjunction with the publicly available datasets from the
same platform and normalization scheme. If normalization schemes, other
than the mainstream MAS5.0, RMA, gcRMA, or RMA-sketch are preferred,
then you should perform the normalization yourself and send us the
normalized data as a matrix (like a tab delimited export from an Excel
sheet). A data matrix should be constructed in the following manner: the
first row is considered to be the header and should preferably start
with the following sign \#H: for the 1^st^ column. The 1^st^ column
should contain the reporter IDs of the platform (such as probe sets, in
the case of Affymetrix). If you are not sure which column represents the
reporters that can be used in R2, then please ask by email (Especially
Illumina arrays contain a number of fields that look usable). The signal
values (preferably non-transformed) of the samples can then be added in
subsequent columns, where the 1^st^ row should contain the sample
identifier (that needs to be identical to the sample identifier in the
annotation file). R2 can perform a range of transformations (such as
log2) on the data itself, thereby allowing the most flexible use of your
expression data, if provided in a non-transformed fashion. The figure
below shows an example for an Affymetrix array.



[![](_static/images/DataSetAddition_table.png)**Figure
1: Example**](_static/images/DataSetAddition_table.png)


A number of platforms and/or normalizations not only provide a signal
intensity, but can also express the likelihood that a reporter is
considered expressed (like present calls or detection p-values for
Affymetrix U\*\* platforms). Such information may be provided in the
matrix file by addition of an additional column (then named
sample\_pval). Alternatively, every sample may be provided in a separate
tab delimited text document, where multiple columns can then be provided
for a sample.







Preparing the gene annotation
-----------------------------



If a platform has already been added to the R2 database, then there is
no need to supply gene annotation again. If a new platform has to be
added, then we require at the very least a list of all the reporters,
together with their mapping to the genome (for human preferably
HG18/NCBI36; for mouse preferably mm9). Furthermore, the relation
between reporters and genesymbols as well as gene ids (NCBI Gene) would
speed up the process of adding a new platform. In many cases, vendors of
the arrays make annotation files available for download. Usually a link
to such an annotation will also be sufficient. In case of doubt, please
contact us by email.







Preparing the sample annotation
-------------------------------



Expression data is not very useful without proper annotation. Annotation
is provided in a separate tab delimited text file. Here the 1^st^ column
contains the sample names and any subsequent column is treated as an
annotation field (termed tracks within R2). Please refrain from using
special characters within the annotation. Also, spaces in track naming
should be avoided (use \_ instead). An example of an annotation file can
be seen in the image below. You can add as many tracks as you like /
find useful. There are a number of special tracks, which you can make
use of, which will now be described.



[![](_static/images/DataSetAddition_sampleanno.png)**Figure
2: Example
2**](_static/images/DataSetAddition_sampleanno.png)


Besides providing the annotation for usage in R2, you can also specify
how R2 makes use of these annotations, specifically in graphical
representations. To make this known, you can prepare a "relate" file for
R2. This document comprises of a number of columns that can be provided
for the different tracks. Below, you can see a section of such a relate
file.



[![](_static/images/DataSetAddition_relatefile.png)**Figure
3: Example
2**](_static/images/DataSetAddition_relatefile.png)


Please make sure that the header of the relate file is identical to the
example, and that the tracknames match to the ones that have been
defined in the sample annotation. The "istrack" column tells R2 whether
the annotation needs to be drawn as color coded information below
YY-plots, and headers of heatmaps. The "isinfo" column defines whether
the information is displayed in the table once you hover over a sample
in graphs within R2. "visible" can enable/disable the use of a track.
The "color" column can preset a specific color to groups which are
defined within a track. These can be indicated by groupname:hexcolor.
The different groups are then separated by the ";" sign. It is not
required to supply this information. R2 will color groupnames
automatically if such information information is not encountered.
Finally, you may describe the contents of a track.





### Special sample annotation



Within R2, some well-defined sample annotation labels and/or additional
files, enable additional functionalities. Below, an example is described
for both.





**Survival information:** When the dataset contains survival
information, then R2 can make use of this to draw Kaplan Meier plots. To
do so, R2 requires a separate tab delimited text document with a
strictly defined header and some rules. Any line starting with \# is
considered comments, and will be excluded. There is 1 exception to this
rule, which if formed by the \#H: combination, which will be interpreted
as a header row. A survival file should contain a header line that is
identical to the example given below, as R2 will then recognize it as
such. How an event is defined, may differ (overall / relapsefree etc).
This can be expressed in the name of the file that is being provided.
For example, the file below would be named "overall.txt". Subsequent
Kaplan curves would get the name "overall survival" on the y-axis.



[![](_static/images/DataSetAddition_survival.png)**Figure
3: Example
3**](_static/images/DataSetAddition_survival.png)


**Time series graphs:** When the samples are annotated with the
appropriate tracks, then R2 can also present datasets as time series.
When R2 encounters a column named "r2\_ts\_timepoint", combined with
either "r2\_ts\_profile" and/or "r2\_ts\_series", then this will enable
the option to represent the dataset as a time series (where
samples/groups are connected by a line following the time variable).
Profiles are intended to connect a single experiment or the following of
a single subject in time. Series are intended as the grouping of
profiles (for example biological replicates of an experiment), which
will also create error bars on the measurements. The "r2\_ts\_timepoint"
annotation should only contain numerical information (the time, in
whatever scale you prefer (minutes / hours / days)). The other 1 or 2
annotations should provide a grouping label (which would be useful for
you). In case of doubt on the usage of these annotations, do not
hesitate to get in contact with us via r2-support.



[![](_static/images/DataSetAddition_timeserie.png)**Figure
4: Example
4**](_static/images/DataSetAddition_timeserie.png)







Describing your dataset
-----------------------



Within R2, your dataset will get a name, so that you can find it back
for analyses. For dataset naming the program makes use of a small number
of parts (some of which can be influenced by you). For example, the
department of oncogenomics has made its Neuroblastoma dataset available
in R2 with the following name "Tumor Neuroblastoma public - Versteeg -
88 - MAS5.0 - u133p2". The naming is achieved by the following parts:





1\. **Dataset Class**. For Human datasets, one can choose from the
classes defined in the table below.



+--------------------------------------+--------------------------------------+
| **Class**                            |           |
|                                      |                                      |
|                                      | **Description**                      |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Cellline**                         |           |
|                                      |                                      |
|                                      | Usually used for cell line panels,   |
|                                      | where no intervention was applied    |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Disease**                          |           |
|                                      |                                      |
|                                      | Datasets, where a specific disease   |
|                                      | has been investigated, other than    |
|                                      | cancer                               |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Exp**                              |           |
|                                      |                                      |
|                                      | Experiment datasets. Usually cell    |
|                                      | line models in which interventions   |
|                                      | have been applied (Gene              |
|                                      | transfection, rna interference etc)  |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Mixed**                            |           |
|                                      |                                      |
|                                      | If a dataset makes used of multiple  |
|                                      | items, then it becomes a mixed set   |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Normal**                           |           |
|                                      |                                      |
|                                      | The profiling of healthy normal      |
|                                      | material                             |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+
| **Tumor**                            |           |
|                                      |                                      |
|                                      | Datasets which are composed of a     |
|                                      | specific tumor type belong in this   |
|                                      | category                             |
|                                      |                                      |
|                                      |                                |
+--------------------------------------+--------------------------------------+



2\. **Tissue**. Depending a little on the choice of class, usually a
description of the tissue / tumor is given in the second part. In the
example, this was "Neuroblastoma", but this could also be "Breast" or
"Colon" if such a dataset was described. For experiments, the tissue or
tumor type is also often described, to make sure that datasets with the
same theme are close together. If we would describe the shRNA knockdown
of the MYCN gene in the neuroblastoma cell line IMR32 for example, then
this would become "Exp Neuroblastoma IMR32 MYCN shRNA".





3\. **Author**. Finally, you can supply the author / consortium in naming
your dataset. This should be self-explanatory.





R2 will add the number of samples within the dataset, a normalization
scheme and finally also a code representing the platform which has been
used. If you are supplying a dataset other than Affymetrix gene
expression arrays (Exon or U\*\*\*), then you should provide us with the
normalization, and platform used as well. The platform, doesn"t have to
be the code that R2 uses, but can also be described by the manufacturer
and the array ID.





Optionally, you can also describe your dataset in more detail in the
following fields (which are also shown if you click on the "i" image
next to a dataset). **Title**: 1 line description of your dataset.
**Summary**: free text option to describe your dataset in as much detail
as you wish (See also GEO for examples). **Design**: free text
describing the design of your dataset (See also GEO for examples).





We hope that this document has been helpful in preparing your dataset
for inclusion in R2,





R2 support (<r2-support@amc.uva.nl>).








