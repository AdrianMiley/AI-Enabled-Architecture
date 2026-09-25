---
title: Domain Component Structure
description: The structure and relationships of domain components
---

#   Domain Component Structure

The Business Entity Component:

- ... realizes two Interfaces
  - ... a single Controller Interface that provides operations for external users to change the state of the managed Business Entity
  - ... a single Query Interface that provides find and retrieval operations for external consumers of the managed Business Entity
- ... and implements a specific Data Domain Class Model
- ... and optionally uses many Query Interfaces provided by other Data Domains
- ... and manages the persistence of the Business Entity in a Business Entity Database
- ... which is also derived from the Data Domain Class Model

```mermaid
classDiagram
    class BusinessEntityManager ["Business Entity Manager"] {
        <<Component>>
    }

    class BusinessEntityControllerInterface ["Controller Interface"] {
        <<Interface>>
    }

    class BusinessEntityQueryInterface  ["Query Interface"] {
        <<Interface>>
    }

    class BusinessEntityEventsInterface  ["Event Interface"] {
        <<Interface>>
    }

    class BusinessEntityClassModel { <<ClassModel>> }
    class BusinessEntityDatabaseSchema { <<ClassModel>> }
    class BusinessEntityDatabase { <<Database>> }
    class BusinessEntityStateMachine { <<StateMachine>> }

    BusinessEntityManager --> BusinessEntityClassModel : implements
    BusinessEntityManager --> BusinessEntityStateMachine : implements
    BusinessEntityManager *-- BusinessEntityDatabase
    BusinessEntityControllerInterface --> BusinessEntityClassModel : derived from
    BusinessEntityQueryInterface --> BusinessEntityClassModel : derived from
    BusinessEntityDatabase --> BusinessEntityDatabaseSchema : derived from
```

[Back](../index.md) [Home](../index.md)
