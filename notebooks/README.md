# 📓 Fabric Notebooks

Microsoft Fabric Notebooks are used to process the data through the Bronze, Silver and Gold layers.

## 1. Bronze Notebook

**Notebook:** `LoadSalesToDeltaTable`

Steps:

1. Read the raw CSV file from the Lakehouse.
2. Load the data into the notebook.
3. Perform the required basic processing.
4. Convert the data into Delta format.
5. Create the `bronze_sales` Delta table.

---

## 2. Silver Notebook

**Notebook:** `TransformBronzeToSilver`

Steps:

1. Read data from `bronze_sales`.
2. Filter the required records.
3. Rename columns where required.
4. Apply data transformations.
5. Clean and standardize the dataset.
6. Write the transformed data to `silver_sales`.

---

## 3. Gold Notebook

**Notebook:** `nb_build_gold_layer`

Steps:

1. Read data from `silver_sales`.
2. Apply business-level transformations.
3. Aggregate the data by region and month.
4. Create the required summary.
5. Write the result to `gold_sales_summary`.

---

## Medallion Flow

```text
Raw Data
   ↓
Bronze
   ↓
Silver
   ↓
Gold
