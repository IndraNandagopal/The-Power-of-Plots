# The-Power-of-Plots

In this assignment, the task is to apply the Matplotlib skills to a real-world situation and dataset.

## Background

Pymaceuticals Inc., is a new pharmaceutical company that specializes in anti-cancer pharmaceuticals. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

In this study, 249 mice identified with SCC tumor growth were treated with a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

### Data preparation

1. Ran the provided package dependency and data imports, and then merged the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Displayed the number of unique mice IDs in the data, and then checked for any mouse ID with duplicate time points. Displayed the data associated with that mouse ID, and then created a new DataFrame where this data is removed. Used this cleaned DataFrame for the remaining step.

3. Displayed the updated number of unique mice IDs.

### Generate Summary Statistics

Created two summary statistics DataFrames:

    * For the first table, used the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This resulted in five unique series objects. Combined these objects into a single summary statistics DataFrames.
![Summary_Statistics_Method1](Pymaceuticals\output/Summary_Statistics_Method1.PNG)

    * For the second table, used the `agg` method to produce the same summary statistics table by using a single line of code.
![Summary_Statistics_Method2](Pymaceuticals\output/Summary_Statistics_Method2.PNG)

### Create Bar Charts and a Pie Charts

1. Generated two bar plots. Both plots are identical and showed the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

    * Created the first bar plot by using Pandas's `DataFrame.plot()` method.
![bar_plot_usingDFPlot](Pymaceuticals\output\bar_plot_usingDFPlot.PNG)

    * Created the second bar plot by using Matplotlib's `pyplot` methods.
![bar_plot_usingPyPlot](Pymaceuticals\output\bar_plot_usingPyPlot.PNG)

2. Generated two pie plots. Both plots are identical and showed the distribution of female or male mice in the study.

    * Created the first pie plot by using both Pandas's `DataFrame.plot()`.
![pie_plot_using_pandas](Pymaceuticals\output\pie_plot_using_pandas.PNG)

    * Created the second pie plot by using Matplotlib's `pyplot` methods.
![pie_plot_using_pyplot](Pymaceuticals\output\pie_plot_using_pyplot.PNG)

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR and determined if there are any potential outliers across all four treatment regimens. Followed these substeps:

    * Created a grouped DataFrame that shows the last (greatest) time point for each mouse. Merged this grouped DataFrame with the original cleaned DataFrame.

    * Created a list that holds the treatment names, as well as a second, empty list to hold the tumor volume data.

    * Looped through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Appended the resulting final tumor volumes for each drug to the empty list. 

    * Determined the outliers by using the upper and lower bounds, and then printed the results.
  
2. Using Matplotlib, generated a box plot of the final tumor volume for all four treatment regimens. Highlighted the potential outliers in the plot by changing their color and style.
![box_plot](Pymaceuticals\output\box_plot.PNG)

### Create a Line Plot and a Scatter Plot

1. Selected a mouse that was treated with Capomulin and generated a line plot of tumor volume vs. time point for that mouse.
![line_plot](Pymaceuticals\output\line_plot.PNG)

2. Generated a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.
![scatter_plot](Pymaceuticals\output\scatter_plot.PNG)

### Calculate Correlation and Regression

1. Calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Ploted the linear regression model on top of the previous scatter plot.
![regression_plot](Pymaceuticals\output\regression_plot.PNG)

### Final Analysis

Added my observations at the top of the Jupiter notebook.

