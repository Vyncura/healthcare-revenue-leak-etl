# healthcare-revenue-leak-etl

An ETL pipeline demonstrating medical claim data extraction, Pandas transformation, and SQLite loading for healthcare fraud detection and revenue integrity.

# Project 1: The 'Revenue Leak' ETL Pipeline

## Goal
Demonstrate an end-to-end ETL process moving healthcare data from a raw CSV state to a structured, actionable SQLite database.

## Tech Stack
- **Python** (Pandas, Scipy, Scikit-learn)
- **Database**: SQLite
- **Visualization**: Matplotlib, Seaborn

## Pipeline Architecture
1. **Extract**: Ingests raw healthcare claim CSV data.
2. **Transform**: Normalizes column names, handles missing CPT/Provider info, and standardizes formats.
3. **Load**: Pushes cleaned data into a SQLite database (`healthcare_revenue.db`).

## Data Lineage Diagram
(The mermaid diagram from the notebook will render directly in GitHub's README!)

Below is a conceptual representation of the data flow:

## graph LR

    A[Raw CSV: healthcare_fraud_detection.csv] --> B[Pandas Extraction]
    
    B --> C{Transformation Layer}
    
    C -->|Clean & Normalize| D[Structured Dataframe]
    
    D --> E[Load: SQLite Database]
    
    E --> F[(healthcare_revenue.db)]
