<a id="one_gene_view"> </a>

One Gene View
=============

*Analyze the expression levels of a single gene within a dataset*


Scope
-----

-   Use R2 to investigate the expression levels of all samples from a
    specific dataset.
-   In this example the expression levels of the MYCN gene will be used.
-   Adjust several parameters in the advanced settings panel to get a
    better insight in the expressions levels or adapt your
    graphic layout.
-   In R2, the samples are annotated with e.g clinical data, each group
    of annotated data is called a “Track” in R2. These tracks can be
    used to filter data in all types of analyses R2 is offering.
-   A separated info panel in the one-gene expression level screen
    provides different types of analyses based on the expression level
    of the chosen gene.
-   Most of the mRNA expression datasets are generated with Affymetrix
    profiling arrays. In general these arrays use more than one so
    called probeset to measure the expression level of one single gene.
    With a separated module “Transcript view”, the details of the
    probesets can be studied.





Step 1: Selecting a gene
---------------

1.  Use “Single Dataset” in field 1 and make sure that the “Tumor
    Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2” dataset is
    selected in field 2.
2.  Choose “View a gene” in field 3 and click next.


![](_static/images/Onegeneview/OneGene_singleselect_v2.png "Figure 1: Single gene selection")

[**Figure 1: Single gene selection**](_static/images/Onegeneview/OneGene_singleselect_v2.png)



Step 2: Probesets for a gene
---------------

1. In many cases more than one probeset is reported for each gene. In
   this example, there are multiple probesets are annotated for the MYCN gene. By
   default, the probeset with the highest average present signal (APS)
   is selected. This APS signal is simply the average of all samples
   that are considered to express a selected gene (have a
   present call). After you entered the mycn gene clicking the reporter ID  will be listed in the right search box.
   Occasionally other probesets assigned to the same  gene could be of interest depending on the structure of the gene
   (for example a potential splice variant). Also realize that the most
   informative probeset is re-determined in every dataset, sometimes
   resulting in a different probeset as the choice of R2. The
   expression levels of datasets are by default 
   converted to log2 values. This does not count for datasets that contain ratio's or logfolds. Clicking the advanced button provided a grid
   where more selection criteria such as gene id, average levels can be can be applied. Also the last column named "R2 default" indicates if a
   whether a gene identifier is considered to be significant expressed (TRUE) or  not (FALSE) this information is not available for each dataset in R2.
   
   ![](_static/images/Onegeneview/OneGene_multipleprobegrid.png "Figure 2: By default the probeset with the highest expression level is selected")
   
   [**Figure 2: By default the probeset with the highest expression level is selected**](_static/images/Onegeneview/OneGene_multipleprobegrid.png)

2. In the adjustable settings screen, use the pre-defined default
   settings and click ‘Next’.
   



Step 3: Plotting Gene expression 
---------------

1. R2 generates a YY-graph (Figure 3) from the MYCN expression levels of
   all samples with expression levels ordered from left (low) to
   right (high). Hovering over the dots reveals additional annotation
   that R2 has stored for the focused sample.
   
   ![](_static/images/Onegeneview/OneGene_MYCN.png "Figure 3: YY plot MYCN expression")

   [**Figure 3: YY plot MYCN expression**](_static/images/Onegeneview/OneGene_MYCN.png)


2. Underneath the X-axis, colored boxes are depicted, representing
   clinical information of the samples in so called "tracks". Again,
   hovering over them will reveal underlying data. For MYCN there is a
   clear relation between the expression levels and the tracks for
   “MYCN amplification” and “INSS-stage“. So these tracks underneath
   the image give a quick glance at some of the clinical parameters,
   defined for the dataset. It is also possible to define your own
   custom made tracks, or disable/adapt the settings for default tracks
   (further explained in “Adapting R2 to your needs")

3. Sometimes you get more insight by reviewing the expression levels
   with other transformations. Scroll down and transform the data
   (Figure 5), choosing “none”, in the ‘transformation’ pulldown menu
   and click adjust settings. In the “adjustable settings” panel, there
   are several other settings to adapt the graph R2 generates (like
   changing font sizes, or adding labels to the datapoints). 

----------
  ![](_static/images/R2d2_logo.png)**Did you know that the Adjustable Settings panel is available under most graphs in R2?**

> *Just scroll down the page to find the Adjustable Settings box with graph options. Don't forget to press the "Adjust Settings" button at the bottom of the box in order for your changes to take effect!*

----------

In adjustable settings many settings adapeted a two geneview can be applied directly from the onegene view adjustable settings menu.
To highlight / mark specific samples in the graph you can enter the R2 sample ID’s in the field 'samples to mark' from the
‘adjustable settings’ box or by double-clicking on a sample. Several marking options can be selected with the 'Mark method' that can be found in the 'More settings' tab (e.g: ‘epicenter’ and ‘arrow’).

![](_static/images/Onegeneview/OneGene_adjustablesettings_v1.png "Figure 4: Adjusting the graph settings")

[**Figure 4: Adjusting the graph settings**](_static/images/Onegeneview/OneGene_adjustablesettings_v1.png)

---------------
 ![](_static/images/R2d2_logo.png)**Did you know that R2 allows you to emphasize samples with marker options?** 

> *R2 knows a couple of mark options, that you can make use of in the advanced prescriptions:* 
> - *'dot': places a thick border around the sample*
> - *'circle': Places a ring around the sample (diameter 9)*
> - *'circle_2': Places a ring around the sample (diameter 4)*
> - *'circle_3': Places a ring around the sample (diameter 1), effectively a thin border*
> - *'epicenter': Places a set of 3 rings descending in width around a sample*
> - *'arrow': Places a block arrow pointing to the sample*
> - *'triangle': Places a filled triangle under the sample*
>
>*Note: The dotsize does not scale with 'arrow' and 'triangle' method.*
---------------

Multiple colors and different markings can be applied to the individual samples you want to highlight. To bring attention to different samples, you may want to use multiple colors and types of marking. In order to do so define the method within the ‘samples to mark’ box by adding another ‘:’ after the color representation. Defining this will overrule the default setting, and thus also enable the use of different markings within the same figure. The skeleton for advanced usage is: ‘sample1,sample2:color1:method1;sample3,sample4:color2:method2’. For example: ‘“itcc0288:ff4444:dot;itcc0021:009999:arrow;itcc0013,itcc0132:00ff00:epicenter”’ creates the markings as shown in the figure below.

![](_static/images/Onegeneview/OneGene_view_samplesmark.png "Figure 5: Adjusting the graph settings")

[**Figure 5: Adjusting the sample mark layout**](_static/images/Onegeneview/OneGene_view_samplesmark.png)

---------------
 ![](_static/images/R2d2_logo.png)**Did you know that converting expression levels using the “transform” option can help you to gain additional insight?**                              

> *There are several data transformations available*                         
>  -   *“none”: Raw untransformed expression values, as they are represented 
>        in the R2 database.*                                                  
>  -   *“2log”: logarithmic values with base of 2. Every increment           
>        constitutes twice the amount.*                                        
>  -   *“rank”: Data transformation in which numerical or ordinal values are 
>        replaced by their rank when the data are sorted by expression. This  
>        transformation is useful for non-parametric statistical tests.*       
>  -   *“zscore”: 2log transformed data, centered around the average and     
>        expressed as the number of standard deviations from the average.*     
>  -   *“zscore\_nonlog”: raw intensity values, centered around the average  
>        and expressed as the number of standard deviations from the average. This transformation is 	 useful when the intensities in R2 are not raw, but for example logfolds as is often the 	 	 case for aCGH data.*    
>  -   *“mad/mad2log”: Median absolute deviation (on raw values, or log2     
>        transformed values).*                                                 
>  -   *“center/log2center”: Expression values centered around 0 (on raw     
>        values, or log2 transformed values).*                                 
>  -   *“zcore\_group”: Coverts the expression levels from the zscore within 
>        a group (track). Applicable when e.g technical variation in          
>        expression levels is expected. A possible reason could be when       
>        samples from the same dataset originate from different centers.*      



Another often requested feature is the svg ca


---------------

Step 4: Probeset verification
---------------


Figure 6 lists for the various reporters of MYCN whether they are in
agreement with the genome position of MYCN reference sequence (RefSeq).
If all are stating “YES” then everything appears alright (from the
perspective of an automated assessment). For the MYCN reporters “NO”
indications indicate there may be an issue with it. Scroll down the page
and click on the “Tview” link in the reporter table.


![](_static/images/Onegeneview/OneGene_Probesettable.png "Figure 6: Probeset verification table")

[**Figure 6: Probeset verification table**](_static/images/Onegeneview/OneGene_Probesettable.png)

1.  A new screen (or tab in the browser) appears with TranscriptView.
    The TranscriptView application depicts the alignment of expressed
    sequence tags (EST) and mRNA sequences to the human reference genome
    sequence (Fig 8. The strand orientation of these sequences are
    indicated by a color (green = positive strand, red = negative
    strand, blue = strand information is missing). The structure of the
    reference sequence has also been indicated. Furtermore, the browser shows the alignement of the sequences that were used to generate the reporters on the array (in the case of Affymetrix microarrays).  
    This view can be used to inspect the quality of a reporter. Note, for instance, that the reporter
    “242026\_at” is aligned to the genomic region of the MYCN reference
    sequence, but that it’s color is different from the rest (colored
    in red). In addition, in this particular case the reporter is 
    located in the intronic (light shaded color) region which is another
    reason not to pick a certain probeset. Indeed, if we compare the
    gene expression values of this reporter, then its expression is 60
    fold lower than R2's standard pick (22 vs 1369). Below the ESTs the
    average gene expression of the individual probesets is illustrating
    that for this example the correct probeset is selected for analysis.
    NB: Currently probeset verification is only provided for various
    human Affymetrix array types.


![](_static/images/OneGene_Colorlegend.png "Figure 7 Color ")

[**Figure 7: Coloring represents type of transcript**](_static/images/OneGene_Colorlegend.png)


![](_static/images/OneGene_Tview.png "Figure 8 MYCN reporters in Transcript view")

[**Figure 8: MYCN reporters in Transcript view**](_static/images/OneGene_Tview.png)



---------------
  ![](_static/images/R2d2_logo.png)**Did you know that you can browse the gene expression values along the genome?**

> *Once you have entered the genome browser with an attached dataset (like above), you can also navigate to / zoom out any other region in the genome. This allows you to look at the neighboring genes in a single go.
>   It can be informative to separate the expression on the basis of a track. This can be achieved by selecting 'dataset\_track' from the sample dropdown in the middle panel. Finally, within the genome browser, the contents for a panel on the left side can be hidden from a view by setting the height to 0.*

---------------


Step 5: Sources for additional information on the selected gene 
----------------

1. Close the Genome Browser tab or go back to the MYCN One Gene View expression screen.

   ![](_static/images/OneGene_menupanel.png "Figure 9:Left menu panel providing additional info (including link-out) andanalyses options")

   [**Figure 9:Left menu panel providing additional info (including link-out) and analyses options**](_static/images/OneGene_menupanel.png)


In the left upper menu-panel several options are available to provide
you with additional information sources of the MYCN gene and additional
analyses. KaplanScan and Time Series analyses will be discussed in
separate tutorials. GeneCards will redirect you to an overview on your
gene of interest composed of many different resources. ProbePlus, will
provide the sequences probed by the U133 Affymetrix platforms (Will not
be shown in other platforms).
Across datasets will generate an overview showing the average expression
of the gene of interest within all datasets of the same
platform/normalization scheme (provided that the normalization supports
dataset additions).


When you click on the link (the name of the gene) under the PubSniffer header in the left menu, a new screen opens thats lists the number of times your gene of interest is found within the NCBI Pubmed database in
combination with dataset keywords. Clicking on one of the "Pubreminder" links redirects you
**to Pubmed Pub-reminer** which is a tool for PubMed query building and
literature mining.

---------------------------------------------------
  ***Did you know that [Pub re-miner](http://hgserver2.amc.nl/cgi-bin/miner/miner2.cgi) is a helpful tool for literature mining?***  

> *In the large amounts of medical literature, finding information tailored to your needs and interest is becoming more and more complex. Using the right keywords is essential for effective searches, but which ones should you use?*
>  *Pub re-miner is a web-based tool that allows simple text-based query building and information gathering (mining) of the NCBI literature search engine PubMed.*
>  *Pub re-miner presents its results, gathered from abstracts, in frequency tables of journals, authors and words, which can be included / excluded in an iterative fashion.*
>  *Next to building efficient queries, Pub re-miner can also be helpful in other areas: selecting a journal for your current work (by scanning the most often used journals of similar research) Finding experts in a research area (by viewing the authors associated with your query) Determine the research interest of an author (by viewing the keywords associated with an author*

--------------------


Step 6: Adapting plot
---------------


1. To investigate the values R2 uses for graph generation click on “Datatable” to open a table with the expression levels for all samples. Within this table you can use filters to restrict samples. By selecting the rows, a second table is generated, that can be copied and subsequently pasted in Excel for further investigation.
    
    ![](_static/images/OneGene_Datatable.png "Figure 10: Unfold the datatable")

	[**Figure 10: Unfold the datatable**](_static/images/OneGene_Datatable.png)
	
2. The “track display selection” section can be opened by clicking on it.
    In here, you are able to toggle which tracks to display and/or hide
    within the YY-plots. Do note that these selections are non-persistent
    and will be forgotten as soon as you leave the One Gene View. Persistent
    changes to the tracks can be made via the ‘User Options’ menu item, which
    is present in the main screen (see the tutorial 'Adapting R2 to your needs'). 
    Note that the Adjustable Settings panel, including the Customize Track parameters, 
    is available throughout R2 for temporary adaptation of Track visibility and other preferences.

	![](_static/images/OneGene_trackdisplay.png)
	
	[**Figure 11: Tick and drag tracks**](_static/images/OneGene_trackdisplay.png "Figure 11: Tick and drag tracks")

3. Other convenient options are revealed by clicking the “more settings”
    section. An extra panel unfolds which allows you to adapt your graph to
    meet for example the requirements of a journal. The appearance of this
    section will change depending on the kind of graph that you are
    selecting.


![](_static/images/OneGene_Extrasettings_v1.png "Figure 12: the extra settings Panel")

[**Figure 12: the extra settings Panel**](_static/images/OneGene_Extrasettings_v1.png)



![](_static/images/OneGene_Adapting.png "Figure 13: Adapting a graph")

[**Figure 13: Legend added**](_static/images/OneGene_Adapting.png)

In Figure 12 sample annotation (“Annot Graph”) and legend (“Draw
Legend”) were added. The “Annot Graph” option, adds the information of a
selected track to the YY-plot. This can be helpful for the addition of
Sample labels, or cell line names etc. Annotations can be shown in 3
ways; just below/on top of the expression value, as a series below the
annotation tracks or at the values for those samples that haven been
marked. The size of the annotation scales with the setting of the
dotsize.  
Check the More Settings panel for extra options, such as changing the color of the axis or showing  link to and SVG output image. 
The Adjustable Settings menu is available in most of the R2
modules where a one-or two gene view is generated.



![](_static/images/OneGene_Adapting2a.png "Figure 14: Fonts and Color changed")

[**Figure 14: Fonts and Color changed**](_static/images/OneGene_Adapting2a.png)



Step 7: View a gene in groups
---------------

1. Thus far, we have been looking at the expression of MYCN ordered by the expression. From the current location, we can also inspect the MYCN expression sub divided in groups. To achieve this, we simply scroll to the end of the page and locate the dropdown box in the 'Group Separations' section of the 'Adjustable Settings'. Here we can select a track to separate the cohort accordingly. Select 'inss' as a track and press the 'Adjust Settings' button at the end of the page. R2 has now separated the patients on the basis of the inss staging track in alphabetical order. 

    ![](_static/images/OneGene_ViewInGroups1.png "Figure 15: Viewing a gene in groups")

    [**Figure 15: View a gene in groups**](_static/images/OneGene_ViewInGroups1.png)

2. The current representation is the most honest way of showing your data, as every single value is visible in the plot. We can also change the graphical representation of the data by selecting another graph type. Select 'boxplot' from the 'graphtype' dropdown and change 'color by' to 'color by track'. Press the 'Adjust' button again to change the view. We now obtain a boxplot image where the respective groups have been colored according to the groups. Adaptations to other graphtypes can be made in a similar way.

    ![](_static/images/OneGene_ViewInGroups2.png "Figure 16: Viewing a gene in groups by boxplot")

    [**Figure 16: View a gene in groups by boxplot**](_static/images/OneGene_ViewInGroups2.png)

3. You can also sort the groups by their average or median gene expression.

    ![](_static/images/OneGene_avgordered_circosplots.png "Figure 17: Order groups by the average gene expression value")

    [**Figure 17: Order groups by the average gene expression value**](_static/images/OneGene_avgordered_circosplots.png)
    
4. You can also adapt the visual representation of the plot with the "more settings".

    ![](_static/images/OneGene_ViewInGroups3.png "Figure 18: Change the graph options")

    [**Figure 18: Change the graph options**](_static/images/OneGene_ViewInGroups3.png) 

-----------
  ![](_static/images/R2d2_logo.png)***Did you know that once you separate a dataset in more than 2 groups, R2 will identify the most significant pair?***

> *If you view a gene in groups within the one-gene-view view page and the number of sub-groups are greater than 2, then R2 will automatically perform a brute-force t-testing to identify the combination of 2 groups that have the most significant difference. Just click on the ‘T-test on combinations’ link underneath the image and gain insight into all the tested combinations. 

----------

Step 8: Selecting subsets
---------------

To generate a graph of a subgroup of samples use the  'Select a track' pulldown from the 'sample filter' section to select a specific group. 

In the neuroblastoma field it is well known that the mync expression is strongly correlated with stage 4. But maybe you are also interested in the mycn expression for the lower risk stages.

Go to the Adjustable Settings menu and select in the pull down the INSS stage. In th epopup window select the lower risk stages  st1,st2,st3 and st4s and click Next. Back in the Adjustable Settings panel click on the Adjust Settings button. These selections can be repeated a couple of times to build your ultimate selection.

 ![](_static/images/OneGene_selectsubgroups.png "Figure 18: Selecting subgroups")

 [**Figure 19: Selecting subgroups**](_static/images/OneGene_selectsubgroups.png)

 The graphs below were drawn with Graphtype BoxDotPlot. All stages are depicted in the right hand side graph and 
 only the lower risk stages on the left. 

 ![](_static/images/OneGene_subgroupvsall.png "Figure 19: All stages (right) versus lower risk only (left)")

 [**Figure 20: All stages (right) versus lower risk only (left)**](_static/images/OneGene_subgroupvsall.png)

You will encounter the filter option in the adjustable settings box in many modules.

![](_static/images/R2d2_logo.png)**Did you know that you can change the order of the groups?**      

 ![](_static/images/OneGene_AdaptOrder.png)                  

> *In the Adapt Settings box the dropdown menu of the setting 'Order Groups By' allows
> you to change the order in which the groups are presented in the graph. 
> The default ordering is the alphabetical ordering of the track name, but 
> you can choose ordering by the median or the average values of the groups as well.*  

Step 9: Find best track separation with CliniSnitch
---------------

 1. We could wonder if our gene of interest associates even more with any annotation that is already available for 
    the current dataset (like e.g. age group) than the example in the previous section. 
    For such an analysis R2 has the CliniSnitch function. 
    Within this functionality a test is performed on each track. In addition, tracks are inspected before doing the test, 
    and the test is changed according to the contents: for a numeric vs numeric track the correlation is calculated resulting in an r-pvalue;
    categorical vs numerical tracks are tested with an anova test; nonrandom associations for categorical vs categorical tracks are tested with 
    a Fisher's exact test. Furthermore, 'ND' samples are automatically removed, and are not considered a valid group.  
    We can run a CliniSnitch analysis directly from the One Gene View page by clicking on the gene name under 
    'CliniSnitch' in the upper-left panel. Click on ‘MYCN’. Private/Group tracks that you may add to this dataset over time, will automatically be included in these analyses.

    ![](_static/images/OneGene_CliniSnitch1.png "Figure 20: CliniSnitch representation")

    [**Figure 21: CliniSnitch result for MYCN**](_static/images/OneGene_CliniSnitch1.png)

2. Every test can also be visualized by clicking on the View-link in the table. 
Not surprisingly, we can see that MYCN expression is best separated by the MYCN amplification track. 
If we look at the ‘inss’ track, we can also see a significant value. 
Click on ‘View’ behind inss to inspect this further.

Step 10: Finding sample extremes.
---------------

In case you wonder whether any unusual expression levels show up for individual samples from a given dataset, you can you use the "Find sample extreme" option. In this example we know that sample ITCC0288 harbors a Phox2b mutation which leads to the question: can we find extreme expression values for this sample?

1. In the one gene view for this dataset select in the right panel sample itcc0288 in the sample overview  section and click 'view', leave all the settings at their default and click next.

    ![](_static/images/OneGene_selectsampleextreme.png "Figure 21: Select your sample to find extremes")

    [**Figure 22: Select your sample to find extremes**](_static/images/OneGene_selectsampleextreme.png)



2. A table shows the negative z-score (left column) and positive z-score (right column) extremes.  In figure 22 genes which are a part of the Nor-Adrenalin pathway are in the top of the negative z-score list. This suggests that wild-type Phox2b is involved in the up-regulation of the Nor-Adrenalin pathway.  
You can click on any of the genes listed in the table (here we clicked on "TH") to obtain the One Gene View of that gene, with your sample marked in the graph. 

    ![](_static/images/OneGene_sampleextremePhox2b.png "Figure 22: Sample extremes in one sample")

    [**Figure 23: Sample extremes in one sample**](_static/images/OneGene_sampleextremePhox2b.png)



Final remarks / future directions
---------------------------------

Some of these functionalities have been developed recently. If you run
into any quirks or annoyances, don't hesitate to contact r2 support
(r2-support@amc.uva.nl).

We hope that this tutorial has been helpful, the R2 support team.
