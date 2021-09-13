# Core Model Classes and Properties



## Core Model Classes


### Assembly
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
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#hascontainsrelation">hasContainsRelation</a> </td>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#containsrelation" title="CoinsCore:ContainsRelation Class">ContainsRelation</a> </td>
<td> Reference to ContainsRelations
</td></tr>
</table>


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
<h2><span class="mw-headline" id="Informative_representation_in_UML">Informative representation in UML</span></h2>
<div class="thumb tright"><div class="thumbinner" style="width:251px;"><a href="/wiki2/index.php/Bestand:Core-BooleanProperty_Class.png" class="image"><img alt="" src="/wiki2/images/c/c7/Core-BooleanProperty_Class.png" width="249" height="254" class="thumbimage" /></a>  <div class="thumbcaption"><div class="magnify"><a href="/wiki2/index.php/Bestand:Core-BooleanProperty_Class.png" class="internal" title="Vergroten"></a></div>Informative representation of BooleanProperty in UML</div></div></div>
<p>This image shows the informative representation of the BooleanProperty class.
</p><p><br />
</p>
<h2><span class="mw-headline" id="Attributes">Attributes</span></h2>
<table class="wikitable">
<tr>
<th> Name
</th>
<th> Type
</th>
<th> Description
</th></tr>
<tr>
<td> <a href="/wiki2/index.php/CoinsCore:datatypeValue_Property" title="CoinsCore:datatypeValue Property">datatypeValue</a> </td>
<td> xsd:boolean </td>
<td> Exactly one Boolean value. Empty value not allowed.
</td></tr>
</table>
<p><br />
</p>
<h2><span class="mw-headline" id="Formal_Representation_in_RDF.2FXML">Formal Representation in RDF/XML</span></h2>
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
<!-- 
NewPP limit report
Cached time: 20210913092422
Cache expiry: 86400
Dynamic content: false
CPU time usage: 0.044 seconds
Real time usage: 0.083 seconds
Preprocessor visited node count: 11/1000000
Preprocessor generated node count: 20/1000000
Post‐expand include size: 0/2097152 bytes
Template argument size: 0/2097152 bytes
Highest expansion depth: 2/40
Expensive parser function count: 0/100
-->

<!-- 
Transclusion expansion time report (%,ms,calls,template)
100.00%    0.000      1 - -total
-->

<!-- Saved in parser cache with key coinsweb-COINS2:pcache:idhash:101-0!*!0!!*!5!* and timestamp 20210913092422 and revision id 1093
 -->
</div>					<div class="printfooter">


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



