# 🚀Snowflake HR Analytics Lakehouse
A complete HR Analytics Lakehouse built on Snowflake, following the Medallion Architecture (Bronze → Silver → Gold) and powered by Dynamic Tables for automated, incremental ELT.

This project simulates a real enterprise (test/mock) HR data platform with:
- 1,850 employees
- 350 terminated employees
- 12 departments
- 50 supervisors
- Full HR history (job history, employment status, location tracking)
- It is designed for People Analytics, Attrition Insights, Department Performance, and Hiring Trend Dashboards.

## ⭐ Project Highlights
- Medallion Architecture: Bronze (raw), Silver (cleaned), Gold (analytics)
- Dynamic Tables: Automated incremental ELT pipelines
- Synthetic enterprise-scale HR dataset: 1,850 employees + related HR dimensions
- Department & attrition analytics: Gold metrics for BI dashboards
- Export schema for BI tools: Clean, flattened views for Power BI/Tableau
- Fully modular SQL project structure: Easy to extend and productionize

🟫 Bronze Layer — Raw Data
- Raw ingestion tables for all HR entities
- Synthetic data generated directly in Snowflake
- Schema-on-read, no transformations

🟦 Silver Layer — Cleaned & Modeled
- Dynamic Tables clean and standardize raw data
- Normalize names, emails, job titles, locations
- Prepare dimensions and fact-like structures

🟨 Gold Layer — Analytics & Metrics
- Employee Master (status + location + supervisor + department)
- Department Metrics (active headcount, terminated count)
- Attrition Metrics (department-level attrition %)
- Hiring Trends (month-over-month hiring)
- Status & Location Master tables

📤 Export Layer — BI Views
- Flattened, analyst-friendly views
- Ideal for Power BI, Tableau, Looker, Excel

## 🚀 How to Run This Project
1. Create Database, Warehouse, and Schemas
Run scripts in: sql=>00_setup=> create_database_warehouse_schema.sql
2. Create Bronze Raw Tables
Run scripts in: sql=>01_bronze=> create_tables_in_bronze _layer_raw.sql
3. Build Silver Dynamic Tables
Run scripts in: sql=>02_silver=> create_tables_in_silver _layer.sql
4. Insert test data 
Run scripts in: data=>insert_test_data.sql
5. Build Gold Dynamic Tables
Run scripts in: sql=>03_gold=>
           01_dt_gold_employee_master.sql
           02_dt_gold_attrition_metrics.sql
           03_dt_gold_department_metrics.sql
           04_dt_gold_employee_location_master.sql
           05_dt_gold_employee_status_master.sql
           06_dt_gold_hiring_trends.sql.sql

           5. Build Gold Dynamic Tables
6. Create Export Views
Run scripts in: 04_views=>igold_export_views.sql