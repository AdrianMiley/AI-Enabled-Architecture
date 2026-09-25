---
title: What Is Architecture
description:  
---
#   What Is "Architecture"

What is the difference between Architecture and Design?

This is a question that I am regularly asked and is often the subject of great debate within the Information Technology community.

My colleague, Simon Watts, recently wrote an article titled “What is I.T. Architecture?” in which he concluded that architecture is simply the collection of principles and operational requirements that are being applied to a business in order to solve and govern the implementation of its strategic data processing requirements.

In the Data Architecture context “Objective” can have more than one applicable meaning, such as:
1.	Something that one's efforts or actions are intended to attain or accomplish; a purpose or goal.
2.	Not influenced by personal feelings, interpretations, or prejudice; based on facts.

Although Architecture is a diagram-oriented activity the diagrams are generally used to present the summary of a set of factual statements and to break a complex problem down into manageable components.
This leads to the conclusion that IT Architecture is an "Objective" based activity whose primary purpose is to define what is required to provide a solution to the Business Requirements defined in the analysis phase.
Certainly this conclusion is supported by the major architectural frameworks, such as Zachman and TOGAF, but is of course is not the full story!

If architecture is an Objective based activity then where do activities such as choosing technology platforms, design patterns, defining database platforms and so on fit in?
“Subjective” also has multiple definitions. The applicable ones are:
1.	Relating to or of the nature of an object as it is known in the mind as distinct from a thing in itself.
2.	Expressing or bringing into prominence the individuality of the artist or author.

The choices can have significant implications on company costs, both balance sheet capital expenditure and profit & loss accounts, and future business capability in addition to the more obvious programme related concerns such as ease of implementation, availability of experienced staff, robustness and stability of chosen platforms.
“Mere Implementation Detail” means “information only important at a level of detail below this one”. In terms of carrying out or implementing any operation there is always a level of detail that may later be important but can be ignored at the level of abstraction under discussion.

This is true no matter what the subject area is or what level of detail is currently being discussed.

For example, I don’t need to know how a DVD Player works in order to utilise it – just that it can be built. 
In order to build the DVD Player I don’t need to know how to manufacture an LED in order to include one as a component in my DVD Player.
Stripping out this implementation detail generally makes things easier to define and understand.
They are all decisions that are obviously more important than mere implementation detail so need to be dealt with at the architectural level but aren’t really architecture per se because they don’t meet the objective characteristics of architecture.

This in fact is what we tend to mean when we talk about Design rather than Architecture and leads us to the title of this discussion, namely:
“Architecture Is Objective, Design Is Subjective”

Architecture & Design are nearly always bundled together into a single activity carried out by “The [Insert Specific Role of Choice] Architect” and the individual features of the final architecture are rarely separated into the “Objective” or “Subjective” aspects.

However there are many reasons why they should be kept separate, including:
•	Architecture is always (or should be) aligned to the overall business strategy whilst Design is usually aligned with the available resources.
•	Business stakeholders usually don’t care about technical details of the Design – the attention of many an audience has been lost by boring them with more detail than they are interested in.
•	The merits of each Architectural component can be quantified and measured whilst Design aspects are debateable. Removing Design from Architecture increases the chances of reaching general agreement over the approach without subjective arguments over technical merits. It improves "Time To Market".
•	The Objective aspects are a matter of necessity to operate the business whilst Subjective features can be modified, superseded or replaced over time without impacting the nature of the business.

For many people who perform both roles in an environment where the separation isn’t important this is probably an academic discussion but in some cases it may actually be that Architecture and Design must be kept separate for business reasons.

Consider the following High-Level Architectural view of a particular business sector (covering the UK Energy Performance Certificates marketplace):

It isn’t the full story of course – there’s a lot of requirements definitions, interface specifications and operational constraints defined behind the scene – but I think is a relatively simple high-level architectural diagram to illustrate a point. It contains all the significant detail required to understand what components will exist in the system but says nothing about how they will be implemented or the tools and technology that will be used.

In this particular case the separation of Architecture from Design is very, very important because:
•	The Accreditation Bodies were all separate companies with their own ways of conducting business and their own in house technical platforms. Some were Java shops and some were .NET and some were plain old C/C++.
•	The two central data repositories were externally procured and managed by a 3rd-party supplier. The platform was at their discretion and all they were provided with as part of the procurement was the architectural framework and a set of objectives to be achieved.
All of these organisations needed clear guidance on which aspects were fixed and which aspects open to interpretation by them. They needed to know the Objective but not the Subjective aspects of the environment.

Unfortunately, separating the Architecture & Design is much easier said then done because it is not always clear whether someone is being objective or subjective when making an assertion about the problem they are trying to both define and solve.

Over subsequent articles we’ll explore some of the issues in separating Architecture from Design such as:
•	How do we recognise when something is Objective or Subjective? There are many terms, concepts and patterns that in some contexts could be regarded as architectural concepts and others that are simply approaches to Design.
•	How do we enforce the separation between Architecture & Design when the activities are carried out by the same role?
•	How do we handle evolution where a design approach evolves into an architectural constraint?

For example until recently using XML would have been regarded as a design issue because there were many alternative methods to specifying interfaces between components. 
Nowadays XML is pretty much the de facto standard and is at the point that “it goes without saying” that all public interfaces should be in XML unless there is an exceedingly good business driver to use anything else. It has stopped being a design decision and become an architectural decision.
•	Removing “Mere Implementation Detail” – how do we strip an architectural proposal down to the absolute minimum so that irrelevant information doesn’t cloud the overall picture?
•	What are the minimum artefacts required to produce a coherent Enterprise Data Architecture? For example, where does the Business Information Model fit into the Enterprise Data Architecture picture? Is it an architectural artefact or just a design artefact?


