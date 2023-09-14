# High-Level Design (HLD) and Low-Level Design (LLD)

System design architecture can be depicted as High-Level Design (HLD) or Low-Level Design (LLD). Let's explore what they signify.

## 1. High-Level Design (HLD):

High-Level Design focuses on the main components that would be developed for the resulting product. It provides a high-level overview, including:

- Principal components
- Database
- Services
- Relationships between each module/component

Here's a brief description of the system:

### Example 1:
Suppose Ram wants to create a social media app. The high-level design will consist of an overview of the system like a mobile app for iOS/Android, an app for OS/X & Windows, Web GUI, SQL/No-SQL database. In contrast, the low-level design would consist of how each user application is logically linked to other modules and all the extra details of each component mentioned in the HLD that’s useful and necessary before developers can start writing the code directly.

### Example 2:
Let’s try to design a Cab Booking System like Ola, Uber, etc. An application like this has extensive design and functionalities involved. Well, let's try designing one.
First, we must understand the Functional and Non-Functional Requirements of such applications.

#### Functional Requirements:
- Checking nearest cab availability
- Booking a cab
- Fare calculation and payment
- GPS tracking for the cab

#### Non-Functional Requirements:
- Security (secure transactions)
- Reliability
- Scalability
- Less Response Time

**High-Level Design** would consist of the major modules for Desktop and Mobile Clients like:

- Manage Car Details
- Manage Customer Details
- Manage Booking Details
- Manage Price Details
- Manage Payment Details
- Manage Car Insurance Details
- Map Service

The admin application would mainly consist of a cab request service and cab finder service. Also, remember that the live location of a driver is always shared with the system; this can be further managed by a tracking module, i.e., the location service. The trip completion event would be managed by the payment service, which would calculate the price based on the distance covered and the rate per unit distance.

High-Level Design would include a brief description of the basic functionalities like user login to the system, checking credentials, checking car availability in the vicinity, etc., and the databases like the profile database and authentication database.

## 2. Low-Level Design (LLD):

In contrast to HLD, Low-Level Design considers the in-depth and detailed design of each component mentioned in the High-Level Design of the system. It exposes the logical relationship between different elements and provides a detailed description of all the modules. Low-Level Design includes more technical information as compared to High-Level Design. It includes the description of the following components:

- IP Address
- Class Diagrams, Sequence Diagrams, Activity Diagrams
- VLAN and Port Numbering
- Information about all the platforms, services, and processes the product would depend on
- Algorithm and pseudocode
- Different Classes, interfaces, and the relationship between them
- Relationships between the modules and system features
- External Interface Requirements, Hardware and Software Interfaces
- Design and Implementation Constraints

**Example 2 (Continued):**

The **Low-Level Design** would be the more detailed description of the High-Level Design. It would carry details such as:

- Payment Gateways linked to the payment service.
- Database details, including the driver service, Payment Service, User Service, Trip Archives, etc.
- Detailed map service for location tracking.
- Private classes, private methods, private attributes.
- Data structures and algorithms to be used.

## High-Level Design Vs Low-Level Design

The table below summarizes the differences between HLD and LLD

| Parameter            | High-Level Design (Macro-Level/System Design)       | Low-Level Design (Micro-Level/ Detailed Design)    |
|----------------------|------------------------------------------------------|----------------------------------------------------|
| Abbreviations        | HLD                                                  | LLD                                                |
| Input                | SRS (Software Requirement Specification)             | Reviewed HLD (High- Level Design).               |
| Definition           | Describes the main components that would be developed for the resulting product. | Describes the design of each element mentioned in the High-Level Design of the system. |
| Content              | The system architecture details, database design, services and processes, the relationship between various modules, and features. | Classes, interfaces, relationships between different classes, and actual logic of the various components. |
| Chronological order in the design phase | Created first                                       | Created after High-Level Design is completed.     |
| Technicality involved| Less technical                                       | More Technical                                    |
| Target Audience      | Management and program team                         | Used by implementers and the coding team.         |
