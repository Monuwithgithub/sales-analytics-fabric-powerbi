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

🏗️ Architecture

The project follows the Medallion Architecture approach.

For detailed architecture documentation:

👉 View Architecture Documentation

🔄 Project Development Steps
1. Data Source
Sales data is obtained from an external HTTP endpoint.
The source data is available in CSV format.
The external source is treated as the data provider for the project.
2. Data Ingestion Pipeline
Created a Microsoft Fabric Data Pipeline named pl_ingest_sales.
Added a scheduled trigger.
Added a Copy Data activity.
Configured the source to access the external HTTP endpoint.
Configured the Lakehouse as the destination.
Stored the incoming CSV file in the raw folder.
3. Bronze Layer
Created the Bronze processing notebook LoadSalesToDeltaTable.
Read the raw CSV file from the Lakehouse.
Processed the raw dataset.
Converted the data into Delta format.
Created the bronze_sales Delta table.
4. Silver Layer
Created the Silver transformation notebook TransformBronzeToSilver.
Read data from bronze_sales.
Applied data cleaning and transformation.
Filtered required records.
Renamed columns where required.
Standardized the dataset.
Created the silver_sales Delta table.
5. Gold Layer
Created the Gold notebook nb_build_gold_layer.
Read data from silver_sales.
Applied business-level transformations.
Aggregated the data by region and month.
Created the gold_sales_summary Delta table.
6. Data Consumption
The processed data is used for analytical consumption.
Fabric Warehouse and Power BI are used as consumption layers.
The curated data provides the foundation for business reporting.
7. Semantic Model
Created the analytical model for Power BI.
Configured relationships between the required tables.
Created business measures using DAX.
Prepared the model for interactive reporting.
8. Power BI Dashboard

The final report contains:

Total Revenue
Total Revenue (USD)
Total Orders
Total Quantity Sold
Average Revenue per Order
Average Quantity per Order
Monthly Revenue & Orders Trend
Orders by Product Category
Revenue by Region
Orders by Region
Revenue by Product Category
Quantity Sold by Product Category
Top 10 Customers by Revenue
Report Filters
Sales Date
Sales Month
Sales Quarter
Sales Year

🎨 Dashboard Customization

The original dashboard design was customized to give the report a personal visual identity.

Improvements
Applied a customized color theme.
Improved visual consistency.
Customized report presentation.
Improved KPI presentation.
Used consistent colors across visuals.
Added/adjusted interactive report features.
🚀 Microsoft Fabric App

The completed Power BI report was published through a Microsoft Fabric App.

🔗 Live App

Open Sales Analytics Fabric App

Access to the app may require appropriate Microsoft account permissions.

📸 Project Screenshots
Fabric Architecture

Fabric Pipeline

Lakehouse Layers

Power BI Dashboard

🛠️ Technology Stack
Technology	Purpose
Microsoft Fabric	Data Engineering & Analytics
Fabric Lakehouse	Data Storage
Delta Lake	Table Storage
Fabric Pipelines	Data Orchestration
Fabric Notebooks	Data Processing
PySpark / Python	Data Transformation
Fabric Warehouse	Data Consumption
Power BI	Data Visualization
DAX	Business Calculations
GitHub	Project Documentation
📁 Repository Structure
sales-analytics-fabric-powerbi/
│
├── README.md
│
├── architecture/
│   ├── Architecture.png
│   └── README.md
│
├── screenshots/
│   ├── 01-fabric-architecture.png
│   ├── 02-fabric-pipeline.png
│   ├── 03-lakehouse-layers.png
│   ├── 04-powerbi-dashboard.png
│   └── README.md
│
├── notebooks/
│   └── README.md
│
├── pipeline/
│   └── README.md
│
├── power-bi/
│   ├── README.md
│
├── fabric-app/
│   └── README.md
│
└── docs/
    └── README.md
📚 Detailed Documentation
Architecture
Fabric Notebooks
Fabric Pipeline
Power BI Report
Fabric App
Project Documentation
🎯 Business Questions

The dashboard helps analyze:

Which product categories generate the highest revenue?
Which regions perform best?
Which customers contribute the most revenue?
How does revenue change over time?
Which categories generate the most orders?
What is the average revenue per order?
🔮 Future Improvements
Automated data refresh
Revenue forecasting
Customer segmentation
Profitability analysis
Advanced drill-through analysis
Row-Level Security
Additional business KPIs
👩‍💻 Author

Monika

B.Tech — Computer Science & Engineering

Interested in Data Analytics, Data Engineering, Machine Learning and Microsoft Fabric.


---

# 11. Your final structure will be simple

After doing the above, your GitHub should look like this:

```text
📁 sales-analytics-fabric-powerbi
│
├── 📄 README.md                    ← MAIN PROJECT STORY ⭐
│
├── 📁 architecture
│   ├── 🖼️ Architecture.png
│   └── 📄 README.md                ← Architecture explanation
│
├── 📁 screenshots
│   ├── 🖼️ 01-fabric-architecture.png
│   ├── 🖼️ 02-fabric-pipeline.png
│   ├── 🖼️ 03-lakehouse-layers.png
│   ├── 🖼️ 04-powerbi-dashboard.png
│   └── 📄 README.md
│
├── 📁 notebooks
│   └── 📄 README.md
│
├── 📁 pipeline
│   └── 📄 README.md
│
├── 📁 power-bi
│   ├── 📄 README.md
│
├── 📁 fabric-app
│   └── 📄 README.md                 ← APP LINK ⭐
│
└── 📁 docs
    └── 📄 README.md                 ← COMPLETE STEPS
