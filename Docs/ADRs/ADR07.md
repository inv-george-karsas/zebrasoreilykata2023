# ADR 07: CosmosDB Database

## Status

Accepted

## Context

* Globally distributed: Azure Cosmos DB is a globally distributed database service, which means that you can replicate your data across multiple regions for high availability and low latency.
* Multi-model: Azure Cosmos DB supports multiple data models, including document, key-value, graph, and column-family, which means that you can choose the best data model for your application.
* Scalability: Azure Cosmos DB is designed to scale horizontally and vertically, which means that you can scale your database to handle any amount of data and traffic.
* Consistency: Azure Cosmos DB provides strong consistency guarantees, which means that your data is always consistent across all regions.
* Multi-API support: Azure Cosmos DB supports multiple APIs, including SQL, MongoDB, Cassandra, Gremlin, and Azure Table Storage, which means that you can use your preferred API and data model.
* Security: Azure Cosmos DB provides several security features, such as encryption at rest and in transit, role-based access control, and Azure Active Directory integration, which help protect your data.

Overall, Azure Cosmos DB provides a powerful and flexible database service that can be used for a wide range of applications, from web and mobile apps to IoT and gaming.

## Decision

We will utilise CosmosDB as the prefered database within our application architecture 

This will also act as the data store that the trigger for the events subscriber will work off

## Consequences

* We will need to provide guidance on how to implement CosmosDB effectively
* We will need to ensure that our Azure Policies cover the usage of CosmosDB
