# MeetingBank Data Engineering Project

This project implements an end-to-end data engineering pipeline using the MeetingBank dataset. It demonstrates data ingestion from JSON, intermediate processing using Parquet, a hybrid storage architecture (MySQL hosted on Aiven + MongoDB), and query optimization across both SQL and NoSQL environments.

## Project Structure

```
MeetingBank_Project/
├── Data/                          # Raw JSON source files
├── Processed_Data/                # Intermediate Parquet files and cleaned data
├── database_schema.jpeg           # Visual ERD/Schema layout for the hybrid setup
├── README.md                      # Project documentation
├── requirements.txt               # Python dependencies
│
├── exploratory.py                 # Initial PoC and data exploration
├── main.py                        # Primary orchestrator to run the full pipeline
│
├── step1_process_metadata.py      # Clean metadata, add PKs/indexes, export Parquet
├── step2_process_transcripts.py   # Extract text, word/speaker counts, export Parquet
├── step3_database_loading.py      # Connection logic for Aiven MySQL & MongoDB
│
├── step4_sql_optimization.ipynb   # SQLAlchemy benchmarking (Notebook version)
├── step4_sql_optimization.py      # SQL optimization logic (Script version)
│
├── step5_mql_queries.js           # MongoDB Query Language (MQL) scripts
│
├── step6_sql_nosql_merge_and_visualization_jupyternotebook.ipynb     # Merge SQL and NoSQL data and analysis (Notebook version)
└── step6_sql_nosql_merge_and_visualization.py                        # Merge SQL and NoSQL data and analysis (Script version)
```
## Please note
- Please visit the below link and download the MeetingBank.json file and save it in this repository before you run the program
- [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7989108

## Pipeline Summary
- Exploration & Processing: Analyze raw JSON, extract metadata, and engineer features (e.g., primary keys, transcript word counts, and speaker counts).

- Intermediate Storage: Processed data is saved into the Processed_Data/ directory as .parquet files for high-efficiency I/O.

- Hybrid Database Loading:

  - MySQL (Aiven): Stores structured summary data across three relational tables (cities, meetings, meeting_metrics).

  - MongoDB: Stores unstructured full-length transcripts and associated flexible metadata.

- Query Optimization: Using step4_sql_optimization, the project benchmarks query execution times and demonstrates performance gains through indexing and SQLAlchemy optimization.

- NoSQL Interaction: step5_mql_queries.js contains native MongoDB queries to interact with the document store.

- Data Integration: The final step merges data from both MySQL and MongoDB into a unified DataFrame for comprehensive analytical visualizations.

## Technologies Used
- Python: ETL, feature engineering, and data manipulation (Pandas/Parquet).

- MySQL (Aiven): Structured relational data storage.

- MongoDB: Document database for unstructured full-text transcripts.

- SQLAlchemy: Executing and benchmarking SQL queries inside Python.

- Jupyter Notebooks: Presentation, query performance analysis, and data visualization.

## Key Focus
- Hybrid database architecture (Relational vs. Document).

- Query benchmarking and optimization presentation via SQLAlchemy.

- Data integration across disparate database systems (SQL + NoSQL).

- Subset: Longbeach & Seattle

## Dataset
- Yebowen Hu, Tim Ganter, Hanieh Deilamsalehy, Franck Dernoncourt, Hassan Foroosh, & Fei Liu. (2023). MeetingBank: A Benchmark Dataset for Meeting Summarization (Version v2) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7989108

## Status
- ✔ Meets all course project requirements
- ✔ Demonstrates both SQL and NoSQL (MQL) query capabilities
- ✔ Includes end-to-end integration from raw JSON to final merged visualizations
