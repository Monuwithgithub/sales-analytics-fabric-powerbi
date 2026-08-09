# 🏗️ Project Architecture

This project implements an end-to-end Sales Analytics solution using Microsoft Fabric and Power BI.

## Architecture Flow

The project follows a Medallion Architecture:

```text
External HTTP Endpoint
        ↓
CSV Source
        ↓
Fabric Data Pipeline
        ↓
Lakehouse Raw Files
        ↓
Bronze Layer
        ↓
Silver Layer
        ↓
Gold Layer
        ↓
Warehouse / Semantic Model
        ↓
Power BI
        ↓
Microsoft Fabric App


Step-by-Step Architecture
Data Source
Sales data is obtained from an external HTTP endpoint in CSV format.
Data Ingestion
A Microsoft Fabric Pipeline fetches the CSV file and stores it in the Lakehouse raw folder.
Bronze Layer
The raw CSV data is converted into a Delta table named bronze_sales.
Silver Layer
The Bronze data is cleaned, filtered, renamed and transformed into silver_sales.
Gold Layer
The Silver data is aggregated by business requirements to create gold_sales_summary.
Data Consumption
The processed data is consumed through the Fabric Warehouse and Power BI.
Power BI Report
An interactive Sales Analytics dashboard is created using the curated data.
Fabric App
The Power BI report is published through a Microsoft Fabric App for end-user consumption.
