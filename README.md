![Sample Image](https://depositphotos.com/editorial/mishawaka-circa-august-2018-walmart-retail-location-walmart-boosting-its-207378496.html)


# Walmart-Sales-Data-Analysis
## Overview
This project focuses on analyzing Walmart's sales data to identify top-performing stores and products, uncover sales trends, and gain insights into customer behavior. The main goal is to improve and optimize sales strategies. The dataset for this analysis comes from the Walmart Sales Forecasting Competition on Kaggle.

## Project Objectives
The primary aim of this project is to derive insights from Walmart's sales data by examining the various factors that impact sales performance across different branches.

## Data Overview
The dataset used in this project was sourced from the Kaggle Walmart Sales Forecasting Competition and includes sales transactions from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. It consists of 17 columns and 1,000 rows, providing detailed insights into the sales performance at each location.
| Column            | Description                                   | Data Type        |
|-------------------|-----------------------------------------------|------------------|
| invoice_id        | Invoice of the sales made                     | VARCHAR(30)      |
| branch            | Branch at which sales were made               | VARCHAR(5)       |
| city              | The location of the branch                    | VARCHAR(30)      |
| customer_type     | The type of the customer                       | VARCHAR(30)      |
| gender            | Gender of the customer making purchase        | VARCHAR(10)      |
| product_line      | Product line of the product sold               | VARCHAR(100)     |
| unit_price        | The price of each product                     | DECIMAL(10, 2)   |
| quantity          | The amount of the product sold                 | INT              |
| VAT               | The amount of tax on the purchase             | FLOAT(6, 4)      |
| total             | The total cost of the purchase                | DECIMAL(12, 4)   |
| date              | The date on which the purchase was made       | DATETIME         |
| time              | The time at which the purchase was made       | TIME             |
| payment           | The total amount paid                         | DECIMAL(10, 2)   |
| cogs              | Cost Of Goods sold                            | DECIMAL(10, 2)   |
| gross_margin_pct  | Gross margin percentage                       | FLOAT(11, 9)     |
| gross_income      | Gross Income                                  | DECIMAL(12, 4)   |
| rating            | Rating                                        | FLOAT(2, 1)      |


## Analysis List:

1.	Product Analysis

> Analyze the data to gain insights into the performance of different product lines, identify top-performing products, and highlight opportunities for improving underperforming product lines.

2.	Sales Analysis
   
> This analysis focuses on examining sales trends across product lines to evaluate the effectiveness of sales strategies and identify necessary adjustments to improve sales performance.

3.	Customer Analysis

> This analysis aims to identify different customer segments, explore their purchasing patterns, and assess the profitability of each segment to gain insights that can guide business strategies.

## Approach Used
***1.	Data Wrangling***

In the initial phase, the data is inspected for NULL or missing values, and appropriate data replacement strategies are applied to handle them effectively.
- A database is created, followed by building a table and inserting the data.
- Columns with NULL values are selected. However, since the tables were created with the "NOT NULL" constraint for each field, no NULL values are present in the database, ensuring clean data from the outset.

***2.	Feature Engineering***

Feature engineering is employed to create new columns from the existing data, providing deeper insights into sales patterns.
- time_of_day: A new column categorizing sales into Morning, Afternoon, and Evening, helping identify the time of day with the highest sales volume.
- day_name: A column that extracts the day of the week (e.g., Mon, Tue, Wed) for each transaction, revealing which day of the week each branch experiences the most activity.
- month_name: A column that extracts the month (e.g., Jan, Feb, Mar) of each transaction, offering insights into which months generate the highest sales and profits.

***3.  Exploratory Data Analysis (EDA)***

Conducting exploratory data analysis is essential to address the project's listed questions and objectives.

## Business Questions to Answer

### Generic Questions
1.	How many distinct cities are present in the dataset?
2.	In which city is each branch situated?

### Product Analysis
1.	How many distinct product lines are there in the dataset?
2.	What is the most common payment method?
3.	What is the most selling product line?
4.	What is the total revenue by month?
5.	Which month recorded the highest Cost of Goods Sold (COGS)?
6.	Which product line generated the highest revenue?
7.	Which city has the highest revenue?
8.	Which product line incurred the highest VAT?
9.	Retrieve each product line and add a column product_category, indicating 'Good' or 'Bad,' based on whether its sales are above the average.
10.	Which branch sold more products than average product sold?
11.	What is the most common product line by gender?
12.	What is the average rating of each product line?

### Sales Analysis
1.	Number of sales made in each time of the day per weekday
2.	Identify the customer type that generates the highest revenue.
3.	Which city has the largest tax percent/ VAT (Value Added Tax)?
4.	Which customer type pays the most VAT?

### Customer Analysis
1.	How many unique customer types does the data have?
2.	How many unique payment methods does the data have?
3.	Which is the most common customer type?
4.	Which customer type buys the most?
5.	What is the gender of most of the customers?
6.	What is the gender distribution per branch?
7.	Which time of the day do customers give most ratings?
8.	Which time of the day do customers give most ratings per branch?
9.	Which day of the week has the best avg ratings?
10.	Which day of the week has the best average ratings per branch?
