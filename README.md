# EcommPipelineandAnalysis


📌 Project Overview

This project implements a real-time data pipeline for processing e-commerce orders using Databricks, Delta Lake, and Structured Streaming.
It follows the Medallion Architecture (Bronze → Silver → Gold) with data quality checks and Unity Catalog governance to enable real-time analytics and dashboards.

🚀 Architecture

Data Source: Simulated real-time orders using Faker scripts

Ingestion: Databricks Auto Loader for incremental streaming ingestion

Processing: Structured Streaming with Bronze, Silver, and Gold Delta tables

Governance: Unity Catalog for fine-grained security and auditing

Analytics: Databricks SQL for interactive dashboards and reporting

🏗️ Project Structure
/RealTimeEcom/
    ├── Notebooks/
    │   ├── 01_setup_unity_catalog       # Unity Catalog and schema setup
    │   ├── 02_data_ingestion_bronze      # Auto Loader for raw data
    │   ├── 03_silver_transformations     # Cleansing and enrichment
    │   ├── 04_gold_aggregations          # Final metrics & analytics tables
    │   ├── 05_dashboards                 # Databricks SQL dashboards
    │
    ├── StreamingJobs/
    │   ├── orders_stream.py              # Orders ingestion stream
    │   ├── order_items_stream.py         # Order items ingestion stream
    │   └── utils.py                      # Common streaming functions
    │
    ├── BatchJobs/
    │   └── dim_tables_load.py            # Dimension tables load
    │
    ├── Config/
    │   ├── dlt_config.yml                # Delta Live Tables configs
    │   └── spark_conf.json               # Spark streaming configs
    │
    ├── FakerScripts/
    │   └── generate_orders.py            # Simulates real-time orders
    │
    └── Tests/
        ├── test_data_quality.py          # Data quality checks
        └── test_streaming_logic.py       # Streaming logic validation

🧰 Tech Stack

Databricks (Structured Streaming, Delta Lake, Unity Catalog)

Python (Faker for data generation, PySpark for processing)

Delta Live Tables (DLT) for declarative pipelines

Databricks SQL for dashboards & analytics

GitHub for version control & CI/CD

📊 Key Features

Real-time ingestion using Auto Loader

Data quality enforcement with DLT expectations

Medallion Architecture for data refinement (Bronze → Silver → Gold)

End-to-end governance via Unity Catalog

Interactive analytics with Databricks SQL dashboards

🏆 Outcomes

Real-time order metrics: sales trends, order counts, revenue analytics

Improved data reliability with quality checks

Easy CI/CD deployment with GitHub integration
