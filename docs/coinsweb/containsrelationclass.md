# ContainsRelation

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

