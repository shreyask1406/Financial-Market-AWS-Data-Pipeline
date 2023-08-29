# Financial-Market-AWS-Data-Pipeline

## Introduction
In today's rapidly changing financial landscape, staying informed about market trends and stock prices is crucial for both investors and companies. This project focuses on creating an end-to-end data pipeline to collect, store, transform, and analyze financial market data. By utilizing cloud-based solutions and automation, we aim to provide a scalable and efficient way to process and interpret the stock market data.

## Problem Definition
The problem entails handling a large volume of stock market data efficiently and extracting meaningful insights from it. Traditional on-premise data warehousing solutions may fall short in handling the scale and complexity of financial data. This project seeks to leverage cloud services to address these challenges and enable comprehensive data analysis and visualization.

## Data Sources
* Yahoo Finance Data: Historical financial data for Google and Amazon stocks obtained using the Yahoo Finance API through Python.
* DJI Index Data: Financial data of the 30 companies constituting the Dow Jones Industrial Average (DJI) index. Data is scraped from https://www.slickcharts.com/dowjones.

## Data Description
The project focuses on analyzing six dimensions of stock prices: Open, Close, Adjusted Close, High, Low, and Volume. This analysis covers 32 companies over the period of January 1, 2020, to December 31, 2022. The data is stored in CSV and JSON formats in AWS S3 buckets.

## Pipeline Architecture
The architecture involves a series of steps, from data collection to visualization:

* Data Ingestion: Data is fetched from the Yahoo Finance API and Dow Jones index API. This data is then uploaded to the S3 bucket using AWS Lambda and BOTO3 library.

*  Data Storage:The collected data is stored in an AWS S3 bucket. AWS Lambda is employed to upload the data into the designated S3 bucket.
* Data Transformation: AWS Glue jobs are used to transform the data. The union operation combines data from different sources, while the rank assignment introduces a rank column for price analysis.

* Data Analysis: AWS Athena is employed to perform SQL-based querying on the transformed data. The analysis includes trend identification, top-performing companies, and more.

* Data Visualization: AWS Athena is connected to Tableau for creating insightful dashboards that present the analyzed data visually. Dashboards are created to provide clear and intuitive representations of the analyzed financial data.

## Conclusion
The Financial Market Data Pipeline project showcases a comprehensive approach to handling and analyzing stock market data using cloud-based solutions. By collecting, transforming, analyzing, and visualizing the data, we enable investors and companies to gain valuable insights into market trends and stock performance.

