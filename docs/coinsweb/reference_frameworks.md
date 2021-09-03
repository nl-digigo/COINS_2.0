# <a>Reference Frameworks</a> 

Reference frameworks: Generic
A Reference Framework is an extension of the Coins 2.0 Core Model ontology for specific domains, for use of libraries and/or for project- or company specific needs.

Usage of frameworks is optional, but when extension of the core model is required, it is recommended to use Standard frameworks where available.


## General

COINS is characterized by flexible schema architecture, based on RDF(S) and OWL. The Coins Core Model is an extension of the OWL Ontology Structure and is formally represented in a COINS entity model. This Core Model defines the minimal set of classes required for storage and exchange of data: Objects, their Properties and their Connections (relationships between Objects). The Core Model can be extended by defining Reference Frameworks.

From functional point of view, there are two types of frameworks:

“standard” frameworks: for extending the Core Model to specific domains according to commonly accepted standards for that domain, and for implementing management- and control issues like the Window of Authorization
“specific” frameworks: containing definitions for specific domains, for use of libraries and/or for project-specific needs.
Parties are free to define and use specific reference frameworks, e.g. for in-company usage, or for use in a limited scope during a specific project, providing these have been harmonised with the core model and do not contain any supplements that conflict with this model.

In order to be COINS compatible, software must support the COINS Core Model and the standard reference frameworks. Support of specific frameworks is optional.

## Usage


Coins Container folder structure
From a technical point of view, a Reference Framework is a file containing the additional ontology, defining extensions to the classes of the COINS Core Model. This file is “included” (referenced) in the OWL-file containing the data model (building information model). To parties involved, Reference Frameworks should be made available through their internet location (URL). When information models are exchanged through a Coins Container, Reference Frameworks can be included in the container by placing them in the Repository folder. The Repository folder is a subfolder of the BIM folder, where the information model is located. The Reference Framework for authorizations (the Window of Autorization) is an exception to this location; this file is placed in the WOA-folder.


## Example

In the following example, the Reference Frameworks “Units-2.0.rdf” and “COINSWOA.rdf” are included:

<code><rdf:RDF

  <rdf:Description rdf:about="">
    <rdf:type rdf:resource="owl:Ontology"/>
    <owl:imports rdf:resource="http://www.coinsweb.nl/units-2.0.rdf"/>
    <owl:imports rdf:resource="http://www.coinsweb.nl/COINSWOA.rdf"/>
  </rdf:Description>

</rdf:RDF>


## Available Frameworks

Standard Frameworks
The following standard frameworks are available:

Window of Authorization (WoA): this framework makes it possible to specify the access rights for a part of the model

## Specific Frameworks

The following standard frameworks are available:

Units (based on QUDT), this framework extends Coins with the ontology for a lot of units that are needed
BranchVersioning, this framework creates an extra versioning principle next to the default Versioning in the Coins core model

Note
A Reference framework for adding Systems Engineering functionalities is being developed. This framework will contain definitions for requirements, verifications and so on.

