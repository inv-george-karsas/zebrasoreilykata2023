# ADR 01: Common Software Application Design Principles and practice

## Status

Accepted

## Context

When creating a microservice, in order to speed up development of the application, a consistent approved pattern of tools, tech and libraries allow for less cognitive load around building a microservice

## Decision

- All applications with a restful interface will use MSAL as an Authorization/Authentication mechanism
- All Applications will follow a CQRS pattern, with a flavor of DDD as well as repository design.
- All applications that will need to consume or publish an event will conform to the EVENTS PLATFORM.
- All applications will have Open Telemetry standards to make support and trouble shooting of an application easy and consistent
- All applications will have a provider layer or use a prebuilt provider to interface with an external resources (db, file, rest, etc)

## Consequences

Failure in design, means its not just one application that will fail, but all. A pattern means we need to due diligence around the implementation of the pattern.

