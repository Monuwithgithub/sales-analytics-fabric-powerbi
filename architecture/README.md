# Architecture

The project follows a Medallion Architecture implemented using Microsoft Fabric.

```text
Source Data
    ↓
Data Ingestion
    ↓
Bronze Layer
    ↓
Silver Layer
    ↓
Gold Layer
    ↓
Semantic Model
    ↓
Power BI Report
    ↓
Microsoft Fabric App
