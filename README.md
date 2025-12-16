# retail-analytics-lakehouse-azure-databricks
The project implements a retail analytics (based on amazon sales) Lakehouse architecture using Azure Data Lake Gen2, Databricks (Delta Lake), and Power BI. The pipeline follows a Bronze → Silver → Gold pattern (medallion architecture) and supports analytical reporting through fact and dimension modeling.

🔹 Architecture

Data Source: Retail Amazon Sales CSV
Storage: Azure Data Lake Gen2 (Hierarchical Namespace)
Processing: Azure Databricks (PySpark)
Storage Format: Delta Lake
Governance: Unity Catalog
Visualization: Power BI

🔹 Data Pipeline Flow

Raw CSV files ingested into Bronze layer
Data cleaned, standardized, and deduplicated in Silver layer
Dimensional modeling performed in Gold layer
Fact table: fact_sales
Dimension tables: dim_date, dim_product, dim_customer, dim_status
Power BI connected to Gold tables for analytics

🔹 Data Model

Fact Table
fact_sales: sales transactions
Dimension Tables
dim_date
dim_product
dim_customer
dim_status

🔹 Key Features

End-to-end Lakehouse implementation
Delta Lake ACID transactions
Scalable dimensional modeling
Power BI semantic layer
Production-style folder & notebook structure

🔹 Future Enhancements

Incremental loading
CDC handling
Snowflake integration
Data quality checks
CI/CD with Azure DevOps