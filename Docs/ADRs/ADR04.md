# ADR 04: 	Event driven architecture

## Status

Accepted

## Context

* Loose coupling: Event-driven architectures allow for loose coupling between services, which means that services can be developed and deployed independently without having to worry about the details of other services.
* Scalability: Event-driven architectures can be scaled horizontally by adding more instances of a service to handle increased load.
Resilience: Event-driven architectures are designed to be fault-tolerant, meaning that if one service fails, it won't bring down the entire system.
* Flexibility: Event-driven architectures allow for greater flexibility in how services are composed and orchestrated, as services can react to events in real-time.
* Real-time processing: Event-driven architectures are well-suited for real-time processing of data, as events can be processed as they occur.
* Asynchronous processing: Event-driven architectures allow for asynchronous processing of data, which can improve performance and reduce latency.

## Decision
We will use an Event Driven Architecture within our Application Architecture


## Consequences

* We need to set guidelines for defining events.
* We need to set standards for implementing events.
* We need to ensure that we can monitor and support an event based architecture.
