---
title: Technical Concepts
keywords: Data
sidebar: home_sidebar
permalink: data_technicalConcepts.html
last_updated: March 30, 2018
tags: [get_started]
folder: Data
---

## The overall data landscape

Data covers a very large set of technologies and concepts. It's helpful to think about the overall data pipeline, and how data flows through a typical system. A good place to start is with the *Lambda Architecture* concept, which is essentially all about data-ingress, processing (both hot- and cold-path), and data-serving.

Note: when talking about hot-path and cold-path:
 - hot path refers to streaming (realtime / near-realtime) data workloads
 - cold path refers to batch-processing and non-realtime data workloads

Many systems deal with both hot-path and cold-path. For example: Imagine a theme park: With hot-path processing, maybe roller coasters are being monitored for variations in ride duration, or count of rides within a given time window. With cold-path processing, imagine taking daily data, over an entire season, to examine ridership for certain days of the week, holidays, etc.

While not every system falls within the Lambda Architecture model, it helps to break down the various Azure services in terms of where they would fit within the overall pipeline.

If we expand just a bit, we can break things down into 5 core areas:

 `INGRESS -> INLINE PROCESING -> PERSISTENT STORAGE -> BATCH -> WAREHOUSE / SEARCHABLE DB`

### Data Ingress

For ingesting lots of data, in a realtime fashion, often technologies such as Event Hubs and IoT Hub are used. IoT Hub uses Event Hubs at its core, and adds additional features such as device registration. And event Hubs, at *its* core, uses Azure Service Bus. For more information on Iot Hub and Event Hubs, please see content for the [Connect Everything](connecteverything.html) pillar.

There are also scenarios that take advantage of Azure Functions, Service Fabric, and Containers to pull data from external sources. For more details about these technologies, please visit the [Compute](compute.html) pillar.

### Inline Processing

Inline processing might be a stream-processing technology, or it could be something like Azure Functions.

Example technologies for inline processing include (but are not limited to):

 - Azure Stream Analytics
 - Apache Spark (with platforms such as HDInsight and Databricks)

 Learning paths for these technologies can be found in the [Data Stream Processing](data-stream-processing.html) page.

### Persistent Storage / Batch / Warehousing

Data storage may be as straightforward as using Azure Storage (e.g. tables, blobs). Or, for more robust searchable solutions, a relational or non-relational (NoSQL) database can be used such as:

 - SQL Database / SQL Managed Instances / MySQL / Postgres (relational database services)
 - Cosmos DB (NoSQL database service)
 - Azure Data Lake Store / Azure Data Warehouse (very large scale archive storage)

 Learning paths for these technologies can be found in the [Data Storage](data_Storage.html) page.


## Technical Concepts

- [Column Stores and Row Stores]()
- [Distributed Computing]()
- [ACID properties]()
- [CAP theorem]()
- [OLTP & OLAP]()
- [Polyglot persistence]()
- [Kappa Architecture]()
- [ETL / ELT]()
