#  Data Analysis Project

## Project Title: BANK LOAN REPORT

### Project Overview
In order to monitor and assess our bank's lending activities and performance, we need to create a comprehensive Bank Loan Report. This report aims to provide insights into key loan-related metrics and their changes over time. The report will help us make data-driven decisions, track our loan portfolio's health, and identify trends that can inform our lending strategies.

### Data Sources
The primary source of data used here is "financial_loan.CSV" and this is an open source data that can be freely downloaded from an open source online such as Kaggle [Download Here](https://www.kaggle.com/datasets) or any other data site

### Tools Used
- Microsoft Excel for Data cleaning and Analysis
- Structured Query Language(SQL) for querying data
- Power BI for Data Visualization
- Github for building portfolio

### Data Cleaning
In the initial phase of the data cleaning, the following actions are performed;
 - Data loading and inspection
 - Removing Duplicates
 - Handling missing values
 - Data formatting

### Exploratory Data Analysis
This involves exploring the data to answer some questions about the data such as;
  1. Total loan Application
  2. Total funded Amount
  3. Total Amount Received
  4. Average interest rate
  5. Average Debt-to-income ratio (DTI)

### Data Analysis
This is where we include some basic lines of code or queries used during the analysis;

TOTAL LOAN APPLICATION
```SQL
select count(id) as total_loan_applications from Bank_Loan_data
```
TOTAL FUNDED AMOUNT
```SQL
select sum(loan_amount) as total_funded_amount from Bank_Loan_data
```
TOTAL AMOUNT RECEIVED
```SQL
select sum(total_payment) as total_amount_received from bank_loan_data
```
AVG INTEREST RATE
```SQL
select ROUND(AVG(int_rate), 4) * 100 AS Avg_interest_rate from bank_loan_data
```
AVG DTI
```SQL
select ROUND(AVG(dti), 4) * 100 AS Avg_dti from bank_loan_data
```
#### Good Loan V Bad Loan
GOOD LOAN PERCENTAGE
```SQL
SELECT 
	(COUNT(CASE WHEN loan_status = 'Fully Paid' or loan_status = 'current' THEN id END)*
100
		/
		COUNT(id)) AS good_loan_percentage
from bank_loan_data
```
GOOD LOAN APPLICATION
```SQL
SELECT COUNT(id) as good_loan_application from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
GOOD LOAN FUNDED AMOUNT
```SQL
SELECT SUM(loan_amount) as good_loan_funded_amount from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
GOOD LOAN RECEIVED AMOUNT
```SQL
SELECT SUM(total_payment) as good_loan_received_amount from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
BAD LOAN PERCENTAGE
```SQL
SELECT 
	(COUNT(CASE WHEN loan_status = 'Charged off' THEN id END)*
100
		/
		COUNT(id)) AS bad_loan_percentage
from bank_loan_data
```
BAD LOAN APPLICATION
```SQL
SELECT COUNT(id) as bad_loan_application from bank_loan_data
where loan_status = 'Charged off'
```
BAD LOAN FUNDED AMOUNT
```SQL
SELECT SUM(loan_amount) as bad_loan_funded_amount from bank_loan_data
where loan_status = 'Charged off'
```
BAD LOAN RECEIVED AMOUNT
```SQL
SELECT SUM(total_payment) as bad_loan_received_amount from bank_loan_data
where loan_status = 'Charged off'
```

### Data Visualization

![image](https://github.com/user-attachments/assets/3544f963-4b80-40a8-af80-09115e8c8e24)


 
