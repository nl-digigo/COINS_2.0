## Exchange

## COINS 1.1 container

The COINS Container is the central means of communication for object related content and associated documents between the various users/contributors of BIM data. Physically the container is a common Zip file with a predefined folder structure. At this stage three folders are recognized:

* **bim** 
In the bim folder the CBIM (sub)model can be found.
* **doc** 
The doc folder will contain all associated documents referenced from the CBIM in the bim folder. Here we may find 3D representation files, text documents, spreadsheets, etc.
* **woa** 
The woa folder is reserved for the window of authorization description file called woa.xml.


### Export procedure

A COINS Container is composed during an export procedure by a COINS compatible application or a COINS Building Information System. During the export procedure a COINS model is serialized using RDF/XML formatting into a physical file. This model file is put into the bim folder of the COINS Container file.

As part of this transfer an inventory is drawn up of all the documents that are referenced by objects in this particular model. In principle, these documents are added to the doc folder of the COINS Container file. However, if a document is only referred to by a web address then this document reference is preserved as a web link. If copies of the document are both available on the web and on the local file system of the exporting party, a choice has to be made to either reference the document with a link to a copy in the doc folder or to reference it with a web link. If different document versions are referenced as a copy in the doc folder and as a weblink the document instance in the container has precedence over the weblink document instance.

If the document file is physically into the doc folder the document object which contains the original file path to the document needs to be updated because the absolute file path is not relevant anymore. By convention the file path is reduced to just the file name. In case of documents with the same name an extra digit or letter should be added to prevent unintentional overwriting.

Exporting from a COINS Building Information System is little bit more complicated. Before the model can be serialized several filter operations are necessary:

* The export model will only contain last object versions that are non-expired.
* Previous object versions will only confuse the COINS compatible applications that are probably less sophisticated in this respect. The information of previous object versions is also not relevant in order to do their assignment correctly.
* The export model will not contain VISI messages (or other document references that contain information about how a particular object has turned up in the central model). Again, this is not relevant for COINS compatible applications.
* As a guideline it is cleaner to strip all version extensions from the export model. Version number are only meaningful within a COINS Building Information System. So for example an object with ID "http://www.example.com/COINS/testmodel.owl#_0d94476b-3b4b-4f4b-beb6-0f6973c6650a.6" is exported as "http://www.example.com/COINS/testmodel.owl#_0d94476b-3b4b-4f4b-beb6-0f6973c6650a" without the version delimiting dot and the version number itself.
* In case of a WoA (Window of Authorization) specification the objects that are marked non-accessible should be stripped from the export model. The WoA specification itself is stored in the woa folder of the COINS Container file.


### Import procedure

Importing a COINS Container is relatively simple for a COINS compatible application:

* Firstly the COINS Container is unpacked in a working directory or folder.
* This is rather straight forward since the COINS Container is an ordinary ZIP file. The result will be a set of sub-folders: at least a bim folder and possibly also a doc and/or woa folder.

Then the model file in the bim folder is loaded. After loading the document objects are updated to point with a correct absolute file path to the documents in the doc folder.
Importing a COINS Container in a COINS Building Information System is in principle the same procedure. However, normally the BIM manager will merge the contents of a COINS Container with the content of the shared project model. This means that the standard import procedure will be followed by the much more complex merge procedure. Merging is described in more detail in the Merging section of Version Management.

### Delta container
Since COINS 1.1 a COINS container may also support modifications to a an earlier communicated reference model. This container format type is called a Delta container. 

#### formaat-uitbreiding
De containerformaat-uitbreiding met deltawaarden betekent in feite dat de COINS 1.0 samenvoegingsoperatie wordt verplaatst van de ontvanger naar de verzender van de container. Onderdeel van de samenvoegingsoperatie is een vergelijking van twee modellen, namelijk het actuele model met een model dat op een eerder moment is opgeslagen. De partij die de container met delta-waarden verstuurt moet dus op basis van deze vergelijking de verschillen vaststellen en deze verschillen in de container plaatsen. In het volgende worden wat basis-mutaties bekeken.


#### Basis-mutaties

1. Nieuw object toevoegen
Het eerste voorbeeld is het meest eenvoudige geval: het toevoegen van een object aan een leeg model. Bij het samenvoegen van het vorige model (Model.0) met het actuele model (Model.1) ontstaat het samengestelde model (Model.1+0) met de 0-versie van het nieuwe object. Het verschilmodel (Model.1-0) dient ook dit nieuwe object te bevatten.

![Nieuw Object Toevoegen](./media/Nieuw_object_toevoegen.png "Nieuw object toevoegen: het vorige model (Model.0) is leeg en het actuele model (Model.1) bevat een object (object 1). De samenvoeging van deze twee modellen (Model.1+0) toont het object met versienummer 0. Het verschilmodel (Model.1-0) bevat het nieuwe object en is inhoudelijk gelijk aan Model.1.") 


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;willemsph&lt;/cbim:name&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
 &lt;/cbim:PersonOrOrganisation&gt;
&lt;/rdf:RDF&gt;
</pre>


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:creator&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:creator&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:creator&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:creator&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
   &lt;cbim:document&gt;
     &lt;cbim:VisiMessage rdf:ID="_55379f23-29b0-499f-9abe-66ee1916190b.0"&gt;
       &lt;cbim:description rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;27-Feb-2014 11:31:51&lt;/cbim:description&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;VISI&lt;/cbim:name&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:31:51.697Z&lt;/cbim:creationDate&gt;
       &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
     &lt;/cbim:VisiMessage&gt;
   &lt;/cbim:document&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl#</a>"
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.1-0.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:creator&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;/cbim:creator&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>


![Model.1-0 serialisatie. Omdat het voorgaande model (0) leeg is is in dit bijzondere geval het verschilmodel (1-0) gelijk aan het actuele model (1). Het linken aan een creator-PersonOrOrganisation is standaard in COINS 1.0. De COINS Navigator creëert dit object automatisch bij een nieuw model.](./media/Model.1-0.png "Model.1-0 serialisatie. Omdat het voorgaande model (0) leeg is is in dit bijzondere geval het verschilmodel (1-0) gelijk aan het actuele model (1). Het linken aan een creator-PersonOrOrganisation is standaard in COINS 1.0. De COINS Navigator creëert dit object automatisch bij een nieuw model.") 


2. Nieuw object toevoegen en verbinden met een bestaand object
Aan het bestaande model met een object (object 1) wordt een nieuw object (object 2) toegevoegd en verbonden met een part-of (parent) relatie.


![Nieuw object toevoegen en verbinden met een bestaand object. Het combinatiemodel (Model.2+1) bevat ook het oorspronkelijke, niet verbonden object maar nu gemarkeerd als “expired”. De actuele versie van dit object (1) is verbonden met het nieuwe object. Het verschilmodel (Model.2-1) bevat het oorspronkelijke object verbonden met het nieuwe object.](./media/Nieuw_object_toevoegen_en_verbinden_met_een_bestaand_object.png "Nieuw object toevoegen en verbinden met een bestaand object. Het combinatiemodel (Model.2+1) bevat ook het oorspronkelijke, niet verbonden object maar nu gemarkeerd als “expired”. De actuele versie van dit object (1) is verbonden met het nieuwe object. Het verschilmodel (Model.2-1) bevat het oorspronkelijke object verbonden met het nieuwe object.") 




<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_060f8f3d-5f7a-45bd-99ed-5f7478bd5591.0"&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 2&lt;/cbim:name&gt;
   &lt;cbim:physicalParent&gt;
     &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;Object 1&lt;/cbim:name&gt;
       &lt;cbim:creator&gt;
         &lt;cbim:PersonOrOrganisation 
           rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
           &lt;cbim:creationDate 
      rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;willemsph&lt;/cbim:name&gt;
         &lt;/cbim:PersonOrOrganisation&gt;
       &lt;/cbim:creator&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
       &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
       &gt;0&lt;/cbim:layerIndex&gt;
     &lt;/cbim:PhysicalObject&gt;
   &lt;/cbim:physicalParent&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T13:11:49.569Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;1&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_060f8f3d-5f7a-45bd-99ed-5f7478bd5591.0"&gt;
   &lt;cbim:physicalParent&gt;
     &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.1"&gt;
       &lt;cbim:creator&gt;
         &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
           &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;willemsph&lt;/cbim:name&gt;
         &lt;/cbim:PersonOrOrganisation&gt;
       &lt;/cbim:creator&gt;
       &lt;cbim:document&gt;
         &lt;cbim:VisiMessage rdf:ID="_333ba994-cab8-4e98-a39f-a0008e4ed520.0"&gt;
           &lt;cbim:description rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;27-Feb-2014 14:13:44&lt;/cbim:description&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;VISI&lt;/cbim:name&gt;
           &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T13:13:44.702Z&lt;/cbim:creationDate&gt;
           &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
         &lt;/cbim:VisiMessage&gt;
       &lt;/cbim:document&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;Object 1&lt;/cbim:name&gt;
       &lt;cbim:modificationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T13:13:44.702Z&lt;/cbim:modificationDate&gt;
       &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
       &gt;0&lt;/cbim:layerIndex&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PhysicalObject&gt;
   &lt;/cbim:physicalParent&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 2&lt;/cbim:name&gt;
   &lt;cbim:document rdf:resource="#_333ba994-cab8-4e98-a39f-a0008e4ed520.0"/&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;1&lt;/cbim:layerIndex&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T13:11:49.569Z&lt;/cbim:creationDate&gt;
 &lt;/cbim:PhysicalObject&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:expired rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#boolean" class='external free' title="http://www.w3.org/2001/XMLSchema#boolean" rel="nofollow">http://www.w3.org/2001/XMLSchema#boolean</a>"
   &gt;true&lt;/cbim:expired&gt;
   &lt;cbim:nextVersion rdf:resource="#_dad954b2-699a-4637-9a4c-f4605e24221e.1"/&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.2-1.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_060f8f3d-5f7a-45bd-99ed-5f7478bd5591.0"&gt;
   &lt;cbim:creator&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;/cbim:creator&gt;
   &lt;cbim:physicalParent&gt;
     &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"/&gt;
   &lt;/cbim:physicalParent&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 2&lt;/cbim:name&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T13:11:49.569Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;1&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

![Model.2-1 serialisatie. Referenties naar het bestaande object PersonOrOrganisation zijn noodzakelijk voor het specificeren van creator en modifier relaties. Het object zelf ondergaat geen modificatie.](./media/Model.2-1.png "Model.2-1 serialisatie. Referenties naar het bestaande object PersonOrOrganisation zijn noodzakelijk voor het specificeren van creator en modifier relaties. Het object zelf ondergaat geen modificatie.") 



Het verschilmodel bevat zowel het oorspronkelijke object (object 1) als het nieuwe object (object 2). De noodzaak om ook object 1 aan het verschilmodel toe te voegen vergt wat uitleg. Men kan redeneren dat het feit dat object 2 naar object 1 verwijst geen verandering van object 1 is. Maar zonder de aanwezigheid van object 1 kan deze relatie niet gespecificeerd worden. Dat in het samenvoegingsmodel voor object 1 een nieuwe versie (1) ontstaat heeft te maken met het feit dat de parent-relatie een expliciete inverse heeft, de relatie is dus bi-directioneel en daarom geldt dit ook als een mutatie van object 1.

3. Verwijderen van een object en (impliciet) zijn relatie met een ander object
In deze stap wordt het laatst toegevoegde object weer verwijderd. In het samenvoegingsmodel worden beide objecten “expired” verklaard maar alleen van object 1 wordt een nieuwe versie (1) aangemaakt.

![Verwijderen van een object en zijn relatie met een ander object.](./media/Verwijderen_van_een_object.png "Verwijderen van een object en zijn relatie met een ander object.") 


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:creator&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:creator&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_060f8f3d-5f7a-45bd-99ed-5f7478bd5591.0"&gt;
   &lt;cbim:expired rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#boolean" class='external free' title="http://www.w3.org/2001/XMLSchema#boolean" rel="nofollow">http://www.w3.org/2001/XMLSchema#boolean</a>"
   &gt;true&lt;/cbim:expired&gt;
   &lt;cbim:modificationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T15:07:20.71Z&lt;/cbim:modificationDate&gt;
   &lt;cbim:modifier&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:modifier&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;1&lt;/cbim:layerIndex&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T13:11:49.569Z&lt;/cbim:creationDate&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:physicalParent&gt;
     &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
       &lt;cbim:expired rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#boolean" class='external free' title="http://www.w3.org/2001/XMLSchema#boolean" rel="nofollow">http://www.w3.org/2001/XMLSchema#boolean</a>"
       &gt;true&lt;/cbim:expired&gt;
       &lt;cbim:nextVersion&gt;
         &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.1"&gt;
           &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
           &lt;cbim:document&gt;
             &lt;cbim:VisiMessage rdf:ID="_c6493e21-ac42-459d-8b0e-e9ed3b286f70.0"&gt;
               &lt;cbim:description 
                 rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
               &gt;27-Feb-2014 16:07:20&lt;/cbim:description&gt;
               &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
               &gt;VISI&lt;/cbim:name&gt;
               &lt;cbim:creationDate 
                 rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
               &gt;2014-02-27T15:07:20.69Z&lt;/cbim:creationDate&gt;
               &lt;cbim:creator 
                 rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
             &lt;/cbim:VisiMessage&gt;
           &lt;/cbim:document&gt;
           &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
           &gt;0&lt;/cbim:layerIndex&gt;
           &lt;cbim:creationDate 
             rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;Object 1&lt;/cbim:name&gt;
           &lt;cbim:modificationDate 
             rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T15:07:20.69Z&lt;/cbim:modificationDate&gt;
         &lt;/cbim:PhysicalObject&gt;
       &lt;/cbim:nextVersion&gt;
       &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
       &gt;0&lt;/cbim:layerIndex&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
       &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;Object 1&lt;/cbim:name&gt;
     &lt;/cbim:PhysicalObject&gt;
   &lt;/cbim:physicalParent&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 2&lt;/cbim:name&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.3-2.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"/&gt;
 &lt;cbim:PhysicalObject rdf:ID="_060f8f3d-5f7a-45bd-99ed-5f7478bd5591.0"&gt;
   &lt;cbim:expired rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#boolean" class='external free' title="http://www.w3.org/2001/XMLSchema#boolean" rel="nofollow">http://www.w3.org/2001/XMLSchema#boolean</a>"
   &gt;true&lt;/cbim:expired&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>


![Verwijderen van een object en zijn relatie met een ander object.](./media/Model.3-2.png "Verwijderen van een object en zijn relatie met een ander object.") 



4 Veranderen van de waarde van een objecteigenschap
In deze stap wordt het veld “Description” van object 1 ingevuld. Het verschilmodel bevat dit object inclusief de ingevulde waarde.

![Veranderen van de waarde van een objecteigenschap.](./media/Veranderen_van_de_waarde_van_een_objecteigenschap.png "Veranderen van de waarde van een objecteigenschap.") 




<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:description rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;My Description&lt;/cbim:description&gt;
   &lt;cbim:modifier&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:modifier&gt;
   &lt;cbim:modificationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T15:32:17.727Z&lt;/cbim:modificationDate&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>

<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:expired rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#boolean" class='external free' title="http://www.w3.org/2001/XMLSchema#boolean" rel="nofollow">http://www.w3.org/2001/XMLSchema#boolean</a>"
   &gt;true&lt;/cbim:expired&gt;
   &lt;cbim:nextVersion&gt;
     &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.1"&gt;
       &lt;cbim:modifier&gt;
         &lt;cbim:PersonOrOrganisation
           rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"&gt;
           &lt;cbim:creationDate 
             rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T10:27:23.391Z&lt;/cbim:creationDate&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;willemsph&lt;/cbim:name&gt;
         &lt;/cbim:PersonOrOrganisation&gt;
       &lt;/cbim:modifier&gt;
       &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
       &lt;cbim:description rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;My Description&lt;/cbim:description&gt;
       &lt;cbim:document&gt;
         &lt;cbim:VisiMessage rdf:ID="_cd198f71-5947-4e7d-8a48-887c6cab335a.0"&gt;
           &lt;cbim:description 
             rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;27-Feb-2014 16:34:32&lt;/cbim:description&gt;
           &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
           &gt;VISI&lt;/cbim:name&gt;
           &lt;cbim:creationDate 
             rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
           &gt;2014-02-27T15:34:32.923Z&lt;/cbim:creationDate&gt;
           &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
         &lt;/cbim:VisiMessage&gt;
       &lt;/cbim:document&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;Object 1&lt;/cbim:name&gt;
       &lt;cbim:modificationDate 
         rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T15:34:32.923Z&lt;/cbim:modificationDate&gt;
       &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
       &gt;0&lt;/cbim:layerIndex&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
     &lt;/cbim:PhysicalObject&gt;
   &lt;/cbim:nextVersion&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Object 1&lt;/cbim:name&gt;
   &lt;cbim:creator rdf:resource="#_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T10:29:56.659Z&lt;/cbim:creationDate&gt;
   &lt;cbim:layerIndex rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#int" class='external free' title="http://www.w3.org/2001/XMLSchema#int" rel="nofollow">http://www.w3.org/2001/XMLSchema#int</a>"
   &gt;0&lt;/cbim:layerIndex&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>


<pre>&lt;?xml version="1.0"?&gt;
&lt;rdf:RDF
   xmlns:rdf="<a href="http://www.w3.org/1999/02/22-rdf-syntax-ns#" class='external free' title="http://www.w3.org/1999/02/22-rdf-syntax-ns#" rel="nofollow">http://www.w3.org/1999/02/22-rdf-syntax-ns#</a>"
   xmlns:owl="<a href="http://www.w3.org/2002/07/owl#" class='external free' title="http://www.w3.org/2002/07/owl#" rel="nofollow">http://www.w3.org/2002/07/owl#</a>"
   xmlns:xsd="<a href="http://www.w3.org/2001/XMLSchema#" class='external free' title="http://www.w3.org/2001/XMLSchema#" rel="nofollow">http://www.w3.org/2001/XMLSchema#</a>"
   xmlns:cbim="<a href="http://www.coinsweb.nl/c-bim.owl#" class='external free' title="http://www.coinsweb.nl/c-bim.owl#" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#</a>"
   xmlns="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl#" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl#" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl#</a>"
   xmlns:rdfs="<a href="http://www.w3.org/2000/01/rdf-schema#" class='external free' title="http://www.w3.org/2000/01/rdf-schema#" rel="nofollow">http://www.w3.org/2000/01/rdf-schema#</a>"
 xml:base="<a href="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl" class='external free' title="http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl" rel="nofollow">http://www.coinsweb.nl/COINS-1.1/DeltaContainer/model.4-3.owl</a>"&gt;
 &lt;owl:Ontology rdf:about=""&gt;
   &lt;owl:imports rdf:resource="<a href="http://www.coinsweb.nl/c-bim.owl" class='external free' title="http://www.coinsweb.nl/c-bim.owl" rel="nofollow">http://www.coinsweb.nl/c-bim.owl</a>"/&gt;
   &lt;owl:versionInfo rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Created with COINS-IO API &lt;/owl:versionInfo&gt;
 &lt;/owl:Ontology&gt;
 &lt;cbim:PhysicalObject rdf:ID="_dad954b2-699a-4637-9a4c-f4605e24221e.0"&gt;
   &lt;cbim:modifier&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_cc08c019-e5a7-43c3-ba94-eac025071236.0"/&gt;
   &lt;/cbim:modifier&gt;
   &lt;cbim:modificationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-02-27T15:32:17.727Z&lt;/cbim:modificationDate&gt;
   &lt;cbim:description rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;My Description&lt;/cbim:description&gt;
 &lt;/cbim:PhysicalObject&gt;
&lt;/rdf:RDF&gt;
</pre>



![Model.4-3](./media/Model.4-3.png "Model.4-3") 


#### Checksum for attached documents

The option to specify a checksum for a referenced document is an new extension to the cbim:Document object class.

A checksum or hash sum is a small-size datum computed from an arbitrary block of digital data for the purpose of detecting errors which may have been introduced during its transmission or storage. The actual procedure which yields the checksum, given a data input is called a checksum function or checksum algorithm. http://en.wikipedia.org/wiki/Checksum

The computational result of the checksum algorithm applied to the file (the hash) is recorded in the datatype property cbim:checksumFile. The applied checksum-algorithm is specified in the datatype property cbim:checksumFileAlgorithm. COINS does not prescribe which checksum algorithm should be applied but leaves this to be agreed by the transaction partners.


![Checksum for attached documents in the container.](./media/ChecksumFile.png "Checksum for attached documents in the container.") 

COINS offers the option to by-pass of actual storing a copy of the document in the container by specifying a web-address where the document can be found. In that event the checksum helps the receiver of the container to assess that the linked document is indeed the correct document.


![Checksum for attached documents outside the container.](./media/ChecksumUri.png "Checksum for attached documents outside the container.") 

Example:

![Checksum for attached documents.](./media/ChecksumNavigator.png "Checksum for attached documents.") 

<pre>&lt;cbim:Document rdf:ID="_599d0edf-984d-48d6-815a-7ffb1427d71a.0"&gt;
   &lt;cbim:checksumUriAlgorithm rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;MD5&lt;/cbim:checksumUriAlgorithm&gt;
   &lt;cbim:checksumFileAlgorithm rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;MD5&lt;/cbim:checksumFileAlgorithm&gt;
   &lt;cbim:modificationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-03-31T10:00:54.14Z&lt;/cbim:modificationDate&gt;
   &lt;cbim:documentAliasFilePath rdf:resource="file:///article1.pdf" /&gt;
   &lt;cbim:documentType rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;PDF&lt;/cbim:documentType&gt;
   &lt;cbim:modifier&gt;
     &lt;cbim:PersonOrOrganisation rdf:ID="_dfdaebdc-9edf-43bb-bb8a-89dd94be62c6.0"&gt;
       &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
       &gt;2014-03-28T10:20:36.479Z&lt;/cbim:creationDate&gt;
       &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
       &gt;willemsph&lt;/cbim:name&gt;
     &lt;/cbim:PersonOrOrganisation&gt;
   &lt;/cbim:modifier&gt;
   &lt;cbim:name rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;Document_1&lt;/cbim:name&gt;
   &lt;cbim:checksumFile rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;f633cae3f6a3c345985a8d31ba2d5a48&lt;/cbim:checksumFile&gt;
   &lt;cbim:checksumUri rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#string" class='external free' title="http://www.w3.org/2001/XMLSchema#string" rel="nofollow">http://www.w3.org/2001/XMLSchema#string</a>"
   &gt;c7f140a5d580047ab868961f28eea295&lt;/cbim:checksumUri&gt;
   &lt;cbim:creator rdf:resource="#_dfdaebdc-9edf-43bb-bb8a-89dd94be62c6.0"/&gt;
   &lt;cbim:documentUri rdf:resource="<a href="http://www.modelservers.org/public/COINS/1.1/models/cbim-1.1.owl" class='external free' title="http://www.modelservers.org/public/COINS/1.1/models/cbim-1.1.owl" rel="nofollow">http://www.modelservers.org/public/COINS/1.1/models/cbim-1.1.owl</a>"/&gt;
   &lt;cbim:creationDate rdf:datatype="<a href="http://www.w3.org/2001/XMLSchema#dateTime" class='external free' title="http://www.w3.org/2001/XMLSchema#dateTime" rel="nofollow">http://www.w3.org/2001/XMLSchema#dateTime</a>"
   &gt;2014-03-28T10:20:46.236Z&lt;/cbim:creationDate&gt;
 &lt;/cbim:Document&gt;
</pre>


## COINS-IO
The COINS-IO software module has built-in functions for both importing and exporting a COINS Container.


## Window of Authorization

An important aspect of the COINS information transaction process using COINS Containers is the control over the data access rights of the person who executes an assignment. A BIM contributor typically needs access to a subset of the central BIM and will generally add, update or delete information objects to this sub-model. It should be completely unambiguous if a certain information object is accessible (read access) or can be updated (write access).

The Window of Authorization is able to specify the access status for all information objects of the central CBIM in a very compact way. The main principle is to mark certain nodes of the object tree with explicit access rights (write access, read access or no access) and to propagate these access rights along the tree branches and along the information objects that can be reached from there.

The Window of Authorization specification forms no part of the CBIM itself. A central BIM may have many parallel WoA's in several concurrent transactions. A WoA is therefore saved in a separate XML file and shipped in a separate folder of the COINS Container.


### WoA Specification

![Window of Authorization specification example.](./media/WoA-en.png "Window of Authorization specification example.") 

The WoA specification uses the object tree as its base structure. The procedure is to specify the access rights for a set of function fulfillers explicitly while afterwards an algorithm uses some rules to decide what the access rights will be of all the other information objects (including object instances of other classes).
A function fulfiller object may express three different access rights:

* write access
Write access means that in principle all attribute and relation types of the function fulfiller are open for updating (adding, removing, modifying). The 'in principle' addition means that certain restrictions may apply.
The function fulfiller that explicitly receives write access rights (in contrast to getting these rights as a derivation from an ancestor) are beforehand limited (limited write access) in updating its relations (especially in the same layer and above).
* read access
Read access means that in principle all attribute and relation types of the function fulfiller are open for reading (inspecting, traversing). The 'in principle' addition means that certain restrictions may apply.
The function fulfiller that explicitly receives read access rights (in contract to getting these rights as a derivation from an ancestor) are beforehand limited (limited read access) in inspecting and traversing its relations (especially in the same layer and above).
* no access
No access means that such an object can in no way be accessed. Even its very existence is hidden, which is practically achieved by leaving them out during the export procedure to a COINS Container.


The WoA specification can be serialized into an XML file. For example the WoA of the COINS BIM shown above could be expressed as follows:

<pre>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;woa:WindowOfAuthorization xmlns:woa="<a href="http://www.coinsweb.nl" class='external free' title="http://www.coinsweb.nl" rel="nofollow">http://www.coinsweb.nl</a>"
   xmlns:xsi="<a href="http://www.w3.org/2001/XMLSchema-instance" class='external free' title="http://www.w3.org/2001/XMLSchema-instance" rel="nofollow">http://www.w3.org/2001/XMLSchema-instance</a>"
   xsi:schemaLocation="nl/coinsweb/cbim/woa/WindowOfAuthorization.xsd"&gt;
   &lt;woa:WriteAccess&gt;
       &lt;woa:RootObject layerDepth="1"
           objectID="<a href="http://www.coinsweb.nl/woa-example.owl#_b6f6ac82-295e-11b2-80a1-840ad48ff048" class='external free' title="http://www.coinsweb.nl/woa-example.owl# b6f6ac82-295e-11b2-80a1-840ad48ff048" rel="nofollow">http://www.coinsweb.nl/woa-example.owl#_b6f6ac82-295e-11b2-80a1-840ad48ff048</a>"&gt;
           &lt;woa:Name&gt;B1.1&lt;/woa:Name&gt;
           &lt;woa:UserID/&gt;
           &lt;woa:LinkAccess&gt;<a href="http://www.coinsweb.nl/c-bim.owl#physicalChild" class='external free' title="http://www.coinsweb.nl/c-bim.owl#physicalChild" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#physicalChild</a>&lt;/woa:LinkAccess&gt;
       &lt;/woa:RootObject&gt;
   &lt;/woa:WriteAccess&gt;
   &lt;woa:ReadAccess&gt;
       &lt;woa:RootObject layerDepth="2"
           objectID="<a href="http://www.coinsweb.nl/woa-example.owl#_b6f6ac80-295e-11b2-80a1-840ad48ff048" class='external free' title="http://www.coinsweb.nl/woa-example.owl# b6f6ac80-295e-11b2-80a1-840ad48ff048" rel="nofollow">http://www.coinsweb.nl/woa-example.owl#_b6f6ac80-295e-11b2-80a1-840ad48ff048</a>"&gt;
           &lt;woa:Name&gt;B1&lt;/woa:Name&gt;
           &lt;woa:UserID/&gt;
       &lt;/woa:RootObject&gt;
   &lt;/woa:ReadAccess&gt;
&lt;/woa:WindowOfAuthorization&gt;
</pre>

The WoA specification may contain up to three sections: to specify the write access area, read access area and no access area respectively. In this example the no-access part is left out which means that it is implicitly defined: any object that has no write access or read access is automatically regarded to be a no-access object.

<pre>&lt;woa:WriteAccess&gt;
    &lt;woa:RootObject layerDepth="1"
        objectID="<a href="http://www.coinsweb.nl/woa-example.owl#_b6f6ac82-295e-11b2-80a1-840ad48ff048" class='external free' title="http://www.coinsweb.nl/woa-example.owl# b6f6ac82-295e-11b2-80a1-840ad48ff048" rel="nofollow">http://www.coinsweb.nl/woa-example.owl#_b6f6ac82-295e-11b2-80a1-840ad48ff048</a>"&gt;
        &lt;woa:Name&gt;B1.1&lt;/woa:Name&gt;
        &lt;woa:UserID/&gt;
        &lt;woa:LinkAccess&gt;<a href="http://www.coinsweb.nl/c-bim.owl#physicalChild" class='external free' title="http://www.coinsweb.nl/c-bim.owl#physicalChild" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#physicalChild</a>&lt;/woa:LinkAccess&gt;
    &lt;/woa:RootObject&gt;
&lt;/woa:WriteAccess&gt;
</pre>

The write access area specification mentions one function fulfiller (B1.1) as a write access area root object that extends one layer deep and thus includes its children (B1.1.1, B1.1.2, B1.1.3). The link access element specifies that only child relations of the root object are open for updating (besides the attribute values), which facilitates, in this particular case, adding or removing child objects to this root object.

<pre>&lt;woa:ReadAccess&gt;
   &lt;woa:RootObject layerDepth="2"
       objectID="<a href="http://www.coinsweb.nl/woa-example.owl#_b6f6ac80-295e-11b2-80a1-840ad48ff048" class='external free' title="http://www.coinsweb.nl/woa-example.owl# b6f6ac80-295e-11b2-80a1-840ad48ff048" rel="nofollow">http://www.coinsweb.nl/woa-example.owl#_b6f6ac80-295e-11b2-80a1-840ad48ff048</a>"&gt;
       &lt;woa:Name&gt;B1&lt;/woa:Name&gt;
       &lt;woa:UserID/&gt;
   &lt;/woa:RootObject&gt;
&lt;/woa:ReadAccess&gt;
</pre>

The read access area specification mentions one function fulfiller (B1) as a read access area root object that extends two layers deep and thus includes its children and grandchildren (B1.1, B1.2, B1.2.1). The write access area has precedence over the read access area so function fulfiller B1.1 is only upward read-only and its children are entirely not affected though they are located in the two-layer read access area.

#### Propagation rules

<p>A WoA specification only specifies access rights for a subset of the function fulfillers. A set of rules dictates how to determine the access rights of the rest of the function fulfillers and all information objects that are no function fulfillers at all.
Those rules are:
</p>
<ul><li> If a so called WoA root object (i.e. a function fulfiller that has explicitly defined access rights) has a layer depth greater than 0 descendant function fulfillers inherit the access rights of this root object.
</li><li> Within the object tree a write access area overrules a read access area and a read access area overrules a no-access area.
</li><li> Function fulfillers outside any access area belong implicitly to the no-access area.
</li><li> Other (no function fulfiller) information objects that are referenced by a function fulfiller inherit the same access rights.
</li><li> If such an information object is referenced by more than one function fulfiller the most restricted rights take precedence, i.e. a read access right takes precedence of a write access right and a no-access rights takes always precedence other access rights. There is one exception with regard to baseline objects. The reason is that baselines often will contain a mix function fulfillers (write access, read access or no-access) and would end therefore as a no-access information object itself. That would be undesirable, besides baselines have a protection mechanism of its own: a baseline can be open or closed for updating. Of course only information objects with write access can be updated in an open baseline. Normally you won't expect information objects with write access in a closed baseline. When this situation occurs the closed baseline status should take precedence.
</li><li> The previous rule can be applied recurrently between the rest of the model objects. The algorithm should take care that all function fulfillers are assigned their access rights first. Other information objects cannot overrule this status afterwards.
</li><li> Finally, all (non-function fulfiller) information objects that cannot be reached using above procedure will receive by default write-access rights.
</li></ul>


#### individual object
Besides the specification method based on object tree access individual CBIM objects can declared explicitly to reside in an authorization class. This possibility is sometimes needed to overrule the standard propagation rules or when, in an early model stage, the object tree is not available yet.

#### transaction

The WoA specification XML file should be part of a COINS container. By convention, it is stored in a folder named woa.

XML Schema
The serialization of the WoA specification is in XML format. The XML Schema is shown below:

<pre>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;xs:schema xmlns:xs="<a href="http://www.w3.org/2001/XMLSchema" class='external free' title="http://www.w3.org/2001/XMLSchema" rel="nofollow">http://www.w3.org/2001/XMLSchema</a>"
	xmlns:woa="<a href="http://www.coinsweb.nl" class='external free' title="http://www.coinsweb.nl" rel="nofollow">http://www.coinsweb.nl</a>" targetNamespace="<a href="http://www.coinsweb.nl" class='external free' title="http://www.coinsweb.nl" rel="nofollow">http://www.coinsweb.nl</a>"
	elementFormDefault="qualified" attributeFormDefault="unqualified"
	version="0.1"&gt;
	&lt;xs:element name="WindowOfAuthorization" type="woa:WindowOfAuthorizationType"&gt;
		&lt;xs:annotation&gt;
			&lt;xs:documentation&gt;Window of Authorization specifies the access rights
				of the accompanying building information model.
			&lt;/xs:documentation&gt;
		&lt;/xs:annotation&gt;
	&lt;/xs:element&gt;
	&lt;xs:complexType name="WindowOfAuthorizationType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="WriteAccess" type="woa:WriteAccessType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
			&lt;xs:element name="ReadAccess" type="woa:ReadAccessType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
			&lt;xs:element name="NoAccess" type="woa:NoAccessType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
		&lt;/xs:sequence&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:complexType name="WriteAccessType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="RootObject" type="woa:RootObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
			&lt;xs:element name="CbimObject" type="woa:CbimObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
		&lt;/xs:sequence&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:complexType name="ReadAccessType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="RootObject" type="woa:RootObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
			&lt;xs:element name="CbimObject" type="woa:CbimObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
		&lt;/xs:sequence&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:complexType name="NoAccessType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="RootObject" type="woa:RootObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
			&lt;xs:element name="CbimObject" type="woa:CbimObjectType"
				minOccurs="0" maxOccurs="unbounded" /&gt;
		&lt;/xs:sequence&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:complexType name="RootObjectType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="Name" type="xs:string" minOccurs="0"
				maxOccurs="1" /&gt;
			&lt;xs:element name="UserID" type="xs:string" minOccurs="0"
				maxOccurs="1" /&gt;
			&lt;xs:element name="LinkAccess" type="woa:PropertyType"
				minOccurs="0" maxOccurs="unbounded"
				default="<a href="http://www.coinsweb.nl/c-bim.owl#physicalChild" class='external free' title="http://www.coinsweb.nl/c-bim.owl#physicalChild" rel="nofollow">http://www.coinsweb.nl/c-bim.owl#physicalChild</a>" /&gt;
		&lt;/xs:sequence&gt;
		&lt;xs:attribute name="objectID" type="woa:ObjectIDType"
			use="required" /&gt;
		&lt;xs:attribute name="layerDepth" type="woa:LayerDepthType"
			default="1" /&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:complexType name="CbimObjectType"&gt;
		&lt;xs:sequence&gt;
			&lt;xs:element name="Name" type="xs:string" minOccurs="0"
				maxOccurs="1" /&gt;
			&lt;xs:element name="UserID" type="xs:string" minOccurs="0"
				maxOccurs="1" /&gt;
		&lt;/xs:sequence&gt;
		&lt;xs:attribute name="objectID" type="woa:ObjectIDType"
			use="required" /&gt;
	&lt;/xs:complexType&gt;
	&lt;xs:simpleType name="LayerDepthType"&gt;
		&lt;xs:restriction base="xs:integer"&gt;&lt;/xs:restriction&gt;
	&lt;/xs:simpleType&gt;
	&lt;xs:simpleType name="ObjectIDType"&gt;
		&lt;xs:restriction base="xs:anyURI" /&gt;
	&lt;/xs:simpleType&gt;
	&lt;xs:simpleType name="PropertyType"&gt;
		&lt;xs:restriction base="xs:anyURI" /&gt;
	&lt;/xs:simpleType&gt;
&lt;/xs:schema&gt;
</pre>

#### WoA Checking

There are two ways to check on violations of the WoA specification:

during the actual updating by a COINS compatible application
during a merge operation of a COINS container with the central BIM
The first option is primarily to assist the person charged to update the model. He/she will be informed immediately that a certain modification is not allowed by the prevailing WoA.
Various (configurable) implementation forms can be used. The COINS Navigator for example warns but enables the user to neglect this warning. The idea behind it is the possibility that the WoA is too restrictively defined for the job in question. Informal communication could agree about broadening the write access area.
It could of course also happen that an application add-on cannot prevent (read: has insufficient access) WoA violations. In that case a separate WoA checker could do the job.
Before the actual merge operation a final check is done. The COINS Building Information System should offer sufficient control how to deal with encountered violations.

As a rule, more than one transaction will stand out at an arbitrary point in time. The BIM manager should have an overview of all those transactions and their corresponding WoA's. In principle, write access areas should not overlap. This will prevent update clashes. The WoA specification offers fine tuning in updating the relationships giving write access for relation type A (for example updating parent/child relations) while blocking write access for relation type B (for example attaching planning objects).

#### Navigator

![Window of Authorization pop-up menu.](./media/NavigatorWoAPopupMenu.png "Window of Authorization pop-up menu.") 

A Window of Authorization can be specified using the object tree panel. Selecting a function fulfiller and right clicking shows a pop-up menu including a Window of Authorization sub-menu. The menu-items trigger the following functions:

<ul><li> <i>Add write access</i><br />Declare this object a read/write access root.
</li><li> <i>Add read access</i><br />Declare this object a read-only access root.
</li><li> <i>Add no access</i><br />Declare this object inaccessible.
</li><li> <i>Link access</i><br />Sub-menu to fine-grain the link accessibility.
</li><li> <i>Remove access</i><br />Remove the access specification.
</li><li> <i>Increase layer depth</i><br />Increase the number of downward layers this access specification can reach. Initially the number of layers is set to 0 meaning: the same layer as the function fulfiller itself.
</li><li> <i>Decrease layer depth</i><br />Inverse function of increase layer depth.
</li><li> <i>Read WoA</i><br />Import a WoA description file.
</li><li> <i>Write WoA</i><br />Export a WoA description file.
</li><li> <i>Propagate WoA</i><br />Propagate the WoA root object specifications over all the information objects of the BIM.
</li><li> <i>Reset WoA</i><br />Remove the current WoA specification.
</li></ul>

#### Colour coding

![Example colour coding in the object tree panel.](./media/NavigatorColourCoding.png "Example colour coding in the object tree panel.") 

To have a quick clue about the access status of a certain information object the COINS Navigator uses colour coding:
* Green
Full read/write access.
* Turquoise
Limited read/write access for certain link types.
* Blue
Full read-only access.
* Violet
Limited read access for certain link types.
* Red
No access.


The red colour code (no access rights) can only be observed in a CBIS environment. During the generation of a COINS Container the no-access information objects are simply skipped.


#### Violation messages


![Window of Authorization violation warning.](./media/NavigatorWoAWarning.png "Window of Authorization violation warning.") 


The COINS Navigator actively checks all changes to a CBIM object. If a violation is detected a warning message is issued.
The COINS Navigator offers the option to ignore the WoA specification. The reason is that during the execution of the assignment it may turn out that the WoA was defined to restrictively. In that case it could be very cumbersome to generate a new COINS Container and restart the transaction. Then it could be handy to circumvent the authorization. Still there is a final check during the merge operation with the central BIM. At that point in the transaction this violation will be detected and must be approved or rejected.







