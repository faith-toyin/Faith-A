## About
My name is Faith Adeogun, I am an undergraduate Finance student at the University of Lagos, eager to gain knowledge, skills, and opportunities for self-improvement and career growth. I am a motivated, highly organized, and detail-oriented virtual assistant and data analyst, I am proficient in using Excel, Power BI, Tableau, SQL, and python. I am committed to delivering high-quality service and achieving outstanding results. i enjoy exploring new data analysis tools and techniques, and i am always looking for opportunities to expand my skills.

My resume in [pdf](https://github.com/faith-toyin/Faith-Adeogun---Data-Analyst-portfolio-/blob/main/faith%20adeogun%20resume%20pdf.pdf)

### Table of Content
1. [About](#about)
2. [Portfolio Project](#portfolio-project)
    - [Project Overview](#project-overview)
    - [Data sources](#data-sources)
    - [Tools used](#tools-used)
    - [Data cleaning](#data-cleaning)
    - [Exploratory Data Analysis](#exploratory-data-analysis)
    - [Data Analysis](#data-analysis)
    - [Data Visualization](#data-visualization)
3. [Education](#education)
4. [Skills](#skills)
5. [Interest](#interest)
6. [Contacts](#contacts)


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
![image](https://github.com/user-attachments/assets/64183719-bb6f-4061-a047-7e8c44210a9a)

TOTAL FUNDED AMOUNT
```SQL
select sum(loan_amount) as total_funded_amount from Bank_Loan_data
```
![image](https://github.com/user-attachments/assets/3823b7b3-e72c-44d3-ae22-ff51f46f60fe)

TOTAL AMOUNT RECEIVED
```SQL
select sum(total_payment) as total_amount_received from bank_loan_data
```
![image](https://github.com/user-attachments/assets/b4abbd72-3c10-40f3-9661-a23da3a7f131)

AVG INTEREST RATE
```SQL
select ROUND(AVG(int_rate), 4) * 100 AS Avg_interest_rate from bank_loan_data
```
![image](https://github.com/user-attachments/assets/13481bcd-c946-4de3-ae4d-a567cd6e8bd5)

AVG DTI
```SQL
select ROUND(AVG(dti), 4) * 100 AS Avg_dti from bank_loan_data
```
![image](https://github.com/user-attachments/assets/c7089eb8-2e06-4e63-b5ca-308027401311)

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
![image](https://github.com/user-attachments/assets/a48f4e1d-7d78-4f27-aff8-388a1975c077)

GOOD LOAN APPLICATION
```SQL
SELECT COUNT(id) as good_loan_application from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
![image](https://github.com/user-attachments/assets/7563e007-4320-4bad-b285-f1ddb0afb46b)

GOOD LOAN FUNDED AMOUNT
```SQL
SELECT SUM(loan_amount) as good_loan_funded_amount from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
![image](https://github.com/user-attachments/assets/0d1e7c01-7900-47dc-af88-7bd2f47242bb)

GOOD LOAN RECEIVED AMOUNT
```SQL
SELECT SUM(total_payment) as good_loan_received_amount from bank_loan_data
where loan_status = 'Fully Paid' or loan_status = 'current'
```
![image](https://github.com/user-attachments/assets/451342b0-48fc-40d8-b054-d4715f023711)

BAD LOAN PERCENTAGE
```SQL
SELECT 
	(COUNT(CASE WHEN loan_status = 'Charged off' THEN id END)*
100
		/
		COUNT(id)) AS bad_loan_percentage
from bank_loan_data
```
![image](https://github.com/user-attachments/assets/96411bd1-688a-4687-858b-702b6d2a15fe)

BAD LOAN APPLICATION
```SQL
SELECT COUNT(id) as bad_loan_application from bank_loan_data
where loan_status = 'Charged off'
```
![image](https://github.com/user-attachments/assets/8253c788-fd57-4ff0-b70e-ddd96a6f46c6)

BAD LOAN FUNDED AMOUNT
```SQL
SELECT SUM(loan_amount) as bad_loan_funded_amount from bank_loan_data
where loan_status = 'Charged off'
```
![image](https://github.com/user-attachments/assets/b1849875-0dfa-4a0c-96a9-381cfd63980f)

BAD LOAN RECEIVED AMOUNT
```SQL
SELECT SUM(total_payment) as bad_loan_received_amount from bank_loan_data
where loan_status = 'Charged off'
```
![image](https://github.com/user-attachments/assets/200264b9-ffcc-4f84-9c41-45581802ae9e)


### Data Visualization

![image](https://github.com/user-attachments/assets/3544f963-4b80-40a8-af80-09115e8c8e24)

![image](https://github.com/user-attachments/assets/b77058e1-5e19-47bc-9982-4afef62062c2)

![image](https://github.com/user-attachments/assets/44c3a43c-b0e6-4345-9a4d-dc20f9498c86)
 
## Education
West African Senior Secondary School Certificate Examination (WASSCE)  ---- Rothmytemmy Schools    July 2019

University Of Lagos -- Akoka, Lagos, Nigeria: Bachelor of science-Bsc, Finance, December 2021-present

## Skills 
  #### Technical skills
    -Microsoft Office Suite
    -Google Workspace
    -Power BI
    -Tableau
    -SQL
    -Python
 #### Soft Skills
     -Verbal and Written Communication
     -Time Management
     -Attention to Details
     -Excellent Organization Skill
     -Self Motivation and Discipline

## Interest
  * Data Analytics
  * Content Creation
  * Research
  * Personal Development

## Contacts
   Email: faithadeogun1@gmail.com
  
   LinkedIn: https://www.linkedin.com/in/faith-adeogun/
  
