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



## Cbim:baseline object

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain baseline that owns the range object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Baseline


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CbimObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** cbim:baseline



## Cbim:catalogue part

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain amount quantity that is typed by the range catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:Amount


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CataloguePart


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:propertyType


## Cbim:child

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range child function fulfiller of the domain parent function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)** cbim:FunctionFulfiller


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:FunctionFulfiller


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:parent	



## Cbim:contains

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range amount quantity owned by the domain physical object or catalogue part.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:CataloguePart or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Amount


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)** cbim:propertyValue


## Cbim:creator

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range person or organisation is creator of the domain object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation 


## Cbim:current state

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range state is the current state of the domain function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:State



## Cbim:document

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain object references the range document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty) 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** 	cbim:Document



## Cbim:document URI

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The URI of the document or identifiable object inside the document. 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)** cbim:Document	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** [rdfs:Resource](http://www.w3.org/2001/01/rdf-schema#Resource)




## Cbim:female terminal

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain connection attaches the range female terminal.

**[rdfs:seeAlso](http://www.w3.org/2000/01/rdf-schema#seeAlso)** Toplological relations, systems engineering layering

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Connection

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Terminal



## Cbim:first parameter

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain explicit 3D representation points to the range parameter as first parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Explicit3DRepresentation

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Parameter



## Cbim:fulfills

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain function fulfiller fulfills the range function.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Function

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:isFulfilledBy



## Cbim:is affected by

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain function fulfiller or state is transformed by the range task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**  cbim:FunctionFulfiller or cbim:State

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**   cbim:Task

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:affects



## Cbim:is fulfilled by

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The domain function is fulfilled by the range function fulfiller.
 
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Function


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:fulfills



## Cbim:is situated in

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain physical object is situated in the range space.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Space


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:situates


## Cbim:locator

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain amount, function fulfiller or terminal specify a range locator as subreference frame.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**    [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:Amount or cbim:FunctionFulfiller or cbim:Terminal


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Locator



## Cbim:male terminal

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


## Cbim:min bounding box

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain locator specifies the range vector as minimum corner location.


**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   	  [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)


**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  cbim:Locator

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector

## Cbim:modifier

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The range person or organisation is modifier of the domain object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**   [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:Object

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation



## Cbim:next parameter

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The domain parameter points to the range parameter as next parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Parameter


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Parameter



## Cbim:next version

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The domain C-BIM object points to the range C-BIM object as its next version.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  Cbim:CbimObject



## Cbim:parent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range parent function fulfiller of the domain child function fulfiller.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:child



## Cbim:performance

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The range performance that characterizes the domain function fulfiller or state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:Performance


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:performanceOf


## Cbim:performance of

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range function fulfiller or state that is characterized by the domain performance.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:ObjectProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Performance


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller or cbim:State

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:performance



## Cbim:physical child

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range child physical object of the domain parent physical object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PhysicalObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:physicalParent


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:child


## Cbim:physical parent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range parent physical object of the domain child physical object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PhysicalObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PhysicalObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:physicalChild


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:parent


## Cbim:previous state

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The range state is the previous state of the domain state.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:TransitiveProperty](http://www.w3.org/2002/07/owl#ObjectProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:State

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:State


## Cbim:primary orientation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:property type

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:property value

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:requirement

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:requirement of

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:secondary orientation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:shape

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:situates

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:spatial child

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:spatial parent

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:state of

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:supertype

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:task type

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:terminal

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:terminal of

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:translation

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:value domain

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:value domain resource

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:verification function fulfiller

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:verification performer

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:verification requirement

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** 

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**