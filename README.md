# SportsCompanyProject
A comprehensive work through of "codebasics" interactive project which can be found under the following link: https://www.youtube.com/watch?v=U6ZUKWdfSLY
markdown# Project Title: [e.g., Real-Time Retail Lakehouse Ecosystem]

## 📌 Project Overview
Atlicon, a leading manufacturer of sporting equipment has recently acquired Sportsbar, a fast growing startup in the Energy bar industry. This project focuses on cleaning and joining Sportsbar's existing data under "Full Load" to match the Schema of the parent company, Atlicon. In addition to this, we also orchestrate a pipeline to append incoming data modeled under "Incremental Load" to mirror the dynamics of a real-world acquisition in which incoming daily data also needs to included in the parent dataset.

## 🛠️ Tech Stack & Architecture
* **Platform:** Databricks Community Edition
* **Language:** PySpark (Python), Spark SQL
* **Storage Layer:** Delta Lake (Bronze, Silver, Gold layers)
* **Orchestration:** Databricks Workflows / Jobs
## 📐 Data Pipeline Architecture
1. **Bronze (Raw):** Ingested CSV streams directly from AWS S3 Cloud Storage into Delta tables.
2. **Silver (Enriched):** Cleaned data by dropping null values, deduplicating records, and enforcing schemas with PySpark.
3. **Gold (Aggregated):** Aggregated metrics (e.g., channel based, time period based) using Spark SQL for business intelligence reporting.


## 📁 Repository Structure
* `/notebooks/01_data_ingestion.ipynb` — Raw data ingestion (Bronze).
* `/notebooks/02_data_transformation.ipynb` — Data cleaning & validation (Silver).
* `/notebooks/03_business_analytics.ipynb` — Final aggregations and KPIs (Gold).
