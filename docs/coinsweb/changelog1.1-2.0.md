# <a>Versions and differences</a> 


## COINS 2.0
Coins 2.0 is major update of the Coins standard. It was first presented on the 7th of April, 2016.

Coins 2.0 replaces COINS 1.1.

### Mandate

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

### Version 1.1 versus 1.2

Differences in the COINS 2.0 Core Model compared to COINS 1.1

</p>
<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> COINS 1.1 Class
</th>
<th> Status in Coins 2.0
</th>
<th> COINS 2.0 Core Model Class
</th>
<th> Remark
</th></tr>
<tr>
<td> Amount </td>
<td> Obsolete </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> Baseline </td>
<td> Obsolete </td>
<td> </td>
<td> To be developed in a reference framework
</td></tr>
<tr>
<td> Building </td>
<td> Obsolete </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> C-BIM Object </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:Concept_Class" title="CoinsCore:Concept Class">Concept</a> </td>
<td>
</td></tr>
<tr>
<td> Catalogue Part </td>
<td> Unchanged </td>
<td> <a href="/wiki2/index.php/CoinsCore:CataloguePart_Class" title="CoinsCore:CataloguePart Class">CataloguePart</a> </td>
<td>
</td></tr>
<tr>
<td> Connection </td>
<td> Modified </td>
<td> <a href="/wiki2/index.php/CoinsCore:Connection_Class" title="CoinsCore:Connection Class">Connection</a> </td>
<td> No longer for terminal objects only
</td></tr>
<tr>
<td> Document </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:DocumentReference_Class" title="CoinsCore:DocumentReference Class">DocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> Explicit 3D Representation </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:ShapeRepresentation_Class" title="CoinsCore:ShapeRepresentation Class">ShapeRepresentation</a> </td>
<td>
</td></tr>
<tr>
<td> Function </td>
<td> Obsolete </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> Function Fulfiller </td>
<td> Obsolete </td>
<td> </td>
<td> In Coins 2.0 there is no distinction between Function Fulfiller and Physical Object. They are replaced by <a href="/wiki2/index.php/CoinsCore:Object_Class" title="CoinsCore:Object Class">Object</a>.
</td></tr>
<tr>
<td> Library Reference </td>
<td> </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> Locator </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:CartesianLocator_Class" title="CoinsCore:CartesianLocator Class">CartesianLocator</a> </td>
<td> The Locator Class in 1.1 is replaced by Cartesian Locator Class in 2.0, a subClassOf the new <a href="/wiki2/index.php/CoinsCore:Locator_Class" title="CoinsCore:Locator Class">Locator</a> Class
</td></tr>
<tr>
<td> Parameter </td>
<td> Obsolete </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> Performance </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> PersonOrOrganisation </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:Party_Class" title="CoinsCore:Party Class">Party</a> </td>
<td>
</td></tr>
<tr>
<td> Physical Object </td>
<td>  Obsolete </td>
<td> </td>
<td> In Coins 2.0 there is no distinction between Function Fulfiller and Physical Object. They are replaced by <a href="/wiki2/index.php/CoinsCore:Object_Class" title="CoinsCore:Object Class">Object</a>.
</td></tr>
<tr>
<td> Property Type </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:StringProperty_Class" title="CoinsCore:StringProperty Class">StringProperty</a><br /> <a href="/wiki2/index.php/CoinsCore:BooleanProperty_Class" title="CoinsCore:BooleanProperty Class">BooleanProperty</a><br /> <a href="/wiki2/index.php/CoinsCore:DateTimeProperty_Class" title="CoinsCore:DateTimeProperty Class">DateTimeProperty</a><br /> <a href="/wiki2/index.php/CoinsCore:NumericProperty_Class" title="CoinsCore:NumericProperty Class">NumericProperty</a><br /> <a href="/wiki2/index.php/CoinsCore:UriProperty_Class" title="CoinsCore:UriProperty Class">UriProperty</a> </td>
<td> Property types are added explictly per datatype
</td></tr>
<tr>
<td> Property Value </td>
<td> Replaced </td>
<td> <a href="/wiki2/index.php/CoinsCore:datatypeValue_Property" title="CoinsCore:datatypeValue Property">datatypeValue Property</a> (for <a href="/wiki2/index.php/CoinsCore:SimpleProperty_Class" title="CoinsCore:SimpleProperty Class">SimpleProperty</a>)<br /><a href="/wiki2/index.php/CoinsCore:ComplexPropertyValue_Class" title="CoinsCore:ComplexPropertyValue Class">ComplexPropertyValue Class</a> (for <a href="/wiki2/index.php/CoinsCore:ComplexProperty_Class" title="CoinsCore:ComplexProperty Class">ComplexProperty</a>) </td>
<td> property Value is split in Simple and Complex values
</td></tr>
<tr>
<td> Requirement </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Space </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> State </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Task </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Task Type </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Terminal </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Value Domain </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> Vector </td>
<td> Unchanged </td>
<td> <a href="/wiki2/index.php/CoinsCore:Vector_Class" title="CoinsCore:Vector Class">Vector</a> </td>
<td>
</td></tr>
<tr>
<td> Verification </td>
<td> Obsolete </td>
<td> </td>
<td> to be developed in a reference framework
</td></tr>
<tr>
<td> VISI Message </td>
<td> Obsolete </td>
<td> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Assembly_Class" title="CoinsCore:Assembly Class">Assembly</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:CoinsContainerObject_Class" title="CoinsCore:CoinsContainerObject Class">CoinsContainerObject</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ComplexProperty_Class" title="CoinsCore:ComplexProperty Class">ComplexProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ComplexPropertyValue_Class" title="CoinsCore:ComplexPropertyValue Class">ComplexPropertyValue</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ContainsRelation_Class" title="CoinsCore:ContainsRelation Class">ContainsRelation</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ContainsRelationGroup_Class" title="CoinsCore:ContainsRelationGroup Class">ContainsRelationGroup</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:DirectedConnection_Class" title="CoinsCore:DirectedConnection Class">DirectedConnection</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:DocumentProperty_Class" title="CoinsCore:DocumentProperty Class">DocumentProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Entity_Class" title="CoinsCore:Entity Class">Entity</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:EntityProperty_Class" title="CoinsCore:EntityProperty Class">EntityProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ExpiredEntity_Class" title="CoinsCore:ExpiredEntity Class">ExpiredEntity</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ExternalDocumentReference_Class" title="CoinsCore:ExternalDocumentReference Class">ExternalDocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:InternalDocumentReference_Class" title="CoinsCore:InternalDocumentReference Class">InternalDocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:LocatorProperty_Class" title="CoinsCore:LocatorProperty Class">LocatorProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Part_Class" title="CoinsCore:Part Class">Part</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Object_Class" title="CoinsCore:Object Class">Object</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Person_Class" title="CoinsCore:Person Class">Person</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:Organisation_Class" title="CoinsCore:Organisation Class">Organisation</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:SecuredDocumentReference_Class" title="CoinsCore:SecuredDocumentReference Class">SecuredDocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:SecuredExternalDocumentReference_Class" title="CoinsCore:SecuredExternalDocumentReference Class">SecuredExternalDocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:SecuredInternalDocumentReference_Class" title="CoinsCore:SecuredInternalDocumentReference Class">SecuredInternalDocumentReference</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:ShapeRepresentationProperty_Class" title="CoinsCore:ShapeRepresentationProperty Class">ShapeRepresentationProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:SimpleProperty_Class" title="CoinsCore:SimpleProperty Class">SimpleProperty</a> </td>
<td>
</td></tr>
<tr>
<td> </td>
<td> New </td>
<td> <a href="/wiki2/index.php/CoinsCore:VersionObject_Class" title="CoinsCore:VersionObject Class">VersionObject</a> </td>
<td>
</td></tr>
</table>
<p><br />
</p>



