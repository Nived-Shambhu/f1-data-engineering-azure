# F1 Race Data Engineering & Analytics Pipeline

## Project Overview

This project demonstrates an end-to-end data engineering pipeline built using Microsoft Azure services and Power BI. It collects Formula 1 race data from the Jolpica REST API, stores it in a data lake, transforms nested JSON data into a structured format, and presents insights through an interactive dashboard.

## Architecture

Jolpica F1 API → Azure Data Factory → Azure Data Lake Storage Gen2 → Data Transformation → Power BI Dashboard

## Technologies Used

- **Azure Data Factory (ADF):** Data ingestion and orchestration
- **Azure Data Lake Storage Gen2 (ADLS Gen2):** Data storage
- **REST API:** Source of Formula 1 race data
- **Mapping Data Flows:** Data transformation and flattening nested JSON
- **Power BI Desktop:** Interactive data visualization
- **Git and GitHub:** Version control and project documentation

## Data Lake Structure

- `raw/` — Original API response
- `ingested/` — Data copied into the ingestion layer
- `presentation/` — Data prepared for analytics and reporting

## Data Pipeline

1. Extract 2024 Formula 1 race data from the Jolpica API.
2. Store the raw JSON response in ADLS Gen2.
3. Copy data through the ingestion layer.
4. Flatten nested JSON and select relevant race and circuit attributes.
5. Prepare structured data for Power BI.
6. Visualize race information, circuits, countries, and locations in a dashboard.

## Data Attributes

The transformed dataset includes:

- Season and round
- Race name and race date
- Circuit ID and circuit name
- Latitude and longitude
- City and country
- Race time

## Key Outcomes

- Built and tested Azure Data Factory pipelines.
- Implemented a layered data lake structure.
- Transformed nested API JSON into structured race data.
- Created an interactive Power BI dashboard.

## Data Source

Jolpica F1 API: https://api.jolpi.ca/ergast/f1/2024/races/

## Future Improvements

- Automate scheduled data ingestion.
- Extend the pipeline to include drivers, constructors, qualifying, and race results.
- Add more analytical measures and dashboard insights.