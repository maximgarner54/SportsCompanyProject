# SportsCompanyProject
A comprehensive work through of "codebasics" interactive project which can be found under the following link: https://www.youtube.com/watch?v=U6ZUKWdfSLY
markdown# Project Title: [e.g., Real-Time Retail Lakehouse Ecosystem]

## 📌 Project Overview
A brief 3-4 sentence summary explaining what problem you solved. 
Example: "Built an end-to-end data engineering pipeline to ingest, clean, and analyze 50GB of streaming retail transaction data using Databricks and the Medallion Architecture."

## 🛠️ Tech Stack & Architecture
* **Platform:** Databricks Community Edition
* **Language:** PySpark (Python), Spark SQL
* **Storage Layer:** Delta Lake (Bronze, Silver, Gold layers)
* **Orchestration:** Databricks Workflows / Jobs
## 📐 Data Pipeline Architecture
1. **Bronze (Raw):** Ingested JSON/CSV streams directly from Cloud Storage into Delta tables.
2. **Silver (Enriched):** Cleaned data by dropping null values, deduplicating records, and enforcing schemas with PySpark.
3. **Gold (Aggregated):** Aggregated metrics (e.g., daily sales, active users) using Spark SQL for business intelligence reporting.

## 🚀 Key Achievements & Results
* Optimized PySpark shuffling and partitioning, reducing notebook execution time by **35%**.
* Handled schema evolution seamlessly using **Delta Lake properties**.

## 📁 Repository Structure
* `/notebooks/01_data_ingestion.ipynb` — Raw data ingestion (Bronze).
* `/notebooks/02_data_transformation.ipynb` — Data cleaning & validation (Silver).
* `/notebooks/03_business_analytics.ipynb` — Final aggregations and KPIs (Gold).
