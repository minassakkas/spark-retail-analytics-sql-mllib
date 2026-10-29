# Retail Customer Analytics with Apache Spark — Spark SQL & MLlib K-Means

> 🚧 Work in progress

End-to-end analysis of **1,000,000 retail transactions** with **Apache Spark 4 (PySpark)**, built as part of the
*Business Intelligence & Data Engineering* course of the MSc in Business Analytics (Athens University of Economics and Business).

The scenario: a quick-commerce company wants to understand its customers' purchasing behaviour.

## What it covers

**1. Exploratory analysis with Spark SQL & the DataFrame API**
- Descriptive statistics, payment methods, customer categories, promotions
- City rankings, top sales days, average spend per store type
- Top customer per city using window functions

**2. Customer segmentation with Spark MLlib**
- Feature engineering pipeline: `StringIndexer` → `OneHotEncoder` → `VectorAssembler` → `StandardScaler`
- K-Means clustering for k = 2…5
- Model evaluation with the silhouette score (squared Euclidean distance)

## Tech stack
Apache Spark 4.0 · PySpark · Spark SQL · Spark MLlib · Jupyter

## Dataset
Synthetic retail transactions (≈161 MB CSV, 13 columns: transaction date, customer, products, items, total cost,
payment method, city, store type, discount, customer category, season, promotion).
The file is not included in the repository because of its size; place `retail-dataset.csv` (or the `.zip`) next to the notebook.

## How to run
Requires Java 17 and Python 3.10–3.12.

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```
