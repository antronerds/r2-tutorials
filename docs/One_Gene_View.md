<a id="one_gene_view"> </a>

One Gene View
=============

*Analyze the expression levels of a single gene within a dataset*


Scope
-----

- Use R2 to investigate the expression levels of all samples from a
    specific dataset.
- In this example the expression levels of the MYCN gene will be used.
- Adjust several parameters in the advanced settings panel to get a
    better insight in the expressions levels or adapt your
    graphic layout.
- In R2, the samples are annotated with e.g. clinical data, each group
    of annotated data is called a “Track” in R2. These tracks can be
    used to filter data in all types of analyses that R2 is offering.
- A separate info panel in the one-gene expression level screen
    provides different types of analyses based on the expression level
    of the chosen gene.
- Many mRNA expression datasets were generated with Affymetrix
    profiling arrays. In general, these arrays use more than one so-called 
    probeset to measure the expression level of one single gene.
    With a separate module “Transcript view”, the details of the
    probesets can be studied.





Step 1: Select the View a Gene module 
---------------

1.  Use “Single Dataset” in field 1 and make sure that the “Tumor
    Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2” dataset is
    selected in field 2.
2.  Choose “View a Gene” in field 3 and click "Next".


![](_static/images/Onegeneview/OneGene_singleselect_v2a.png "Figure 1: Single gene selection")

[**Figure 1: Single gene selection**](_static/images/Onegeneview/OneGene_singleselect_v2a.png)



Step 2: Select the gene or reporter
---------------

1. We will take a look at the expression levels of the samples for the MYCN gene. Type "mycn" in the left "Search by Gene" textfield and click on the first MYCN reporter that shows up in the list of the dropdown. The reporter ID will then be listed in the right "Search by Reporter" box.  
   
   In the case of Affymetrix datasets, the term probeset is often used instead of reporter, and more than one probeset can be associated with a gene. As you can see in dropdown list for MYCN in this example, multiple probesets are annotated for the MYCN gene.  
   
   By default, *the probeset with the highest average present signal (APS) is annotated as the default probeset in R2*. This APS signal is simply the average of all samples that are considered to express a selected gene (have a present call). After you enter the first letters for the mycn gene in the textfield, you can choose from the available probesets that are listed in a small dropdown. The default R2 probeset will be the first one in the list.   
   Occasionally, other probesets assigned to the same gene could be of interest depending on the structure of the gene (for example a potential splice variant). Also realize that the most informative probeset is re-determined by R2 in every dataset, sometimes resulting in a different probeset.  
      
   The expression levels of datasets are by default converted to log2 values. This does not apply to datasets that contain ratios or logfolds such as methylation arrays and certain Agilent arrays.  
     
   Clicking the *advanced search* button provides a grid where other selection criteria can be applied, such as gene symbol or average signal. Additionally, the sorting option allows for quick checking of genes with a given expression level.  
   The last column of the grid, named "R2 default", indicates whether the reporter is set as default in R2 (TRUE) or not (FALSE). This information is not available for each dataset in R2.
   
   ![](_static/images/Onegeneview/OneGene_multipleprobegrid2.png "Figure 2: By default the reporter with the highest expression level is selected")
   
   [**Figure 2: Top, by default the reporter with the highest expression level is selected. Bottom, the advanced search option with the grid**](_static/images/Onegeneview/OneGene_multipleprobegrid2.png)

2. To follow the example of this tutorial, use the pre-defined default settings in the rest of the adjustable settings menu, and click ‘Next’.
   

Step 3: Plotting Gene expression 
---------------

1. R2 generates a YY-graph (Figure 3) from the MYCN expression levels of
   all samples with expression levels ordered from left (low) to
   right (high). Hovering over the dots reveals additional annotation
   that R2 has stored for the focused sample.

     
   ![](_static/images/Onegeneview/OneGene_MYCN1a.png "Figure 3: YY plot MYCN expression")

   [**Figure 3: YY plot MYCN expression**](_static/images/Onegeneview/OneGene_MYCN1a.png)
  
2. Underneath the X-axis, colored boxes are depicted, representing
   clinical information of the samples in so-called "tracks". Again,
   hovering over them will reveal underlying data. For MYCN there is a
   clear relationship between the expression levels and the tracks for
   “MYCN amplification” and “INSS-stage“. The display of these tracks underneath
   the image gives a quick glance at some of the clinical parameters,
   defined for the dataset. Clicking the triangle at  **View additional detail** provides functional information for the reporters and the genome location if available.  It is also possible to define your own
   custom-made tracks, or disable/adapt the settings for default tracks
   (further explained in the chapter “Adapting R2 to your needs“)

3. Sometimes you get more insight by reviewing the expression levels
   with other transformations. In order to change the transformation, scroll down to the "Adjustable settings" panel underneath the graph and tracks. In the pulldown menu of the ‘Transformation’ setting (top red arrow in Figure 4), choose “none” 
   and then click the button *Submit* at the bottom of the panel.   
   

---------------
 ![](_static/images/R2d2_logo.png)**Did you know that converting expression levels using the “transform” option can help you gain additional insight?**                              

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
>        and expressed as the number of standard deviations from the average. This transformation is useful when the intensities in R2 are not raw, but for example logfolds as is often the case for aCGH data.*    
>  -   *“mad/mad2log”: Median absolute deviation (on raw values, or log2     
>        transformed values).*                                                 
>  -   *“center/log2center”: Expression values centered around 0 (on raw     
>        values, or log2 transformed values).*
>  -   *“Rank”: numerical or ordinal values are replaced by their rank when the data are sorted*
>  -   *“zscore\_group”: Coverts the expression levels from the zscore within 
>        a group (track). Applicable when e.g. technical variation in          
>        expression levels is expected. A possible reason could be when       
>        samples from the same dataset originate from different centers.*  
>  -   *“Square root”: The square root of a number is the number that gets multiplied to itself to give the product.*
>  -   *“log2 grouped zscore”: 2log transformed data within each group of a selected track separately and re-merged after calculation*
----------

---------------
Step 4: Selecting analysis types: View a gene in groups
----------------

In the one gene view plot we have investigated the gene expression of a single gene together with the sample annotation depicted below the graph.

1. Thus far, we have been looking at the expression of MYCN ordered by the expression. From the one-gene-view adjustable settings menu there are also other analyses to select. Above the adjustable settings menu you can select different analysis types which are at you disposal as illustrated in Figure 4. 

![](_static/images/Onegeneview/OneGene_otheranalysis.png "Figure 4: Other analysis type")

[**Figure 4: Select other analysis types**](_static/images/Onegeneview/OneGene_otheranalysis.png)

2. Select in the analysis type menu, the gene vs gene option the adjustable settings will adapt automatically according to the type which has been selected. As illustrated in Figure 5 you simply fill in a different Gene for Gene/Reporter 1 than for Gene/Reporter 2 (upper red box in Figure 5).

![](_static/images/Onegeneview/OneGene_adjustablesettings_v2.png "Figure 5: Adjusting the graph settings")

[**Figure 5: Adjusting the 2 gene plot**](_static/images/Onegeneview/OneGene_adjustablesettings_v2.png)


3. In the “Adjustable settings” panel, several other settings can be found to change the specific input for the analysis or to adapt the looks of the graph:

* Many layout settings can be adjusted in the *More Settings* option, such as font size, colors and marker type. In order to view the extra options, click on the small + sign on the right side of the 'More Settings' tab.
* To highlight specific samples in the graph, you can simply double-click in the graph on the marker-points of the samples that you want to highlight, or you can enter the R2 sample IDs in the field 'Samples to mark' from the ‘Adjustable settings’ panel. If you enter multiple IDs, separate them with a comma.
* Several marking options can be selected with the 'Mark method' that can be found in the 'More settings' tab (e.g.; ‘epicenter’ and ‘arrow’, Figure 5, the "red arrow"). Changes in marker type and marker color can be achieved as well with a specific syntax applied in the before mentioned 'Samples to mark' text field. Keep reading to find examples of how to use the syntax yourself.

*Always click on 'Submit' button at the bottom of the 'Adjust settings' panel for your adjustments to take effect!*


You can adjust the marker color and type of the samples that you marked with a syntax in the 'Samples to mark' field. In order to do so, add a ‘:’ after the IDs with a color code, and/or add a ':' with a marker type, for example; 'itcc0288,itcc0021:ff4444:dot'.  
To bring attention to different samples, you may want to use multiple colors and types of marking. Defining this will overrule the default setting, and thus also enable the use of different markings within the same figure. The skeleton for advanced usage is: ‘sample1,sample2:color1:method1;sample3,sample4:color2:method2’. For example: ‘“itcc0288:ff4444:epicenter;itcc0021:#FF0000:arrow;itcc0013,itcc0132:00ff00:epicente”’ creates the markings as shown in the figure below.

![](_static/images/Onegeneview/OneGene_view_samplesmark_v2.png "Figure 6: Adjusting the graph settings")

[**Figure 6: Adjusting the sample mark layout**](_static/images/Onegeneview/OneGene_view_samplesmark_v2.png)

---------------
![](_static/images/R2d2_logo.png)**Did you know that R2 allows you to emphasize samples in the graph with many different marker options?**

> *R2 knows a couple of marker options, that you can make use of in the advanced prescriptions:*
> - *'dot': places a thick border around the sample*
> - *'circle': Places a ring around the sample (diameter 9)*
> - *'circle_2': Places a ring around the sample (diameter 4)*
> - *'circle_3': Places a ring around the sample (diameter 1), effectively a thin border*
> - *'epicenter': Places a set of 3 rings descending in width around a sample*
> - *'arrow': Places a block arrow pointing to the sample*
> - *'triangle': Places a filled triangle under the sample*
> - *'colors': use an html color code*
> 
>*Note: The dotsize does not scale with 'arrow' and 'triangle' method.*
---------------

Another often used feature is the **Vector (SVG) output** option. The vector images are often used in manuscripts. Click on the + sign on the right of the tab to unfold the 'More Settings' tab, where you can find a dropdown next to the 'Vector (SVG) output' setting. When the dropdown is set to "True", and the 'Submit' button is clicked, a link appears above the 'Adjustable Settings' panel, that you can right-click to save the vector image to your computer. SVG vector images can be manipulated in any vector graphics software, such as Illustrator, GIMP or Inkscape.

![](_static/images/Onegeneview/OneGene_adjustablesettings_svg.png "Figure 7: Obtain a vector (SVG) image of your graph")

[**Figure 7: Obtain a vector (SVG) image of your graph**](_static/images/Onegeneview/OneGene_adjustablesettings_svg.png)

----------
![](_static/images/R2d2_logo.png)**Did you know that the 'Adjustable settings' panel is available under most graphs and analysis results in R2?**

> *Just scroll down the page to find the Adjustable settings box with options to adjust the settings of the analysis or to adjust the looks of the graph. **Don't forget to press the Submit** button at the bottom of the panel in order for your changes to take effect!*



4. When you are in the one gene view plot, a logical step is to investigate the expression levels in correspondence  with a group parameter. Select in the analysis type menu "gene vs track" in the track selection menu, the inss track and click "submit", Figure 8. The cohort is separated accordingly by the patient INSS staging in alphabetical order. It could be that the ordering of the group parameters is not the most convenient representation for your analysis. In order to customize this, you can create your own track as described in  (the chapter “Adapting R2 to your needs”) and make your own track with the correct ordering eg: a_stage IV, b_stage 1 etc. 

   ![](_static/images/Onegeneview/OneGene_genevstrack.png "Figure 8: Gene vs track")

   [**Figure 8: Gene versus track**](_static/images/Onegeneview/OneGene_genevstrack.png)

5. The current representation is the most honest way of showing your data, as every single value is visible in the plot. In the adjustable settings you can fine-tune your graph for example by switching on the genesort within the groups (Figure 9).

   ![](_static/images/Onegeneview/OneGene_genevstracksort.png "Figure 9: Gene vs track sorted")

   [**Figure 9: Gene versus track sorted**](_static/images/OnegeneviewOneGene_genevstracksort.png)


6. We can also change the graphical representation of the data by selecting another graph type. Select 'boxplot' from the 'graphtype' dropdown and change 'color by' to 'color by track', such that the inss track is used to color the boxes. Press the 'Submit' button again to change the view. We now obtain a boxplot image where the respective groups have been colored according to the inss groups. Adaptations to other graph types can be made in a similar way.

7. We can also change the graphical representation of the data by selecting another graph type. Select 'boxplot' from the 'graphtype' dropdown and change 'color by' to 'color by track', such that the inss track is used to color the boxes. Press the 'Submit' button again to change the view. We now obtain a boxplot image where the respective groups have been colored according to the inss groups. Adaptations to other graph types can be made in a similar way.

![](_static/images/Onegeneview/OneGene_boxplots.png "Figure 10: Fonts and Color changed")

[**Figure 10: Making boxplots**](_static/images/Onegeneview/OneGene_viewinGroups_v1.png)

8. You can also sort the groups by their average or median gene expression and customize your graph in various ways. In Figure 11 this illustrated by the INSS stage sequence according to the average gene expression and enlarged dots.

![](_static/images/Onegeneview/OneGene_boxplotsorderby.png "Figure 11: Fonts and Color changed")

[**Figure 11: Ordering boxplots**](_static/images/Onegeneview/OneGene_viewinGroups_v1.png)


9. Also, directly accessible from this menu is the track vs track option described in more detail in Chapter 5: Annotation Analyses; "relate two tracks". Keep in mind that the analysis type options described in this chapter can also be selected directly from the main menu. 

![](_static/images/Onegeneview/OneGene_boxmainmnu.png "Figure 11: track vs track and main menu ")

[**Figure 11: Track versus Tracks / Main menu**](_static/images/Onegeneview/OneGene_viewinGroups_v1.png)



- *'single gene': In main menu: "view a gene"*
- *'gene vs track': In main menu: "View a gene in groups"*
- *'track vs track': In main menu: "Relate two tracks"*




-----------
![](_static/images/R2d2_logo.png)***Did you know that once you separate a dataset in more than 2 groups, R2 will identify the most significant pair?***

> *If you view a gene in groups within the one-gene-view view page and the number of sub-groups is greater than 2, R2 will automatically perform brute-force t-testing to identify the combination of 2 groups that have the most significant difference. Just click on the ‘T-test on combinations’ link underneath the image and gain insight into all the tested combinations.



Step 5: Sources for additional information on the selected gene 
----------------

1. Close the Genome Browser tab or go back to the MYCN One Gene View expression screen.

   ![](_static/images/Onegeneview/OneGene_menupanel.png "Figure 12:Left menu panel providing additional info (including link-out) and analyses options")

   [**Figure 12: Left menu panel providing additional info (including link-out) and analyses options**](_static/images/Onegeneview/OneGene_menupanel.png)


In the left upper menu-panel several options are available to provide
you with additional information sources of the MYCN gene and additional
analyses. KaplanScan and Time Series analyses will be discussed in
separate tutorials. GeneCards will redirect you to an overview on your
gene of interest composed of many different resources. ProbePlus, will
provide the sequences probed by the U133 Affymetrix platforms (will not
be shown in other platforms).
Across datasets will generate an overview showing the average expression
of the gene of interest within all datasets of the same
platform/normalization scheme (provided that the normalization supports
dataset additions).


When you click on the link (the name of the gene) under the PubSniffer header in the left menu, a new screen opens that lists the number of times your gene of interest is found within the NCBI Pubmed database in
combination with dataset keywords. Clicking on one of the "PubReMiner" links redirects you
**to Pubmed PubReMiner** which is a tool for PubMed query building and
literature mining.

---------------------------------------------------
  ***Did you know that [PubReMiner](http://hgserver2.amc.nl/cgi-bin/miner/miner2.cgi) is a helpful tool for literature mining?***  

> *In the large amounts of medical literature, finding information tailored to your needs and interest is becoming more and more complex. Using the right keywords is essential for effective searches, but which ones should you use?*
>  *PubReMiner is a web-based tool that allows simple text-based query building and information gathering (mining) of the NCBI literature search engine PubMed.*
>  *PubReMiner presents its results, gathered from abstracts, in frequency tables of journals, authors and words, which can be included / excluded in an iterative fashion.*
>  *Next to building efficient queries, PubReMiner can also be helpful in other areas: selecting a journal for your current work (by scanning the most often used journals of similar research) Finding experts in a research area (by viewing the authors associated with your query) Determine the research interest of an author (by viewing the keywords associated with an author*

--------------------





Step 6: Adapting plot
---------------


1. To investigate the values R2 uses for graph generation click on “Datatable” to open a table with the expression levels for all samples. Within this table you can use filters to restrict samples. By selecting the rows, a second table is generated, that can be copied, and subsequently pasted in Excel, for further investigation.
    
    ![](_static/images/Onegeneview/OneGene_Datatable.png "Figure 13: Unfold the datatable")

	[**Figure 13: Unfold the datatable**](_static/images/Onegeneview/OneGene_Datatable.png)
	
2. The “track display selection” section can be opened by clicking on it.
    In here, you are able to toggle which tracks to display and/or hide
    within the YY-plots. Do note that these selections are non-persistent
    and will be forgotten as soon as you leave the One Gene View. Persistent
    changes to the tracks can be made via the ‘User Options’ menu item, which
    is present in the main screen (see the tutorial 'Adapting R2 to your needs'). 
    Note that the Adjustable Settings panel, including the Customize Track parameters, 
    is available throughout R2 for temporary adaptation of Track visibility and other preferences.

	![](_static/images/Onegeneview/OneGene_trackdisplay.png)
	
	[**Figure 14: Tick and drag tracks**](_static/images/Onegeneview/OneGene_trackdisplay.png "Figure 14: Tick and drag tracks")

3. Other convenient options are revealed by clicking the “more settings”
    section. An extra panel unfolds which allows you to adapt your graph to
    meet, for example, the requirements of a journal. The appearance of this
    section will change depending on the kind of graph that you are
    selecting.


![](_static/images/Onegeneview/OneGene_Extrasettings_v1.png "Figure 15: the extra settings Panel")

[**Figure 15: the extra settings Panel**](_static/images/Onegeneview/OneGene_Extrasettings_v1.png)



![](_static/images/Onegeneview/OneGene_Adapting.png "Figure 13: Adapting a graph")

[**Figure 15: Legend added**](_static/images/Onegeneview/OneGene_Adapting.png)

In Figure 12 sample annotation (“Annot Graph”) and legend (“Draw
Legend”) were added. The “Annot Graph” option, adds the information of a
selected track to the YY-plot. This can be helpful for the addition of
Sample labels, or cell line names etc. Annotations can be shown in 3
ways; just below/on top of the expression value, as a series below the
annotation tracks or at the values for those samples that haven been
marked. The size of the annotation scales with the setting of the
dotsize.  
Check the More Settings panel for extra options, such as changing the color of the axis or showing a link to and SVG output image. 
The Adjustable Settings menu is available in most of the R2
modules where a one-or two gene view is generated.



![](_static/images/Onegeneview/OneGene_Adapting2a.png "Figure 16: Fonts and Color changed")

[**Figure 16: Fonts and Color changed**](_static/images/Onegeneview/OneGene_Adapting2a.png)




----------

Step 7: Selecting subsets
---------------

To generate a graph of a subgroup of samples, use the 'Select a track' pulldown from the 'sample filter' section to select a specific group. 

In the neuroblastoma field it is well known that the mycn expression is strongly correlated with stage 4. But maybe you are also interested in the mycn expression for the lower risk stages.

Go to the Adjustable Settings menu and select in the pull down the INSS stage. In the popup window select the lower risk stages st1, st2, st3 and st4s and click Next. Back in the Adjustable Settings panel click on the Submit button. These selections can be repeated a couple of times to build your ultimate selection.

 ![](_static/images/Onegeneview/OneGene_selectsubgroups.png "Figure 17: Selecting subgroups")

 [**Figure 17: Selecting subgroups**](_static/images/Onegeneview/OneGene_selectsubgroups.png)

 The graphs below were drawn with Graphtype BoxDotPlot. All stages are depicted on the right hand side graph and 
 only the lower risk stages on the left. 

 ![](_static/images/Onegeneview/OneGene_subgroupvsall.png "Figure 18: All stages (right) versus lower risk only (left)")

 [**Figure 18: All stages (right) versus lower risk only (left)**](_static/images/Onegeneview/OneGene_subgroupvsall.png)

You will encounter the filter option in the adjustable settings box in many modules.


Step 8: Find best track separation with CliniSnitch
---------------

 1. We could wonder if our gene of interest associates even more with any annotation that is already available for 
    the current dataset (like e.g. age group) than the example in the previous section. 
    For such an analysis R2 has the CliniSnitch function. 
    Within this functionality a test is performed on each track. In addition, tracks are inspected before doing the test, 
    and the test is changed according to the contents: for a numeric vs numeric track the correlation is calculated resulting in an r-pvalue, in other words the correlation between the p-values.
    categorical vs numerical tracks are tested with an anova test; nonrandom associations for categorical vs categorical tracks are tested with 
    a Fisher's exact test. Furthermore, 'ND' samples are automatically removed, and are not considered a valid group.  
    We can run a CliniSnitch analysis directly from the One Gene View page by clicking on the gene name under 
    'CliniSnitch' in the upper-left panel. Click on ‘MYCN’. Private/Group tracks that you may add to this dataset over time, will automatically be included in these analyses.

    ![](_static/images/Onegeneview/OneGene_CliniSnitch1.png "Figure 19: CliniSnitch representation")

    [**Figure 19: CliniSnitch result for MYCN**](_static/images/Onegeneview/OneGene_CliniSnitch1.png)

2. Every test can also be visualized by clicking on the View-link in the table. 
Not surprisingly, we can see that MYCN expression is best separated by the MYCN amplification track. 
If we look at the ‘inss’ track, we can also see a significant value. 
Click on ‘View’ behind inss to inspect this further.

Step 9: Finding sample extremes.
---------------

In case you wonder whether any unusual expression levels show up for individual samples from a given dataset, you can you use the "Find sample extreme" option. In this example we know that sample ITCC0288 harbors a Phox2b mutation which leads to the question: can we find extreme expression values for this sample?

1. In the one gene view for this dataset select in the right panel sample itcc0288 in the sample overview  section and click 'view', leave all the settings at their default and click next.

    ![](_static/images/Onegeneview/OneGene_selectsampleextreme.png "Figure 20: Select your sample to find extremes")

    [**Figure 20: Select your sample to find extremes**](_static/images/Onegeneview/OneGene_selectsampleextreme.png)



2. A table shows the negative z-score (left column) and positive z-score (right column) extremes. In Figure 22, genes which are a part of the Nor-Adrenalin pathway are in the top of the negative z-score list. This suggests that wild-type Phox2b is involved in the up-regulation of the Nor-Adrenalin pathway.  
You can click on any of the genes listed in the table (here we clicked on "TH") to obtain the One Gene View of that gene, with your sample marked in the graph. 

    ![](_static/images/Onegeneview/OneGene_sampleextremePhox2b.png "Figure 20: Sample extremes in one sample")

    [**Figure 20: Sample extremes in one sample**](_static/images/Onegeneview/OneGene_sampleextremePhox2b.png)


---------------
Step 10: Probeset verification
---------------


The table displayed in Figure 6 lists whether the various reporters of MYCN are in
agreement with the genome position of MYCN reference sequence (RefSeq).
If all are stating “YES” then everything appears alright (from the
perspective of an automated assessment). The MYCN reporters with a “NO”
indicate there may be an issue with it. Scroll down the page
and click on the “Tview” link in the reporter table.


![](_static/images/Onegeneview/OneGene_Probesettable.png "Figure 21: Probeset verification table")

[**Figure 21: Probeset verification table**](_static/images/Onegeneview/OneGene_Probesettable.png)

1.  A new screen (or tab in the browser) appears with TranscriptView.
    The TranscriptView application depicts the alignment of expressed
    sequence tags (EST) and mRNA sequences to the human reference genome
    sequence (Fig 8. The strand orientation of these sequences are
    indicated by a color (green = positive strand, red = negative
    strand, blue = strand information is missing). The structure of the
    reference sequence has also been indicated. Furthermore, the browser shows the alignment of the sequences that were used to generate the reporters on the array (in the case of Affymetrix microarrays).  
    This view can be used to inspect the quality of a reporter. Note, for instance, that the reporter
    “242026\_at” is aligned with the genomic region of the MYCN reference
    sequence, but that its color is different from the rest (colored
    in red). In addition, in this particular case the reporter is
    located in the intronic (light shaded color) region which is another
    reason not to pick a certain probeset. Indeed, if we compare the
    gene expression values of this reporter, then its expression is 60
    fold lower than R2's standard pick (22 vs 1369). Below the ESTs the
    average gene expression of the individual probesets is illustrating
    that for this example the correct probeset is selected for analysis.
    NB: Currently probeset verification is only provided for various
    human Affymetrix array types.


![](_static/images/Onegeneview/OneGene_Colorlegend.png "Figure 22 Color ")

[**Figure 22: Coloring represents type of transcript**](_static/images/Onegeneview/OneGene_Colorlegend.png)


![](_static/images/Onegeneview/OneGene_Tview.png "Figure 23 MYCN reporters in Transcript view")

[**Figure 23: MYCN reporters in Transcript view**](_static/images/Onegeneview/OneGene_Tview.png)



---------------
![](_static/images/R2d2_logo.png)**Did you know that you can browse the gene expression values along the genome?**

> *Once you have entered the genome browser with an attached dataset (like above), you can also navigate to / zoom out any other region in the genome. This allows you to look at the neighboring genes in a single go.
>   It can be informative to separate the expression on the basis of a track. This can be achieved by selecting 'dataset\_track' from the sample dropdown in the middle panel. Finally, within the genome browser, the contents for a panel on the left side can be hidden from a view by setting the height to 0.*

---------------


Final remarks / future directions
---------------------------------

Some of these functionalities have been developed recently. If you run
into any quirks or annoyances, do not hesitate to contact r2 support
(r2-support@amsterdamumc.nl).

We hope that this tutorial has been helpful, the R2 support team.