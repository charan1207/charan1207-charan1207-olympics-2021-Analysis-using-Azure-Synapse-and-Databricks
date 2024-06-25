# Olympics 2021 Analysis using Azure Synapse and Databricks

## Project Overview

This project involves analyzing the Olympics 2021 dataset using Azure Synapse and Databricks. The dataset includes CSV files for athletes, coaches, medals, and teams, sourced from Kaggle. The project utilizes Azure Data Factory to load the data into Azure Data Lake, and then Databricks for further processing and analysis. Finally, Azure Synapse is used to visualize the data through charts.

## Dataset

The dataset used in this project consists of the following CSV files:
- athletes.csv
- coaches.csv
- medals.csv
- teams.csv
- EntriesGender

## Tools and Technologies

- **Azure Data Factory:** Used for data ingestion into Azure Data Lake.
- **Azure Data Lake:** Storage for the ingested data.
- **Databricks:** Used for data processing and transformation.
- **Azure Synapse:** Used for data analysis and visualization.

## Project Steps

### Step 1: Data Ingestion with Azure Data Factory

The CSV files from Kaggle were ingested into Azure Data Lake using Azure Data Factory.

### Step 2: Data Processing with Databricks after config with Azure data lake storage

# Calculate the average number of entries by gender for each discipline
average_entries_by_gender = entriesgender.withColumn(
    'Avg_Female', entriesgender['Female'] / entriesgender['Total']
).withColumn(
    'Avg_Male', entriesgender['Male'] / entriesgender['Total']
)
average_entries_by_gender.show()

### Step 3: Data Analysis with Azure Synapse
After processing the data in Databricks, Azure Synapse was used for analysis and visualization. Various charts and graphs were created to represent the data insights.

Here are some of the visualizations created during the analysis:

<img width="1195" alt="Screenshot 2024-06-25 at 4 31 49 PM" src="https://github.com/charan1207/charan1207-charan1207-olympics-2021-Analysis-using-Azure-Synapse-and-Databricks/assets/28255223/71b17956-cda5-40aa-b918-208eed38561a">

Description of Visualization 1


Description of Visualization 2

# Conclusion
This project demonstrates the use of Azure Synapse and Databricks for data analysis, from data ingestion to visualization. The combination of these tools allows for efficient data processing and insightful visualizations.

