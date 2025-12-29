
# 🚀 End-to-End Data Engineering Project: GlobalRetail Lakehouse
### Built with Azure Databricks, PySpark, and Delta Lake

##  **Project Overview**
This project implements a modern **Data Lakehouse architecture** using **Databricks** and **Delta Lake** for GlobalRetail, a multinational corporation. The goal is to consolidate massive volumes of historical and daily transactional data from 27 countries and 11,000 stores into a single, scalable source of truth (massive amounts of data from multiple countries and channels).

GlobalRetail's main challenges include dealing with data quality issues, managing varying data formats, and handling complex ETL processes. These challenges hinder their ability to effectively consolidate and analyze data, leading to inefficiencies and missed opportunities.

## Challenges Solved:

- Data quality issues and varying source formats (CSV, JSON, Parquet).

- Complex ETL processes required for cross-channel analysis.

- Need for high-performance reporting for executive decision-making.


###  **🛠️ Technical Implementation**
The solution leverages the full Databricks ecosystem for end-to-end data engineering:

- **Python & PySpark:** Core engine for complex data cleaning, schema enforcement, and high-volume transformations.

- **Spark SQL**: Used for business-level aggregations and creating optimized views in the Gold layer.

- **Delta Lake:** Ensures data integrity with ACID transactions across the Medallion architecture.

- **Power BI:** Connected via Databricks SQL Warehouse for interactive executive reporting.

###  **The Medallion Framework**
- **Bronze Layer**: Data ingestion layer where data in CSV, JSON, and Parquet formats is dumped. Raw data ingestion from CSV, JSON, and Parquet formats.
   - Create the Bronze layer database.
   - Load CSV, JSON, and Parquet files to respective delta tables.


- **Silver Layer:** Data processing where data/records are cleaned and transformed based on business rules.
   - Create the Silver layer database.
   - Load data into Silver layer delta tables for customers, products, and orders.


- **Gold Layer:** Creates a unified customer, aggregated view of customer and sales data across all channels and regions for business analysis and reporting.
   - Create the Gold layer database.
   - Load data into Gold tables


- **Reporting & Dashboarding Layer:** Final visualization dashboards for business intelligence units. Connects Power BI to the Databricks environment to create dashboards for different business units.
   - Install Power BI Desktop.
   - Integrate Databricks with Power BI.
   - Create a Power BI dashboard from Databricks data.


The components needed for this solution include Databricks, Delta Lake, Databricks SQL, and Power BI.

### 📂**Repository Structure**
- `01_Bronze/, 02_Silver/, 03_Gold/`: Medallion layer notebooks.

- `04_Visualization/`: Dashboard images and visualization logic.

- `data/`: Project source datasets.