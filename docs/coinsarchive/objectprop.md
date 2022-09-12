# Object Properties


## Cbim:Affects

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain task transforms the range function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** 	
cbim:isAffectedBy



## Cbim:AmountPropertyType

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** Range property type that is used to specify the quantity of the domain catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CataloguePart

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** 	cbim:PropertyType



## Cbim:Baseline

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range baseline that owns the domain object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Baseline


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** cbim:baselineObject



## Cbim:BaselineObject

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain baseline that owns the range object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Baseline


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CbimObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** cbim:baseline



## Cbim:CataloguePart

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain amount quantity that is typed by the range catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:Amount


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CataloguePart


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:propertyType


## Cbim:Child

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range child function fulfiller of the domain parent function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)** cbim:FunctionFulfiller


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:FunctionFulfiller


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:parent	



## Cbim:Contains

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range amount quantity owned by the domain physical object or catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:CataloguePart or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Amount


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)** cbim:propertyValue


## Cbim:Creator

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range person or organisation is creator of the domain object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation 


## Cbim:CurrentState

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range state is the current state of the domain function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:State



## Cbim:Document

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain object references the range document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty) 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** 	cbim:Document



## Cbim:DocumentURI

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The URI of the document or identifiable object inside the document. 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)** cbim:Document	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** [rdfs:Resource](http://www.w3.org/2001/01/rdf-schema#Resource)




## Cbim:FemaleTerminal

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain connection attaches the range female terminal.

**[rdfs:seeAlso](http://www.w3.org/2000/01/rdf-schema#seeAlso)** Toplological relations, systems engineering layering

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Connection

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Terminal



## Cbim:FirstParameter

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain explicit 3D representation points to the range parameter as first parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Explicit3DRepresentation

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Parameter



## Cbim:Fulfills

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain function fulfiller fulfills the range function.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Function

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:isFulfilledBy



## Cbim:IsAffectedBy

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain function fulfiller or state is transformed by the range task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**  cbim:FunctionFulfiller or cbim:State

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**   cbim:Task

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:affects



## Cbim:IsFulfilledBy

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain function is fulfilled by the range function fulfiller.
 
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Function


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:fulfills



## Cbim:IsSituatedIn

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain physical object is situated in the range space.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Space


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:situates


## Cbim:Locator

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain amount, function fulfiller or terminal specify a range locator as subreference frame.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**    [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:Amount or cbim:FunctionFulfiller or cbim:Terminal


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Locator



## Cbim:MaleTerminal

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain connection attaches the range male terminal.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**     [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Connection


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Terminal

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:max bounding box

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain locator specifies the range vector as maximum corner location.

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   	  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  cbim:Locator

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector


## Cbim:MinBoundingBox

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain locator specifies the range vector as minimum corner location.


**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   	  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  cbim:Locator

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector

## Cbim:mMdifier

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range person or organisation is modifier of the domain object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:Object

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation



## Cbim:NextParameter

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain parameter points to the range parameter as next parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Parameter


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Parameter



## Cbim:NextVersion

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain C-BIM object points to the range C-BIM object as its next version.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  Cbim:CbimObject



## Cbim:Parent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range parent function fulfiller of the domain child function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:child



## Cbim:Performance

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range performance that characterizes the domain function fulfiller or state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Performance


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:performanceOf


## Cbim:PerformanceOf

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range function fulfiller or state that is characterized by the domain performance.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Performance


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller or cbim:State

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:performance



## Cbim:PhysicalChild

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range child physical object of the domain parent physical object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PhysicalObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:physicalParent


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:child


## Cbim:PhysicalParent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range parent physical object of the domain child physical object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PhysicalObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:physicalChild


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:parent


## Cbim:PreviousState

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range state is the previous state of the domain state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:State

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:State


## Cbim:PrimaryOrientation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range vector that specifies the primary orientation of the domain locator.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 	cbim:Locator


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Vector



## Cbim:PropertyType

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range type of the domain property value.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PropertyValue


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:PropertyType



## Cbim:PropertyValue

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range property value owned by the domain amount or catalogue part or parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Amount or cbim:CataloguePart or cbim:Parameter


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PropertyValue



## Cbim:Requirement

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range requirement that characterizes the domain function.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Function

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Requirement

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:requirementOf


## Cbim:RequirementOf

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range function that is characterized by the domain requirement.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Requirement

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Function

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:requirementOf

## Cbim:SecondaryOrientation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range vector that specifies the secondary orientation of the domain locator.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Locator

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Vector

## Cbim:Shape

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range explicit 3D representation that specifies the 3D shape of the domain function fulfiller or terminal or catalog part or state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:Terminal or cbim:CataloguePart or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Explicit3DRepresentation



## Cbim:Situates

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain space situates the range physical object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Space


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PhysicalObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:IsSituatedIn


## Cbim:SpatialChild

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range child space of the domain parent space.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Space

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	cbim:Space

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:spatialParent

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:child

## Cbim:SpatialParent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range parent space of the domain child space.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Space

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	cbim:Space

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:spatialChild

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:parent

## Cbim:StateOf

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range function fulfiller is the container of the domain state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:State

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller


## Cbim:Supertype

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range catalogue part is the supertype of the domain catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CataloguePart

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:CataloguePart



## Cbim:TaskType

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range task type is the type of the domain task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Task


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:TaskType



## Cbim:Terminal

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range terminal that is attached to the domain function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:FunctionFulfiller

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Terminal

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:terminalOf



## Cbim:TerminalOf

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range function fulfiller that is attached by the domain terminal.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Terminal

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller  

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:terminal

## Cbim:Translation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range vector that specifies the translation of the domain locator.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Locator

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Vector



## Cbim:ValueDomain

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The value domain of the property type.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:PropertyType

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:ValueDomain


## Cbim:ValueDomainResource

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The value domain resource of the value domain.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:ValueDomain

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  rdfs:Resource


## Cbim:VerificationFunctionFulfiller

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range function fulfiller that identifies the domain verification.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**    [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Verification

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller


## Cbim:VerificationPerformer

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range person or organisation that performs the domain verification.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Verification

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation

## Cbim:VerificationRequirement

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range requirement that identifies the domain verification.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Verification

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Requirement