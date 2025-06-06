# 🛠️ CSV to Parquet Data Pipeline using AWS, Databricks & PySpark

This is a beginner-friendly end-to-end data engineering project where I built a pipeline to ingest, clean, transform, and query COVID-19 data using **AWS S3**, **Databricks (Community Edition)**, **PySpark**, and **Athena**.

---

## 🚀 Project Overview

- ✅ Ingested the **Our World in Data COVID-19 dataset (CSV)** into **Amazon S3**
- 🧹 Cleaned missing values using **PySpark**:
  - Categorical columns (`string`) → filled with `"Unknown"`
  - Numeric columns (`int`, `double`) → filled with the **mean**
- 🔄 Converted the dataset to **Parquet format**
- 💾 Saved the transformed data back to **S3**
- 🔍 Queried the Parquet data using **AWS Athena**

---

## 🧰 Tools & Technologies

- **AWS S3** – Storage for raw CSV and Parquet files  
- **AWS IAM** – Secure programmatic access for Databricks  
- **Databricks Community Edition** – Spark-powered data processing  
- **PySpark** – Distributed data cleaning and transformation  
- **Athena** – SQL querying directly on Parquet in S3

---

## 📁 Folder Structure

```text
raw/
└── owid-covid-data.csv           # Original dataset

clean/
└── owid-covid-parquet/           # Cleaned parquet output

athena-results/
└── ...                           # Athena query outputs
# aws-databricks-pipeline
