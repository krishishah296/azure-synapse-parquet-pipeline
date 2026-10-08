


# azure-synapse-parquet-pipeline

# Cloud Big Data Analytics & Parquet Lakehouse Pipeline

An end-to-end cloud data engineering pipeline built on **Azure Synapse Analytics** and **Azure Data Lake Storage Gen2 (ADLS Gen2)**. This project demonstrates converting legacy plain-text/JSON datasets into compressed, columnar **Apache Parquet** format and performing high-performance serverless SQL and PySpark analytics.

## 📌 Architecture & Overview

1. **Storage Layer:** Provisioned ADLS Gen2 storage hierarchy using Azure Resource Manager (ARM) and Azure CLI.
2. **Data Transformation:** Processed raw plain-text data into strongly-typed, binary Apache Parquet files to optimize storage and query efficiency.
3. **Analytics Layer:** Integrated Azure Synapse Serverless SQL Pools and PySpark notebooks to query data directly in the lakehouse without dedicated cluster overhead.

## 🛠️ Tech Stack & Tools

* **Cloud Platform:** Microsoft Azure (Synapse Analytics, ADLS Gen2, Resource Groups)
* **Data Processing & Formats:** PySpark, T-SQL, Apache Parquet
* **Infrastructure / Automation:** Azure CLI, Azure Resource Manager (ARM)

## 🚀 Key Features & Performance Improvements

* **Column-Oriented Storage:** Converted row-oriented text logs to Parquet, reducing storage footprint and improving column-scan query speeds.
* **Serverless Querying:** Executed external table queries over Parquet data using Synapse Serverless SQL pools.
* **Automated Provisioning:** Used CLI scripts to set up storage containers, access keys, and RBAC permissions.

## Visualization & Output

<img width="1167" height="861" alt="image" src="https://github.com/user-attachments/assets/3d16f063-e668-4ca5-b455-7842cef0cbe5" />
## 🏃 How to Run / Reproduce

1. **Azure CLI Setup:**
   ```bash
   az group create --name datalake02krishna2026 --location canadaeast
   az storage account create --name <your-account-name> --resource-group datalake02krishna2026 --kind StorageV2 --hns true
