# Semantics

This chapter introduces the principles of the COINS 2.0 semantics.


## Introduction

COINS 2.0 is based upon W3C's RDF/OWL technology and has formalised its interpretation of standardized resources. The precise formalisation is done using the W3C's Sparql language. More information can be found [Here](https://github.com/bimloket/COINS_2.0/blob/master/docs/coinsweb/presentaties_introductie_COINS_2016/COINS_2.0_Semantiek_ConceptVersieV5.pdf)

## validating a Coins 2.0 container
It is now possible to validatie the information in a COINS 2.0 container if it complies with the COINS core model and other models such as OTL-ontologies and other extending ontologies.

You can validate a container using the COINS-Validator which is accessible via the COINS 2.0 Command Line Utility. You can download a java based [Jar file](https://github.com/bimloket/COINS_2.0/tree/master/Coins-cli-1.1.605-jar-with-dependencies)

In order to validate a COINS container you need this jar file and a valid Java runtime environment on your computer. The validation is based upon enriching the datasets via Sparql and at the end validate the data according to "restriction based" interpretation of OWL vocabulary such as cardinality constraints, etc. More on this topic will be available soon. The validation sparql 'rules' are separated from the implementation via a so-called ProfileFile. These files contain all the sparql queries that need to be executed. The CLI can automatically find these files online. The following example runs the java command with extra memory (-Xmx8G setting) to start the commandline (in the Jar file) and orders it to "validate" your coinscontainer. It specifies a profile via "-p" command with a particular version (-v). This profile and version is available online. The validatior will produce a html report with the name "reportWeb.html"

java -Xmx8G -jar coins-cli-1.1.603-jar-with-dependencies.jar validate -p "COINS 2.0 Lite0.9.60-Original" -v "0.9.60-Original" -o reportWeb.html yourCoinsContainer.ccr


## Background information on RDF/OWL semantics
Semantics tells you about the meaning of something. You can define something by adding a relationship. When you implement this concept in computerlanguage the computer is able to interpret this. This concept, called a Triple, contains 2 resources that are related to eachother via a predicate. A predicate tells something about the relationship between the resources, like "has a property", "has a part".

<code>Triple: Resource Predicate Resource</code>

## Semantic web technologies
* These triples are used in RDF (Resource Description Framework).
*  On top of this OWL (Web Ontology Language) defines its own vocubalair for typical relationships. This vocabulair uses COINS also


## Ontology
An ontology is a formal way of naming and definition of the types, properties, and relations of the entities that really or fundamentally exist for a particular domain, for instance the COINS domain. In Coins the Owl:Ontology Class is available. In this way other ontologies can extend the Coins Core Model.

## Serialisation or Exchange formats
These technologies make it possible to exchange the information in several formats (serialisations), like JSON, RDF/XML, Turtle etc. This is shown in this OWL sample.



# Container validation

This chapter is dedicated to an opensource a software tool that can validate a COINS 2 container using a Pro-File which is file containing a set of sparql queries.


## Introduction
COINS 2.0 is an data exchange format based upon a structured Zip file with an W3C's RDF/OWL information model called a semantic BIM model that can be based upon other RDF/OWL models called reference models and ObjectTypeLibraries. The zip file is called a Coins container and the container must comply to certain rules. These rules will be listed in the section Container structure.
The semantic BIM model can be entailed to support data validation. The assumptions to do this will be explained in the section Semantic Bim entailment and data validation.
The last section is about software that enables the validation of Coins containers. It validates the structure of a Container and it validates a semantic BIM model in the container. All results are documented in a report. See for an example of such a report.


## Container structure
The following rules apply for the container structure:

- The Container must be a valid Zip file
- The Container must have bim folder with a mandatory an rdf file (only one).Different W3C serialisations are allowed.
- The bim folder can only have a subfolder "repository' for rdf files that are used by the rdf file in de bim folder. Different W3C serialisations are allowed.
- The container must have the “.ccr” filename extension.
- The container can have a doc folder. All documents listed in this doc folder must be referred to.
- The container can have a WOA folder container a single rdf file. Different W3C serialisations are allowed.
The software tool described at the end of this page will validate if a Coins container meets these requirements.


## Semantic BIM Entailment and Data validation
Closed World and Unique Naming Assumptions
For data-exchange purposes COINS 2.0 adopts the following principles:

- Closed World Assumptions (CWA)
- Unique naming assumption (UNA) 

RDF/OWL uses an Open World Assumption (OWA) while COINS 2 assumes a Closed World Assumption (CWA). CWA assumes that what is not known is false where the OWA states that a lack of information does not mean it is false. Using the CWA RDF/OWL cardinality constraints can be used to test the data and 'missing data' (e.g. objects that do not fulfill these constraints as they miss the necessary information) can be reported.

COINS 2 adopts Unique naming assumption meaning that each individual is unique as truth. Consequenlty entailment that two individuals are the same is not part of the COINS2 entailments.

The exact results of these principles for COINS 2 are documented in COINS 2 profile files or COINS 2 Pro-File. A COINS 2 Pro-File is a file that formalises the exact inference and validation of rdf/owl vocabulary in a data-exchange context using the W3C's Sparql language. As the rdf/owl vocabulary is very rich and can result in intensive reasoning efforts a subset is currently supported by COINS 2 Pro-Files. More COINS 2 Pro-Files can be envisionend supporting more RDF/OWL resources similarly to current existing RDF/OWL profiles such as OWL-RL, etc. A Pro-File consists of the following sections container sparql queries:

-Vocabulary check. a set of sparql queries Checking if all the used RDF/OWL vocabulary can be supported by this Pro-File
-Schema entailment. a set of sparql queries entailing COINS 2 OTL and other ontologies
-Data entailment. a set of sparql queries for entailing the semantic BIM file
-Data validation. a set of sparql queries for validating a semantic BIM file against its schema.

When extensions of COINS2 such as OTL's and reference models are compliant with the supported RDF/OWL vocabulary of a Pro-File then Coins containers can be validated against these extensions.

## Data validation queries (COINS-Lite profile)
This chapter describes the validations that can executed using the COINS-Lite Pro-File. A validationreport will have hyperlinks to these pages.


* COINS-minCar  : minimum cardinality check
* COINS-maxCar  : maximum cardinality check
* COINS-carex  : exact cardinality check
* COINS-QCREx  : exact qualitative cardinality check
* COINS-QCRMax  : maxiumum qualitative cardinality check
* COINS-QCRMin  : minimum qualitative cardinality check
* COINS-FUP  : functional property check
* COINS-DTVC  : datatype value check
* COINS-DPVL  : datatype property check
* COINS-OPVU  : objectproperty value check
* COINS-DTC  : coins datatype constraints
* COINS-dom  : domain as a restriction check
* COINS-rng  : range as a restriction check
* COINS-HVC  : hasValue restriction check
* COINS-AVFOneOf  : AllValuesFrom via OneOf check
* COINS-AVFClass  : AllValuesFrom via Class check
* COINS-UO  : unionOf as restriction (abstract class) check
* Cax-adx  : disjoint via allDisjoint check
* Cax-dw  : disjoint via disjointWith check

## Coins container validator software

It is now possible to validatie the information in a COINS 2.0 container if it complies with the COINS core model and other models such as OTL-ontologies and other extending ontologies.

### download
The validator can be downloaded [Here](https://github.com/bimloket/COINS_2.0/tree/master/ValidatorV1/validator). This zip contains the validator.jar, the latest Pro-File, an example coins container (with errors so that the validator can find them) and a batch file to run the validator.

To run this software it is necessary to have:

1) a recent Java version installed on your computer (JDK >1.6)
2) GraphDB triplestore running on your computer.

The older release of the validator can be found on the Semantics chapter. Also more information how validation is performed can be found here.

### install
1) Firstly make sure that Java is installed. You can test this by running "java -version" in a commandshell.
2) Secondly make sure that GraphDB is running. A default configuration of GraphDB can be accessed using a webbrowser using portnumber 7200 of your localhost [//localhost:7200](http://localhost:7200)
3) Thirdly you can run the validator by unzipping the zip and by running runVC_CardinalityCheck.bat. The batch file starts the validator using the VC_CardinalityCheck.ccr container. The validator should produce the following [Example Report](https://www.buildingbits.nl/coins2/exampleReport.html)

The validator uses the following input:
1) yml file containing various configuration options for the validator
2) Pro-File containing inference and validation queries. (more information can be found in the Semantics chapter)

to run the validator you can use the following command:
java -Xmx8G -jar coins-validator.jar -l run config.yml yourContainer.ccr
This command uses java to run the coins-validator. the -Xmx8G argument specifies that java can use 8Gigabytes of Ram. The '-l' argument specifies that the validator produces a log file. The run config.yml points to the yml file. The yml file can specify a Coinscontainer. This can be overriden by specifying a container in the command. In this case the 'yourContainer.ccr' will be validated.

yml configuration
The yml contains a reference to the GraphDB sparql endpoint. The default yml file points to [http://localhost:7200](http://localhost:7200) as default sparql endpoint which corresponds with the default endpoint for GraphDB. When your graphDB uses another endpoint then you will need to change the yml accordingly.
The yml also contains a reference to the Pro-File. The validator comes with a default Pro-File named 'COINSLite.xml'. The yml points to this file. If you would like to use another Pro-File then you change the yml file to point to the other Pro-File.
The validator can export the results in JSON,xml and in HTML. The following snippet can be addes to the yml file to produce json and xml reports:
* type: json 

 location: 

     type: file 

     path: report.json

* type: xml

location

     type: file

     path: report.xml

