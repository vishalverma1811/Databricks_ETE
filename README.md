# 🏆 Databricks ETL Pipeline - Medallion Architecture

## 📊 Project Overview
An end-to-end data pipeline implementing the medallion (bronze-silver-gold) architecture on Azure Databricks. Processes raw operational data (Customers, Orders, Products, Regions) into analytically ready datasets for business intelligence and analytics.

## Technologies Used
- Databricks
- Apache Spark
- Azure Data Lake Storage
- Python
- SQL

## 🏗️ Architecture
```mermaid
graph TD
    A[Raw Source Data] --> B[Bronze Layer: Raw Ingestion]
    B --> C[Silver Layer: Cleaned & Enriched]
    C --> D[Gold Layer: Business Aggregates]
    D --> E[Analytics & Reporting]
