# ADR 09: Data lake

## Status

Accepted

## Context

A data lake is a good option for big data architecture solutions for several reasons:

* Scalability: Data lakes can store vast amounts of data, from structured to unstructured, and can scale to meet the needs of large and complex data sets.
* Agility: Data lakes are flexible and agile, allowing data to be ingested, processed, and analyzed quickly and efficiently.
* Cost-effectiveness: Data lakes are typically more cost-effective than traditional data warehousing solutions, as they can be built on commodity hardware and open-source software.
* Data exploration: Data lakes provide a centralized repository for data, allowing analysts and data scientists to explore and analyze data in a self-service manner.
* Data variety: Data lakes can store a variety of data types, including structured, semi-structured, and unstructured data, which means that they can be used for a wide range of use cases.
* Integration: Data lakes can integrate with a variety of data processing and analytics tools, including Hadoop, Spark, and machine learning frameworks, which means that they can support a wide range of analytical workloads.

Overall, data lakes provide a powerful and flexible big data architecture solution that can support a wide range of data processing and analytical use cases.

## Decision

In order to enable the reporting requirements of our solution we will implement a Data Lake.

## Consequences

* We will need to develop the skills to be able to effectively implement a Data Lake environment