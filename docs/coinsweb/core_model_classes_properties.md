# Core Model Classes and Properties

Description of core model Classes and Properties


## Core Model Classes

Description of core model Classes 


### Assembly

**Assembly** is a subclass of <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#entity" title="CoinsCore:Entity Class">Entity</a>.
Assembly is an abstract class; it can not be instantiated directly. Members of intantiatable subclasses of Entity can additionally be typed as Assembly.

The Assembly class is extendable.

The <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#nexttrunkversion" title="CoinsCore:nextTrunkVersion Property">nextTrunkVersion</a> is restricted to one other individual of Assembly.


**History**

* New in COINS

**Informative representation in UML**

This image shows the informative representation of the Assembly class.

![Informative representation of Assembly in UML](./media/600px-Core-Assembly_Class.png "Informative representation in UML")

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
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#hascontainsrelation" title="CoinsCore:hasContainsRelation Property">hasContainsRelation</a> </td>
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#containsrelation" title="CoinsCore:ContainsRelation Class">ContainsRelation</a> </td>
<td> Reference to ContainsRelations
</td></tr>
</table>


**Formal Representation in RDF/XML**

<code> &lt;owl:Class rdf:ID="Assembly"&gt;
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
</code>


### BooleanProperty

**BooleanProperty** is disjoined with <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#stringproperty"CoinsCore:StringProperty Class">StringProperty</a>, 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#numericproperty" title="CoinsCore:NumericProperty Class">NumericProperty</a>, 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#datetimeproperty" title="CoinsCore:DateTimeProperty Class">DateTimeProperty</a> and 
<a href="https://bimloket.github.io/COINS_2.0/coinsweb/#uriproperty" title="CoinsCore:UriProperty Class">UriProperty</a>.

BooleanProperty is not an abstract class; it can be instantiated directly. 

The <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#nexttrunkversion" title="CoinsCore:nextTrunkVersion Property">nextTrunkVersion</a> is restricted to one other instance of BooleanProperty.

   
**History**
* New in COINS 2.0

   
**Informative representation in UML**
 
This image shows the informative representation of the BooleanProperty class
 
![Informative representation of Assembly in UML](./media/Core-BooleanProperty_Class.png "Informative representation in UML")
 
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
<td> <a href="https://bimloket.github.io/COINS_2.0/coinsweb/#datatypevalue" title="CoinsCore:datatypeValue Property">datatypeValue</a> </td>
<td> xsd:boolean </td>
<td> Exactly one Boolean value. Empty value not allowed.
</td></tr>
</table>
	
**Formal Representation in RDF/XML**

