# SQL-Retail-Analytics-Portfolio
End-to-end relational data modeling, data quality remediation, and advanced SQL analytics for a retail enterprise.
# 🛒 Retail Store SQL Data Modeling & Advanced Analytics

## 📌 Project Overview
This project demonstrates an end-to-end database implementation for a retail enterprise using *MySQL*. It covers Star Schema design, automated diagnostic data cleaning, core business KPI tracking, and advanced window functions to drive business insights.

---

## 📐 Data Architecture & ER Diagram
The database follows a normalized *Star Schema* centered around business transactions.

<img width="1333" height="747" alt="retail_db_diagram(1)" src="https://github.com/user-attachments/assets/1f31e35a-8c5e-4c97-835d-079eed663018" />


### Schema Breakdown:
* *dim_customers*: Demographics table containing unique customer attributes (customer_id, gender, age).
* *dim_products*: Product catalog detailing categories and base pricing (category, default_price).
* *fact_transactions*: Core transactional table capturing line-item sales metrics (transaction_id, customer_id, category, quantity, price_per_unit, total_amount, transaction_date).

---

## 🛠️ Repository Structure
* [scripts/schema.sql](./scripts/schema.sql): DDL scripts for table structures and foreign key constraints.
* [scripts/data_cleaning.sql](./scripts/data_cleaning.sql): Remediation logic for handling duplicates, missing values, and orphan records.
* [scripts/eda_and_kpis.sql](./scripts/eda_and_kpis.sql): Executive queries measuring AOV, total revenue, monthly growth, and order volume.
* [scripts/advanced_analytics.sql](./scripts/advanced_analytics.sql): Complex analytical queries using CTEs, DENSE_RANK(), LAG(), and cumulative window functions.

  <img width="1335" height="749" alt="retail_db_queries" src="https://github.com/user-attachments/assets/49aed8eb-c126-43e9-af25-4072accb8d62" />


---

## 💡 Key Technical Highlights
1. *Data Quality Audit:* Implemented window-function-based deduplication and subquery-driven missing value imputation based on individual customer historical averages.
2. *Customer Segmentation:* Leveraged CTEs to partition high-value repeat buyers vs. one-time transaction customers.
3. *Advanced Window Functions:* Calculated running spend totals per customer and isolated top spenders within product categories using DENSE_RANK().
