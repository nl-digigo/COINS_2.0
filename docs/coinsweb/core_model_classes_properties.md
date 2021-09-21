# Core Model Classes and Properties
Description of core model Classes and Properties


## Core Model Classes
Description of core model Classes 


### Assembly
<b>Assembly</b> is a subclass of <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#entity" title="CoinsCore:Entity Class">Entity</a>.
</p><p>Assembly is an abstract class; it can not be instantiated directly. Members of intantiatable subclasses of Entity can additionally be typed as Assembly.
</p><p>The Assembly class is extendable.
</p><p>The <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#nexttrunkversion" title="CoinsCore:nextTrunkVersion Property">nextTrunkVersion</a> is restricted to one other individual of Assembly.
</p><p><br />
<b>History</b><br />* New in COINS
</p><p><br />
</p>
<b>Informative representation in UML</b><br />

<p>This image shows the informative representation of the Assembly class.</p>

![Informative representation of Assembly in UML](./media/600px-Core-Assembly_Class.png "Informative representation in UML")

<b>Attributes</b><br />

<table class="wikitable">
<tr>
<th> Name
</th>
<th> Type
</th>
<th> Description
</th></tr>
<tr>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#hascontainsrelation" title="CoinsCore:hasContainsRelation Property">hasContainsRelation</a> </td>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#containsrelation" title="CoinsCore:ContainsRelation Class">ContainsRelation</a> </td>
<td> Reference to ContainsRelations
</td></tr>
</table>
<p><br />
</p>
<b>Formal Representation in RDF/XML</b><br />
<pre> &lt;owl:Class rdf:ID="Assembly"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;Assembly&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;Parent&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#Entity"/&gt;

   &lt;isClassAbstract rdf:datatype="xsd:boolean"&gt;true&lt;/isClassAbstract&gt;
   &lt;isClassExtendable rdf:datatype="xsd:boolean"&gt;true&lt;/isClassExtendable&gt;

   &lt;rdfs:subClassOf&gt;
     &lt;owl:Restriction&gt;
       &lt;owl:onProperty rdf:resource="#nextTrunkVersion"/&gt;
       &lt;owl:allValuesFrom rdf:resource="#Assembly"/&gt;
     &lt;/owl:Restriction&gt;
   &lt;/rdfs:subClassOf&gt;

   &lt;classCreator rdf:resource="#COINSTechnicalManagementGroup"/&gt;
   &lt;classCreationDate rdf:datatype="xsd:dateTime"&gt;2016-04-04T12:00:00.00&lt;/classCreationDate&gt;
   &lt;classVersionID rdf:datatype="xsd:string"&gt;1.0&lt;/classVersionID&gt;

 &lt;/owl:Class&gt;
</pre>


### BooleanProperty

</p><p>BooleanProperty is disjoined with <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#stringproperty"CoinsCore:StringProperty Class">StringProperty</a>, 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#numericproperty" title="CoinsCore:NumericProperty Class">NumericProperty</a>, 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#datetimeproperty" title="CoinsCore:DateTimeProperty Class">DateTimeProperty</a> and 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#uriproperty" title="CoinsCore:UriProperty Class">UriProperty</a>.
</p><p>BooleanProperty is not an abstract class; it can be instantiated directly. 
</p><p>The <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#nexttrunkversion" title="CoinsCore:nextTrunkVersion Property">nextTrunkVersion</a> is restricted to one other instance of BooleanProperty.
</p><p><br />
</p><p><b>History</b><br />* New in COINS 2.0
</p><p><br /> 
</p>
</p><p><b>Informative representation in UML</b><br /> 
<div class="thumb tright"><div class="thumbinner" style="width:251px;"><a href="/wiki2/index.php/Bestand:Core-BooleanProperty_Class.png" class="image"><img alt="" src="/wiki2/images/c/c7/Core-BooleanProperty_Class.png" width="249" height="254" class="thumbimage" /></a>  <div class="thumbcaption"><div class="magnify"><a href="/wiki2/index.php/Bestand:Core-BooleanProperty_Class.png" class="internal" title="Vergroten"></a></div>Informative representation of BooleanProperty in UML</div></div></div>
<p>This image shows the informative representation of the BooleanProperty class.
</p><p><br />
</p>
</p><p><b>Attributes</b><br />
<table class="wikitable">
<tr>
<th> Name
</th>
<th> Type
</th>
<th> Description
</th></tr>
<tr>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#datatypevalue" title="CoinsCore:datatypeValue Property">datatypeValue</a> </td>
<td> xsd:boolean </td>
<td> Exactly one Boolean value. Empty value not allowed.
</td></tr>
</table>
<p><br />
</p>
</p><p><b>Formal Representation in RDF/XML</b><br />
<pre> &lt;owl:Class rdf:ID="BooleanProperty"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;BooleanProperty&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;BooleanProperty&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#SimpleProperty"/&gt;

   &lt;owl:disjointWith rdf:resource="#StringProperty"/&gt;
   &lt;owl:disjointWith rdf:resource="#NumericProperty"/&gt;
   &lt;owl:disjointWith rdf:resource="#DateTimeProperty"/&gt;
   &lt;owl:disjointWith rdf:resource="#UriProperty"/&gt;

   &lt;owl:equivalentClass&gt;
     &lt;owl:Class&gt;
       &lt;owl:intersectionOf rdf:parseType="Collection"&gt;
         &lt;rdf:Description rdf:ID="SimpleProperty"/&gt;
         &lt;owl:Restriction&gt;
           &lt;owl:onProperty rdf:resource="#datatypeValue"/&gt;
           &lt;owl:allValuesFrom rdf:resource="xsd:boolean"/&gt;
         &lt;/owl:Restriction&gt;
       &lt;/owl:intersectionOf&gt;
     &lt;/owl:Class&gt;
   &lt;/owl:equivalentClass&gt;

   &lt;rdfs:subClassOf&gt;
     &lt;owl:Restriction&gt;
       &lt;owl:onProperty rdf:resource="#datatypeValue"/&gt;
       &lt;owl:allValuesFrom rdf:resource="xsd:boolean"/&gt;
     &lt;/owl:Restriction&gt;
   &lt;/rdfs:subClassOf&gt;

   &lt;isClassAbstract rdf:datatype="xsd:boolean"&gt;false&lt;/isClassAbstract&gt;
   &lt;isClassExtendable rdf:datatype="xsd:boolean"&gt;true&lt;/isClassExtendable&gt;

   &lt;rdfs:subClassOf&gt;
     &lt;owl:Restriction&gt;
       &lt;owl:onProperty rdf:resource="#nextTrunkVersion"/&gt;
       &lt;owl:allValuesFrom rdf:resource="#BooleanProperty"/&gt;
     &lt;/owl:Restriction&gt;
   &lt;/rdfs:subClassOf&gt;

   &lt;classCreator rdf:resource="#COINSTechnicalManagementGroup"/&gt;
   &lt;classCreationDate rdf:datatype="xsd:dateTime"&gt;2016-04-04T12:00:00.00&lt;/classCreationDate&gt;
   &lt;classVersionID rdf:datatype="xsd:string"&gt;1.0&lt;/classVersionID&gt;

 &lt;/owl:Class&gt;
</pre>


### CartesianLocator


### CataloguePart


### CoinsContainerObject


### ComplexProperty


### ComplexPropertyValue


### Concept



### Connection



### ContainsRelation
   
ContainsRelation is a subclass of Entity.

ContainsRelation is not an abstract class; it can instantiated directly.

The ContainsRelation class can be extended.

The nextTrunkVersion is restricted to one other individual of ContainsRelation.


History
* New in COINS 2.0


## Informative representation in UML


This image shows the informative representation of the ContainsRelation class.

![ContainsRelation class in UML](./media/600px-Core-ContainsRelation_Class.png "Informative representation of ContainsRelation in UML")



## Attributes
| Col1 | Col2 | Col3 |
| :--- | :--- | :--- |
| Name | Type |	Description |
| hasAssembly |	Assembly |	Reference to exactly 1 instance of Assembly |
| hasPart | Part | Reference to exactly 1 instance of Part
| groupedBy | ContainsRelationGroup | ContainsRelations can be grouped in ContainsRelationGroup


## Formal Representation in RDF/XML

 <code> <owl:Class rdf:ID="ContainsRelation">

   <rdfs:label xml:lang="en-GB">ContainsRelation</rdfs:label>
   <rdfs:comment xml:lang="en-GB">ContainsRelation</rdfs:comment>

   <rdfs:subClassOf rdf:resource="#Entity"/>

   <owl:disjointWith rdf:resource="#Part"/>
   <owl:disjointWith rdf:resource="#Assembly"/>

   <rdfs:subClassOf>
     <owl:Restriction>
       <owl:onProperty rdf:resource="#hasAssembly"/>
       <owl:cardinality rdf:datatype="xsd:nonNegativeInteger">1</owl:cardinality>
     </owl:Restriction>
   </rdfs:subClassOf>

   <rdfs:subClassOf>
     <owl:Restriction>
       <owl:onProperty rdf:resource="#hasPart"/>
       <owl:cardinality rdf:datatype="xsd:nonNegativeInteger">1</owl:cardinality>
     </owl:Restriction>
   </rdfs:subClassOf>

   <isClassAbstract rdf:datatype="xsd:boolean">false</isClassAbstract>
   <isClassExtendable rdf:datatype="xsd:boolean">true</isClassExtendable>

   <rdfs:subClassOf>
     <owl:Restriction>
       <owl:onProperty rdf:resource="#nextTrunkVersion"/>
       <owl:allValuesFrom rdf:resource="#ContainsRelation"/>
     </owl:Restriction>
   </rdfs:subClassOf>

   <classCreator rdf:resource="#COINSTechnicalManagementGroup"/>
   <classCreationDate rdf:datatype="xsd:dateTime">2016-04-04T12:00:00.00</classCreationDate>
   <classVersionID rdf:datatype="xsd:string">1.0</classVersionID>

 </owl:Class> </code>




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
Description of core model Properties



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



