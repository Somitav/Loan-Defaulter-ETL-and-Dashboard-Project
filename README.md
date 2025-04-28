# Loan Defaulter ETL and Dashboard Project

## 🚀 Project Overview
This project builds a complete end-to-end ETL pipeline and an interactive reporting dashboard for **Loan Defaulter Analysis**. It covers data ingestion, transformation, storage, and visualization using **Azure Data Factory**, **PostgreSQL**, and **Power BI**.

## 🛠️ Tech Stack
- **Azure Data Factory** — ETL orchestration and data flow transformations
- **Azure Blob Storage** — Data storage via SAS URI
- **PostgreSQL** — Staging and reporting schemas
- **Power BI** — Visualization and dashboarding
- **DAX** — Advanced calculated columns and measures

## 📁 Project Workflow

### 1. Data Ingestion
- **Source**: Excel file uploaded to Azure Blob Storage.
- **Pipeline in Azure Data Factory**:
  - Configured Blob Storage Linked Service using SAS URI.
  - Set up PostgreSQL Linked Service as the sink destination.

### 2. Data Staging
- Data loaded from Blob Storage to a **staging table** in the PostgreSQL database.

### 3. Data Validation
Performed validation tests in the staging layer:
- **Row Count Matching**: Verified between source and staging tables.
- **Sum Checks**: Conducted on key numerical columns to ensure data integrity.

### 4. Data Transformation
- Created a **Data Flow** in Azure Data Factory:
  - Performed data type transformations for reporting compatibility.
  - Conducted feature engineering by creating new derived columns.
- Loaded transformed data into a new **reporting table** (`rpt` table) under the reporting schema.

### 5. Power BI Reporting
- Connected to the PostgreSQL database using **Direct Query** mode.
- Imported the `rpt` table for visualization.
- In Power Query:
  - Applied additional light transformations for usability.
- Using DAX:
  - Created calculated columns to derive new business insights.
  - Built custom measures for deeper analytics.

## 📊 Dashboard Features
- **Loan Defaulter Overview Dashboard** includes:
  - **Custom Filters** for user-driven interactive exploration.
  - **Chart Switch Option**: Allows users to toggle dynamically between a Funnel Chart and a Bar Chart.
  - **Clear All Filters Button**: Easily reset all selections.

The dashboard empowers users with actionable insights into **loan defaulter patterns** and **critical KPIs** through an intuitive and dynamic interface.

---

Feel free to explore the repository to learn more about the project implementation!

