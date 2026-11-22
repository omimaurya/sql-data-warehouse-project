# Data Warehouse and Analytics Project
Building a modern data warehouse with SQL Server, including ETL processes, data modeling and analytics.

```
sql-data-warehouse-project/
├── 00_setup/               the setup guide, and the one-click Docker start for Mac
├── 01_datasets/            the six source files the project loads
│   ├── source_crm/         three files from the CRM system
│   └── source_erp/         three files from the ERP system
├── 02_docs/                the requirements, the diagrams and the notes
├── 03_scripts/             the project scripts, in the order of the videos
│   ├── init_database.sql   creates the database: run it first
│   ├── bronze/             loads the raw files
│   ├── silver/             cleans and prepares the data
│   └── gold/               builds the tables for analysis
└── 04_tests/               checks the quality of the silver and gold data
```
# Data Architecture
The data architecture for this project follows Medallion Architecture Bronze, Silver, and Gold layers:
<img width="1544" height="792" alt="data_architecture" src="https://github.com/user-attachments/assets/0b28db63-77ac-4b78-a075-90868b2d6739" />
 **1.** **Bronze Layer:** Stores raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.
 
 **2.** **Silver Layer:** This layer includes data cleansing, standardization, and normalization processes to prepare data for 
 analysis.
 
 **3** **Gold Layer:** Houses business-ready data modeled into a star schema required for reporting and analytics.
