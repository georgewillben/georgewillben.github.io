---
layout: post
title:      "A Brief Introduction To Plotting In Python with Seaborn"
date:       2020-05-01 16:58:56 +0000
permalink:  a_brief_introduction_to_plotting_in_python_with_seaborn
---


Seaborn Is a great module in python for creating more complex plots. In this post I will cover a few ways to plot in seaborn: kernel density estimation plots and heatmaps

## Kernel Density Estimation Plots
A kernel density estimation plot (KDE) is good for finding the distribution of a set of data. It is similar to a histogram, except instead of showing the frequency each value occurs in a set of data, it shows the probability of a piece of data landing within a range of values in the plot. If the area under the line is calculated that area is the probability of the point being in that range. To make a KDE call sns.distplot() and pass in the data. It will automatically include a histogram, but if you do not want one just pass in the parameter hist=False.


## Heat maps
Heat maps are a good for checking for correlation between variables. It takes in a dataframe of values and displays them in a grid. To check for correlation between variables with a seaborn heat map take a pandas dataframe and pass in dataframe.corr() to sns.heatmap(). You can pass in the parameter “annot = True” and it will generate numbers with each value. Also it is optional to pass in a colormap such as “coolwarm” to the parameter “cmap” to change the color style of the plot.

