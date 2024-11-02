# FDIC-Banking-Data-Pipeline

## Description
This project is designed to retrieve comprehensive banking data from the FDIC API, overcoming various challenges to create a consolidated panel dataset. The goal was to download data from different sections of the FDIC API and merge these datasets into a structured panel format using Stata.

## Overview
The FDIC Banking Data Pipeline allows for the efficient fetching of banking data, including institutions, locations, summary of deposits, and financials. By addressing issues such as rate limits and data segmentation, the project successfully compiles a large volume of banking data into a single dataset that can be easily analyzed.

## Features
- **Data Retrieval**: Utilizes the FDIC API to fetch detailed banking data, including both active and inactive institutions, branch locations, annual deposits, and quarterly financial information.
- **Multithreading**: Implements multithreading to optimize download speed, allowing multiple requests to be sent simultaneously. This significantly reduces the time required to retrieve large datasets.
- **Pagination**: Uses a pagination approach to manage large volumes of data efficiently, ensuring that requests are broken down into smaller chunks that can be easily processed.
- **Resume Capability**: Incorporates a resume functionality to continue downloading from the last successful point in case of interruptions, avoiding the need to restart the entire data retrieval process.
- **Data Labeling**: Applies clear labels to each variable in the dataset, ensuring they are categorized appropriately for seamless merging.
- **Panel Structure Creation**: Merges multiple datasets into a comprehensive panel format that includes key identifiers for branches and institutions across various years and quarters.

## Dataset Size
The final output consists of nearly **10 million rows** of panel data, resulting in an uncompressed dataset of approximately **40 GB** in Stata (.dta) format.

## Challenges Overcome
- **Data Volume Management**: Faced with the limitation of retrieving only 10,000 observations per request, the project implemented a chunked download strategy to handle larger datasets without exceeding API constraints.
- **Variable Consistency**: Ensured consistency in variable labels and definitions across multiple datasets, facilitating a smooth merging process.
- **Integration of Diverse Data Types**: Successfully merged annual and quarterly financial data, aligning them within the panel structure while maintaining data integrity.

## Important Notes
The project has been structured to allow for sequential execution of scripts, ensuring that data processing flows smoothly from fetching to merging. This facilitates easy updates and maintenance of the dataset as new data becomes available.

Last Updated: November 2, 2024
