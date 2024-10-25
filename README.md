# Project_ETL_Crime-Data

BigQuery ETL with Python Project
===============================

This project demonstrates how to query a BigQuery public dataset, perform ETL (Extract, Transform, Load) operations using Python, and load the processed data into a data warehouse. The data pipeline follows a flow from data extraction from BigQuery, transformation in Python, storage in Google Cloud Storage, and loading back into BigQuery with a predefined schema.

Project Flow
============

1. **Query a Public BigQuery Dataset:**
   - Fetch the dataset using BigQuery client.
   - Use Python for querying and extracting data from a BigQuery public dataset.
   
2. **ETL Process in Python:**
   - **Extract:** 
     - Extract data from BigQuery.
   - **Transform:**
     - Perform data cleaning:
       - Handle missing data.
       - Remove duplicate data.
     - Convert data types for compatibility.
     - Timestam of current data
     - Regex
     - Filter data based on relevant conditions.
     - Apply aggregation logic if needed.
     - Conduct any necessary transformations for analysis.
     
3. **Load Data to Cloud Storage:**
   - Store the processed CSV file in Google Cloud Storage (GCS).
   - Create a bucket in GCS and load the transformed data as CSV.

4. **Load Data into BigQuery Data Warehouse:**
   - Create a new BigQuery dataset and table.
   - Define the schema for the new table.
   - Load the CSV file from GCS into BigQuery.
   - Use SQL queries for further analysis and querying in BigQuery.

Setup and Prerequisites
=======================

**Prerequisites:**
- Python 3.x
- Google Cloud SDK
- BigQuery and Cloud Storage access

**Python Libraries Required:**
- `google-cloud-bigquery`
- `google-cloud-storage`
- `pandas`

**Environment Setup:**
1. Install Google Cloud SDK and authenticate using your Google Cloud credentials:
   ::
   
       gcloud auth login
       gcloud config set project <your_project_id>
   
2. Install the required Python libraries:
   ::
   
       pip install google-cloud-bigquery
       pip install google-cloud-storage
       pip install pandas

Diagram Overview
================

The flowchart below summarizes the ETL process followed in this project:

1. **BigQuery → Python:**
   - Extract public dataset from BigQuery.

2. **Python (ETL Process):**
   - Data Cleaning (missing data, duplicates).
   - Data Transformation (type conversions, filtering).
   - Aggregation logic (if needed).

3. **Python → Google Cloud Storage:**
   - Load the transformed CSV data into a GCS bucket.

4. **Google Cloud Storage → BigQuery:**
   - Load data into a new BigQuery table and define its schema.

5. **BigQuery Data Warehouse:**
   - The dataset is now available for querying and analysis.

Contact Information
===================
For any questions or issues, please contact the repository owner or raise an issue in the repository.

