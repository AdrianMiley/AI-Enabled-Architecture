---
title: Defining Architectural Principles
---
#   Defining Architectural Principles

There are many architectural methodologies, such as The Zachman Framework and The
Open Group Architecture Framework (TOGAF), that provide a comprehensive framework
for developing and governing an Enterprise Architecture  at all stages in its lifecycle from
conception through to retirement (or a significant sub-set of those stages).
Most of the artefacts in these frameworks are predominantly management activities and
the traditional Architects role of setting design patterns and drafting the application
framework plays only a small role in this.

However an Enterprise Data Architect shouldn't be concerned with the operational
monitoring of the environment once it becomes operational any more than a Buildings
Architect is interested in the procedures that should be followed to maintain a building
once it has been built.

Everything else has its place but it is the designers that govern implementation,
operations manager that governs running the applications and the accountants that
control the financing of the application.

The Enterprise Architect may want to influence these areas but they are not a core
activity of the architectural function.

Given that, in the next couple of articles we are going to focus on defining the minimum
requirements for an Architectural Framework.

As many, many other people have previously noted, IT Architecture is predominantly a
collection of rules and patterns that the architect has applied to solve a particular
problem. This is the real Architectural Framework and at the highest level covers::
*	The Architectural Principles that define what must be true (or what is assumed
     must be true) at the boundaries between different components of the domain.
*	The Architectural Patterns that describe re-usable concepts underpinning
     significant parts of the architecture.
*	The Architectural Component Parts that describe how the domain is divided into
     sub-domains to reflect the business activities and, if we�re lucky, make it
     manageable.

A key point about a Framework is that it should avoid making any mention of systems or
applications that currently exist within the enterprise - its main purpose is to provide
something that the operational environment can be compared against once it is built.

The Architectural Framework is too large a subject area to be covered in a single article
so this instalment covers the first item on the list � Architectural Principles - and explains
their purpose within an objective Architectural Framework and an explanation of the
underlying principles for defining them.

##	The Purpose of Architectural Principles

###    What They Are

Architectural Principles mean different things in different contexts.
To a Solutions Architect they may include statements about the technology that will be
used. To a Data Architect they may include statements about denormalisation or
database organisation; to a Network Architect they may include statements about routing
mechanisms or authentication and so on. Irrespective of what type of architecture is
being produced the reasons and principles underpinning the architecture are pretty
similar.

Architectural Principles are critically important in any Architecture (not just Information
Technology) because The main purpose of an Architectural Principle is to set a policy for
governing the processes of developing, implementing and testing the architecture.

At the Enterprise level Architectural Principles are also about defining the rules that
govern the behaviour between sub-domains within the overall environment whilst leaving
as much wriggle-room as possible for each Sub-Domain Architect  to define �fit for
purpose� systems.

###	What They Are Not

In addition to describing what an Architectural Principle is we should also mention what
an Architectural Principle shouldn't be. They are not:

*	Business Requirements which are a result of Business Analysis and define the
     Business Processes that are to be supported. An Architectural Principle should not
     be tied to a particular Business Process because obviously if the business re-
     organises itself (which they do a lot) and the process changes then the
     Architectural Principle becomes invalidated as well. As with Morals & Ethics,
     Principles should not be that easily discarded
*	Development Approaches - some "architectures" such as Model Driven
     Architecture (MDA) are really just describing the software development process
     and this should always be left to the implementers to decide how they want to do
     it.
*	Ambitions - Architectural Principles may be ambitious but should define intent not
     ambitions because ambitions (1) may not be realistic and (2) even if realistic are
     just "nice to do" rather than "must do". Ambitions are definitely Design
     Guidelines.
*	Service Level Agreements and other contractual obligations between the IT
     function and other parts of the business. Most of these are operational in nature
     so should be left to the people who are going to run the systems to agree them
     with the rest of the business.
*	Business Mission Statements � statements like �The systems must support the
     business requirements� or �The IT will be aligned with the business� are both
     �bleeding obvious� and pointless statements. Every business area (Accounting,
     Human resources, Sales & Marketing) exists to support the business and
     Information Technology is no different so why bother saying it!
     This isn�t to say that the Enterprise Architect should not be concerned with any of these
     areas (because they are all of interest and might inform the choices being made) but
     rather that none of these things should be encapsulated in an Architectural Principle.

##	The Principles Of Defining Principles

Just forming a statement of intent and calling it an Architectural Principle doesn�t
generally lead to a good principle. Instead, like most things that require explanation,
they have a clear set of characteristics that can be objectively defined as being �good�
rather than �bad�.
For want of a better phrase these are the Principles of Defining Principles and those
described here are the most significant traits.

###	Straightforward

There are many that would argue that if the core concept of each Principle cannot be
summarised in a single sentence then it is probably too complicated to easily
communicate to other people and as a result will be unenforceable. If the principle is
difficult to define then how do we expect other people to understand and apply it?  
A well-defined Architectural Principle should be summarised in a single sentence or
phrase although it may be defined in any amount of detail for those that would like to
explore it further. (No doubt using the Glossary that everyone is now maintaining as a
critical communication tool.:))

###	Unambiguous

 An Architectural Principle is to all intents and purposes a rule stipulating a design
 constraint that has been applied to the proposed architecture and must be true for all
 artefacts within the architecture.

 A memo generally referred to in many industry standards as RFC-2119 "Key words to
 Indicate Requirement Levels" (see http://www.faqs.org/rfcs/rfc2119.html by Scott
 Bradner, March-1997,) defines a number of keywords that should be used to categorise
 requirements, assertions and rules. The (slightly edited) core of the memo defines the
 following:
```
 The key words "MUST", "MUST NOT", "SHOULD", "SHOULD NOT",
 "RECOMMENDED", "MAY" � in this document are to be interpreted as�

1.	MUST - This word mean that the definition is an absolute
      requirement of the specification.

2.	MUST NOT - This phrase means that the definition is an absolute
      prohibition of the specification.

3.	SHOULD - This word means that there may exist valid reasons in
      particular circumstances to ignore a particular item.

4.	SHOULD NOT - This phrase means that there may exist valid
      reasons in particular circumstances when the particular behavior
      is acceptable or even useful.

5.	MAY - This word means that an item is truly optional. An
      implementation which does not include a particular option MUST
      be prepared to interoperate with another implementation which
      does include the option. In the same vein an implementation
      which does include a particular option MUST be prepared to
      interoperate with another implementation which does not include
      the option.
```

These were originally intended to provide definitions for writing Technical Standards and
work very well in that area but don't cover the whole story when defining Architectural
Principles.

When stating an Architectural Principle the word "MAY" should never appear because it
indicates something that is optional. It is therefore a Design Guideline and the designer
will decide whether it will be implemented or not.

SHOULD and SHOULD NOT are a little more complex because, as stated in RFC-2119,
they also appear to indicate conditions that a designer can subsequently ignore and
decide not to adhere to the requirements of the statement if they feel they have a good
case not to.

However SHOULD logically translates into "MUST ... EXCEPT WHERE ..." and SHOULD NOT
translates into "MUST NOT ... EXCEPT WHERE". In both cases we have an absolute
MUST statement coupled with a set of documented "exceptions to the rule". It is the
exceptions that are important here and as they are identified must be incorporated into
the rule and hence becomes part of the rule.

The absence of the EXCEPT WHERE clause doesn't mean that the Principle must be
blindly applied everywhere but does mean that, at the time of drafting the Architectural
Principle, there are no known exceptions� but one can always be defined later if and
when one is identified.

Each architectural principle therefore translates into a Boolean assertion that is either
true or false when applied to the design proposals and deployment plans.
That certainly meets our "unambiguous" criteria.

Given the above we can conclude that things that MUST be true are objective
Architectural Principles because the do not give the Designer any flexibility in approach
whereas things that MAY be true are just subjective Design Guidelines.

###	Consistent

Hopefully the previous instalment on Definition of Terms will have provided sufficient
reasons for why consistency is very important but it�s worth emphasising here. If
definitions are not consistent then they cause confusion and conflict which slows progress
and in the worse cases will guarantee failure of the architecture because the parts will
not fit together properly.

Although it�s not a necessity, the number of principles imposed on a particular
architecture should be kept to a minimum because the complexity of the resulting
implementation will be proportional to the number of principles. With complexity we also
have am increased probability that the principles will become inconsistent with each
other.

However even though the principles need to be consistent with each other we do need to
ensure that they are not overly prescriptive and allow some flexibility because strict
adherence to one principle may require a loose interpretation of another principle.
The set of principles must be expressed in a way that allows a range of non-conflicting
interpretations so the words that define a principle also need to be carefully chosen so
that there will not be conflicting interpretations.

Finally, Architectural Principles should not be contradictory to the point that adherence to
one principle will violate another.
###	Appropriate
In order to produce a set of usable Architectural Principle is it is also important to have
an understanding of the activities of the business (both current and future plans) and a
realistic estimate of the resources that will be available. Defining an Architectural
Principle without an understanding of how it will impact the business is a good way to
pick a political fight with the business stakeholders.

For example, stating that "All data-items MUST be maintained through a single "Database
Of Record" that will be the authoritive source for that data-item." is a sound Architectural
Principle to ensure that the minimum of manual effort is put into actual data
maintenance and provide consistency across the entire organisation.

However there may be many logistical and regulatory reasons why it is impractical to
only have one copy of any data-item and, depending on the organisation, it may be
necessary to replicate or distribute some information.  

For example, consider the following scenarios:
-   Some countries may have data protection legislation that restricts what can be
done with "personal" data and where it can be stored which, in a global
organisation, may make it unfeasible to gather all the personal data together in a
single data repository.
-   ...Or the network latency of both New York, USA and Tokyo, Japan accessing high
volatility information stored in the Bangalore, India data centre may cause some
business activities to become unsustainable.
-   ...Or two business divisions want to maintain operational independence for some
reason e.g. one of them might be a non-core business and sold-off in the future.
-   ...Or transaction throughput requirements may require some applications with a high
data usage to locally cache data
- ...Or	some applications may have a significantly different view of the data required for
their operation and may want it stored in a transformed "ready to use" state
rather than do the transformation every time they access the information.

So, although we start with a single unambiguous Architectural Principle we must always
recognise that even the most desirable principles may not be appropriate to our
particular business and either ignore the principle or define any exceptions to the rule
that may be required.

###	Robust
Trying to ensure that the selected principles are robust (i.e. unlikely to break or need to
be rescinded later) is a key factor in their selection and definition because the �wrong�
principle that doesn't withstand scrutiny can have a significant impact on the overall
success of the project.

Questions we need to consider include:

**Q: How may technology changes impact the principle?**

This might seem obvious but everything changes and things change faster in the
IT industry than most other places - it's the downside with using technology and
employing creative problem-solvers. Being a highly volatile industry we seem to
bring out paradigm changes in high-level IT Architecture every 5 years or so.
Unfortunately, as someone once opined  (and I�m para-phrasing), Enterprise
Architecture is also on a 5-year cycle from conception to final realisation so there
will probably be some sort of major IT shift emerge during that time with the
potential to invalidate or make obsolete the architecture.

Sometimes there is a foreseeable evolution path such as...

    from Central Processing Systems (1-tier)
    --> Client / Server Systems (2-tier) 
    --> Message Based Systems (3-tier) 
    --> Service-Oriented Systems (N-tier)

...or...

    from Single Processor 
    --> Multi-Processor 
    --> Distributed Processing 
    --> Grid Processing 

...and if we have a migration path then the principle is supportable.

Although it's not possible to predict the next big change in IT Architecture we
should still keep an eye on emerging technology and consider whether the desired
principle would still be sound.

**Q: What are the assumptions that have been made in deciding on the principle?**

A certain US General Schwartzkopf once stated "Assumption is the mother of all
f**k-ups". It is certainly the quality of the underlying assumptions that strengthen
or weaken any assertion and a false assumption will almost certainly invalidate
anything derived from it. Architectural Principles are no different.

Consequently assumptions MUST be documented and should be �tested to
destruction� as much as possible in order to ensure that the resulting principle
stands up to scrutiny.

**Q:	What is the cost of applying the principle?**

Cost can be measured in many ways other than just money  - it can cover
"availability of materials", "effort to produce", "time to produce" or any other
quantifiable measurement - but however we measure it there is a cost to
everything.

There are many possible ambitions that look fine on paper but are unworkable
once the bean-counters apply the cost / benefit analysis or become
unimplementable due to an excessively high start-up cost. This is always worth
establishing before significant time and money is spent on producing the
architecture.

Given that we are always dealing with an unclear future it is not possible  to be
absolutely certain that any of our Architectural Principles will survive the test of time but
applying group thought and experience to developing them and asking the right
questions can only help.

###	Quantifiable

Only define Architectural Principles that can be quantified i.e. where the success criteria
can be defined and compared to the actual deployment.

Too often principles are listed that, to say the least, are pretty wishy-washy i.e.
statements like "_The architecture must be flexible" without actually quantifying what "flexible" actually means and what is expected of it.

They also need to be �quantifiable� so that the people who have to meet the constraints
of the principles know when they have achieved it.

I was once asked in an interview �How would you performance tune a database?�. My
answer was �What targets are you trying to achieve and in what order do you want to
achieve them?�. I then explained that I could take years �tuning a database� and shaving
fractions of a second off of different things - it�s a never ending task and without defined
success criteria I would never know when the database was good enough.

The same applies to IT Architecture and Architectural Principles � if the principle is not
quantifiable then how will the designers of each sub-domain know when they have done
enough work to meet the architectural requirements?

They could do it by negotiation with the Enterprise Architecture team but that would just
make compliance a subjective issue based on who you talk to and what they will agree
with.

Even worse the Sub-Domain Architect could just decide that they meet the criteria, build
the application and then have the arguments over compliance later.

I think most people would agree that this isn�t a good position to be in and it�s much
better is to know in advance that the design is �fit for purpose� and not �subject to
opinion� when later reviewed for architectural compliance.

###	Platform Independent
 Enterprise Architecture is probably the one area of IT Architecture where Platform
 Independence is crucial because of how far up in the clouds it is. It needs to be that
 high-level in order to make sense of the overall picture of the enterprise.
 Being platform independent is a particularly difficult area to be objective about because
 like-minded people tend to gather together and, being like-minded, will have pretty
 similar views of the enterprise  so it may not always be obvious within the group that a
 particular assertion is platform specific.
 
For example, stating that "All transactional interactions between domains will be Service-
 Oriented" is a sound (if possibly undesirable) Architectural Principle but stating that "All
 transactional interactions between domains will be based on Web Services" is not so
 sound.

 It takes inside knowledge of the IT Standards industry to recognise that Web Services is
 not a generalised concept but a particular technology and so which will almost certainly
 become obsolete over time.

 Often a principle can be identified as platform specific if it restricts the consumer of the
 principle to only have one way of solving a problem or forces them to adopt a particular
 niche technology to the exclusion of any other.

 Probably the simplest approach to ensuring that a principle is platform independent is to
 have it reviewed and challenged by external parties who have no vested interest in the
 outcome of the review and don�t come from a similar background to the author of the
 Architectural Principles. Ideally the author shouldn't even know the reviewer but that
 might be unfeasible.

##	Handing Out "Architectural Waivers"
In an ideal world each new architectural initiative would be a green-field project and
everything that existed before can be ignored. Unfortunately the opportunities to do that
are few and far between and for the majority of us there will be a whole mess of existing
business applications and systems that will either need to be integrated into the
proposed architectural framework or deprecated once a replacement is in place.
The choices we have are either (1) make the Architectural Framework flexible enough to
accommodate what already exists or (2) carry out a planned migration so that the
existing systems are conformant with the target architecture or (3) specifically allow just
that component to be non-conformant.

The second option is always the desirable path but sometimes option (3) has to be taken
because of other business pressures. If so then we need a formal means of deferring
conformance - namely the Architectural Waiver.

There are only really three things to say about Architectural Waivers, which are:
*	Waivers should be handed out when an exception to the rule isn�t desirable. The
     problem with an exception to the rule is that it becomes part of the rule so is
     becomes acceptable practice for every one else as well. This may not be what we
     want.
*	Whenever a waiver is asked for then a divergence / convergence plan should be
     produced to explain how the non-conformance will affect other components of the
     architecture and what will need doing in the future in order to conform to the
     Architectural Framework.
*	Once convergence is achieved then there should never be a need for that
     component to ever diverge from the Architectural Framework again. Only legacy
     (pre-existing) functionality can ever be non-conformant and there is never a need
     to new functionality to not conform to the Architectural Framework. Hence, once
     convergence is achieved Architectural Waivers are no longer required.
##	Conclusion
Hopefully this article has provided a useful overview of the Architectural Framework and
Architectural Principles � what they are, what they are not and the principles that should
underpin defining them.

In the next article we will consider Architectural Patterns and the value they add to the
Architectural Framework.

##  Footnotes

As discussed in the previous article on Definition of Terms every item that is capitalised is the name of
something and so will require a definition to be produced. Unfortunately I'm going to break that rule in
this article (and probably every subsequent one) in order to improve readability so I'll assume that people
have a general idea what each capitalised term means.

Enterprise Domains are nearly always split into Business Areas or Sub-Domains in order to make the
business manageable. Each of these Sub-Domains will probably have a separate Architect (who may or
may not be one of the Enterprise Architects) responsible for designing the systems in that area.

It was Andrew Preston, Senior Enterprise Architect at a global Media & Market Data company that shall
remain nameless :).

Many heavyweight economists, including Karl Marx (Capital) , John Maynard Keynes (The General
Theory of Employment, Interest & Money), Adam Smith (The Wealth of Nations) and Max Weber (The
Protestant Ethic and the Spirit of Capitalism), have written extensively on this point much better than I
ever could so I�ll leave it at this.

I worried about making this statement because it is possible to conceive of being "_absolutely certain_"
which, philosophically, in a multi-verse where all possible outcomes must eventually occur then makes it
possible to achieve. However for the foreseeable future I think it's safe to say that the future is neither
certain nor knowable in advance

There has been a lot of wasted effort in producing Sociology studies to prove something that should be
obvious. People tend to like other people with similar traits and given the choice will congregate with
people we like and people we do not like get excluded from the group or ignored. Groupings within a
Company work the same way with the same inevitable consequences. It's one of the reasons why
frequent change and re-organisations are seen as a good thing by company management.

