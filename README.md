This project focuses on data transformation and integration into Azure Cosmos DB using Azure Data Factory. The goal is to create a nested JSON structure where each Order contains an embedded list of OrderLines.

Technologies Used:
Azure Data Factory – For ETL processes and data pipelines

Cosmos DB – A document-based database for storing transformed data

Data Transformation – Use of Flatten, Filter, Group By, and JSON structuring

Contents files that has been added:

aggregate_1, aggregate_2, aggregate_groupby:	Screenshots of aggregation transformations in the data flow

cosmos_data_2, cosmos_data_2_1, cosmos_data_2_2:	Screenshots showing Cosmos DB data and new structures

cosmosdb_data_1:	Image of Cosmos DB database setup before I tried to create a nested structure

data_factory_dataflow_2, data_factory_dataflow_datasets_1:	Screenshots of the data flow in Azure Data Factory. datasets_1 is for the first attemp and dataflow_2 is from when I tried to create a nested structure

derived_1, derived_2:	Screenshots of derived column transformations

EnsureOrderID_data_preview, Filter_data_preview, Flatten_data_preview, GroupOrderLines_data_preview: Previews of transformation results

filter_settings, flatten_settings: Configuration settings for Filter and Flatten transformations

pipeline:	Image of the entire pipeline process in Azure Data Factory

Key Challenges and Solutions:
During data transformation and loading into Azure Cosmos DB, several issues were encountered, such as incorrect delimiters, NULL values, and pipeline execution inconsistencies. To resolve these:

Used Flatten to manage nested structures.
Applied Filters to limit columns and rows for faster debugging.
Deleted and recreated the container when data transfer failed.
Restricted row count to 10 for efficient testing.
After troubleshooting and verifying data sources, the correct dataset was obtained, leading to a successful data transfer to Cosmos DB.
