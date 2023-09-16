# ADR 03: Microservice architecture

## Status

Accepted 

## Context

* Scalability: Microservices can be scaled independently, which allows for greater flexibility and responsiveness to changes in demand.
* Resilience: Microservices are designed to be fault-tolerant, meaning that if one service fails, it won't bring down the entire system.
* Agility: Microservices allow for faster development and deployment cycles, as each service can be developed and deployed independently.
* Technology heterogeneity: Microservices allow you to use different technologies for different services, which can be useful if you have different requirements for each service.
* Easy maintenance: Microservices are typically smaller and easier to maintain than monolithic applications, as each service can be updated or replaced without affecting the entire system.
* Team autonomy: Microservices allow for greater autonomy for development teams, as each team can focus on a specific service without having to worry about the entire system.

## Decision
We will utilise a Microservice Architecture where appropriate in our application architecture


## Consequences

* We need to ensure that we have defined standards for implementing Microservices.
* We need to ensure that we have defined practices and guidelines for versioning, deploying, testing and monitoring Microservices. 
