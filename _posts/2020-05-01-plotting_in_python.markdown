---
layout: post
title:      "Plotting in Python"
date:       2020-05-01 17:03:54 +0000
permalink:  plotting_in_python
---


In this blog I demonstrate how to make several plots in python using matplotlib. Simply import matplotlib.pyplot with an alias (I use “plt”) and follow the instructions to start making plots! Before making plots consider you can change the size of the plot by calling plt.figure and passing in a figsize. Also you can set labels such as a title, a label for the x-axis, and a label for the y-axis. Finally make sure to call plt.show() after every plot to prevent code showing above your plot.

## Histograms
Histograms are good for finding the distribution of a set of data. They the frequency that a value appears in a set of data. A histogram only needs one variable, I will call it “x”. To plot a histogram call plt.hist() and pass in x.

## Bar Plots
ar plots are good for comparing the values of multiple variables. Some examples could be showing the GDP of different countries or the win rate of different sports teams. To make a bar plot you need two variables, I will call them “x” and “y”. The x variable can be a list or array of numbers or strings. The y variable should be a list or array of numbers (integers or floats). The lists or arrays must be ordered. The first item in x should match the first item in y and so on. To make a bar plot call pyplot.bar() and pass in the x and y variables in that order.

## Scatter Plots
Scatter plots are good at checking the relationships between variables. For example it may be important to check if two sets of data have a linear relationship. Just like bar plots, scatter plots require two sets of data, x and y, and they must be ordered. Their is a difference in scatter plots that both sets of data have to be numerical (integer or float) as these values will coordinate where a point lies between the x and y axes. To make a scatter plot simply call plt.scatter() and pass in x and y in that order.

## Line Plots
Line plots are good for showing how something changes over time. A Lineplot is much like a scatter plot but all the points are connected. One thing to keep in mind is that in a line plot the values need to be in ascending or descending order or else the line will jump around. To make a line plot simply call plt.plot() and pass in x and y.

## Final Notes
Now that you know the basics of plotting it is time to introduce colors and alpha levels. Pass in a color parameter (i.e. “color=’green’) to change the color of your plot and an alpha parameter (i.e. “alpha=0.7”) to change its transparency! Also to show two plots on top of each other simply call the plotting method twice before calling plt.show(). If plotting more than one plot on top of another make sure to pass in a label parameter (i.e. “label=’customers’”) to your plots and use plt.legend() at the end to create a legend for your plot!

