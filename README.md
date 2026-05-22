# Olist ETL Pipeline

ETL pipeline built with PySpark and Databricks using the Medallion Architecture (Bronze → Silver → Gold).

## Project Overview
This project processes the Brazilian E-Commerce dataset from Olist, transforming raw data into a Star Schema ready for business analysis.

## Architecture
- **Bronze** → Raw CSV files ingested as-is
- **Silver** → Cleaned and validated data (nulls, duplicates, data types)
- **Gold** → Star Schema with Fact and Dimension tables (Delta Tables)

## Tech Stack
- Python / PySpark
- Databricks (Serverless)
- Delta Lake
- SQL
- Parquet

## Notebooks
| Notebook | Description |
|---|---|
| 00_exploration | Data exploration and schema analysis |
| 01_extract | Load raw CSV files into Bronze layer |
| 02_silver | Data cleaning and validation |
| 03_gold | Star Schema creation |
| 04_load | Save as Delta Tables in Unity Catalog |

## Star Schema
- **fact_orders** → Central fact table with sales data
- **dim_customers** → Customer information
- **dim_products** → Product and category information
- **dim_sellers** → Seller information
- **dim_dates** → Date dimension extracted from orders

## Dataset
[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
