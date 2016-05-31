<a id="annotation_analyses"> </a>

Annotation analyses
===================



*Using (custom) annotation tracks as input for analyses*





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
    
	![Figure 1: Select relate two tracks.](_static/images/AnnotationAnalyses_relate.png "Figure 1: Select relate two tracks")
	
	[**Figure 1: Select "relate two tracks".**](_static/images/AnnotationAnalyses_relate.png)
	
2.  For the different tracks, make sure that you select a categorical
    one (which can be recognized by (cat)). Let"s investigate whether
    there is a relation between the neuroblastoma age-group
    (track=agegroup, flip point being 18 months at diagnosis) and the
    survival status (track=alive). Then press next to generate
    the result.
    
	![Figure 2: Select Selecting categorical tracks](_static/images/AnnotationAnalyses_adjust.png "Figure 2: Select Selecting categorical tracks")
	
	[**Figure 2: Select Selecting categorical tracks**](_static/images/AnnotationAnalyses_adjust.png)
	
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


	![Figure3: Color samples by track](_static/images/AnnotationAnalyses_colorsamples.png "Figure3: Color samples by track")
	
	[**Figure3: Color samples by track**](_static/images/AnnotationAnalyses_colorsamples.png)
	





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


	![Figure 4: Output of relating numericaltracks](_static/images/AnnotationAnalyse_relatetracks.png "Figure 4: Output of relating numericaltracks")
	
	[**Figure 4: "Output of relating numericaltracks**](_static/images/AnnotationAnalyse_relatetracks.png)
	





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


	![Figure 5: Representing the relation between categorical and numerical tracks](_static/images/AnnotationAnalyse_relationnumcat.png "Figure5: Representing the relation between categorical and numericaltracks")
	
	[**Figure 5: Representing the relation between categorical and numerical tracks**](_static/images/AnnotationAnalyse_relationnumcat.png)
	


As a recap for the last 3 tutorial steps, you have used the "relate 2
tracks" option from the annotation methods in R2 and represented
different types of tracks with each other to gain new insights from
combining 2 tracks. Below the 3-different representations are depicted
side by side. Do remember, that this module allows you to use "meta
data" tracks that you can assemble either within, but also outside of R2
via the uploading of a track option that will be shown in the "adapting
r2 to your needs" chapter.




	![Figure 6: Representations of relations between different types of tracks in R2](_static/images/AnnotationAnalyse_representation.png "Figure6: Representations of relations between different types of tracks in R2")
	
	[**Figure6: "Representations of relations between different types of tracks in R2**](_static/images/AnnotationAnalyse_representation.png)
	





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


	![Figure7: Plotting the annotationtracks](_static/images/AnnotationAnalyse_plotting.png "Figure7: Plotting the annotationtracks")
	
	[**Figure7: Plotting the annotationtracks**](_static/images/AnnotationAnalyse_plotting.png)
	





Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,





The R2 support team.






