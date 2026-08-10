# SportsCompanyProject
A comprehensive work through of "codebasics" interactive project which can be found under the following link: https://www.youtube.com/watch?v=U6ZUKWdfSLY

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
#Data
* `/Data` — All the parent and child datasets provided for this project.

#Setup
* `/1_setup/setup_catalog.ipynb` — Defining catalog and table schemas.
* `/1_setup/utilities.ipynb` — Schema reference variables.
* `/1_setup/dim_date_table_creation.ipynb` — Creating a date table to later adjust the timestamps in child companies data.

#Dimensional Table Cleaning
* `/2_dimension_data_processing/1_Customer_data_processing.ipynb` — Customer data cleaning & validation (Bronze -> Silver -> Gold).
* `/2_dimension_data_processing/2_Products_data_processing.ipynb` — Product data cleaning & validation (Bronze -> Silver -> Gold).
* `/2_dimension_data_processing/3_pricing_data_processing.ipynb` — Time varied pricing data cleaning & validation (Bronze -> Silver -> Gold).

#Fact Table Cleaning
* `/3_fact_table_processing/1_full_load_fact.ipynb` — Historical order cleaning & validation (Bronze -> Silver -> Gold).
* `/3_fact_table_processing/2_incremental_load_fact.ipynb` — Incoming order cleaning & validation (Bronze -> Silver -> Gold).

#Dashboarding
* `/Dashboarding/SQL Queries/ParentIncrementalJoin.dbquery.ipynb` — Combining incremental and full load for dashboarding purposes.
* `/Dashboarding/SQL Queries/DashboardQuery.dbquery.ipynb` — Creating a denormalized view to utilize in dashboarding environments.
* `/Dashboarding/SportsProjectDashboard.pdf` — A sample dashboard.

#Orchestration
* `/SuccessfulRun.png` — A screenshot of a successful run in which a pipeline updates the dataset with daily additions.
