# Pymaceuticals


## Matplolib homework for MSU bootcamp.


This analysis was done to describe the results of a drug study testing the effecacy of seevral drugs in treating tumors in mice.  

The following brief description of the study and the analysis completed is adapted from the information provided as the homework assignment.

In this study, 249 mice identified with  tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

The following tasks were completed for this analysis.

The data was checked for any mouse ID with duplicate time points and remove any data associated with that mouse ID.  One moyse (g989) was found and it's associateed data removed (leaving 248 mice in the study.


Summary statistics tables consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen were generated using two methods.  In the first, each measure was calculated separately, added to a dictionary, which was then converted to a dataframe and displayed.  The second method used the aggregation method and was much shorter.  gby_regimen.agg({'Tumor Volume (mm3)': ['mean','median', 'std', 'var', 'sem']})

Bar plots using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the total number of measurements taken for each treatment regimen throughout the course of the study.

Pie plots using both Pandas's DataFrame.plot() and Matplotlib's pyplot that showed the distribution of males and females to be close to 50:50.

Final tumor volume (ie at the 45 minute timpoint) was retrieved from the cleaned dataframe for each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Quartiles and IQR were calculated and outliers were sought using the 1.5 x IQR method.  No outliers were identified.  

Using Matplotlib,  a box and whisker plot of the final tumor volume was generated for all four treatment regimens. No outliers were identified.

All four box plots were displayed in the same figure. (I'm starting to think I should have found outliers, but none showed up in the quantitative analysis or in the boxplot.  I even added a vlaue and checked for outliers which did show up.) so I'm sticking with it.

I did a second boxplot comparison - adding the placebo, and plotting all 5 on the same axis.  This showed a good direct comparison and highlighted the smaller tumor growth in Capomulin and Ramicane.

We were also directed to select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.  I did this as an average of all mice treated with Capomulin.  It seemed like a more relevant comparision.

I generated  a scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen, calculated the correlation coefficient (which turned out to be 0.95) and did a linear regression model between mouse weight and average. The linear regression model was plotted 'on top of' the previous scatter plot.

Three observations or inferences made from the data were included at the top of notebook.  These were.

1.  Capomulin and Ramicane resulted in lower tumor volumes when compared with Infubinol or Ceftamin treatment and placebo treatment. Results for Infubinol and Ceftamin were similar to mice treated with Placebo.

2.  Tumors treated with Capomulin showed a steady decrease in volume over time, with the lowest tumor volume found at the last tmpepoint.

3.  Tumor volume was directly correlated with mouse weight in Capomulin treated mice, with a Pearson's correlation coefficient of (r) or 0.95.



