# [Customer Segmentation/ Data Analytics](https://rushikeshpatil23.github.io/Customer-Segmentation-Data-analytics/)

## Goal of the project

The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing an RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behaviour-based approach grouping customers into segments. It groups the customers based on their previous purchase transactions. In this analysis, the customer segment was divided into 11 groups. The analysis will help in determining which customer segments should be targeted to enhance sales revenue for the company. A Sales Dashboard for Customer Segmentation is developed using Tableau and the data quality assessment and analysis are done using Python.

### Tableau Dashboard
![Animation](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/0c63c901-8fbe-457e-b71b-6face2a60404)

### Jupyter Notebooks
 - [CustomerAddresss_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/CustomerAddress_Cleaned.csv)
 - [CustomerDemograpic_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/Customer%20Demographic.ipynb)
 - [Newcustomerslist_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/NewCustomerList_Cleaned.csv)
 - [Transaction_cleaned.csv](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/Transactions.ipynb)
 - [RFMAnalysis](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/blob/main/RFM_Analysis.ipynb)

 - Analysis Approach
### 1. Data Quality Assessment and Data Cleaning
The data preparation, quality assessment and cleaning step was the first step towards generating useful insights from the data. After the cleaning process, exploratory data analysis on the dataset and identification of customer purchasing behaviours to generate insights can be performed.

In the data cleaning step, the data quality of the following datasets was first assessed. After a data quality assessment, the following data quality issues were observed and the necessary process to mitigate the issue was followed :

- CustomerDemographics.xlsx :
1 Irrelevant column was present and such columns were dropped from the dataset.
There were 5 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
For the gender column, there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discrepancies in age distribution. An outlier was observed and the record was removed.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
- NewCustomerList.xlsx :
5 Irrelevant columns were present and such columns were dropped from the dataset.
There were 4 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discrepancies in age distribution.
There was no data inconsistency.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
- Transaction_data.xlsx :
The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.
There were 7 columns where Missing values were present. For such columns based on the volume of the missing values either the records were dropped or appropriate values were imputed at places of missing values
A new feature column 'Profit' was created which is the difference between the list price and the standard price.
There was no data inconsistency.
Checked whether there are duplicate records present in the dataset. In this dataset, there were no duplicate records.
- CustomerAddress.xlsx :
For the states column, there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.
Certain customer IDs from the Customer Demographics table were getting dropped in the Address table.


### 2. Exploratory Data Analysis on Customer Segments
After the data cleaning process, exploratory analysis of the dataset is performed and the following insights are obtained :

New vs Old Customers Age Distribution

Most New customers are aged between 40-49 also Old Customers the most of them are aged between 40-49
The lowest number for both types of customers is in the age bracket under 20 and above 80.
The automobile company is popular among New Customers aged 20-29 and 40-49.
A steep drop in customers is observed in the 30-39 age group among the New Customers

![Screenshot 2024-05-29 132323](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/684fdc75-290e-4fb8-9741-522b21f5986a)![Screenshot 2024-05-29 132307](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/209b83d4-a8cc-433d-8c0b-f6cec3605ba5)

- Bike purchases over the last 3 years by Gender

Females made most bike purchases over the last 3 years. Approximately 51% of the bike purchases are done by Females compared to 49% of the purchases being done by Male.
The Female purchases are 10,000 more than that of Male purchases (numerically).

![Screenshot 2024-05-29 132857](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/1328bfd0-a225-4c5e-b912-904ea62a40a2)

- Wealth Segmentation by Age Category

Across all age categories the largest number of customers are from 'Mass Customer' Segment
The next category comes from the 'High Net Worth' customers.
In the age group 40-49, Affluent segment out performs the High Net Worth customers in terms of number of customers.

![Screenshot 2024-05-29 145817](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/f9c0a19f-0eeb-4a12-99d5-92790a74c206)
![Screenshot 2024-05-29 145836](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/b8f7d0ff-1bb5-4dfa-913d-de8acb17eb48)

- Cars owned by States

New South Wales has the largest number of people who donot own a car.
In Victoria the proportion is quite even.
In Queensland the number of people owning a car is greater than who donot have a car.

![Screenshot 2024-05-29 150114](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/81bc0ce4-6f1e-4cae-ba36-a2e52bb68e85)

### 3. RFM Analysis and Customer Segmentation
In this stage of analysis the customer segmentation was done by developing an RFM Model. The RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions.

In this analysis the customer segment was divided into 11 groups. The groups being :

Platinum Customers
Very Loyal Customers
Recent Customers
Potential Customers
Lost Customers
Losing Customers
Late Bloomer
High Risk Customers
Evasive Customers
Becoming Loyal
Almost lost Customers
![Screenshot 2024-05-29 150531](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/d5413c82-3707-4482-92d2-2d9bd9ebe5e6)

- Scatter Plots
- Recency vs Monetary :
The visualization shows that recent customers have purchased more products and generated relatively more revenue than the customers who visited a while ageo.

![Screenshot 2024-05-29 150912](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/411aac23-a611-4e9b-8e6f-e41767df7ca7)

- Frequency vs Monetary :
The visualization shows that customers belonging to Platinum/ Very Loyal/ Becoming Loyal Customer Segments have a greater frequency and generate greater monetary for the business

![Screenshot 2024-05-29 150937](https://github.com/RushikeshPatil23/Customer-Segmentation-Data-analytics/assets/169757781/12fc84c1-a59d-4f3c-b857-bb5ed3b44e84)

### Datasets Used
- The datasets used include:

- Raw_data.xlsx: This excel file dataset included the following sheets of data:
- Transactions_data.xlsx: This dataset included the transactions data of the customers across all the different states in Australia.
- NewCustomerList.xlsx: This dataset included the new customers who visted the automobile bike company recently.
- CustomerDemographic.xlsx: This dataset included entire details of the Customer Demographics.
- CustomerAddress.xlsx: This dataset included the address of the Customers.
  
### Tools and Technologies used
The tools used in this project include:

- Python - This was needed to conduct Data Quality Assessment and also for Data Cleaning processes. With Python libraries pandas, matplotlib, seaborn exploratory data analysis of the datasets and to gain useful -insights from the data was possible.
- Tableau - This Business Intelligence tool was required to explore data and create charts, graphs, visualizations to come up with a Sales Dashboard for Customer Segmenatation for the automobile bike company. 
