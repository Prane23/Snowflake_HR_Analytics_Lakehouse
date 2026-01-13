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
