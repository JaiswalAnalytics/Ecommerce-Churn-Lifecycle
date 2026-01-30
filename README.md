# E-Commerce Churn: An End-to-End AI Lifecycle Solution

![Databricks](https://img.shields.io/badge/Databricks-Runtime%2014.3-orange)
![Spark](https://img.shields.io/badge/Apache%20Spark-3.5.0-red)
![MLflow](https://img.shields.io/badge/MLflow-Managed-blue)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success)

## 📋 Project Overview
This project implements a fully governed, production-grade Machine Learning pipeline to predict customer churn. Unlike standard modeling experiments, this solution focuses on the **entire AI lifecycle**: from raw data ingestion to an actionable retention strategy.

**Business Impact:**
- Identified **5,881 high-risk customers** for immediate intervention.
- Automated a **25% Discount Voucher** campaign for high-value/high-risk segments.
- Scalable architecture tested on **1M+ transactions** with a design target of **1B rows**.

---

## 🏗️ Technical Architecture
The solution utilizes a **Medallion Architecture** managed by **Unity Catalog** for end-to-end governance.

| Layer | Notebook | Function |
| :--- | :--- | :--- |
| **Bronze/Silver/Gold** | `01_Data_Engineering_Medallion.ipynb` | Ingests raw logs, cleans 1M+ records, and aggregates features. |
| **Machine Learning** | `02_Model_Training_MLflow.ipynb` | Trains Logistic Regression model, tracking experiments via MLflow (AUC 1.0). |
| **Business Strategy** | `03_Retention_Strategy_SQL.ipynb` | Applies retention logic (High Risk + High Value = Discount) and generates SQL dashboard data. |

---

## 🚀 Key Features
* **Automated Orchestration:** Uses Databricks Workflows to ensure model training only runs after data quality checks pass.
* **Governance:** Unity Catalog ensures full lineage and auditability from Bronze to Gold.
* **SQL Analytics:** A Serverless SQL Warehouse enables business stakeholders to query high-risk profiles directly.

---

## 📊 Evidence
* **Verified Run ID:** `9b9d1c8c8838499c85c0010a05a4a661`

## 🛡️ License
This project is for educational/portfolio purposes.
