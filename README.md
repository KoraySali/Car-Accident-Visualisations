# Car Accident Visualisations
# Title: Exploratory Data Analysis and Interactive Visualization of Road Accident Data

## Description:
This data science portfolio project delves into the intricate process of conducting in-depth exploratory data analysis (EDA) and creating interactive visualizations for road accident data. The project harnesses the power of Python, particularly libraries like pandas, numpy, seaborn, matplotlib, plotly, and folium, to dissect the dataset, uncover hidden insights, and present the findings in an engaging visual format. The primary goal is to unearth trends and patterns in road accidents, especially when influenced by specific weather conditions.

### Technical Aspects:

* Data Import: The code kicks off by importing essential Python libraries, including pandas, numpy, seaborn, matplotlib, plotly, and folium.
The main dataset, containing road accident records, is loaded into a pandas DataFrame named 'Accidents_df' using the pd.read_csv method. This provides an efficient structure for data manipulation and analysis.

### Data Preprocessing:

# Missing Value Handling: 

To ensure data quality, a check for missing values is executed using the .isnull().sum() method. The results, indicating the count of missing values for each column, are displayed for reference.

* Data Cleansing:
Rows with missing values are removed from the DataFrame using the .dropna(inplace=True) method. This step is essential for maintaining data integrity.
Date Format Transformation: The 'Date' column is transformed into a datetime format to enable precise temporal analysis. The pd.to_datetime method is employed, specifying the date format via the format='%d/%m/%Y' parameter.

* Data Filtering:
The code applies a filter to segment the data into distinct subsets, focusing on accidents occurring under specific weather and road surface conditions.
'Accidents_df_ice' is created to represent accidents during icy weather conditions (when 'Weather_Conditions' is not equal to 7 and 'Road_Surface_Conditions' is equal to 4).
'Accidents_df_fog' is formed to encapsulate accidents during foggy weather conditions (when 'Weather_Conditions' equals 7 and 'Road_Surface_Conditions' does not equal 4).

### Data Visualization:

* Folium HeatMaps:
Dynamic heatmaps are constructed using the Folium library to visualise the geographical distribution of accidents for both icy and foggy conditions.

These heatmaps incorporate a time dimension, allowing viewers to explore how accident patterns evolve over time, especially in relation to varying speed limits. This is achieved by employing the HeatMapWithTime plugin from Folium.

* Marker Clustering:
Another visualization technique involves marker clustering. This method groups accidents based on their geographical proximity, thus creating clusters.

Each marker is assigned a distinct size and colour, corresponding to the accident's severity. Red markers represent accidents with the highest severity (Level 1), yellow for Level 2, and blue for lower severity levels.

The marker cluster maps are produced for both icy and foggy conditions.

* Exporting Visualizations:
To ensure the generated visualizations are accessible outside the code environment, the code saves them as HTML files.
Four files are produced: 'cluster_ice_map.html', 'cluster_fog_map.html', 'heatmap_ice.html', and 'heatmap_fog.html'. These files can be shared, embedded in reports, or used for interactive exploration.

!(https://github.com/KoraySali/Car-Accident-Visualisations/blob/master/Number%20of%20accidents%20ice%20vs%20fog.png?raw=true)

## Summary:

To wrap up the analysis, the code provides insightful statistics for both icy and foggy conditions. These statistics include the total number of accidents, the count of days with accidents, and the average number of accidents per day for each condition. This numerical analysis offers a succinct summary of the dataset. In summary, this project showcases the areas of data preprocessing, exploratory data analysis, and interactive data visualization. By applying advanced Python libraries and techniques, this project offers a valuable demonstration of data-driven insights into road accidents, particularly under different weather conditions, making it a compelling addition to a data science portfolio.
