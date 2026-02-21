---
title: Business Entity Component Structure
---
#   Domain Service Component Structure

```mermaid
---
title: General structure of a Business Entity Service Component
---
classDiagram
    class BusinessEntityManager ["Business Entity Manager"] {
        <<Component>>
    }

    class BusinessEntityControllerInterface ["Controller Interface"] {
        <<Interface>>
        create ( CreateBusinessEntityRequest)
        update ( UpdateBusinessEntityRequest)
        delete ( DeleteBusinessEntityRequest)
    }

    class BusinessEntityQueryInterface  ["Query Interface"] {
        <<Interface>>
        query( FetchBusinessEntityRequest) FetchBusinessEntityResponse
        query( FindBusinessEntityRequest) FindBusinessEntityResponse
        query( CheckBusinessEntityRequest) CheckBusinessEntityResponse
    }

    class BusinessEntityEventsInterface  ["Event Interface"] {
        <<Interface>>
        post( BusinesEntityCreated )
        post( BusinesEntityUpdated )
        post( BusinesEntityDeleted )
    }

    class OtherDataDomainQueryInterface { <<interface>> }
    class BusinessEntityDatabase { <<Database>> }

    BusinessEntityControllerInterface <|.. BusinessEntityManager : realizes
    BusinessEntityQueryInterface <|.. BusinessEntityManager : realizes
    BusinessEntityManager ..|> BusinessEntityEventsInterface : realizes

    BusinessEntityManager ..> "0..*" OtherDataDomainQueryInterface : uses
    BusinessEntityManager *-- BusinessEntityDatabase : manages
```

The Business Entity Component...
-   ... realizes two Interfaces
    - ... a single Controller Interface that provides operatiosn for external users to change the state of the managed Business Entity
    - ... a single Query Interface that provides find and retrieval operations for external consumers of the managed Business Entity
-   ... and implements a specific Data Domain Class Model 
-   ... and optionally uses many Query Interfaces provided by other Data Domains
-   ... and manages the persistence of the Business Entity in a Business Entity Database
-   ... which is also derived from the Data Domain Class Model

```mermaid
---
title: How the specifications are derived
---
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
