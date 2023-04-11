# Alteryx Superstore data transformation

Introduction:

This Alteryx project is designed to clean and prepare the "Superstore" dataset for further analysis. The project includes steps to remove blank rows, replace null values, change data types, assign state abbreviations, select useful columns, and verify the completeness of random data. This document serves as a guide to understand the steps involved in the project.


![image](https://user-images.githubusercontent.com/114254453/231294502-0e1fb6ec-a6c1-45b3-85cc-c120db46dab9.png)
![image](https://user-images.githubusercontent.com/114254453/231294538-99d1edc8-58ae-4c85-8b4a-8e33484c17fd.png)

Step 1: Load the dataset "Superstore"

The first step is to load the "Superstore" dataset into Alteryx. To do this, open Alteryx and create a new workflow. Drag and drop the input tool onto the workflow and select the "Superstore" dataset. Connect the output of the input tool to the next step.

Step 2: Browse the data and delete blank rows and replace null with 0

Use the browse tool to visualize the data and check for any blank rows or null values. If any blank rows exist, use the filter tool to remove them. Replace any null values with 0 using the replace tool.

Step 3: Check the datatype and change it if it is necessary i.e. ID to Varchar

Check the data type of each column using the select tool. If any column needs to be converted to a different data type, use the select tool to change the data type. For example, if the ID column needs to be converted to Varchar, use the select tool and change the data type to Varchar.

Step 4: Assign abbreviation of every state using external database with state names and appropriate abbreviations for visualization purposes.

Assign state abbreviations using an external database that contains state names and their corresponding abbreviations. Use the join tool to join the Superstore dataset with the external database based on the state name column. Add a select tool to select the state abbreviation column and remove the state name column.

Step 5: Choose only columns that will come in handy to reduce set size

Select only the necessary columns to reduce the size of the dataset. Use the select tool to select the columns that will be used for further analysis and remove the rest.

Step 6: Use sample tool to check completion of random data

Use the sample tool to randomly select a small portion of the dataset to check for completeness. If any missing values or errors are found, go back and correct them.

Step 7: Save the set

Finally, save the cleaned and prepared dataset to a file using the output tool. The cleaned dataset is now ready for further analysis.

Conclusion:

This Alteryx project helps to clean and prepare the Superstore dataset for further analysis. The project involves several steps, including removing blank rows, replacing null values, changing data types, assigning state abbreviations, selecting useful columns, and verifying the completeness of random data. By following the steps outlined in this readme, the user can clean and prepare any dataset in Alteryx for further analysis.
