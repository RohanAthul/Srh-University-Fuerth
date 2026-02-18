# MeetingBank Data Engineering Project

This project implements an end-to-end data engineering pipeline using the MeetingBank dataset. It demonstrates data ingestion from JSON, intermediate processing using Parquet, hybrid storage architecture (MySQL hosted on Aiven + MongoDB), and query optimization across both SQL and NoSQL environments, culminating in combined visualizations.

## Project Structure

```
MeetingBank_Project/
├── Data/                              # Raw JSON source file
├── Processed_Data/                    # Parquet files storage
├── README.md
├── .gitignore
│
├── step0_exploratory.py               # MeetingBank.json data exploration
├── step1_process_metadata.py          # Clean metadata, add PK/indexes, export Parquet
├── step2_process_transcripts.py       # Extract text, word/speaker counts, export Parquet
├── step3_database_loading.py          # Connect to Aiven MySQL & MongoDB, load tables
│
├── step4_sql_optimization.ipynb       # SQLAlchemy query execution and benchmarking
├── step5_mql_queries.py               # MongoDB query exploration and data generation
│
└── step6_visualization.ipynb          # Merge SQL & NoSQL data for future comprehensive analysis
```

## Pipeline Summary
- Exploration & Processing: Analyze raw JSON, extract metadata, and engineer features (e.g., primary keys, transcript_word_count, speaker_count).

- Intermediate Storage: Export processed data as highly efficient .parquet files.

- Hybrid Database Loading: * Split structured summary data into three relational tables (cities, meetings, meeting_metrics) in MySQL (Aiven).

- Load unstructured full-length transcripts and associated numerical metrics into MongoDB.

- Query Optimization: Use SQLAlchemy in a Jupyter Notebook to present before-and-after query optimization results.

- NoSQL Exploration: Generate and retrieve data using MongoDB Query Language (MQL).

- Data Integration & Visualization: Link and merge data from both the MySQL and MongoDB servers into a single unified dataframe for final analytical visualizations.

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
