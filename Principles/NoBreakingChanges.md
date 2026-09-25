---
title: No Breaking Changes
description: Guidelines to avoid breaking changes in deployed systems
---

#   No Breaking Changes

Once an application is deployed into an operational environment and integrated with any other application then all changes made to any interface must be non-breaking.

[Back](../index.md) [Home](../index.md)

A Breaking Change in an interface is any change where both Producer (the Sender of a Communication) and Consumer (the Receiver of the Communication) must be upgraded at the same time in order to continue interacting with each other.

|                |     |
|----------------|-----|
| Breaking       |     |
| Consumer First |     |
| Producer First |     |
| Non-Breaking   |     |

##  Change Scenarios

###  Information Model Change Scenarios

| Action | Change              | Change Type    | Mitigation              |
|--------|---------------------|----------------|-------------------------|
| Add    | Mandatory Attribute |                | Provide a default value |
| Add    | Optional Attribute  | Non-Breaking   |                         |
| Remove | Mandatory Attribute | Consumer First |                         |
| Remove | Optional Attribute  | Consumer First |                         |

### Component Model Change Scenarios

### Communication Model Change Scenarios
