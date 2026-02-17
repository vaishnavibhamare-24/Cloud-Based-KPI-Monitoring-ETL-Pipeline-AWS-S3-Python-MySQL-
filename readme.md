## 📌 Project Overview

This project demonstrates an end-to-end cloud data pipeline built using AWS S3, Python, and MySQL to automate data ingestion, cleaning, validation, KPI computation, and storage for business analytics.

The system simulates a real-world order and delivery dataset, processes it using Python ETL logic, and stores curated data in a MySQL database for reporting and dashboard consumption.

## 🎯 Business Objective

Organizations receive operational data daily (orders, deliveries, cancellations).
Manual processing leads to:

Inconsistent reporting

Data quality issues

Delayed KPI visibility

Revenue leakage

This project automates the process to provide:

Clean and validated data

Automated KPI calculations

Anomaly detection

Structured database storage for BI tools

## 🏗️ Architecture
CSV Order Data
      ↓
AWS S3 (Raw Storage)
      ↓
Python ETL Script
      ↓
Data Cleaning & Validation
      ↓
MySQL Database (AWS RDS or Local MySQL)
      ↓
KPI Tables for Analytics / BI Dashboard

## 🛠️ Tech Stack

Python (Pandas, NumPy, SQLAlchemy)

AWS S3 (Cloud Storage)

MySQL (AWS RDS or local instance)

CloudWatch / Logging

Optional: Power BI / Tableau for visualization

## 🗄️ Database Schema (MySQL)
1️⃣ cleaned_orders
Column	Description
order_id	Unique order identifier
order_date	Order date
region	Sales region
product_category	Product segment
order_value	Revenue per order
discount	Discount applied
shipping_cost	Delivery cost
delivery_status	Delivered / Cancelled / Failed
delivery_time_mins	Delivery time

2️⃣ kpi_summary
Column	Description
report_date	Aggregation date
total_orders	Total number of orders
total_revenue	Sum of order values
cancellation_rate	% cancelled
failure_rate	% failed
avg_order_value	Average revenue
total_profit_proxy	Revenue - Discount - Shipping

## 🔍 Data Quality Checks Implemented

Missing value detection

Duplicate record removal

Negative value validation

Data type validation

Outlier detection using IQR

Logging of pipeline events

## 📊 KPIs Computed

Total Orders

Total Revenue

Average Order Value

Cancellation Rate

Failure Rate

Delivered Rate

Profit Proxy

Outlier Orders (High-Value Transactions)

## 🔄 ETL Process

Load raw CSV from S3

Perform validation checks

Clean missing and inconsistent data

Calculate operational KPIs

Insert cleaned data into MySQL

Insert KPI summary into MySQL

Log pipeline execution details

## 📈 Sample Insights Generated

Identified high cancellation rates in specific regions

Detected outlier orders impacting revenue reporting

Automated KPI generation reducing manual reporting effort

Structured data ready for BI dashboard integration

## 💡 Key Learning Outcomes

Cloud data ingestion using AWS S3

ETL pipeline design in Python

Data quality validation techniques

MySQL schema design for analytics

KPI engineering for operational monitoring

Logging and automation practices

### Author: Vaishnavi Bhamare
