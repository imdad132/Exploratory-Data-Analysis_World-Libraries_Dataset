# Exploratory-and-Statistical-Analysis_World-Libraries_Dataset

## Data Import and Setup

The code begins by using Google Colab's file upload functionality to import a CSV file from the user's desktop. It then imports essential data analysis libraries including pandas for data manipulation, numpy for numerical operations, matplotlib and seaborn for visualization.

## Loading and Exploring the Dataset
The script loads a CSV file called "World Libraries.csv" using the latin-1 encoding, which helps handle special characters that might be present in international data. It then displays the first few rows to get an initial look at the data structure. The code checks for missing values in each column and displays all column names to understand the dataset's composition.

## Data Cleaning
The data cleaning process involves three main steps:

Renaming a column with a problematic name that contains a newline character from 'Expenditures \n(US Dollars)' to simply 'Expenditures'
Removing all rows that contain any missing values to ensure complete data for analysis
Dropping three columns that aren't needed for the analysis: "Country", "Expenditures", and "Total Librarians"

## Correlation Analysis
The code performs correlation analysis on three numerical columns: 'Total Libraries', 'Total Volumes', and 'Total Users'. This creates a correlation matrix showing how strongly these variables are related to each other, with coefficients ranging from -1 (strong negative correlation) to 1 (strong positive correlation).

## Regional Analysis
This section conducts a detailed regional analysis for each of the three key metrics. For each metric (Total Libraries, Total Volumes, Total Users), the code:

Calculates the total sum across all regions
Determines each region's percentage contribution to the global total
Sorts the regions from highest to lowest percentage contribution
Prints these distributions to show which regions have the highest values for each metric

## Data Visualizations 

### Libraries vs Users Scatter Plot
The part helps creating a scatter plot visualizing the relationship between the number of libraries and users. It calculates and displays the correlation coefficient between these two variables in the plot's title, helping to quantify the strength of this relationship. The visualization is then saved as a PNG file.

### Regional User Analysis Bar Chart
This visualization shows the total number of library users by region in a bar chart format. The data is grouped by region, the total users for each region are summed, and the results are displayed in a bar chart. This visualization provides a clear comparison of library usage across different global regions.

### Interactive Geo-Spatial Map Visualization
The final section creates an interactive geographical visualization using the folium library:

The code installs and imports necessary mapping libraries
Defines approximate geographical coordinates for each region on a world map
Creates a base world map
Calculates the total number of libraries in each region
Places circle markers on the map for each region, with the circle size proportional to the number of libraries
Adds tooltips showing region name and total libraries when hovering over each marker
Saves this interactive visualization as an HTML file and displays it in the notebook

This interactive map provides a geographical perspective on library distribution across world regions, making patterns more immediately visible than in tabular data.
