# YouTube Data Analysis | Azure Data Engineering Project

## Introduction
This project focuses on **analyzing YouTube data** using **Azure cloud services** with an end-to-end data pipeline. It follows the **Medallion Architecture (Bronze, Silver, Gold)** to ensure **efficient data processing, governance, and analytics**.

The project involves:
- Extracting **YouTube JSON and CSV data** from a **raw-input container** in **Azure Data Lake Gen2**.
- Storing raw data in the **Bronze Layer**.
- Cleaning and transforming data using **PySpark in Azure Databricks**.
- Storing structured data in the **Silver Layer**.
- Creating aggregated business insights in the **Gold Layer**.
- Loading transformed data into **Azure Synapse Analytics (Serverless SQL Pool)**.
- **Visualizing insights in Power BI**.
- Implementing **Role-Based Access Control (RBAC) using Microsoft Entra ID**.
- **Managing secrets securely** with Azure Key Vault.
- **Using GitHub for version control**.

---

## Project Architecture
The project is built using the **Medallion Architecture**, which includes:
1. **Bronze Layer**: Stores raw, unprocessed JSON data from YouTube.
2. **Silver Layer**: Cleans and transforms JSON into a structured format.
3. **Gold Layer**: Stores aggregated, business-ready data for reporting.

This architecture ensures **scalability, data quality, and performance optimization**.

### High-Level Architecture Diagram
Below is the **high-level architecture** of the project:

![Project Architecture](Project%20files/YoutubeDataAnalysisArchitecture.png)

## Key Components
- **Data Ingestion**: Azure Data Factory extracts data from **Raw-Input Container**.
- **Storage**: Azure Data Lake Gen2 with **Bronze, Silver, and Gold layers**.
- **Processing & Transformation**: Azure Databricks (PySpark-based ETL).
- **Analytics**: Azure Synapse Serverless SQL Pool.
- **Visualization**: Power BI for interactive dashboards.
- **Security & Access Control**: Microsoft Entra ID for RBAC.
- **Secret Management**: Azure Key Vault for storing secrets.
- **Code Repository**: GitHub for version control.

---

## Project Workflow
1. **Extract & Load (EL)**
   - Azure Data Factory ingests **YouTube JSON files** into the **Bronze Layer**.

2. **Transformation (ETL in Databricks)**
   - PySpark processes JSON:
     - Extracts relevant nested arrays (e.g., `items`, `statistics`).
     - Converts JSON into tabular format.
     - Cleans and standardizes data.
   - Stores transformed data in **Silver Layer**.

3. **Aggregation & Business Insights (Gold Layer)**
   - Performs aggregations on **views, likes, comments, categories**.
   - Stores optimized data in **Gold Layer**.

4. **Loading into Azure Synapse Analytics**
   - **Gold Layer data is queried using Serverless SQL Pool**.

5. **Data Visualization in Power BI**
   - Power BI connects to **Azure Synapse for dashboards**.
     
     **Data Model**
     ![Data Model](Project%20files/youtube-data-analysis-data-model.png)
     
     **Dashboard**
     ![Dashboard](Project%20files/youtube-data-analysis-dashboard.png)

6. **Security & Governance**
   - **Azure Entra ID** manages **Role-Based Access Control (RBAC)**.
   - **Azure Key Vault** stores **secure credentials**.
   - **GitHub** manages **source code versioning**.

---

## Technologies Used
| Component             | Technology Used                     |
|----------------------|----------------------------------|
| **Data Ingestion**   | Azure Data Factory (ADF)         |
| **Storage**         | Azure Data Lake Storage Gen2     |
| **Processing**      | Azure Databricks (PySpark)       |
| **Analytics**       | Azure Synapse Analytics (SQL)   |
| **Visualization**   | Power BI                         |
| **Security**       | Azure Active Directory (RBAC)   |
| **Secret Management** | Azure Key Vault                 |
| **Code Repository** | GitHub                           |

---

## Key Features
- **End-to-End Cloud-Based Data Pipeline** using Azure.  
- **Multi-Hop Data Architecture** (Bronze, Silver, Gold).  
- **PySpark-Based Transformations** in Azure Databricks.  
- **Optimized Data Querying** with Azure Synapse Analytics.  
- **Interactive Dashboards** in Power BI.  
- **Enterprise-Grade Security** with Entra ID & Azure Key Vault.  
- **Scalable & Automated ETL Workflows** using Azure Data Factory.  

---

## Dataset Used
- **Source**: **YouTube Data (JSON & CSV Format)**
- **Dataset**:
  - JSON Dataset: https://github.com/sureshchalla0139/YouTube-Data-Analysis-AzureDataEngineering-Project/tree/main/Dataset%20Json
  - CSV Dataset: https://github.com/sureshchalla0139/YouTube-Data-Analysis-AzureDataEngineering-Project/tree/main/Dataset%20CSV

- **File Format**: JSON & CSV → Parquet  
- **Storage**: Azure Data Lake Gen2  

---

## Project Setup
### **Prerequisites**
1. Azure Subscription.
2. Access to **YouTube Data API** (for JSON files).
3. Azure Data Lake Gen2, Databricks, Data Factory, Synapse, and Power BI.
4. GitHub for version control.

### **Deployment Steps**
1. **Set up Azure Data Factory** to ingest YouTube JSON into **Bronze Layer**.
2. **Mount Data Lake Gen2 in Azure Databricks**.
3. **Transform Bronze → Silver → Gold using PySpark** in Databricks.
4. **Load Gold Layer data into Azure Synapse Analytics**.
5. **Connect Power BI to Synapse SQL Pool** for reporting.
6. **Secure data using Azure Entra ID and Key Vault**.
 

---

## Key Takeaways
- **Azure Data Engineering Best Practices**: Implemented **Medallion Architecture** for structured data processing.  
- **Optimized ETL Workflows**: Using **PySpark in Azure Databricks** for scalable transformations.  
- **Serverless Analytics**: Leveraged **Azure Synapse SQL Pool** for optimized querying.  
- **Data-Driven Insights**: Created **Power BI Dashboards** for business intelligence.  
- **Enterprise Security**: Implemented **RBAC, Key Vault, and GitHub for governance**.  

---

## Conclusion
This project **demonstrates the power of Azure** in **processing and analyzing large-scale YouTube data** using **scalable, secure, and efficient cloud-based data pipelines**. It follows **industry best practices for Data Engineering** and enables **data-driven decision-making**.


