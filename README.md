Table of Contents

1. [The Road Warrior](#the-road-warrior)  
    1.1 [Architects and Engineers](#architects-and-engineers)  
    1.2 [Background](#background)  
    1.3 [Objective](#objective)  
    1.4 [Business Requirements](#business-requirements)  
    1.5 [Principles](#principles)  
    1.6 [Drivers](#drivers)  
    1.7 [Benefits](#benefits)  
    1.8 [Technical considerations](#technical-considerations)  
    1.9 [ADR Registry](#adr-registry)  
    1.10 [NFR Registry](#nfr-registry)  

2. [Architecture](#architecture)  
    2.1 [Conceptual Architecture](#conceptual-architecture)  
    2.2 [Logical Architecture](#logical-architecture)  
    2.3 [Component Descriptions](#component-descriptions)  
    2.4 [General Application Design ](#general-application-design)  
    2.5 [Logical Architecture Overview](#logical-architecture-overview)  
    2.6 [User Interface](#user-interface)  

# The Road Warrior 

## Architects and Engineers

- [George Karsas](https://www.linkedin.com/in/george-karsas-5591816b)
- [Chris Kleb](https://za.linkedin.com/in/chris-kleb-75738218)
- [Hiren Chhiba](https://www.linkedin.com/in/hiren-c-24a2601/)
- [Henry Oliver](https://za.linkedin.com/in/henry-oliver-6263356)

## Background

Road Warrior, a new startup wants to build the next generation online trip management dashboard to allow travelers to see all of their existing reservations organized by trip either online (web)or through their mobile device.

## Objective

An online platform to make travel plans easier which organises to book a flight, hotel or car from anywhere, globally.

## Business requirements
### Short term
- A self-booking software travelers can use to make business travel booking system online.
- Alerts travelers with flight changes and reminders
- Available globally, 2 million users, 15 million user accounts.
- Integrate with travel systems abd travel agents

### Long term
- Allow booking for other travel mediums
- Travel expense reporting (capture images of receipts and submit expense reports)
- Provide summary reports for users
- Concierge Services
- Interactive airport and travel maps

## Principles
- Simple business processes
- Scalable and maintainable landscape, ensuring standardized infrastructure
- Leveraging SMAC (social, mobile, analytics, and cloud)  for a digital estate

## Drivers

- Number of Roadwarrior employees : 4 employees
- How many people use Road Warrior: 12 million+ users
- Countries that has users in : Worldwide
- Service hours: 24 *7
- Peak hours: 10h00 - 18h00 (GMT)
- Availability percentage: 99.99905% 

## Benefits
- Simplifies booking - by combining flight and hotel options into a single package.
- Enhances travel personalization - enhances personalization by studying employees’ booking patterns and using predictive analytics
- Enables travel cost savings -  offers an extensive inventory of flights and hotels sourced from a Global Distribution System.
- Provides 24/7 support - can reach out to the solution provider’s support team via multiple channels like calls, chats, and emails and get the required help.
- Leverages travel analytics - summarizes your travel booking data into customizable travel analytics dashboards and reports for better understanding.

## Technical considerations 

- Achieving a high level of availability with minimal downtime, such as allowing only up to 5 minutes of unplanned downtime per month, for a globally accessible cloud application:
    - Availability 99.99905%
    - Leverage CSP Regions and AZ's
    - Fault tolerance + mechanism (graceful degradation)
    - Automated monitoring
    - Chaos engineering
    - Elastic scaling ( 2mil + users) - Compte, network (and storage?)
- Performance - 5 miuntes unplanned downtime annualy allowed + 800ms response time
    - Data caching + content delivery network ( content compression + Edge computing)
    - Load balancing
    - Asynchronous processing??
    - DB query optimization
- Security
    - Authentication
        - User access (2fa for web)
        - API permissions
        - Service accounts
    - Data encryption
        - Rest - AES 256
        - Transit TLS 1.2
    - Data compliance
        - Data Protection (European Union - GDPR)

## [NFR Registry](./Docs/NFR_Registry.md)
We have identified several Non Functional Requirements that need to be addressed in the solution.
## [ADR Registry](./Docs/ADR_Registry.md)
We have made several Architecture Decisions that will allow the solution to deliver the NFRs.

## ADR to NFR Mapping
This table illustrates how the Architecture Decisions Map to the Non Functional Requirements

| NFR                  | ADR 01 | ADR 02 | ADR 03 | ADR 04 | ADR 05| ADR 06 | ADR 07 | ADR 08| ADR 09 |
| ---                  | ------ | ------ | ------ | ------ | ----- | ------ | ------ | ----- | ------ |
| 01 - Performance     |   x    |    x   |   x    |        |   x   |        |   x    |       |   x    |
| 02 - Scalability     |        |    x   |   x    |    x   |   x   |        |   x    |       |   x    |
| 03 - Availability    |        |    x   |        |        |   x   |        |   x    |       |        |
| 04 - Security        |   x    |        |        |        |   x   |        |        |   x   |        |
| 05 - Reliability     |        |    x   |        |    x   |   x   |        |        |       |        |
| 06 - Maintainability |   x    |        |   x    |    x   |   x   |    x   |        |   x   |        |

# Architecture 

## Conceptual Architecture

Description of the conceptual architecture navigation can be found [here](./Conceptual%20Architecture/ConceptualArchitectureDescription.md)

![ConceptualArchitecture](./Conceptual%20Architecture/Conceptual_Architecture.jpg)

## Logical Architecture


### General Application Design 

![GeneralApplicationDesign](./Logical%20Architecture/General_Application_Design.jpg)

#### Component Descriptions

- **MSAL**: Microsoft Authentication Library, a set of client libraries used to authenticate users and acquire tokens in order to access protected resources such as Microsoft Graph or other APIs that support Microsoft Azure Active Directory (Azure AD) authentication.
- **RESTful Interface**: A type of web service that uses HTTP methods (GET, POST, PUT, DELETE) to interact with resources in a stateless manner.
- **Business Logic Layer**: The layer of an application that contains the core business logic and rules that govern the behavior of the system.
- **Repository Layer**: The layer of an application that provides an abstraction over the database, allowing the application to interact with data in a more object-oriented way.
- **Provider Layer**: The layer of an application that provides access to external services, such as payment gateways or email services.
- **Observability**: The ability to measure and monitor the performance and behavior of a system, often through the use of logging, metrics, and tracing.
- **Event Subscriber**: A component that listens for events published by other components and takes action based on those events.
- **Event Publisher**: A component that publishes events to a message broker or other system, allowing other components to subscribe to those events.
- **External Service**: A service provided by a third-party, such as a payment gateway or email service.
- **Database**: A structured collection of data that is stored electronically, often used to persist application data.

### Logical Architecture Overview 
Description of the logical architecture navigation can be found [here](./Logical%20Architecture/LogicalArchitectureDescription.md)

![LogicalArchitectureOverview](./Logical%20Architecture/Logical_Architecture.jpg)

Individual Component Design can be found [here](./Logical%20Architecture/Individual%20Components/IndividualComponents.md)

## User Interface

A mock up of the potential application mobile interface can be found [here](./User%20Interface%20Design/interfaceDesign.md)