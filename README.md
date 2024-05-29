# [Customer Segmentation/ Data Analytics](https://rushikeshpatil23.github.io/Customer-Segmentation-Data-analytics/)

## Goal of the project

The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing an RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behaviour-based approach grouping customers into segments. It groups the customers based on their previous purchase transactions. In this analysis, the customer segment was divided into 11 groups. The analysis will help in determining which customer segments should be targeted to enhance sales revenue for the company. A Sales Dashboard for Customer Segmentation is developed using Tableau and the data quality assessment and analysis are done using Python.

### Tableau Dashboard
![Animation](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/0c63c901-8fbe-457e-b71b-6face2a60404)

### Jupyter Notebooks
 - [CustomerAddresss_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/CustomerAddress_Cleaned.csv)
 - [CustomerDemograpic_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/CustomerDemographic_Cleaned.csv)
 - [Newcustomerslist_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/NewCustomerList_Cleaned.csv)
 - [Transaction_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/Transactions_Cleaned.csv)
 - [RFMAnalysis](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/RFM_Analysis.ipynb)

 - Analysis Approach
### 1. Data Quality Assessment and Data Cleaning
The data preparation, quality assessment and cleaning step was the first step towards generating useful insights from the data. After the cleaning process, exploratory data analysis on the dataset and identification of customer purchasing behaviours to generate insights can be performed.

In the data cleaning step, the data quality of the following datasets was first assessed. After a data quality assessment, the following data quality issues were observed and the necessary process to mitigate the issue was followed :

CustomerDemographics.xlsx :
1 Irrelevant column was present and such columns were dropped from the dataset.
There were 5 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
For the gender column, there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discrepancies in age distribution. An outlier was observed and the record was removed.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
NewCustomerList.xlsx :
5 Irrelevant columns were present and such columns were dropped from the dataset.
There were 4 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discrepancies in age distribution.
There was no data inconsistency.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
Transaction_data.xlsx :
The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.
There were 7 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
A new feature column 'Profit' was created which is the difference between the list price and the standard price.
There was no data inconsistency.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
CustomerAddress.xlsx :
For the states column, there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
Certain customer IDs from the Customer Demographics table were getting dropped in the Address table.


### 2. Exploratory Data Analysis on Customer Segments
After the data cleaning process, exploratory analysis of the dataset is performed and the following insights are obtained :

New vs Old Customers Age Distribution

Most New customers are aged between 40-49 also Old Customers the most of them are aged between 40-49
The lowest number for both types of customers is in the age bracket under 20 and above 80.
The automobile company is popular among New Customers aged 20-29 and 40-49.
A steep drop in customers is observed in the 30-39 age group among the New Customers

(![Screenshot 2024-05-29 132323](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/684fdc75-290e-4fb8-9741-522b21f5986a)![Screenshot 2024-05-29 132307](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/209b83d4-a8cc-433d-8c0b-f6cec3605ba5)

- Bike purchases over the last 3 years by Gender

Females made most bike purchases over the last 3 years. Approximately 51% of the bike purchases are done by Females compared to 49% of the purchases being done by Male.
The Female purchases are 10,000 more than that of Male purchases (numerically).

![Screenshot 2024-05-29 132857](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/1328bfd0-a225-4c5e-b912-904ea62a40a2)
