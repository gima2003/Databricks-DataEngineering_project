# 🏗️ Sports Bar Data Platform Modernization using Databricks

## 📖 Project Overview

This project simulates a real-world acquisition scenario where **Atlon**, a leading sports equipment manufacturer, acquires **Sports Bar**, a fast-growing athletic nutrition company.

While Atlon already operates a mature data platform, Sports Bar's data is fragmented across spreadsheets, cloud drives, and disconnected systems. The objective of this project is to build a modern data engineering pipeline using Databricks and integrate Sports Bar's data into a centralized analytics platform.

Using the **Medallion Architecture (Bronze → Silver → Gold)**, raw business data is transformed into analytics-ready datasets that can support reporting, dashboards, and AI-powered insights.

---

## 🎯 Business Problem

Following the acquisition, leadership faced several challenges:

- Data stored across multiple sources
- Inconsistent data formats
- Lack of centralized governance
- No unified reporting structure
- Difficulty generating business insights

The goal was to create a reliable and scalable data pipeline that transforms raw operational data into trusted business information.

---

## 🏛️ Architecture

```text
Raw CSV Files (Unity Catalog Volumes)
            │
            ▼
     ┌─────────────┐
     │   BRONZE    │
     │   Layer     │
     └──────┬──────┘
            │
            ▼
     ┌─────────────┐
     │   SILVER    │
     │   Layer     │
     └──────┬──────┘
            │
            ▼
     ┌─────────────┐
     │    GOLD     │
     │   Layer     │
     └──────┬──────┘
            │
            ▼
 Databricks Dashboards & Genie AI
```

---

## 🔄 Medallion Architecture

### 🥉 Bronze Layer
- Raw data ingestion
- Source data stored without transformation
- Maintains auditability and traceability

### 🥈 Silver Layer
- Data cleaning
- Type casting
- Currency conversion
- Data standardization
- Data quality validation
- Duplicate removal

### 🥇 Gold Layer
- Business-ready datasets
- Fact tables
- Dimension tables
- KPI calculations
- Analytics and reporting models

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| Databricks Free Edition | Core Data Engineering Platform |
| Apache Spark / PySpark | Distributed Data Processing |
| Delta Lake | ACID Transactions & Time Travel |
| Unity Catalog | Data Governance & Security |
| Unity Catalog Volumes | File Storage |
| Databricks Workflows | Pipeline Scheduling |
| Python | ETL Logic |
| SQL | Data Modeling & Queries |
| Databricks Dashboards | Visualization |
| Databricks Genie | AI-Powered Analytics |

---

## 🚀 Databricks Services Explored

### Lakehouse Architecture
Combines the flexibility of Data Lakes with the performance of Data Warehouses in a unified platform.

### Delta Lake
Provides:
- ACID Transactions
- Schema Enforcement
- Data Versioning
- Time Travel

### Unity Catalog
Provides:
- Centralized Governance
- Access Control
- Data Discovery
- Metadata Management

### Databricks Workflows
Used to automate and schedule data pipelines.

### Databricks Dashboards
Allows users to create interactive visualizations directly within Databricks without external BI tools.

### Databricks Genie
An AI-powered assistant that enables users to query data using natural language.

Example Questions:
- What were the top-selling products?
- Which region generated the highest revenue?
- What is the monthly sales trend?

---

## ☁️ Storage Layer

In production environments, organizations commonly use cloud storage services such as:

- AWS S3
- Azure Data Lake Storage (ADLS)
- Google Cloud Storage (GCS)

For this project, **Unity Catalog Volumes** were used instead of AWS S3, allowing the entire solution to be built directly within Databricks Free Edition.

---

## 📊 Project Outcomes

✅ Built an end-to-end Data Engineering pipeline

✅ Implemented Medallion Architecture

✅ Performed data cleaning and transformations

✅ Created analytics-ready Gold tables

✅ Built dashboards using Databricks

✅ Explored AI-powered analytics with Databricks Genie

✅ Applied modern Lakehouse Architecture concepts

---

## 📚 Key Learnings

- Data Engineering Fundamentals
- ETL Pipeline Development
- Apache Spark & PySpark
- Delta Lake
- Data Governance
- Data Modeling
- Lakehouse Architecture
- Dashboard Development
- AI-Powered Analytics
- Enterprise Data Platform Design

---

## 💼 Business Value

This solution provides:

- A single source of truth for reporting
- Improved data quality and consistency
- Faster business insights
- Self-service analytics capabilities
- Scalable architecture for future growth

By integrating Sports Bar's data into Atlon's analytics ecosystem, leadership gains a unified view of business performance across both organizations.

---

## 👤 Author

**Gimhani Pabodha**

BSc (Hons) Information Technology – Data Science

Passionate about Data Engineering, Analytics, and AI-driven solutions.
