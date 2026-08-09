# 🔄 Microsoft Fabric Pipeline

## Pipeline: `pl_ingest_sales`

The Fabric pipeline automates the movement and processing of sales data.

### Steps

1. Created a Data Pipeline named `pl_ingest_sales`.
2. Added a scheduled trigger.
3. Configured the source as an external HTTP endpoint.
4. Used a Copy Data activity to fetch the CSV file.
5. Stored the CSV file in the Lakehouse raw folder.
6. Executed the Bronze notebook to create the `bronze_sales` Delta table.
7. Executed the Silver transformation notebook.
8. Created the `silver_sales` Delta table.
9. Executed the Gold transformation notebook.
10. Created the `gold_sales_summary` Delta table.
11. Passed the processed data to the consumption layer.
12. Connected the curated data to Power BI.

## Pipeline Flow

```text
HTTP Endpoint
     ↓
Copy Data
     ↓
Lakehouse Raw
     ↓
Bronze Notebook
     ↓
Silver Notebook
     ↓
Gold Notebook
     ↓
Power BI
