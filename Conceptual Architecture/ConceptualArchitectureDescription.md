## Conceptual Architecture
A conceptual solution architecture is a high-level design that outlines the structure and components of a system or application. It provides a conceptual framework for how the system or application will be built, including the major components, their interactions, and how they fit together to achieve the desired functionality.


A conceptual solution architecture typically includes the following elements:

* **Business requirements**: The business requirements define the goals and objectives of the system or application, and help to guide the design process.
* **Functional requirements**: The functional requirements define the specific features and functions that the system or application must provide to meet the business requirements.
* **Technical requirements**: The technical requirements define the specific technologies, platforms, and tools that will be used to build the system or application.
* **High-level design**: The high-level design outlines the major components of the system or application, their interactions, and how they fit together to achieve the desired functionality.
* **Data model**: The data model defines the structure and relationships of the data that will be used by the system or application.
* **Architecture patterns**: The architecture patterns define the specific design patterns and approaches that will be used to build the system or application, such as microservices, event-driven architecture, or serverless architecture.

Overall, a conceptual solution architecture provides a high-level view of how a system or application will be built, and helps to ensure that the design meets the business and technical
 requirements.

 The image below represents the Conceptual Architecture for the Road Warrior Mobile and Web Application. 

 ![ConceptualArchitecture](../Conceptual%20Architecture/Conceptual_Architecture.jpg)

 The Solution Comprises the following Platorms:
 ### Digital Platform
 * **The Road Warrior Mobile App**, which will be the primary channel for Users.
 * **The Road Warrior Web**, which will be a browser based option for users.
 * **Trip Backend for Front End** which is the backend service for the frontend applications.

### Identity Platform 
This manages information around the client identity, preferences and communication preferences.
* **Identity Service** will enable the registration and security for the applications. Allows users to securely view the Trips and Insights.
* **Preference** will all the administrators with set preferences for which templates to use and which emails to whitelist for the email ingester. It also manages the preferences for the user.

### Trip Platform
This is the core of the solution, which aggregates data from the various sources.
* **Trip Aggregator** pulls together the various reservations into a trip to allow a user to engage at a trip grouping level.

### Data and Insights Platform
The enables the reporting and analytics for the entire solution.
* **Trip Insights**
* **Data products** for the Data and Insights Platform contains data pushed from the Identity and Trip Platform.

### Reservation Platform
This manages the reservation events from email and agencies.
* **Reservation Manager** manages and stores unique reservations.
* **Reservation Ingester** Consumes and filters reservation events.
* **Email Ingester** processes the emails that contain reservation details.
* **Agency Ingester**

### Events Platform
This is the core events backbone for the Eventing Architecture.
* **Event Publisher** publishes events for applications to consume.
* **Events Hub** enable the applications for consume the events that have been published.

### Notification Platform
This enables the notifications to users.
* **Notification Engine** sends notifications about changes to reservations.




