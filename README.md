# Spotify-Ednd-To-End Data-Engineering-ETL-Project

### Introduction
In this project, we will build an ETL(Extract, Transform, Load) pipeline using the Spotify API on AWS. The pipeline will retrieve data from the Spotify API, transform it to the desired format, and load it into the AWS data store.

### Architecture
![Architecture Diagram](https://github.com/gitanksagar/spotify-data-engineering-ETL/blob/main/DESIGN.png)

### AbouT Dataset/API
This API contains information about alums, music artists, songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Installed packages
```
pip install pandas
pip install StringIO
pip install spotipy
```

### Service Used
1. **S3 (Simple Storage Service):** Amazon Simple Storage Service (S3) is a scalable, secure, and durable object storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve any amount of data from anywhere on the web.

2. **AWS Lambda:** AWS Lambda is a serverless compute service provided by Amazon Web Services (AWS) that allows you to run code without provisioning or managing servers. It is part of the broader AWS serverless platform, enabling you to build and deploy applications without dealing with the underlying infrastructure.

3. **CLoud Watch:** Amazon CloudWatch is a monitoring and observability service provided by Amazon Web Services (AWS). It allows you to collect, monitor, and analyze data from various AWS resources, applications, and services in real-time.

4. **Glue Crawler:** AWS Glue Crawler is a service provided by Amazon Web Services (AWS) that automatically discovers, catalogues, and organizes metadata about your data sources. It is a key component of AWS Glue, a fully managed extract, transform, and load (ETL) service.

5. **Data Catalog:** The AWS Glue Data Catalog is a fully managed metadata repository provided by Amazon Web Services (AWS) as part of the AWS Glue service. It serves as a centralized and persistent store for metadata associated with your data assets.

6. **Amazon Athena:** 
Amazon Athena is an interactive query service provided by Amazon Web Services (AWS) that enables you to analyze data stored in Amazon S3 using standard SQL queries. It allows you to quickly and easily query large-scale datasets without the need for complex ETL (Extract, Transform, Load) processes or the need to set up and manage a database.

### Project Execution FLow
Extract data from API-> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data And Load It-> Query Using Athena  
