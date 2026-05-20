# Titanic Data Engineering Pipeline

A containerized data engineering project demonstrating how to process, clean, and query the classic Titanic dataset using **PySpark**, **HDFS**, and **Apache Hive**.

## 🛠 Tech Stack
* **Apache Spark (PySpark):** For data processing and imputation.
* **Apache Hive:** For SQL-based data querying and management.
* **HDFS:** Distributed storage for processed data.
* **Docker:** Environment orchestration to ensure reproducibility.

## 🚀 Workflow
1. **Data Ingestion:** Loading the Titanic dataset from JSON format using PySpark.
2. **Data Cleaning:** Handling missing values, specifically calculating the average age and filling null values in the `Age` column.
3. **Data Storage:** Saving the cleaned data into **Parquet** format, which is optimized for performance in distributed systems.
4. **Data Analytics:** Creating an **External Table** in Hive and mapping it to the Parquet files to enable standard SQL analytics.

## 📊 Results
The project successfully transforms raw, messy data into a structured format ready for analysis. Below are the key steps performed:

* **Processing:** Imputed missing age values with the global mean (`29.69`).
* **Storage:** Data written to HDFS in Parquet format.
* **Querying:** Verified data integrity through SQL queries in the Hive shell.

## 📂 Project Structure
```text
├── data/              # Source dataset (titanic.json)
├── scripts/           # PySpark scripts for transformation
├── docker-compose.yml # Docker configuration for the cluster
└── README.md          # Project documentation
