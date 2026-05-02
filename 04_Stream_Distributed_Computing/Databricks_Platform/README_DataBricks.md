# Data Bricks:
 

## 📌 Overview
This repository contains a collection of batch and streaming data processing pipelines developed using **Databricks**. The projects here demonstrate the implementation of a modern **Data Lakehouse** architecture, focusing on scalability, reliability, and real-time data ingestion.

By practicing with end-to-end scenarios from my current coursework, I have implemented patterns for Change Data Capture (CDC), Delta Table optimization, and Structured Streaming.

---

## 🚀 What is Databricks?
Databricks is a cloud-based **Unified Analytics Platform** built on top of Apache Spark. It provides a collaborative environment for data engineers to build, deploy, and share enterprise-grade data solutions. 

Key advantages of the platform include:
- **Decoupled Compute and Storage:** Scaling resources independently based on workload.
- **Collaborative Notebooks:** Multi-language support (PySpark, SQL, Scala, R) with real-time co-authoring.
- **Optimized Engine:** Uses the **Photon** execution engine for significantly faster processing compared to standard Spark.


---

## 🛠 Compatibility & Integration
Databricks is designed to be the "central nervous system" of a data ecosystem:
* **Cloud Providers:** Fully compatible with **AWS**, **Microsoft Azure**, and **Google Cloud Platform (GCP)**.
* **Storage Formats:** Native support for Parquet, Avro, JSON, CSV, and **Delta Lake**.
* **Tools:** Seamless integration with BI tools (Power BI, Tableau), orchestration (Airflow, Azure Data Factory), and version control (GitHub).

---

## 📊 Databricks vs. Cloud Storage (S3, ADLS, GCS)
It is important to distinguish between where data *lives* and where it is *processed*.

| Feature | Cloud Storage (e.g., S3 / ADLS) | Databricks Platform |
| :--- | :--- | :--- |
| **Primary Role** | **Storage Layer** (The "Hard Drive") | **Compute Layer** (The "Processor") |
| **Capability** | Stores raw files in their native format. | Transforms, cleans, and analyzes data. |
| **Intelligence** | Static; no awareness of data schema. | Dynamic; manages metadata, schema, and ACID transactions. |
| **Performance** | Limited by network I/O and file size. | Uses caching, Z-Ordering, and indexing for high-speed queries. |

---

## 🧩 Core Components

### 1. Clusters (Compute)
The backbone of Databricks. I configure Spark clusters to handle distributed processing. This includes:
- **All-Purpose Clusters:** Used for interactive analysis and development in notebooks.
- **Job Clusters:** Cost-efficient, short-lived clusters that run specific automated tasks.

DataBricks-Compute Engine image:
![Databricks_Compute.png](../../Z_Ruff_Images_Text_Links/Images/Databricks_Compute.png)

### 2. Workspace & Notebooks
A unified interface where I organize code, libraries, and dashboards. Using **Databricks Repos**, I sync these notebooks directly with GitHub for professional version control.

### 3. Delta Lake
An open-source storage layer that brings **ACID transactions** to Apache Spark. In this project, I use Delta Lake to:
- Handle **Upserts** and **Deletes** easily.
- Implement **Time Travel** (Data Versioning) to query previous states of the data.
- Ensure data integrity during streaming writes.

### 4. Structured Streaming
The engine used for real-time data processing. I use this component to ingest data from sources like Kafka or cloud folders as it arrives, ensuring low-latency insights.

### 5. Databricks SQL & Catalog
A dedicated workspace for SQL-native analytics and a centralized metadata repository (Catalog) to manage databases, tables, and permissions.

---

## ⚙️ Project Setup & Execution
* **Platform:** Databricks Community Edition
* **Runtime:** 13.x+ (includes Apache Spark 3.4.x, Scala 2.12)
* **Storage:** Databricks File System (DBFS) for local practice and simulated cloud storage.


DataBricks-Compute Engine:
![Databricks_Compute.png](../../Z_Ruff_Images_Text_Links/Images/Databricks_Compute.png)