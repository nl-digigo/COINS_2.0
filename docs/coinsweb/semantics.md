# Semantics

This chapter introduces the principles of the COINS 2.0 semantics.


## Introduction

COINS 2.0 is based upon W3C's RDF/OWL technology and has formalised its interpretation of standardized resources. The precise formalisation is done using the W3C's Sparql language. More information can be found here Bestand:COINS 2.0 Semantiek ConceptVersieV5.pdf

## validating a Coins 2.0 container
It is now possible to validatie the information in a COINS 2.0 container if it complies with the COINS core model and other models such as OTL-ontologies and other extending ontologies.

You can validate a container using the COINS-Validator which is accessible via the COINS 2.0 Command Line Utility. You can download a java based Jar file via the following link Bestand:Coins-cli-1.1.605-jar-with-dependencies.zip. This link contains a zip file where you can find a Jar file.

In order to validate a COINS container you need this jar file and a valid Java runtime environment on your computer. The validation is based upon enriching the datasets via Sparql and at the end validate the data according to "restriction based" interpretation of OWL vocabulary such as cardinality constraints, etc. More on this topic will be available soon. The validation sparql 'rules' are separated from the implementation via a so-called ProfileFile. These files contain all the sparql queries that need to be executed. The CLI can automatically find these files online. The following example runs the java command with extra memory (-Xmx8G setting) to start the commandline (in the Jar file) and orders it to "validate" your coinscontainer. It specifies a profile via "-p" command with a particular version (-v). This profile and version is available online. The validatior will produce a html report with the name "reportWeb.html"

java -Xmx8G -jar coins-cli-1.1.603-jar-with-dependencies.jar validate -p "COINS 2.0 Lite0.9.60-Original" -v "0.9.60-Original" -o reportWeb.html yourCoinsContainer.ccr


Background information on RDF/OWL semantics
Semantics tells you about the meaning of something. You can define something by adding a relationship. When you implement this concept in computerlanguage the computer is able to interpret this. This concept, called a Triple, contains 2 resources that are related to eachother via a predicate. A predicate tells something about the relationship between the resources, like "has a property", "has a part".

Triple: <Resource> <Predicate> <Resource>
Semantic web technologies
These triples are used in RDF (Resource Description Framework).
On top of this OWL (Web Ontology Language) defines its own vocubalair for typical relationships. This vocabulair uses COINS also
Ontology
An ontology is a formal way of naming and definition of the types, properties, and relations of the entities that really or fundamentally exist for a particular domain, for instance the COINS domain. In Coins the Owl:Ontology Class is available. In this way other ontologies can extend the Coins Core Model.

Serialisation or Exchange formats
These technologies make it possible to exchange the information in several formats (serialisations), like JSON, RDF/XML, Turtle etc. This is shown in this OWL sample.

Validation