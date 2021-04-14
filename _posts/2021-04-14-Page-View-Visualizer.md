---
published: true
layout: post
title: Page View Visualizer
category: Data Analytics with Python
---

In this analysis, We will be visualizing time series data using a line chart, bar chart and box plots.
The data we are looking at will be the number of page views each day on freeCodeCamp.org forum from 2016-05-09 to 2019-12-03.

The dataset that we have consists of 1304 rows and 2 columns, 'date' and 'value' which shows the number of visits in the day.

The steps taken to do the plot is as follow:
1. Read in the data from the csv file with pandas and parse the date column.
Note that when you parse the date column, the data type changes.
2. Plot the line graph with matplotlib
3. Make a copy of the data frame and convert the date column to string so that you can carry out string manipulation
4. Once the date column is in string format, you can manipulate it and apply groupby function to generate the bar plot.
5. Plot the bar graph using seaborn catplot function.
Note that seaborn is a visualization library and you can think of it as an extension to matplotlib
6. Make a copy of the data frame like before.
7. Plot the box plots using seaborn boxplot function.

![line_plot.png]({{site.baseurl}}/images/page_view_visualizer/line_plot.png)

![bar_plot.png]({{site.baseurl}}/images/page_view_visualizer/bar_plot.png)

![box_plot.png]({{site.baseurl}}/images/page_view_visualizer/box_plot.png)

If you would like to find out more about my python code, check out the repo [here](https://github.com/ye-song/page-view-time-series-visualizer/blob/master/time_series_visualizer.py)
