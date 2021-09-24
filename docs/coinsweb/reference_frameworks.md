# <a>Reference Frameworks</a> 

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

<code><rdf:RDF

  <rdf:Description rdf:about="">
    <rdf:type rdf:resource="owl:Ontology"/>
    <owl:imports rdf:resource="http://www.coinsweb.nl/units-2.0.rdf"/>
    <owl:imports rdf:resource="http://www.coinsweb.nl/COINSWOA.rdf"/>
  </rdf:Description>

</rdf:RDF>


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


<WARNING: The objective of the COINS Navigator is aimed primarily as a demonstration tool. As a result it performs well with small containers, however, because its architecture as an in-memory application, its use for importing large containers is strongly discouraged. This typically includes all containers that import the Rijkswaterstaat object type library. As a rule of thumb the performance is acceptable for containers with roughly max. 10,000 COINS entity instances, though it may be necessary to increase the heap size of the involved Java runtime engine.>


The COINS Navigator 2 can be downloaded from the [Github repository](https://github.com/bimloket/COINS_2.0)

## Installation
The COINS Navigator is a Java desktop application and needs a [Java](https://www.java.com/nl/) runtime environment (JRE), which may already be available on your platform (Java version 8+).
Unzip the download file into a folder where you have write permission.
Double click the Java archive (.jar) file.
For a quick start use the following tutorial based on the COINS 2.0 Starter kit. Coins Navigator 2 Starter Kit

### Create Organization (instance)

* Start the COINS Navigator 2 application.

![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

* Open a new container form.
![Open a new container form.](./media/CN2-OpenNewContainerForm.PNG "Open a new container form.")

* Give the model a name (no spaces).
![Create a new model.](./media/600px-CN2-CreateNewModel.png "Create a new model.")
Create a new model.

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")
* Open a new container form.
![Open a new container form.](./media/CN2-OpenNewContainerForm.PNG "Open a new container form.")
Open a new container form.
* Give the model a name (no spaces).
![Create a new model.](./media/600px-CN2-CreateNewModel.png "Create a new model.")
Create a new model.

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")
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
Result container


### Create StringProperty (instance)
* Start the COINS Navigator 2 application.
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![Start the COINS Navigator 2 application.](./media/CN2-Start.PNG "Start the COINS Navigator 2 application.")

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
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")

### Relate Person to InternalDocumentReference (instance)
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")

### Relate to CataloguePart
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")

### Example: A very simple case
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")

### Type column and property in library
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")
![](./media/.png "")

