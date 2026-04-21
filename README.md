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
[cite_start]I utilized BigQuery's `LOAD DATA` capabilities to ingest external CSV mappings, defining explicit schemas for geographic subregions to ensure data integrity[cite: 2, 8, 9, 10].

### 2. Handling Nested Data & Structs
[cite_start]A major challenge was navigating **Nested Data Structures**[cite: 39]. [cite_start]I wrote specialized queries to extract `purpose` attributes from within `application` structs, effectively flattening complex data for easier analysis[cite: 20, 21].

### 3. Data Deduplication & Transformation
Using **CTAS (Create Table As Select)** statements, I architected a cleaned "Single Source of Truth" by:
* [cite_start]Deduplicating loan purposes into a standalone reference table[cite: 23, 24, 25].
* [cite_start]Aggregating loan volumes by `issue_year` to track historical growth[cite: 34, 35, 37].

### 4. Advanced Relational Joins
[cite_start]I implemented `INNER JOIN` logic to bridge the gap between loan transactions and regional mapping, allowing for high-level geographic analysis[cite: 11, 12, 17, 18].

## Key Business Insights
* [cite_start]**Historical Volume:** Successfully tracked loan counts per year, identifying growth trends in the fintech portfolio[cite: 31, 35].
* [cite_start]**Regional Distribution:** Developed queries to map loan IDs directly to specific subregions and regions for localized risk assessment[cite: 13, 15].

##  Future-Proofing 
To ensure this pipeline remains performant as the data grows, I focused on:
* [cite_start]**Derived Tables:** Reducing query costs by pre-calculating common aggregates[cite: 40].
* [cite_start]**Optimization:** Preparing the infrastructure for **Partitioned and Clustered tables** to optimize BigQuery scan costs[cite: 41].

---
*This project was completed as part of the Google Cloud Data Analytics Professional Certificate.*
