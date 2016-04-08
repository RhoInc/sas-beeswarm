# sas-beeswarm

This repository contains a SAS<sup>&reg;</sup> macro for producing a beeswarm plot (i.e., a strip plot with non-random jittering). 

![sas beeswarm plot](https://github.com/RhoInc/sas-beeswarm/blob/master/img/BeeswarmPlot.png)

Visit the [Wiki]() for more details.

For more details on producing beeswarm plots in SAS, please visit http://graphics.rhoworld.com/tools/beeswarm/.

The beeswarm is a relatively new type of plot and one that SAS<sup>&reg;</sup> does not yet produce automatically (as of version 9.4). For those unfamiliar with beeswarm plots, they are related to strip plots and jittered strip plots. Strip plots are scatter plots with a continuous variable on the vertical axis and a categorical variable on the horizontal axis (e.g., systolic blood pressure vs. treatment group). The strip plot is hamstrung by the fact that tightly packed data points start overlaying one another, obscuring the story that the data are trying to tell. A jittered strip plot seeks to remedy
this problem by randomly moving data points off of the categorical center line. Depending on the volume of data and the particular sequence of random jitters, this technique does not always eliminate all overlays. In order to guarantee no overlays we must adopt a non-random approach. This is where the beeswarm comes in. The beeswarm approach is to plot data points one at a time, testing candidate locations for each new data point until one is found that does not conflict with any previously plotted data points. The macro presented here performs the preliminary calculations necessary to avoid overlays and thereby produce a beeswarm plot.
