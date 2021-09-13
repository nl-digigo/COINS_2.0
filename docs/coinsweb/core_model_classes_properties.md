# Core Model Classes and Properties



## Core Model Classes

Class

Assembly

BooleanProperty

CartesianLocator

CataloguePart

CoinsContainerObject

ComplexProperty

ComplexPropertyValue

Concept

Connection

ContainsRelation

ContainsRelationGroup

DateTimeProperty

DirectedConnection

DocumentProperty

DocumentReference

Entity

EntityProperty

ExpiredEntity

ExternalDocumentReference

FloatProperty

IntegerProperty

InternalDocumentReference

Locator

LocatorProperty

NumericProperty

Object

Organisation

Part

Party

Person

SecuredDocumentReference

SecuredExternalDocumentReference

SecuredInternalDocumentReference

ShapeRepresentation

ShapeRepresentationProperty

SimpleProperty

StringProperty

UriProperty

Vector

VersionObject


### CoinsCore:Assembly Class
Assembly is a subclass of Entity.

Assembly is an abstract class; it can not be instantiated directly. Members of intantiatable subclasses of Entity can additionally be typed as Assembly.

The Assembly class is extendable.

The nextTrunkVersion is restricted to one other individual of Assembly.


**History**
* New in COINS 2.0


**Informative representation in UML**


This image shows the informative representation of the Assembly class.

![Informative representation of Assembly in UML](*/coinsweb/media/600px-Core-Assembly_Class.png "Informative representation in UML")


**Attributes**
<table class="wikitable">
<tr>
<th> Name
</th>
<th> Type
</th>
<th> Description
</th></tr>
<tr>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#hasContainsRelation">hasContainsRelation</a> </td>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#containsrelation" title="CoinsCore:ContainsRelation Class">ContainsRelation</a> </td>
<td> Reference to ContainsRelations
</td></tr>
</table>

### Assembly


### BooleanProperty


### CartesianLocator


### CataloguePart


### CoinsContainerObject


### ComplexProperty


### ComplexPropertyValue


### Concept



### Connection



### ContainsRelation



### ContainsRelationGroup



### DateTimeProperty



### DirectedConnection



### DocumentProperty



### DocumentReference



### Entity



### EntityProperty



### ExpiredEntity



### ExternalDocumentReference



### FloatProperty



### IntegerProperty



### InternalDocumentReference



### Locator



### LocatorProperty



### NumericProperty



### Object



### Organisation



### Part



### Party



### Person



### SecuredDocumentReference



### SecuredExternalDocumentReference



### SecuredInternalDocumentReference



### ShapeRepresentation



### ShapeRepresentationProperty



### SimpleProperty



### StringProperty



### UriProperty


### Vector



### VersionObject



## Core model properties



### belongsToAssembly



### checksumFile



### checksumFileAlgorithm



### checksumUri



### checksumUriAlgorithm



### coordinate



### creationDate



### creator



### datatypeValue



### description



### documentFragment




### documentMimeType



### documentType



### documentUri



### filePath



### fromObject



### groupedBy



### groups



### hasAssembly
### hasConnectedObjects




### hasConnections




### hasContainsRelation



### hasIncomingConnections



### hasOutgoingConnections




### hasPart



### hasProperties




### IDFieldname



### modificationDate



### modifier



### name



### nextTrunkVersion



### objectValue



### partOf




### primaryOrientation



### propertyBelongsTo



### secundaryOrientation



### toObject



### translation



### unit


### userID



### VersionID



