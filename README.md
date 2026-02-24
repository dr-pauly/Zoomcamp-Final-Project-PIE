# Zoomcamp-Final-Project-PIE

### Objective

The goal of this project is to apply everything we have learned
in this course to build an end-to-end data pipeline.

### Problem statement

Develop a dashboard with two tiles by:

* Selecting a dataset of interest (see [Datasets](#datasets))
* Creating a pipeline for processing this dataset and putting it to a datalake
* Creating a pipeline for moving the data from the lake to a data warehouse
* Transforming the data in the data warehouse: prepare it for the dashboard
* Building a dashboard to visualize the data


## Data Pipeline 

The pipeline could be **stream** or **batch**: this is the first thing you'll need to decide 

* **Batch**: If you want to run things periodically (e.g. hourly/daily)

## Technologies 

You don't have to limit yourself to technologies covered in the course. You can use alternatives as well:

* **Cloud**: AWS, GCP, Azure, ...
* **Infrastructure as code (IaC)**: Terraform, Pulumi, Cloud Formation, ...
* **Workflow orchestration**: Airflow, Prefect, Luigi, ...
* **Data Warehouse**: BigQuery, Snowflake, Redshift, ...
* **Batch processing**: Spark, Flink, AWS Batch, ...
* **Stream processing**: Kafka, Pulsar, Kinesis, ...

If you use a tool that wasn't covered in the course, be sure to explain what that tool does.

## Dashboard

You can use any of the tools shown in the course (Looker Studio or Streamlit) or any other BI tool of your choice to build a dashboard.

Your dashboard should contain at least two tiles, we suggest you include:

- 1 graph that shows the distribution of some categorical data 
- 1 graph that shows the distribution of the data across a temporal line

Ensure that your graph is easy to understand by adding references and titles.

## Peer reviewing

> [!IMPORTANT]  
> To evaluate the projects, we'll use peer reviewing. This is a great opportunity for you to learn from each other.
> * To get points for your project, you need to evaluate 3 projects of your peers
> * You get 3 extra points for each evaluation

## Evaluation Criteria

* Problem description
    * 0 points: Problem is not described
    * 2 points: Problem is described but shortly or not clearly 
    * 4 points: Problem is well described and it's clear what the problem the project solves
* Cloud
    * 0 points: Cloud is not used, things run only locally
    * 2 points: The project is developed in the cloud
    * 4 points: The project is developed in the cloud and IaC tools are used
* Data ingestion (choose either batch or stream)
    * Batch / Workflow orchestration
        * 0 points: No workflow orchestration
        * 2 points: Partial workflow orchestration: some steps are orchestrated, some run manually
        * 4 points: End-to-end pipeline: multiple steps in the DAG, uploading data to data lake
    * Stream
        * 0 points: No streaming system (like Kafka, Pulsar, etc)
        * 2 points: A simple pipeline with one consumer and one producer
        * 4 points: Using consumer/producers and streaming technologies (like Kafka streaming, Spark streaming, Flink, etc)
* Data warehouse
    * 0 points: No DWH is used
    * 2 points: Tables are created in DWH, but not optimized
    * 4 points: Tables are partitioned and clustered in a way that makes sense for the upstream queries (with explanation)
* Transformations (dbt, spark, etc)
    * 0 points: No tranformations
    * 2 points: Simple SQL transformation (no dbt or similar tools)
    * 4 points: Tranformations are defined with dbt, Spark or similar technologies
* Dashboard
    * 0 points: No dashboard
    * 2 points: A dashboard with 1 tile
    * 4 points: A dashboard with 2 tiles
* Reproducibility
    * 0 points: No instructions how to run the code at all
    * 2 points: Some instructions are there, but they are not complete
    * 4 points: Instructions are clear, it's easy to run the code, and the code works
