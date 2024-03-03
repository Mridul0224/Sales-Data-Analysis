# Sales Data Analysis

## Table of Contents
1. [Problem Statement](#problem-statement)
2. [Data Discovery](#data-discovery)
3. [Data Analysis using MySQL](#data-analysis-using-mysql)
4. [Data Cleaning and ETL](#data-cleaning-and-etl)
5. [Data Modeling](#data-modeling)
6. [Data Analysis with DAX](#data-analysis-with-dax)
7. [Dashboard and Report Development](#dashboard-and-report-development)
8. [Tools, Software, and Libraries](#tools-software-and-libraries)
9. [References](#references)

## Problem Statement
AtliQ Hardware, a leading supplier of computer hardware across India, faces challenges due to rapidly evolving market dynamics. The sales director is struggling with tracking sales effectively, which is hindering growth and performance. This project seeks to address these challenges by developing a data analysis and visualization solution to facilitate informed decision-making.

## Data Discovery
The project begins with leveraging the AIMS Grid for project planning to clearly define the purpose, stakeholders, desired end results, and success criteria. This structured approach ensures clarity and alignment with business objectives from the outset.

## Data Analysis using MySQL
An in-depth analysis of sales data is performed using MySQL to uncover trends, insights, and areas of opportunity. This includes importing data, examining table structures, and conducting various queries to understand customer behaviors and transaction patterns.

The SQL database dump (`db_dump.sql`) is available for download. This file contains the necessary data for importing into MySQL Workbench, setting the stage for our analysis.

### Identifying and Correcting Data Discrepancies

We observed and corrected various data inconsistencies, such as incorrect market values and negative transaction amounts. These corrections were vital for ensuring the accuracy of our subsequent analyses.

### Key SQL Queries for Analysis

Below are some of the SQL queries we executed to uncover insights from the data:

```sql
-- Check for incorrect market values
SELECT * FROM sales.market WHERE market_value_condition;

-- Identify transactions with negative amounts
SELECT * FROM sales.transactions WHERE amount < 0;

-- Calculate total revenue for 2020 in Chennai
SELECT SUM(sales_amount) FROM sales.transactions
JOIN sales.date ON transactions.order_date = date.date
WHERE year = 2020 AND market_code = 'Mark001';


## Data Cleaning and ETL (Extract, Transform, Load)
This stage focuses on preparing the data for analysis, connecting MySQL databases to Power BI, importing data, and utilizing Power Query for data cleaning. Steps include filtering out inconsistencies, removing duplicates, and currency conversion to ensure data integrity.

## Data Modeling
Post-cleaning, the data undergoes modeling to facilitate efficient analysis. The model organizes data into a star schema, simplifying the relationships between different data entities and enabling more straightforward query execution.

## Data Analysis with DAX
Advanced analysis is conducted using DAX (Data Analysis Expressions) within Power BI. This includes creating measures and calculations to derive deeper insights into sales performance, customer behaviors, and other vital business metrics.

## Dashboard and Report Development
Dynamic dashboards and reports are developed using Microsoft Power BI, providing real-time insights into sales performance and trends. This empowers the sales director and other stakeholders with actionable information for strategic decision-making.

## Tools, Software, and Libraries
- **MySQL**: For database management and data analysis.
- **Microsoft Power BI**: For creating interactive dashboards and reports.
- **Power Query Editor**: For data cleaning and transformation.
- **DAX Language**: For conducting advanced data analysis.

## References
- Engage with comprehensive guides and tutorials from Codebasics and SQLBI.
- Explore official documentation and best practices from MySQL and Microsoft.
