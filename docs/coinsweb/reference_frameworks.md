# Reference Frameworks

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

<pre>&lt;rdf:RDF

  &lt;rdf:Description rdf:about=""&gt;
    &lt;rdf:type rdf:resource="owl:Ontology"/&gt;
    &lt;owl:imports rdf:resource="<a rel="nofollow" class="external free" href="http://www.coinsweb.nl/units-2.0.rdf">http://www.coinsweb.nl/units-2.0.rdf</a>"/&gt;
    &lt;owl:imports rdf:resource="<a rel="nofollow" class="external free" href="http://www.coinsweb.nl/COINSWOA.rdf">http://www.coinsweb.nl/COINSWOA.rdf</a>"/&gt;
  &lt;/rdf:Description&gt;

&lt;/rdf:RDF&gt;
</pre>


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


# COINS Navigator

The **Coins Navigator** tool shows the concepts of COINS in an application.

At this moment the Coins Navigator is developed on base of Coins 2.0.


**WARNING**: The objective of the COINS Navigator is aimed primarily as a demonstration tool. As a result it performs well with small containers, however, because its architecture as an in-memory application, its use for importing large containers is strongly discouraged. This typically includes all containers that import the Rijkswaterstaat object type library. As a rule of thumb the performance is acceptable for containers with roughly max. 10,000 COINS entity instances, though it may be necessary to increase the heap size of the involved Java runtime engine.

The COINS Navigator 2 can be downloaded from the [Github repository](https://github.com/bimloket/COINS_2.0)


## Installation

The COINS Navigator is a Java desktop application and needs a [Java](https://www.java.com/nl/) runtime environment (JRE), which may already be available on your platform (Java version 8+).
Unzip the download file into a folder where you have write permission.
Double click the Java archive (.jar) file.
For a quick start use the following tutorial based on the COINS 2.0 Starter kit. Coins Navigator 2 Starter Kit

### Create Organization (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Open a new container form.

![Open a new container form.](./media/CN2-OpenNewContainerForm.png "Open a new container form.")

* Give the model a name (no spaces).

![Create a new model.](./media/600px-CN2-CreateNewModel.png "Create a new model.")


* Open a new object form.
![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")


![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Make a choice between a guaranteed unique ID.

![GUID-form ID.](./media/CN2-ObjectIdentification.png "GUID-form ID.")

* or a readable ID.

![Readable ID.](./media/CN2-ObjectIdentification2.png "Readable ID.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType.png "Select the static type.")


* Give the organisation a name.

![Give the organisation a name.](./media/CN2-DescriptionName.png "Give the organisation a name.")

* Click the create entity button.

![Location of the create entity button.](./media/CN2-NewObjectCreationButton.png "Location of the create entity button.")

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* And the new organisation is added.

![New organisation represented as tree node.](./media/CN2-NewOrganisationTreeNode.png "New organisation represented as tree node.")

![New organisation represented as node on the canvas.](./media/CN2-OrganisationNode.png "New organisation represented as node on the canvas.")

* Save the model in a container.

![Coins container.](./media/CN2-SaveContainer.png "Coins container.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")
Result container


### Create Person (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Open a new container form.

![Open a new container form.](./media/CN2-OpenNewContainerForm.png "Open a new container form.")

Open a new container form.

* Give the model a name (no spaces).

![Create a new model.](./media/600px-CN2-CreateNewModel.png "Create a new model.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Make a choice between a guaranteed unique ID.

![GUID-form ID.](./media/CN2-ObjectIdentification.png "GUID-form ID.")

* or a readable ID.

![Readable ID.](./media/CN2-ObjectIdentification2.png "Readable ID.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType2.png "Select the static type.")

* Give the person a name.

![Give the person a name.](./media/CN2-DescriptionName2.png "Give the person a name.")

* Click the create entity button.

![Location of the create entity button.](./media/CN2-NewObjectCreationButton.png "Location of the create entity button.")


![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* And the new person is added.

![New person represented as tree node.](./media/CN2-NewPersonTreeNode.png "New person represented as tree node.")


![New person represented as node on the canvas.](./media/CN2-MijnNaam-PersonNode.png "New person represented as node on the canvas.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")

Result container


### Increment version (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Select the person object of the previous tutorial.

![New person represented as tree node.](./media/CN2-NewPersonTreeNode.png "New person represented as tree node.")

* Check expired under the "Object"-tab section "Identification".

![Check expired.](./media/600px-CN2-ExpiredCheckBox.png "Check expired.")

* Create a next version object.

![Click next version button.](./media/CN2-NextVersionButton.png "Click next version button.")

* Make a change to the object's name.

![Make a change to the object's name.](./media/CN2-DescriptionName3.png "Make a change to the object's name.")

* A new version object node is added.

![New person version represented as tree node.](./media/CN2-NewPersonTreeNode2.png "New person version represented as tree node.")

* The previous version points to the next version.

![Previous version points to the next version.](./media/CN2-NextVersionLink.png "Previous version points to the next version.")

![Previous version points to the next version.](./media/CN2-MijnNaam(expired)-PersonNode.png "Previous version points to the next version.")

* The new version has incremented the version ID.

![Incremented version ID.](./media/CN2-MijnNaam(expired)-PersonNode.png "Incremented version ID.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create StringProperty (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType3.png "Select the static type.")

* Give the string property a name.

![Give the organisation a name.](./media/CN2-DescriptionName4.png "Give the organisation a name.")

* Click the create entity button.

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* Open tab "Properties" section "Static properties/Entity property/Datatype value" and click the "Change"-button.

![Click change button.](./media/600px-CN2-StringPropertyValue1.png "Click change button.")


* Enter the string value.

![Click change button.](./media/600px-CN2-StringPropertyValue2.png "Click change button.")

![String property node on the canvas](./media/CN2-StringPropertyNode.png "String property node on the canvas")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create BooleanProperty (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType4.png "Select the static type.")

* Give the string property a name.

![Give the organisation a name.](./media/600px-CN2-DescriptionName5.png "Give the organisation a name.")

* Click the create entity button.

![Create entity button](./media/CN2-NewObjectCreationButton2.png "Create entity button")

* Open tab "Properties" section "Static properties/Entity property/Datatype value" and click the "Change"-button.

![Click change button.](./media/600px-CN2-BooleanPropertyValue1.png "Click change button.")

* Enter the booleanvalue and click the "Done"-button.

![Click change button.](./media/CN2-BooleanPropertyValue2.png "Click change button.")

![BooleanProperty Node on the canvas.](./media/CN2-BooleanPropertyNode.png "BooleanProperty Node on the canvas.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create DateTimeProperty (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType5.png "Select the static type.")

* Give the date time property a name.

![Give the organisation a name.](./media/600px-CN2-DescriptionName6.png "Give the organisation a name.")


* Click the create entity button.

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")


* Open tab "Properties" section "Static properties/Entity property/Datatype value" and click the "Change"-button.

![Click change button.](./media/600px-CN2-DateTimePropertyValue1.png "Click change button.")


* Enter the date time value and click the "Done"-button.

![Click change button.](./media/CN2-DateTimePropertyValue2.png "Click change button.")

![DateTimeProperty on the canvas.](./media/CN2-DateTimePropertyNode.png "DateTimeProperty on the canvas.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create IntegerProperty (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType6.png "Select the static type.")

* Give the integer property a name.

![Give the organisation a name.](./media/CN2-DescriptionName7.png "Give the organisation a name.")

* Click the create entity button.

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* Open tab "Properties" section "Static properties/Entity property/Datatype value" and enter the integer value.

![Click change button.](./media/600px-CN2-IntegerPropertyValue.png "Click change button.")

![IntegerProperty on the canvas.](./media/CN2-IntegerPropertyNode.png "IntegerProperty on the canvas.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create FloatProperty (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType7.png "Select the static type.")

* Give the integer property a name.

![Give the organisation a name.](./media/CN2-DescriptionName8.png "Give the organisation a name.")

* Click the create entity button.

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* Open tab "Properties" section "Static properties/Entity property/Datatype value" and enter the integer value.

![Click change button.](./media/600px-CN2-FloatPropertyValue.png "Click change button.")

![IntegerProperty on the canvas.](./media/CN2-FloatPropertyNode.png "IntegerProperty on the canvas.")

Optionally, a unit can be specified.

![Unit combo box.](./media/CN2-FloatPropertyUnit.png "Unit combo box.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Create InternalDocumentReference (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

* ... or open a model in an existing container.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Open a new object form.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

* Select the static type.

![Select the static type.](./media/CN2-SelectStaticType8.png "Select the static type.")

* Give the document reference a name.
![Give the organisation a name.](./media/CN2-DescriptionName9.png "Give the organisation a name.")

* Click the create entity button.

![Create entity button.](./media/CN2-NewObjectCreationButton2.png "Create entity button.")

* Open tab "Properties" section "Static properties/Document Reference" and upload the local file.

![Click change button.](./media/600px-CN2-DocumentReference.png "Click change button.")

* After successful uploading most of the document reference properties are filled in.

![Document reference properties.](./media/600px-CN2-DocumentReferenceProperties.png "Document reference properties.")

![Internal document reference node on the canvas.](./media/CN2-InternalDocumentReferenceNode.png "Internal document reference node on the canvas.")


* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Relate Person to InternalDocumentReference (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Open the previous model.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Select the "Object"-tab/"Governance"-section and select a creator party.

Creator relation on the canvas.

![Open an existing container.](./media/600px-CN2-SelectCreatorParty.png "Open an existing container.")

![Creator relation on the canvas.](./media/CN2-CreatorNode.png "Creator relation on the canvas.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")



### Relate to CataloguePart

**Create a new library.**

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")


* Open a new container form to create a library.

![Open a new container form.](./media/CN2-OpenNewContainerForm.png "Open a new container form.")

* Give the library a name (no spaces).
* ![Create a new library.](./media/600px-CN2-CreateNewLibrary.png "Create a new library.")


* Select the "Classes"-tab, find and select the COINS Object class, right click and select the "Create"-menu item.

![Create a new subclass.](./media/CN2-CreateSubclass.png "Create a new subclass.")

* Select the "Identification"-section, toggle the "GUID"-button to enable the specification of a readable class ID.

![Specify "Column" as the class local ID.](./media/CN2-ClassIdentification.png "Specify "Column" as the class local ID.")


* Select the "Super types"-section and make sure that the "Catalogue Part"-check box is selected.

![Select "Catalogue Part" as a role type.](./media/CN2-ClassSuperTypes.png "Select "Catalogue Part" as a role type.")

* Select the "Description"-section and enter a user friendly name for the class.

![Enter a class name.](./media/CN2-DescriptionName10.png "Enter a class name.")

* Click the "Create"-button...

![Create button.](./media/CN2-CreateButton.png "Create button.")

... and the new subclass is added to the class tree.
![New subclass added to the class tree.](./media/CN2-NewSubclassTreeNode.png "New subclass added to the class tree.")


* Save the library in a container.

![Save the library in a container.](./media/CN2-SaveContainer.png "Save the library in a container.")

![Container file.](./media/CN2-LibraryFile.png "Container file.")


**Create Instance model**

* Create a new model.

![Open a new container form.](./media/CN2-OpenNewContainerForm.png "Open a new container form.")

* Give the model a name (no spaces).

![Specify model name.](./media/CN2-CreateNewModel2.png "Specify model name.")


* Select the "Container"-tab/"Models"-tab and click the "Add"-button to import the "Library"-model.

![Add library model.](./media/CN2-AddContainerModel.png "Add library model.")

* Select the "Objects"-tab and open the create new object form. Select the "Types"-section and add "MyLibrary:Column" as a dynamic type:

![Select dynamic type.](./media/CN2-AddDynamicType1.png "Select dynamic type.")

![Click Add dynamic type](./media/CN2-AddDynamicType2.png "Click Add dynamic type")

![Dynamic type added.](./media/CN2-AddDynamicType3.png "Dynamic type added.")


* Give the object a name and click the "Create"-button.

![Object name.](./media/CN2-DescriptionName11.png "Object name.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

* The dynamically typed object is added to the model.

![Column object added.](./media/CN2-ColumnObjectTreeNode.png "Column object added.")

![Canvas with Column object added.](./media/CN2-ColumnObjectCanvas.png "Canvas with Column object added.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Example: A very simple case

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

* Start a new model ...

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

**Create Bench**

* Open a new object form, select the static type, give it a name and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-DescriptionName12.png "Select the static type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

![Bench object added to the model.](./media/CN2-ZitbankObjectTreeNode.png "Bench object added to the model.")

**Create Platform (dutch: "perron")
* Open a new object form, select the static type, give it a name and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-DescriptionName13.png "Select the static type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

![Bench object added to the model.](./media/CN2-PerronObjectTreeNode.png "Bench object added to the model.")

**Create connection**

* Open a new object form, select the static type, give it a name and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-SelectStaticType10.png "Select the static type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

![Give the object a name.](./media/.png "Give the object a name.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

![Connection added to the model.](./media/CN2-ConnectionTreeNode.png "Connection added to the model.")

* Select "Properties"-tab/"Static Properties"-section/"Connection"-section and select the connected objects.

![Connect to the connecting objects.](./media/CN2-ConnectionProperties.png "Connect to the connecting objects.")

![Connection on the canvas.](./media/CN2-ConnectionNode.png "Connection on the canvas.")

**New connection version**

* Select the Connection object and then select the "Object"-tab/"Identification"-section. Select the "Expired"-check box and click then the "Next version"-button.

![Expired check box.](./media/CN2-ExpiredCheckBox2.png "Expired check box.")

![Clone new version button.](./media/CN2-NextVersionButton.png "Clone new version button.")

![](./media/.png "")
New connection version added to the model.

* Select the new Connection version.

![Select new Connection version.](./media/CN2-ConnectionTreeNode2.png "Select new Connection version.")

* Make a change to the name.

![](./media/.png "")
Make a change to the name.

* Select the expired version.

![Select the expired version.](./media/CN2-ConnectionTreeNode3.png "Select the expired version.")

* The expired version points to the next version.

![Select the expired version.](./media/600px-CN2-NextVersion2.png "Select the expired version.")

![Canvas presentation.](./media/CN2-ConnectionNode2.png "Canvas presentation.")

**Decomposition**

* Select the "Zitbank" tree node and select under Object/Types the Assembly role type.

![Select the bench object.](./media/ZitbankObjectTreeNode2.png "Select the bench object.")

![Select the Assembly role type.](./media/AssemblyCheckBox.png "Select the Assembly role type.")

**Create support left (Steun links)**

* Open a new object form, select the static type, give it a name, check the "Part"-role type and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-SelectStaticType9.png "Select the static type.")

![Give the object a name.](./media/CN2-DescriptionName16.png "Give the object a name.")

![Select Part role type.](./media/PartCheckBox.png "Select Part role type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

**Create support right (Steun rechts)**

* Open a new object form, select the static type, give it a name, check the "Part"-role type and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-SelectStaticType9.png "Select the static type.")

![Give the object a name.](./media/CN2-DescriptionName17.png "Give the object a name.")

![Select Part role type.](./media/PartCheckBox.png "Select Part role type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

**Create beam (Ligger)**

Open a new object form, select the static type, give it a name, check the "Part"-role type and click the "Create"-button.

![Create a new object.](./media/CN2-CreateObjectButtonLocation.png "Create a new object.")

![Open a new object form.](./media/CN2-OpenNewObjectForm.png "Open a new object form.")

![Select the static type.](./media/CN2-SelectStaticType9.png "Select the static type.")

![Give the object a name.](./media/CN2-DescriptionName18.png "Give the object a name.")

![Select Part role type.](./media/PartCheckBox.png "Select Part role type.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

**Connect**

* Select the "Zitbank" object

![Select the bench object.](./media/CN2-ZitbankObjectTreeNode3.png "Select the bench object.")

* Select and add the three subpart objects.

![Add subpart.](./media/CN2-AddSubpart1.png "Add subpart.")

![Add subpart.](./media/CN2-AddSubpart2.png "Add subpart.")

![Add subpart.](./media/CN2-AddSubpart3.png "Add subpart.")

![Bench decomposition.](./media/CN2-ZitbankDecomposition.png "Bench decomposition.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


### Type column and property in library

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.png "Start the COINS Navigator 2 application.")

**Edit the previous created MyLibrary model**

* Open the previous created "MyLibrary" model.

![Open an existing container.](./media/CN2-OpenContainer.png "Open an existing container.")

* Select the "Properties"-tab and next the "hasProperties" property.

![Select the "hasProperties" property.](./media/CN2-PropertiesTab.png "Select the "hasProperties" property.")

* Open the create subproperty form.

![Open the create subproperty form.](./media/CN2-OpenNewObjectForm.png "Open the create subproperty form.")

* Give the new property an identification.

![Open the create subproperty form.](./media/CN2-PropertyIdentification.png "Open the create subproperty form.")


* Restrict the domain specification to "Column".

![Specify the property domain.](./media/CN2-PropertyDomain.png "Specify the property domain.")

* Restrict the range specification to "FloatProperty".

![Specify the property domain.](./media/Specify the property domain..png "Specify the property domain.")

* Give the property a name and click the create button.

![Specify the property name.](./media/CN2-DescriptionName19.png "Specify the property name.")

![Create the property.](./media/CN2-CreateButton.png "Create the property.")

* Select the "Classes"-tab and next the "Column"-class.

![Select the Column class.](./media/CN2-ColumnClassTreeNode.png "Select the Column class.")

* Select the "Restrictions"-tab and then click the create restriction button.

![Select the Restrictions tab.](./media/CN2-ClassRestrictionsTab.png "Select the Restrictions tab.")

![Create restriction button.](./media/CN2-CreateClassRestrictionButton.png "Create restriction button.")

* Select the "hasHeight"-property.

![Select restriction property.](./media/CN2-CreateClassRestrictionProperty.png "Select restriction property.")

* Select "Cardinality" as restriction type, specify its value and click the create button.

!Select restriction type.[](./media/CN2-CreateClassRestrictionType.png "Select restriction type.")

![Specify restriction value.](./media/CN2-CreateClassRestrictionValue.png "Specify restriction value.")

![Create button.](./media/CN2-CreateButton.png "Create button.")

![Class property restriction.](./media/CN2-ClassRestriction.png "Class property restriction.")

* Save the library in a container.

![Save the library in a container.](./media/CN2-SaveContainer.png "Save the library in a container.")


**Create an instance model that uses the libary**

* Create a new model and give it a name.

![Create a new model.](./media/CN2-OpenNewContainerForm.png "Create a new model.")

![Create a new model.](./media/CN2-CreateNewModel2.png "Create a new model.")

* Add the library as an imported model.

![Import the library.](./media/CN2-AddContainerModel.png "Import the library.")

* Create a float property, next give it a name and a value.

![Select static type float property.](./media/CN2-SelectStaticType7.png "Select static type float property.")

![Static float property name.](./media/CN2-DescriptionName20.png "Static float property name.")

![Static float property value.](./media/CN2-FloatPropertyValue2.png "Static float property value.")

* Create an object with static type "Object" and dynamic type "Column".

![Static type "Object" with dynamic type "Column".](./media/CN2-AddDynamicType3.png "Static type "Object" with dynamic type "Column".")

* Select the "Properties"-tab/"Dynamic properties"-section and select the float property as the value of the "column height"-property.

![Dynamic properties.](./media/600px-CN2-DynamicProperties.png "Dynamic properties.")

![Dynamic property value.](./media/CN2-DynamicPropertyValue.png "Dynamic property value.")

![Canvas presentation.](./media/CN2-LibColumnHeight.png "Canvas presentation.")

* Ready.

![Ready.](./media/CN2-End.png "Ready.")


# Window of Authorization framework


## Intorduction

The Window of Authorization is a standard Reference Framework of Coins for defining permissions to read, write or restrict access to information supplied in the information model. The framework contains classes which specify the permissions for accessing members of the Coins 2.0 Object class. These permissions are subclasses of the ObjectPermissions class.
Permissions are:

NoAcces; members of this class can not be accessed (neither for reading nor for writing)
ReadAccess; members of this class can be accessed for reading but not for writing)
WriteAccess; members of this class can be accessed for reading and writing.
This figure gives an illustrative representation of how implementation of the Window of Authorszation reflects in a Building Information Model: - the red elements are not visible because they are typed as NotAccess - the blue elements are visible, but not editable (ReadAccess) - the green elements are visible and editable (WriteAccess)

Permissions for a member of the Coins 2.0 Object class are set by typing it also as a member of the applicable Permission class. This Permission class is available in this Reference Framework.

The ObjectPermission class has two additional attributes:

layerDepth; property for defining the number of levels the permission is valid (following the linkAccess properties)
linkAccess; defines the objecttype property to use for determining the layer depth.
The Window of Authorization file is called COINSWOA.rdf.

![Acces Permissions](./media/WoA.png "Acces permissions"]

## Details


**Informative representation of WoA in UML**

This image shows an informative representation of the Window of Authorization classes in UML.

![Informative representation of WoA in UML](./media/WoA_-_UML.png "Informative representation of WoA in UML")

### PermissionClass

PermissionClass is a subclass of owl:Thing. It serves as superclass for all permission classes. The Permission class has no further attributes.

**Formal Representation in RDF/XML**

<pre> &lt;owl:Class rdf:ID="PermissionClass"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;PermissionClass&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;Specifies the modification rights for this object&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="owl:Thing"/&gt;

   &lt;rdf:type rdf:resource="cbim-2.0.rdf#COINSClass"/&gt;

 &lt;/owl:Class&gt;
</pre>


### ObjectPermissions

ObjectPermissions is a subclass of PermissionClass. It serves as superclass for all permissions pertaining to members of Cbim-2.0:Object. The ObjectPermissions class has a property for the layerDepth, defining the number of levels the permission is valid, following the object defined in the linkAccess property.


**Attributes**
| Name | Type | Description |
| :--- | :--- | :--- |
| layerDepth | xsd:integer | number of levels the permission is valid | 
| linkAccess | ObjectProperty | the property path to folow for determining the layer depth | 

**Formal Representation in RDF/XML**

<pre> &lt;cbim-2.0:COINSClass rdf:ID="ObjectPermissions"&gt;
 
   &lt;rdfs:label xml:lang="en-GB"&gt;ObjectPermission&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;Specifies the rights for this Object&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#PermissionClass"/&gt;
   &lt;rdfs:subClassOf rdf:resource="cbim-2.0.rdf#Object"/&gt;

   &lt;rdfs:subClassOf&gt;
     &lt;owl:Restriction&gt;
       &lt;owl:onProperty rdf:resource="#layerdepth"/&gt;
       &lt;owl:cardinality rdf:datatype="xml:nonNegativeInteger"&gt;1&lt;/owl:cardinality&gt;
     &lt;/owl:Restriction&gt;
   &lt;/rdfs:subClassOf&gt;
 
   &lt;rdfs:subClassOf&gt;
     &lt;owl:Restriction&gt;
       &lt;owl:onProperty rdf:resource="#linkAccess"/&gt;
       &lt;owl:cardinality rdf:datatype="xml:nonNegativeInteger"&gt;1&lt;/owl:cardinality&gt;
     &lt;/owl:Restriction&gt;
   &lt;/rdfs:subClassOf&gt;
   &lt;rdf:type rdf:resource="owl:Class"/&gt;

 &lt;/cbim-2.0:COINSClass&gt;

</pre>

<p><br /> 
</p>
<pre> &lt;owl:DatatypeProperty rdf:ID="layerdepth"&gt;
   &lt;rdfs:label xml:lang="en-GB"&gt;layerdepth&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;determines the layerdepth via the linkAccess relation on which this permission applies&lt;/rdfs:comment&gt;
   &lt;rdf:type rdf:resource="owl:FunctionalProperty"/&gt;
   &lt;rdfs:domain rdf:resource="#ObjectPermissions"/&gt;
   &lt;rdfs:range rdf:resource="xsd:integer"/&gt;
 &lt;/owl:DatatypeProperty&gt;

</pre>
<p><br /> 
</p>
<pre> &lt;owl:ObjectProperty rdf:ID="linkAccess"&gt;
   &lt;rdfs:label xml:lang="en-GB"&gt;linkAccess&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;specifies the objecttype property used by the layerdepth&lt;/rdfs:comment&gt;
   &lt;rdf:type rdf:resource="owl:FunctionalProperty"/&gt;
   &lt;rdfs:domain rdf:resource="#ObjectPermissions"/&gt;
   &lt;rdfs:range rdf:resource="owl:ObjectProperty"/&gt;
 &lt;/owl:ObjectProperty&gt;
</pre>

### NoAccess
NoAccess is a subclass of ObjectPermissions. Members of this class may not be accessed, nor for reading neither for writing.

**Formal Representation in RDF/XML**

<pre> &lt;cbim-2.0:COINSClass rdf:ID="NoAccess"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;NoAccess&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;No Access for this Object&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#ObjectPermissions"/&gt;

   &lt;rdf:type rdf:resource="owl:Class"/&gt;

 &lt;/cbim-2.0:COINSClass&gt;
</pre>


### ReadAcces

ReadAccess is a subclass of ObjectPermissions. Members of this class may be accessed for display (reading) but not for modifying (writing).


**Formal Representation in RDF/XML**

<pre> &lt;cbim-2.0:COINSClass rdf:ID="ReadAccess"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;ReadAccess&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;ReadAccess for this Object&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#ObjectPermissions"/&gt;

   &lt;rdf:type rdf:resource="owl:Class"/&gt;

 &lt;/cbim-2.0:COINSClass&gt;
</pre>

### WriteAccess

WriteAccess is a subclass of ObjectPermissions. Members of this class may be accessed for display (reading) and for modifying (writing).

**Formal Representation in RDF/XML**

<pre> &lt;cbim-2.0:COINSClass rdf:ID="WriteAccess"&gt;

   &lt;rdfs:label xml:lang="en-GB"&gt;WriteAccess&lt;/rdfs:label&gt;
   &lt;rdfs:comment xml:lang="en-GB"&gt;Writeaccess for this Object&lt;/rdfs:comment&gt;

   &lt;rdfs:subClassOf rdf:resource="#ObjectPermissions"/&gt;

   &lt;rdf:type rdf:resource="owl:Class"/&gt;

 &lt;/cbim-2.0:COINSClass&gt;
</pre>



## Example


This figure shows an element, typed as a Cbim-2.0:Object with ReadAccess.
Since the properties for layerDepth and linkAccess (inherited from the ObjectPermission class) are set, the permission applies to 3 levels following ContainsRelation.

![WoA Example](./media/WoA_-_Example.png "Example of WoA")
