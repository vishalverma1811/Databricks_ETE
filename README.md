# 🏆 Databricks ETL Pipeline - Medallion Architecture

## 📊 Project Overview
This project implements a complete, production-grade data pipeline on Azure Databricks using the Medallion (Bronze-Silver-Gold) architecture. It processes raw retail data (Customers, Orders, Products, Regions) through incremental ingestion, transformation, and loading into analytics-ready tables with full historical tracking using Slowly Changing Dimensions Type 2.

## 🏗️ Architecture
```mermaid
graph TD
    A[Raw Data in ADLS Gen2] --> B[Bronze Layer: Raw Ingestion]
    B --> C[Silver Layer: Cleansed & Enriched]
    C --> D[Gold Layer: Business Aggregates]
    D --> E[Analytics & Reporting]
    
    subgraph Azure Cloud
        B --> F[Unity Catalog Governance]
        C --> F
        D --> F
    end

🛠️ Tech Stack
Cloud Platform: Microsoft Azure
Data Processing: Azure Databricks, Apache Spark 3.5.0
Data Format: Delta Lake
Data Governance: Unity Catalog
Storage: Azure Data Lake Storage Gen2 (ADLS Gen2)
Orchestration: Databricks Workflows

Languages: Python, SQL, PySpark

