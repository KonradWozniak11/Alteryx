Introduction

Data Source: Download financial data from the BusinessRadar website. This data includes stock prices, financial results, and other relevant information for various companies. https://www.biznesradar.pl/raporty-finansowe-bilans/ORLEN

Excel Preparation: Import the downloaded data into Microsoft Excel. The Excel file will have a structure similar to what you retrieved from the website.

Save and Close Excel: After importing the data, save the Excel file and close it. Although manual processing using Excel's features like queries and text to columns is possible, we will leverage Alteryx to create a universal workflow for automated data processing.
It is worth mentioning that Alteryx also enables webscrapping.

Alteryx Workflow Steps in Data Transformation

1. Importing Data
   
Use the "Input Data" tool to import the Excel file. Make sure to select the option "First Row Contains Data" to facilitate the removal of header information.

Our starting data looks like this (dataset_before.xlsx in branch):
![image](https://github.com/KonradWozniak11/Alteryx/assets/114254453/753241d4-e9c3-4c99-a777-fde45f740319)
2. Data Cleansing

Use the "Data Cleansing" tool to perform initial data cleaning tasks, such as removing leading/trailing spaces and converting NULLs to 0's.

3. Extract Relevant Data

Apply the "Multi-Field Formula" tool to extract the financial data of interest, which is located before the "/" character in the cells. To achieve this, use the following formula:

REGEX_Replace([_CurrentField_], '/.*', '')

This formula extracts the relevant financial data and discards the rest, that we do not need. By using that we get:

![image](https://github.com/KonradWozniak11/Alteryx/assets/114254453/5c194acb-4603-42ab-9a31-a7726c0aade5)

4. Select and Rename Columns

Use the "Select" tool to choose the newly created columns containing the extracted financial data.

Rename these columns according to the specific financial metrics they represent.

5. Filtering

Apply the "Filter" tool to exclude data from the year 2023. This step is necessary as the data for that year consists of quarterly and semi-annual figures, which could distort the analysis.

6. Final Data Cleansing

Once again, use the "Data Cleansing" tool to remove any remaining whitespace and letters that were not extracted using the Regex formula.

7. Select Relevant Columns

Use the "Select" tool again to choose only the columns that are relevant to your analysis. This step helps optimize performance when creating visualizations. We also change datatypes.

8. Export Data

Finish the workflow by using the "Output Data" tool to save the cleaned and processed data in CSV format. (Dataset_after.csv in the branch)

Running the Workflow
After setting up the workflow as described above, you can run it by clicking the "Run" button within Alteryx.
The workflow will automatically perform the series of data transformation steps, resulting in a CSV file containing clean and organized financial data ready for analysis.
By following this Alteryx workflow, you can easily process financial data from various companies obtained from the Biznesradar website. The automated nature of this workflow streamlines the data processing tasks, ensuring that you have clean and accurate data for analysis without the need for manual intervention.
