# Alteryx
Readme File: Preparing Covid-19 Data from WHO for Visualization

Introduction

This readme file provides a brief overview of the steps taken to prepare global Covid-19 data downloaded from WHO for visualization purposes. 
The data was transformed using the Alteryx program to filter and clean the data, and prepare it for visualization in a tool such as Power BI.

Data Source

The data used in this project was obtained from the WHO website, and included global Covid-19 statistics.
The data was downloaded in CSV format and contained information on cases, deaths, and vaccinations by country, date, and continent.
Source: https://covid19.who.int/data

Data Preparation

The Alteryx program was used to transform the data for visualization. The following steps were taken:
1.	Input data: The data was imported into Alteryx as a CSV file.
2.	Cleanse data: Null rows were removed and null values were replaced with 0 to ensure data consistency.
3.	Filter data: The data was filtered to include only the dates from 01.01.2022 to 31.12.2022, and separated into data for each continent.
4.	Select Tool: The Select tool was used to choose only the columns that were relevant for visualization in Power BI. 
This included data on date, cases, deaths, and vaccinations by country, hospitalized people and cases and deaths per thousand residents.
5.	Save data: The final data was saved as a CSV file for use in Power BI.


![image](https://user-images.githubusercontent.com/114254453/230885409-3ba94699-053d-443a-98f2-715af21fe0f4.png)
Preview

![image](https://user-images.githubusercontent.com/114254453/230885510-98a22e7f-f656-494c-8bad-1f9f3e97e718.png)
Description with formulas

Conclusion
The global Covid-19 data downloaded from WHO was transformed using the Alteryx program to prepare it for visualization in Power BI. 
The data was cleansed, filtered, and selected to include only the relevant columns. 
The final data was saved as a CSV file for use in Power BI to create an informative dashboard.
