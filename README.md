# Spotify User Insights Data Platform

This project builds a scalable **ETL (Extract, Transform, Load) pipeline** to analyze Spotify user data. It leverages cloud-based services like **AWS Lambda**, **AWS Glue**, **Amazon S3**, and **Snowflake**, with interactive visualizations created using **Power BI**. The goal is to provide actionable insights into user engagement and listening habits.

---

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Architecture](#architecture)
3. [Technologies Used](#technologies-used)
4. [Steps Implemented](#steps-implemented)
5. [Key Features](#key-features)
6. [How to Run](#how-to-run)
7. [Results & Insights](#results--insights)
8. [Future Enhancements](#future-enhancements)

---

## **Project Overview**
This platform processes data from the **Spotify API** to extract insights into user behavior. The ETL pipeline efficiently handles data extraction, transformation, and loading into a cloud data warehouse (**Snowflake**) for analysis and reporting.

- **Data Volume**: Processed over **500,000 Spotify user records** (~50MB of data).
- **Outcome**: Generated actionable insights, visualized through Power BI dashboards.

---

## **Architecture**
![Architecture Diagram](./Spotify_User_Insights_ETL_Architecture.png)

### **Pipeline Flow**
1. **Extract**: Data is fetched from Spotify API using Python and stored in **Amazon S3**.
2. **Transform**: Data is cleaned and processed using **AWS Glue** with PySpark.
3. **Load**: Transformed data is loaded into **Snowflake** using **Snowpipe**.
4. **Visualize**: Insights are presented through **Power BI dashboards**.

---

## **Technologies Used**
- **Programming Languages**: Python, SQL
- **Cloud Services**:
  - **AWS Lambda**: Serverless compute for data extraction.
  - **Amazon S3**: Storage for raw and processed data.
  - **AWS Glue**: Managed ETL for data transformation using PySpark.
  - **Snowflake**: Cloud data warehouse for structured data.
  - **Snowpipe**: Automated data ingestion from S3 to Snowflake.
- **Visualization**: Power BI

---

## **Steps Implemented**

### 1. **Data Extraction**
- Connected to the Spotify API using Python.
- Triggered **AWS Lambda** to fetch user data.
- Stored raw JSON data in **Amazon S3**.

### 2. **Data Transformation**
- Used **AWS Glue** to process raw data.
- Cleaned and transformed data into a tabular format using PySpark.
- Scheduled AWS Glue jobs for periodic data updates.

### 3. **Data Loading**
- Configured **Snowpipe** to ingest transformed data from S3 into **Snowflake**.
- Created tables in Snowflake for structured querying.

### 4. **Visualization**
- Connected Snowflake to Power BI.
- Built interactive dashboards showcasing:
  - User engagement patterns.
  - Popular songs, artists, and playlists.
  - Trends in listening habits.

---

## **Key Features**
- **Scalable ETL Pipeline**: Processes over 500,000 records efficiently using cloud services.
- **Automation**: Utilized serverless computing (AWS Lambda) and scheduled jobs (AWS Glue).
- **Insights-Driven**: Delivered actionable insights via Power BI dashboards.
