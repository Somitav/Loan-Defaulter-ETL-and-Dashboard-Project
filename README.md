Loan Defaulter ETL and Dashboard Project
🚀 Project Overview
This project focuses on building a complete end-to-end ETL pipeline and interactive reporting dashboard for loan defaulter analysis.
It covers data ingestion, transformation, storage, and visualization using Azure Data Factory, PostgreSQL, and Power BI.

🛠️ Tech Stack
Azure Data Factory – ETL orchestration and data flow transformations

Azure Blob Storage – Data storage using SAS URI

PostgreSQL Database – Staging and reporting schemas

Power BI – Visualization and dashboarding

DAX – Calculated columns and measures for advanced analytics

📑 Project Workflow
1. Data Ingestion
Source: Excel file uploaded to Azure Blob Storage.

Azure Data Factory pipeline created:

Blob Storage Linked Service configured via SAS URI.

PostgreSQL Linked Service configured as sink.

2. Data Staging
Data transferred from Blob Storage to a staging table in PostgreSQL database.

3. Data Validation
Validation tests performed in staging:

Row Count Matching between source and staging.

Sum checks on numerical columns for data integrity.

4. Data Transformation
Data Flow created in Azure Data Factory:

Data type transformations for better reporting compatibility.

Feature engineering by creating new columns with complex transformations.

Output loaded into a new reporting table (rpt table) in the reporting schema.

5. Power BI Reporting
PostgreSQL database connected to Power BI using Direct Query.

Imported rpt table for visualization.

In Power Query:

Additional light transformations done for better usability.

DAX used to:

Create calculated columns for new business features.

Build custom measures for deeper insights.

📊 Dashboard Features
Loan Defaulter Overview Dashboard created with:

Custom Filters for interactive exploration.

Chart Switch Option: Users can dynamically switch between Funnel Chart and Bar Chart view.

Clear All Filters Button for resetting selections easily.

The dashboard focuses on providing insightful, user-driven analytics for loan defaulter patterns and KPIs.
