📖 Business Scenario

Atlon is a leading sports equipment manufacturer with a mature ERP-driven data infrastructure built on Databricks (Bronze → Silver → Gold layers).

Sports Bar is a fast-growing startup in the energy bars and athletic nutrition space that Atlon recently acquired. Their data is scattered across spreadsheets, cloud drives, and hastily-built APIs — no proper data engineering system.

The goal: Build a reliable data pipeline for Sports Bar and merge its Gold layer with Atlon's existing Gold layer, so leadership can see unified insights across both companies from a single dashboard.


🏗️ Architecture

Raw CSV Files (Unity Catalog Volume)
          │
          ▼
   ┌─────────────┐
   │   BRONZE    │  ← Raw ingestion, no transformation
   │   Layer     │
   └──────┬──────┘
          │
          ▼
   ┌─────────────┐
   │   SILVER    │  ← Cleaning, type casting, currency conversion
   │   Layer     │
   └──────┬──────┘
          │
          ▼
   ┌─────────────┐
   │    GOLD     │  ← BI-ready dimension & fact tables
   │   Layer     │
   └──────┬──────┘
          │
          ▼
  Databricks Genie (AI Analysis) + BI Dashboards


🔧 Tech Stack

ToolPurposeDatabricks Free EditionCore platformApache Spark / PySparkDistributed data processingDelta LakeACID transactions, time travelUnity CatalogData governance, 3-level namespaceUnity Catalog VolumesFile storage (replaces AWS S3)Databricks Workflows / JobsPipeline orchestration & schedulingDatabricks GenieAI-powered natural language analysisPythonNotebook logic & transformationsSQLTable creation & queries
