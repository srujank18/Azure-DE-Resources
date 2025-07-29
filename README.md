# Azure-DE-Resources
Contains Azure Data Engineering resources and sample datasets for hands-on learning and project development.
# Azure Data Engineering Project

This project demonstrates a complete data engineering pipeline using **Azure Data Factory**, **Azure Databricks**, and **Delta Lake** following the **medallion architecture** (Bronze → Silver → Gold). The goal is to transform raw sales data into a structured, analytics-ready star schema model.

---

## Tech Stack
- **Azure Data Factory**: Orchestrates the pipeline and performs incremental data ingestion.
- **Azure Databricks**: Cleans, transforms, and loads data using notebooks.
- **Delta Lake**: Stores data in Silver and Gold layers with ACID guarantees.
- **ADLS Gen2**: Storage for raw, cleaned, and modeled data.

---
---

## Datasets

- **SalesData.csv**: Historical sales data
- **IncrementalSales.csv**: New sales data for testing incremental loads

---

## Project Highlights

- **Incremental Ingestion**: Using watermark logic with ADF pipelines
- **Data Transformation**: Implemented in Databricks notebooks for Silver and Gold layers
- **Star Schema Modeling**: Includes fact and dimension tables (`dim_date`, `dim_dealer`, `dim_branch`, `dim_model`, `fact_sales`)
- **SCD Type 1**: Handled for dimension updates using `MERGE INTO` logic
- **Parameterization**: ADF pipelines are fully parameterized for reusability

---

