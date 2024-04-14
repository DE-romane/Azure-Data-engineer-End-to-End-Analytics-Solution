<div align="center">
  <a href="#">
    <img src="https://github.com/DE-romane/Azure-Data-engineer-End-to-End-Analytics-Solution/blob/main/PowerBI-dashboard.PNG" alt="Banner" width="720">
  </a>

  <div id="user-content-toc">
    <ul>
      <summary><h1 style="display: inline-block;">🔧 AdventureWorks Sales Insight: A Data Journey 🔌</h1></summary>
    </ul>
  </div>
  
  <p>Migration from On-premises Database to Azure Cloud Pipeline via Data Factory, Lake Storage, Spark, Databricks, Synapse, PowerBI</p>
</div>
<br>

## 📝 Table of Contents
1. [Project Overview](#introduction)
2. [Key Insights](#key-insights)
3. [Project Architecture](#project-architecture)  
  3.1. [Data Ingestion](#data-ingestion)  
  3.2. [Data Transformation](#data-transformation)  
  3.3. [Data Loading](#data-loading)  
  3.4. [Data Reporting](#data-reporting)
4. [Credits](#credits)
5. [Contact](#contact)

<a name="introduction"></a>
## 🔬 Project Overview 

This project entails a comprehensive data engineering initiative on the Azure cloud. It involved the transfer of data from an on-premises SQL Server to Azure Data Lake through Data Factory, followed by transformation via Databricks and Spark, loading into Synapse, and reporting using PowerBI. Additionally, Azure Active Directory (AAD) and Azure Key Vault were utilized for data monitoring and governance purposes.

### 💾 Dataset

**AdventureWorks** is a database provided by Microsoft for free on online platforms. It is a product sample database originally published by Microsoft to demonstrate the supposed design of a SQL server database using SQL server 2008. Here are some key points to know about AdventureWorks:

- AdventureWorks database supports a manufacturing MNC named Adventure Works Cycles.
- It is a sample Online Transaction Processing (or OLTP) database, which is a type of data processing where multiple transactions occur concurrently. These are shipped by Microsoft with all of their SQL server products.

> For this project I used the **Lightweight (LT) data**: a lightweight and pared down version of the OLTP sample. [Download here](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksLT2022.bak)

### 🎯 Project Goals

- Establish a connection between on-premise SQL server and Azure cloud.
- Ingest tables into the Azure Data Lake.
- Apply data cleaning and transformation using Azure Databricks.
- Utilize Azure Synapse Analytics for loading clean data.
- Create interactive data visualizations and reports with Microsoft Power BI.
- Implement Azure Active Directory (AAD) and Azure Key Vault for monitoring and governance.

<a name="key-insights"></a>
## 🕵️ Key Insights

- 💸 **Total Revenue by Product Category**
  - *Touring Bikes* is the top 1 category generating revenue with 32% followed by *Road Bikes* with 26% and *Mountain Bikes* with 24%.
 
- 🌍 **Sales by Country**
  - **N°1:** The United Kingdom (UK) have the most total sales with 278 and $572,000 of total revenue.
  - **N°2:** The United States of America (USA) is second with total sales with 264 and $383,810 of total revenue.

- 🚻 **Revenue by Gender**
  - 81% of the revenue is generated by Male customers
  - 19% of the revenue is generated by Female customers  

> This can be explained by males have more interest in doing outdoor activites with the different categories of Bikes than females.

<a name="project-architecture"></a>
## 📝 Project Architecture

You can find the detailed information on the diagram below:

![AzurePipeline](link)

<a name="data-ingestion"></a>
### 📤 Data Ingestion
- Connected the on-premise SQL Server with Azure using Microsoft Integration Runtime.


- Setup the **Resource group** with needed services (Key Vault, Storage Account, Data Factory, Databricks, Synapse Analytics)

![ressource-group]()

- Migrated the tables from on-premise SQL Server to Azure Data Lake Storage Gen2.

![Migrated_tables]()
![df-pipeline]()

<a name="data-transformation"></a>
### ⚙️ Data Transformation
- Mounted Azure Blob Storage to Databricks to retrieve raw data from the Data Lake.
- Used Spark Cluster in Azure Databricks to clean and refine the raw data.
- Saved the cleaned data in a Delta format; optimized for further analysis.

![Databricks]()

<a name="data-loading"></a>
### 📥 Data Loading
- Used Azure Synapse Analytics to load the refined data efficiently.
- Created SQL database and connected it to the data lake.

![synapse-pipeline]()
![db-synapse]()

<a name="data-reporting"></a>
### 📊 Data Reporting
- Connected Microsoft Power BI to Azure Synapse, and used the Views of the DB to create interactive and insightful data visualizations.

![PowerBI-dashboard]()

### 🛠️ Technologies Used

- **Data Source**: SQL Server
- **Orchestration**: Azure Data Factory
- **Ingestion**: Azure Data Lake Gen2
- **Storage**: Azure Synapse Analytics
- **Authentication and Secrets Management**: Azure Active Directory and Azure Key Vault
- **Data Visualization**: PowerBI

<a name="credits"></a>
## 📋 Credits

- This Project is inspired by the video of the [YouTube Channel "Mr. K Talks Tech"](https://www.youtube.com/watch?v=iQ41WqhHglk)  
