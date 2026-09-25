---
title: Architecture As Information
description: Managing Architecture Artefacts as Data
---

# Architecture As Information

"Architecture as Data" treats the structure and design of a system (whether physical, digital, or organizational) as a dynamic dataset rather than just a static blueprint. This allows architects to use computational tools to modify, analyze, and automate management of architectural artefacts.

[Back](../../index.md) [Home](../../index.md)

Core Interpretations

    Digital Preservation: In physical architecture, this means treating 3D renderings and BIM models as the primary cultural "data" of a building, which can outlast the physical structure itself.
    System Modeling: In software and engineering, it involves defining system interfaces, constants, and data types in a centralized, machine-readable format. This allows for model-based diagramming and automated documentation where the "data" generates the view.
    Executable Architecture: Some modern frameworks use "Spec-Driven Development," where the architectural specifications are actually executable code that enforces system rules and prevents "architectural drift". 

Key Benefits

    Single Source of Truth: Centralizing architectural definitions ensures that all teams (security, dev, ops) are working from the same data-driven model.
    Scalability: By treating architecture as modular data (e.g., Data Mesh), organizations can scale individual domains independently without creating centralized bottlenecks.
    Predictive Analysis: Using architectural data allows for AI-integrated modelling to predict things like energy waste, environmental impact, or system failures before they happen. 

Are you interested in this from a software engineering perspective, or are you looking at how physical building design is becoming more data-centric?

"_Architecture As Code_" is really a misnomer as what we are really talking about is "Architecture As Information" because information is really what we are trying to capture and manage.

Whilst visual representations can be useful for communication and understanding, they often lack the depth and detail needed to fully capture the complexities of the subject area being described and, even worse, are frequently produced in a (mostly binary) format that makes them unusable for anything other than to show people.
Binary pictures are pretty much unusable as input to actual systems development work.

This is important because I've always considered the tendency to produce "_pretty pictures_" as the primary artifacts of architecture work as a waste of time.

The start point, as with most other kinds of data processing, is to produce a Domain Data Model describing the Architectural Artefacts that we're interested in defining and managing.
Some would call this a **Meta-Model** because it represents a "Model of Models" but in reality it's just another Class Model defining Objects, Attributes and Relationships albeit with one added restriction that the Model of Models must also be able to describe itself 
i.e. the Meta-Model forms, as much as possible, a closed universe where every  