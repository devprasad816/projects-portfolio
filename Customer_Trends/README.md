# Customer Shopping Trends Analysis

## Business Problem Statement
A leading retail company aims to better understand customer shopping behavior to improve sales performance, customer satisfaction, and long-term loyalty. By analyzing purchasing patterns across demographics, product categories, seasons, payment methods, discounts, and sales channels (online vs. offline), this project seeks to identify the key drivers influencing consumer decisions and provide actionable insights to optimize marketing and product strategies.

## Project Deliverables
- **Data Preparation & Modeling (Python):** Cleaned, transformed, and engineered features from raw transactional data to prepare it for analysis.
- **Data Analysis (SQL):** Structured the data and executed business-focused queries to uncover insights on customer segments, purchase drivers, discounts, and subscriptions.
- **Visualization & Insights (Power BI):** Developed an interactive dashboard to highlight trends, patterns, and performance metrics for stakeholder decision-making.
- **Report Writing:** Documented key findings, insights, and business recommendations in a concise analytical report.
- **GitHub Repository:** Organized all project assets, including Python notebooks, SQL queries, Power BI files, datasets, and documentation, in a professional repository structure.

## Project Path

```
Customer_Trends/
├── data/
│   ├── raw/
│   │   └── customer_shopping_behaviour.xlsx
│   └── processed/
│       └── customer_shopping_trends_clean.xlsx
├── notebooks/
│   └── customer_shopping_trends_eda.ipynb
├── sql/
│   └── customer_shopping_trends_analysis.sql
├── powerbi/
│   └── Customer_Shopping_Trends.pbix
├── reports/
│   └── Customer_Shopping_Behavior_Analysis.pdf
├── visuals/
│   └── dashboard.png
└── README.md
```

---

## Project Overview

This project analyzes customer shopping behavior using transactional data from ~3,900 purchases to identify trends across demographics, product categories, shipping preferences, payment methods, seasons, and sales channels, supporting data-driven business decisions in marketing, product strategy, and operations.

---

## Dataset Summary

* **Records:** ~3,900 transactions
* **Columns:** 18
* **Key Data Points:**

  * **Customer Demographics:** Age, Gender, Location, Subscription Status
  * **Shopping Behavior:** Discount Applied, Promo Code Used, Review Rating, Shipping Type, Purchase Frequency
  * **Transactional Metrics:** Revenue, Orders, Product Category
* **Missing Data:** 37 missing values in `review_rating`, handled during data cleaning

---

## ETL & Data Preparation (Python)

Data preparation and feature engineering were performed using Python:

* Loaded raw data from Excel using Pandas
* Performed structural checks using `df.info()` and `df.describe()`
* Imputed missing review ratings using **median rating per product category**
* Standardized column names to **snake_case**
* Created derived features:

  * `age_group` for demographic analysis
  * `purchase_frequency_days` for behavioral insights
* Exported cleaned data for downstream SQL analysis and Power BI visualization

---

## Exploratory Data Analysis (SQL – PostgreSQL)

Structured analysis was performed using PostgreSQL to answer business-driven questions. The SQL file contains both **questions and corresponding queries**.

Key analyses include:

* Revenue contribution by gender and age group
* Subscriber vs non-subscriber spending comparison
* Impact of discounts on high-spending customers
* Shipping type comparison (Standard vs Express)
* Top-rated and top-selling products
* Discount-dependent products analysis
* Customer segmentation (New, Returning, Loyal)
* Repeat buyers and subscription relationship
* Top 3 products per category using `DENSE_RANK()`

Database Details:

* **DBMS:** PostgreSQL
* **Database:** perfectdb
* **Table:** orders

---

## Power BI Dashboard

An interactive Power BI dashboard was developed to communicate insights to stakeholders.

### Dashboard Preview

![Customer Shopping Trends Dashboard](visuals/Dashboard.png)

### Dashboard Highlights

* Executive KPIs: Total Revenue, Total Customers, Average Rating, Average Revenue
* Category vs Shipping Type heatmap to identify fulfillment preferences
* Customer distribution by gender and age group
* Seasonal order trends
* Payment method preferences
* Top products by revenue
* Target vs actual revenue performance

The dashboard focuses on **descriptive and diagnostic analytics**, aligning with the available transactional data.

---

## Business Recommendations

* **Subscription Growth:** Promote exclusive benefits to convert high-frequency buyers
* **Customer Loyalty:** Design seasonal rewards for repeat customers
* **Product Optimization:** Prioritize top-rated and best-selling products in campaigns
* **Discount Strategy:** Use targeted discounts for loyal customers while maintaining margins
* **Operational Focus:** Optimize shipping and payment options based on customer preferences

---

## Data Limitations

This dataset does not contain persistent customer identifiers across long time periods. As a result, advanced retention metrics such as Customer Lifetime Value (CLV) were not calculated. Insights focus on **transactional behavior and aggregated customer trends**.

---

## How to Use This Project

1. Review raw and cleaned datasets in the `data/` directory
2. Explore Python-based cleaning and feature engineering in the notebook
3. Review business-driven SQL queries in the `sql/` folder
4. Open the Power BI file to interact with the dashboard
5. Refer to the PDF report for summarized insights

---

## Project Type

End-to-end Data Analytics Project | Python • SQL • Power BI • EXCEL 
