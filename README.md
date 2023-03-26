# Pymaceuticals

You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Project Outline & Steps
1. Prepare the Data.
2. Generate Summary Statistics.
3. Create Bar Charts and Pie Charts.
4. Calculate Quartiles, Find Outliers, and Create a Box Plot.
5. Create a Line Plot and a Scatter Plot.
6. Calculate Correlation and Regression.

### Prepare the Data
1. Run the provided package dependency and data imports, and then merge the "mouse_metadat" and "study_results" DataFrames into a single DataFrame.
2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps. 
3. Display the updated number of unique mice IDs.

### Summary Statistics
1. Creates a DataFrame of summary statistics including:
   - A row for each drug regimen. These regimen names should be contained in the index column.
   - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.
   
### Bar Charts and Pie Charts
1. Generate two bar charts. Both charts should be identical and show the total number of time points for all mice tested for each drug regimen throughout the study.
    - Create the first bar chart with the Pandas DataFrame.plot() method.
    - Create the second bar chart with Matplotlib's pyplot methods.
2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.
    - Create the first pie chart with the Pandas DataFrame.plot() method.
    - Create the second pie chart with Matplotlib's pyplot methods.

### Quartiles, Outliers, Box Plots
1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:
    - Creating a grouped DataFrame that shows the last (greatest) time point for each mouse. 
    - Merging this grouped DataFrame with the original cleaned DataFrame.
    - Creating a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.
    - Looping through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. 
    - Appending the resulting final tumor volumes for each drug to the empty list.
    - Determining outliers by using the upper and lower bounds, and then printing the results.
2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

### Line Plot and Scatter Plot
1. Select a mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Correlation and Regression
1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment.
2. Plot the linear regression model on top of the previous scatter plot.
