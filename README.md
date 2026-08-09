# 📊 Sales Analytics — Microsoft Fabric & Power BI

An end-to-end Sales Analytics project built using **Microsoft Fabric and Power BI**.

This project demonstrates the complete journey of transforming raw sales data into business-ready insights using a Medallion Architecture, Fabric Pipelines, Notebooks, Delta Tables, Semantic Modeling and Power BI.

---

## 🚀 Project Overview

The project starts with sales data available through an external HTTP endpoint.

The data is ingested into Microsoft Fabric, processed through Bronze, Silver and Gold layers, and finally consumed through Power BI.

### End-to-End Flow

```text
External HTTP Endpoint
          ↓
       CSV Data
          ↓
   Fabric Data Pipeline
          ↓
     Lakehouse Raw
          ↓
    Bronze Delta Table
          ↓
    Silver Delta Table
          ↓
     Gold Delta Table
          ↓
    Semantic Model
          ↓
       Power BI
          ↓
   Microsoft Fabric App
