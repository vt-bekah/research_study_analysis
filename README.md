# Mod5_Pymaceuticals
This repository contains challenge files for UT DAV Bootcamp Module 5 Data Visualization


# File Notes
* pymaceuticals.ipynb contains my written analysis in the top cell and the complete code to output results as indicated by the instrustions and starter code in the following cells.
* PymaceuticalsReport.docx contains the same written analysis as pymaceuticals.ipynb but with the figures and tables embedded.
* Additional_pymaceuticals.ipynb contains additional views created for the report and alternate methods to achieve the homework solution. This should not be considered as part of the grading rubric listed in BCS/Canvas
* data folder contains the two data files analyzed by pymaceuticals.ipynb
* Starter_Code folder contains the files provided in BCS/Canvas for completing the challenge.
   


# References
The following references were used in creating the solution within the PyCitySchools folder:
 * Starter_Code\Pymaceuticals\pymaceuticals_starter.ipynb leveraged for file dependencies, setup, and some code execution as well as guiding output visuals

# Instructions

Prepare the Data

1. Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.
2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.
3. Display the updated number of unique mice IDs.

Generate Summary Statistics

Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.
Your summary statistics should include:
 * A row for each drug regimen. These regimen names should be contained in the index column.
 * A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

Create Bar Charts and Pie Charts

1. Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.
   * Create the first bar chart with the Pandas DataFrame.plot() method.
   * Create the second bar chart with Matplotlib's pyplot methods.
2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.
   * Create the first pie chart with the Pandas DataFrame.plot() method.
   * Create the second pie chart with Matplotlib's pyplot methods.

Calculate Quartiles, Find Outliers, and Create a Box Plot

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:
   * Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.
   * Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
   * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.
   * Determine outliers by using the upper and lower bounds, and then print the results.
2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

hint: All four box plots should be within the same figure. Use this Matplotlib documentation pageLinks to an external site. for help with changing the style of the outliers.

Create a Line Plot and a Scatter Plot

1. Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
2. Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
2. Plot the linear regression model on top of the previous scatter plot.
