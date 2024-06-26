<a id="graphs_settings"> </a>

## Graphs: Adjustable Settings menu versus Repsonsive Settings

*Adapt and export graphs in R2*

R2 often offers the user settings to adapt or enhance the looks of a visualization. Adaptations could be purely 
aesthetical preferences, but often they are functional, for instance to overlay the plot with extra layers of information.   
Traditionally, the user can control such settings with an *Adjustable Settings* menu that is placed 
underneath many graphs in the platform. Adjustments in the settings of these graphs take effect after 
the button at the bottom of the menu is hit. Increasingly, the platform offers responsive controls as well: 
when a setting is adjusted, the changes in the menu are directly visible in the graph without the need to 
click any submit button. Certain graph elements can even be adjusted directly within the plot interface. Plots that 
offer responsive functionalities can be recognized by a settings wheel in the upper left corner of the graph. 
Some options may not be immediately evident to users, however, they facilitate swift adaptability. Therefore, this 
chapter aims to show a few examples as showcases of how to tweak the plots with the different setting types. 

### Example settings: color the sample maps

In the Sample maps module, underneath the scatter plots we can find the R2-wide grey Adjustable Settings menu and a 
Color settings menu.
Options listed in these menus require the user to press the "Set [setting name]" button in order for the requested
changes to the specific setting to take effect.
For instance, here the graph colors can be set to the colors of a track, or they can be set to the expression levels
of a gene. This setting requires the user to click on the button "Set colors" in order to take effect.  
Other settings can be adjusted directly in the plot itself. When your mouse hovers over the legend categories, an
information pop up tells you that the respective subgroup of samples can be toggled off and on in the plot with a click on the
legend box. Also, a click on the legend title "histology" will invert the selection. If all groups are shown, which 
is the default situation when you color a map with a track, then the invert option will deselect all groups leaving the
plot blank. One more click allows you to subsequently single out a subgroup quickly. 
With one more click you then toggle one or a few groups on. 


![](_static/images/Graphs/samplemaps_color_settings_legend_toggle.gif "Figure 1: Submit buttons (color by track) vs responsive settings (toggle legend subgroups)")

[**Figure 1: Submit buttons (color by track) vs responsive settings (toggle legend subgroups)**](_static/images/Graphs/samplemaps_color_settings_legend_toggle.gif)

In the animation below, we show several responsive settings that you can find in various graphs in R2. In
responsive graphs, samples can be marked with a click on the sample in the graph; you can zoom in and out with the
scrolling wheel of your mouse and the graph can be repositioned by dragging the plot while holding the right mouse 
button.

![](_static/images/Graphs/samplemaps_zoom_drag_mark.gif "Figure 2: Zoom in / out and reposition the plot, mark a
sample")

[**Figure 2: Zoom in / out and reposition the plot, mark a
sample**](_static/images/Graphs/samplemaps_zoom_drag_mark.gif)

Some graphs offer additional responsive options outside the graph. Below the animation shows several other options in 
the Sample maps module. 


![](_static/images/Graphs/sample_maps_dot_size.gif "Figure 3: Adapt dot size / add border/ copy paste to powerpoint")

[**Figure 3: Adapt dot size / add border/ copy paste to powerpoint**](_static/images/Graphs/sample_maps_dot_size.gif)
