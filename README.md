# LinkedIn-Data-Mart-
Sure, here's an updated README file incorporating the information about wildcards in the ETL process:

---

# LinkedIn Data Mart Project

## Overview

This project involves the development and implementation of an ETL (Extract, Transform, Load) pipeline designed to extract LinkedIn data, ensuring efficient data integration into SQL databases for streamlined storage and management. Additionally, it leverages the dataset to create insightful visualizations using PowerBI, enhancing data accessibility and supporting strategic decision-making processes.

## Features

- **ETL Pipeline**: Streamlined extraction, transformation, and loading of LinkedIn data into SQL databases.
- **Data Integration**: Ensures seamless data integration for efficient storage and management.
- **PowerBI Visualizations**: Creates insightful visualizations .


## ETL Pipeline

The ETL pipeline consists of the following steps:

1. **Extract**: Fetch LinkedIn data using the LinkedIn API or from provided datasets.
   - **Wildcards in Extract Phase**: In file operations, wildcards can be used to specify a subset of files. For example, using `data_*.json` will match all filenames that start with "data_" and end with ".json". In SQL queries, wildcards with the `LIKE` operator (e.g., `%` for any sequence of characters, `_` for any single character) help in matching patterns in text fields.

2. **Transform**: Clean and transform the data to ensure consistency and accuracy.
   - **Wildcards in Transform Phase**: Wildcards can be used in search-and-replace functions within strings to alter data based on patterns. For example, replacing any number in a string with a placeholder.

3. **Load**: Integrate the transformed data into the SQL database for efficient storage and management.
   - **Wildcards in Load Phase**: Wildcards might be used in scripts or commands to specify which files to load if there’s a batch of similarly named files in a directory.

### Key Components

- `extract.py`: Handles data extraction from LinkedIn.
- `transform.py`: Contains data cleaning and transformation logic.
- `load.py`: Manages data loading into the SQL database.
- `etl_pipeline.py`: Orchestrates the entire ETL process.

## Data Visualization

The PowerBI dashboard provides various visualizations to make data accessible and support strategic decision-making. Key visualizations include:

- **Profile Analysis**: Overview of LinkedIn profiles and their attributes.
- **Connection Trends**: Analysis of connection growth over time.
- **Engagement Metrics**: Metrics related to post engagement, such as likes, comments, and shares.
- **Demographic Insights**: Insights into demographic data of connections and network.

### Steps to Create Visualizations

1. **Connect PowerBI to the SQL database**:
   - Open PowerBI Desktop.
   - Go to `Home` -> `Get Data` -> `SQL Server`.
   - Enter the server and database details and load the data tables.

2. **Load the data tables**:
   - Select the relevant tables and load them into PowerBI.

3. **Create visualizations and configure reports**:
   - Use the available data fields to create visualizations.
   - Arrange the visualizations into meaningful reports.

4. **Publish the dashboard**:
   - Save the PowerBI file.
   - Publish the dashboard to the PowerBI service for access by stakeholders.

## Project Structure

```
linkedin-data-mart/
│
├── data/                   # Raw and processed data files
│
├── etl/
│   ├── extract.py          # Script to extract data
│   ├── transform.py        # Script to transform data
│   └── load.py             # Script to load data into the database
│
├── visualizations/
│   └── LinkedIn_Visualizations.pbix   # PowerBI file for visualizations
│
├── config.py               # Configuration file for database connection
├── etl_pipeline.py         # Main ETL pipeline script
├── requirements.txt        # Python dependencies
└── README.md               # Project README file
```




