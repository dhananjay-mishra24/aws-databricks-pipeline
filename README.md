# 📦 CSV to Parquet Data Engineering Pipeline (AWS + Databricks + PySpark)

This is my first Data Engineering project where I built an end-to-end pipeline using **AWS S3**, **Databricks Community Edition**, **PySpark**, and **AWS Athena**. The goal was to convert a raw CSV dataset into optimized Parquet format, perform basic data analysis, and make the data queryable using Athena.

---

## 🧠 Objective

- Ingest real-world COVID-19 CSV data from [Our World in Data](https://ourworldindata.org/)
- Clean and transform data using PySpark
- Store intermediate results in Parquet format on S3
- Query the final data using AWS Athena

---

## 🔧 Tools & Technologies

- **Apache Spark** (via Databricks Community Edition)
- **PySpark**
- **Amazon S3**
- **AWS Athena**
- **Parquet file format**


## ✅ Pipeline Steps

1. **CSV Upload to S3**
   - Uploaded `owid-covid-data.csv` to `s3://dj-databricks-pipeline/`

2. **Data Cleaning with PySpark**
   - Loaded data using Spark
   - Filtered out rows with `continent IS NULL` (e.g., "World", "High income", etc.)
   - Casted `date` column to proper date type

3. **Data Analysis**
   - Aggregated `new_cases` to calculate:
     - Average
     - Median (`percentile_approx`)
     - Total per day
   - Also explored per-country population and metrics

4. **Data Writing to S3**
   - Saved transformed data as Parquet to:
     - `day_wise_parquet/`
     - `country_wise_parquet/`

5. **Querying with Athena**
   - Defined external tables in Athena
   - Queried Parquet data directly for insights


