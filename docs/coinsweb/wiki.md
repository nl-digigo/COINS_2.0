# <a>Background information</a> 

## Introduction

Building information modelling provides a digital technology for describing and displaying information required in the planning, design, construction and operation of constructed facilities. Increasingly, this modelling approach is expanding to encompass all aspects of the built environment, including civil infrastructure, utilities and public space and all disciplines. These are collectively referred to as construction processes. This approach to managing information brings together the diverse sets of information used during the life cycle of the built environment into a common information environment - reducing, and often eliminating, the need for the many types of paper documentation currently in use.
This approach is commonly referred to as BIM (building information modelling, reflecting its initial application in the architectural domain), while the same acronym is used to refer to the product of the process, the information model itself, or BIM (Building Information Model).

The introduction of BIM leads to an increasing need to describe the information deliveries (data drops) on the interface between actors in the process. In practice these data drops are a combination of data sets according to multiple formats and differing standards, as well as proprietary formats. Available BIM standards are not equipped to support this practical situation.

This standard provides an information model and exchange format by means of a container for BIM related data.

The importance of this standard is the integration of open data based on differing standards (as well as proprietary formats, where needed), but packaged up in a way that makes explicit links between multiple representations of the same object. For example, a construction component such as a road abutment may be defined in a BIM library (as a type), linked to text specification or meta data, and include a 3D representation in a IFC file and/or a 2D representation in a GIS file.

The current version is ICDD; this document describes the previous version, COINS 2.0.

## Reader's guide

Essentials; In the Essentials section the general concepts of COINS are explained
Core Model; The Coins 2.0 Core Model section specifies the classes and relations defined in this standard.
Semantics; The page Semantics give some initial concepts and explaination about semantics, triples, OWL, RDF and ontologies. For more detailed information there will be links available to external resources.

## Mandate

Since it's first publication in 2010, the Coins standard was tested and implemented in medium and large scale infrastructural projects.
Based on these experiences, the standard was evaluated in workpackage3 “Rethinking the standard” of 'Projectplan COINS' by the Dutch "Bouw Informatie Raad" (14th of January, 2014).

This resulted in a specification for Coins 2.0. It has been documented in "Rethinking COINS" (15th of June, 2014) The important specifications are:

Coins 2.0 should not impose a working method, it must focus on exchange of information
In Coins 1.0 it was possible to create just one type of relations between objects. With Coins 2.0 multiple relations between objects can be created.
The concept of information exchange must not be limited to the maintain phase of a project. It mus be used through the whole life-cycle (design, built, operate and maintain, demolish)
The implementation of Coins 2.0 must be simplified. Besides, Coins must be independent of language and sustainable
The 'core model' of Coins 2.0 must be configurable and extensible (e.g. by using Reference Frameworks), without changing the core itself
The definition (semantics) of the exchanged information must be unambiguously by using references to Reference Frameworks or accepted objecttype libraries.
The document "Rethinking COINS" resulted in a number of reports:

Concepts of collaboration; principles of how and when we want to exchange information.
Versionmanagement; what kind of versionmanagement will be supported by Coins 2.0.
Data Description Language (DDL); create insight in OWL, RDF, RDFS and type of serialisations.
Coins core model; what classes have to be added to/removed from the core model.
These findings are used as input for the definition of Coins 2.0. This definition has been presented at the 7th of April, 2016.