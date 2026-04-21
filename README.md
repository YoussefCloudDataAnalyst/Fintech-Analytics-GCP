# Fintech Cloud Analytics: End-to-End Loan Data Pipeline

## 📌 Project Overview
This project serves as a technical case study in building a scalable data infrastructure on **Google Cloud Platform**. Using a fintech dataset, I designed and implemented a data pipeline that moves from raw ingestion to complex relational modeling and executive-level visualization.

##  The Tech Stack
* **Data Warehouse:** Google BigQuery
* **Business Intelligence:** Looker / Looker Studio
* **Language:** SQL (Standard SQL)
* **Core Concepts:** Schema Design, Nested Data (Structs), Table Partitioning, and CTAS Modeling.

##  Data Architecture & Engineering
The project involved several key stages of "Data Detective" work to transform raw, semi-structured data into a relational gold mine:

### 1. Data Ingestion & Schema Definition
I utilized BigQuery's `LOAD DATA` capabilities to ingest external CSV mappings, defining explicit schemas for geographic subregions to ensure data integrity.

### 2. Handling Nested Data & Structs
A major challenge was navigating **Nested Data Structures**[cite: 39]. [cite_start]I wrote specialized queries to extract `purpose` attributes from within `application` structs, effectively flattening complex data for easier analysis.

### 3. Data Deduplication & Transformation
Using **CTAS (Create Table As Select)** statements, I architected a cleaned "Single Source of Truth" by:
* Deduplicating loan purposes into a standalone reference table.
* Aggregating loan volumes by `issue_year` to track historical growth.

### 4. Advanced Relational Joins
I implemented `INNER JOIN` logic to bridge the gap between loan transactions and regional mapping, allowing for high-level geographic analysis.

## Key Business Insights
* **Historical Volume:** Successfully tracked loan counts per year, identifying growth trends in the fintech portfolio.
* **Regional Distribution:** Developed queries to map loan IDs directly to specific subregions and regions for localized risk assessment.

##  Future-Proofing 
To ensure this pipeline remains performant as the data grows, I focused on:
* **Derived Tables:** Reducing query costs by pre-calculating common aggregates.
* **Optimization:** Preparing the infrastructure for **Partitioned and Clustered tables** to optimize BigQuery scan costs.

---
*This project was completed as part of the Google Cloud Data Analytics Professional Certificate.*
