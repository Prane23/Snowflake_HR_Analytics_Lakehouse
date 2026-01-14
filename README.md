# ❄️ Snowflake HR Analytics Lakehouse
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

## 🔮 Key Features
- Medallion Architecture (Bronze/Silver/Gold)
- Dynamic Tables for automated ELT
- Enterprise-scale synthetic HR dataset
- Employee Master table combining status, location, supervisor, and department
- Attrition & hiring trend metrics
- Department performance metrics
- BI-ready export schema
- Modular SQL project structure
- Extensible design for ML, SCD2, and real-time ingestion

## 🖥️  How to Run This Project
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
6. Create Export Views
Run scripts in: 04_views=>igold_export_views.sql

## 🧰 Tech Stack
<img width="718" height="338" alt="image" src="https://github.com/user-attachments/assets/1e4bb12a-a929-4b0f-bfbf-df352755d031" />

## 🏗️ Architecture
<img width="729" height="568" alt="image" src="https://github.com/user-attachments/assets/e478c09f-7e0a-414f-a7a9-0789f2daf22d" />

## 📁 Repository Structure
```
Snowflake_HR_Analytics_Lakehouse/
│
├── README.md
│
├── architecture/
│   ├── medallion-architecture.png
│   ├── dynamic-table-lineage.png
│
├── sql/
│   ├── 00_setup/
│   ├── 01_bronze/
│   ├── 02_silver/
│   ├── 03_gold/
│   ├── 04_views/
│
└── data/
```
## Database & schema structure
<img width="1509" height="1120" alt="image" src="https://github.com/user-attachments/assets/8b72736f-2ee8-4ad1-bc3b-540abba36734" />

##  Gold Dynamic table graph 
<img width="1585" height="1040" alt="image" src="https://github.com/user-attachments/assets/924745fb-d13f-4c27-8361-198b09b809bf" />


## 📊 Analytics Use Cases
- Attrition Analysis
- Hiring Trend Forecasting
- Department Performance Metrics
- Employee Tenure Analysis
- Supervisor → Employee Hierarchy
- Location Distribution

## 🔮 Future Enhancements
- Add SCD Type 2 for employee attributes
- Add Snowpipe for real-time ingestion
- Add Power BI dashboard templates
- Add Snowpark ML for attrition prediction
- Add RBAC and row-level security

## 🙌 Author
Prashant  
Snowflake | Data Engineering | Cloud Analytics
