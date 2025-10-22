# 🛒 Walmart Sales Data Analysis using SQL

## 📘 Project Overview

This project focuses on **analyzing Walmart sales data** using **SQL** to gain insights into product performance, sales trends, and customer behavior across different branches.
The goal is to help understand key business metrics and improve sales strategies based on data-driven insights.

The dataset used in this project was obtained from the **Kaggle Walmart Sales Forecasting Competition**, which contains sales data from **three branches located in Mandalay, Yangon, and Naypyitaw**.

---

## 🎯 Project Objectives

The main purpose of this project is to:

* Analyze **sales performance** across branches and products
* Identify **top-performing products and categories**
* Examine **customer behavior** and segmentation
* Understand the **impact of time, day, and month** on sales
* Suggest strategies for improving profitability and operational efficiency

---

## 🧩 About the Dataset

The dataset includes **1,000 rows** and **17 columns**, covering sales transactions from three Walmart branches.

| Column                  | Description                              |
| ----------------------- | ---------------------------------------- |
| invoice_id              | Unique identifier for each transaction   |
| branch                  | Branch where the sale occurred           |
| city                    | City of the branch                       |
| customer_type           | Type of customer (Member / Normal)       |
| gender                  | Gender of the customer                   |
| product_line            | Category of product sold                 |
| unit_price              | Price per product                        |
| quantity                | Quantity sold                            |
| VAT                     | Value Added Tax applied (5%)             |
| total                   | Total transaction amount (including VAT) |
| date                    | Transaction date                         |
| time                    | Transaction time                         |
| payment_method          | Payment mode used                        |
| cogs                    | Cost of Goods Sold                       |
| gross_margin_percentage | Gross margin in percentage               |
| gross_income            | Gross income per transaction             |
| rating                  | Customer rating                          |

---

## ⚙️ Approach and Methodology

### 1. 🧹 Data Wrangling

* Checked for missing or NULL values
* Ensured proper data types for each column
* Created database and tables in SQL
* Defined all fields with `NOT NULL` constraints to maintain data integrity

### 2. 🧠 Feature Engineering

Generated additional columns to improve insights:

* `time_of_day` → to analyze sales in Morning, Afternoon, and Evening
* `day_name` → to find which day of the week each branch is busiest
* `month_name` → to find the most profitable month of the year

### 3. 🔍 Exploratory Data Analysis (EDA)

Used SQL queries to answer key business questions:

* Which product lines perform best?
* What are the top cities and branches by revenue?
* Which customer types bring in the most profit?
* Which payment methods are most used?
* What times of day see the highest sales?

---

## 📊 Key Business Insights

### 🛍️ Product Analysis

* Identified top-performing product lines and those needing improvement
* Found the most commonly used payment method
* Analyzed revenue, tax, and ratings by product line

### 💰 Sales Analysis

* Determined total revenue and profit per month
* Found peak months and branches for sales
* Discovered that **VAT** and **COGS** influence total revenue trends

### 👥 Customer Analysis

* Explored gender distribution and purchasing behavior
* Found that **Members** contribute higher revenue than **Normal customers**
* Identified which times of day and days of the week customers rate products highest

---

## 📈 Revenue and Profit Calculations

Key formulas used in the analysis:

[
\text{COGS} = \text{Unit Price} \times \text{Quantity}
]

[
\text{VAT} = 5% \times \text{COGS}
]

[
\text{Total (Gross Sales)} = \text{COGS} + \text{VAT}
]

[
\text{Gross Profit} = \text{Total} - \text{COGS}
]

[
\text{Gross Margin} = \frac{\text{Gross Profit}}{\text{Total Revenue}}
]

---

## 🧱 SQL Implementation

The project includes an SQL script (`SQL_queries.sql`) that:

* Creates the **WalmartSales** database and **sales** table
* Inserts data from the dataset
* Performs analytical queries to answer business questions

Example:

```sql
CREATE DATABASE IF NOT EXISTS walmartSales;

CREATE TABLE IF NOT EXISTS sales(
    invoice_id VARCHAR(30) PRIMARY KEY,
    branch VARCHAR(5) NOT NULL,
    city VARCHAR(30) NOT NULL,
    customer_type VARCHAR(30) NOT NULL,
    gender VARCHAR(30) NOT NULL,
    product_line VARCHAR(100) NOT NULL,
    unit_price DECIMAL(10,2) NOT NULL,
    quantity INT NOT NULL,
    tax_pct FLOAT(6,4) NOT NULL,
    total DECIMAL(12,4) NOT NULL,
    date DATETIME NOT NULL,
    time TIME NOT NULL,
    payment VARCHAR(15) NOT NULL
);
```

---

## 🏁 Conclusion

This SQL project demonstrates the use of **data wrangling**, **feature engineering**, and **analytical querying** to derive actionable insights from retail data.
It highlights how SQL can be used effectively to understand:

* Customer purchasing behavior
* Sales trends
* Profitability of product lines and locations

These insights can help businesses like Walmart **optimize inventory, pricing, and marketing strategies**.

---

## 👩‍💻 Author

**Abinaya Priya K**
*Data Analytics Project – SQL Domain*


