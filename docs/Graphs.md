<a id="graphs"> </a>

## Graphs

*Adapt and export graphs in R2*

Visualization is a key feature of R2, with an ongoing commitment to developing new types of visualizations and
enhancing existing ones. The recently developed graphs often offer adaptability in an interactive way. While some 
graph options may not be immediately evident to users, they facilitate swift adaptability once users become familiar 
with how to tweak the plots. This tutorial aims to offer a comprehensive overview of frequently employed or 
requested plots, alongside lesser-known yet valuable visualization functionalities.

### Settings with submit buttons versus Interactive Settings

In the Sample maps module, underneath the scatter plots we can find the R2-wide grey Adjustable Settings menu.
Options listed in these menu require the user to press the "Set [functionality]" button in order for the requested
changes to take effect.
For instance, here the graph colors can be set to the colors of a track, or they can be set to the expression levels
of a gene. This setting requires the user to click on the button "Set colors" in order to take effect.  
Other settings can be adjusted directly in the plot itself. When your mouse hovers over the legend categories, an
information pop up tells you that the respective subgroup of samples can be toggled off and on in the plot with a click on the
legend box. Also, a click on the legend title "histology" will invert the selection. If all groups are shown, which 
is the default situation when you color a map with a track, then the invert option will deselect all groups leaving the
plot blank. One more click allows you to subsequently single out a subgroup quickly. 
With one more click you then toggle one or a few groups on such that you can view them 


![](_static/images/Graphs/samplemaps_color_settings_legend_toggle.gif "Figure 1: Submit buttons (color by track) vs
interactive settings (toggle legend subgroups)")

[**Figure 1: Submit buttons (color by track) vs interactive settings (toggle legend subgroups)**](_static/images/Graphs/samplemaps_color_settings_legend_toggle.gif)

In the animation below, we show several interactive settings that you can find in various graphs in R2. In
interactive graphs, samples can be marked a click on the sample in the graph; you can zoom in and out with the
scrolling wheel of your mouse; the graph can be repositioned by dragging the plot while holding the right mouse button.

![](_static/images/Graphs/samplemaps_zoom_drag_mark.gif "Figure 2: Zoom in / out and reposition the plot, mark a
sample")

[**Figure 2: Zoom in / out and reposition the plot, mark a
sample**](_static/images/Graphs/samplemaps_zoom_drag_mark.gif)

Some graphs offer additional interactive options outside the graph. Belowwe show the options in the Sample maps module. 