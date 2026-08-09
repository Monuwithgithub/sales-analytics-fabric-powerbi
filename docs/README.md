# 📚 Project Documentation

This section documents the complete development process of the Sales Analytics project.

## Development Steps

### Step 1 — Source Data

Sales data was obtained from an external HTTP endpoint in CSV format.

### Step 2 — Data Pipeline

A Microsoft Fabric Data Pipeline named `pl_ingest_sales` was created.

### Step 3 — Data Ingestion

A scheduled trigger and Copy Data activity were configured to fetch the CSV data.

### Step 4 — Raw Data Storage

The incoming CSV was stored in the Lakehouse raw folder.

### Step 5 — Bronze Layer

The `LoadSalesToDeltaTable` notebook converted the raw data into the `bronze_sales` Delta table.

### Step 6 — Silver Layer

The `TransformBronzeToSilver` notebook cleaned and transformed the Bronze data into `silver_sales`.

### Step 7 — Gold Layer

The `nb_build_gold_layer` notebook aggregated the Silver data and created `gold_sales_summary`.

### Step 8 — Data Consumption

The processed data was made available for analytical consumption through Fabric and Power BI.

### Step 9 — Semantic Model

The analytical data was modeled for Power BI reporting.

### Step 10 — Power BI Dashboard

An interactive Sales Analytics dashboard was created with KPIs, trends, category analysis, regional analysis and customer analysis.

### Step 11 — Dashboard Customization

The report was given a customized visual theme and improved presentation.

### Step 12 — Fabric App

The completed Power BI report was published through a Microsoft Fabric App.

### Step 13 — GitHub Documentation

The project architecture, screenshots, notebooks, pipeline, Power BI report and Fabric App are documented in this repository.
