# Zomato_data_lake

This project demonstrates the design and implementation of a modern data lake architecture on Google Cloud Platform using a real-world Zomato-style dataset. It includes raw data ingestion, transformation, enrichment, aggregation, and visualization.

#Project Overview

This project builds an end-to-end data pipeline for food delivery analytics.
It uses:

GCS to store data in Bronze/Silver/Gold layers

Dataproc (Spark) to transform and enrich data

BigQuery as a scalable analytics warehouse

Looker Studio to visualize final business metrics

#Architecture

[Raw Storage - GCS] → [Processing - Dataproc (Spark)] → [Analytics - BigQuery] → [Visualization - Looker Studio]

1. Bronze Layer (Raw Data)

Raw CSV files as received

No transformations

Used for auditability

2. Silver Layer (Cleaned & Standardized Data)

Converted into Parquet

Datatype corrections

Missing value handling

Partitioned by date (dt)

3. Gold Layer (Business-Ready Aggregates)

Restaurant-level KPIs

Aggregated daily metrics

Optimized for BI tools


