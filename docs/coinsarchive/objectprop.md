# Object Properties


## Cbim:Affects

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** owl:ObjectProperty

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:FunctionFulfiller

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** 	
cbim:isAffectedBy



## Cbim:AmountPropertyType

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  owl:ObjectProperty

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CataloguePart

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** 	cbim:PropertyType



## Cbim:Baseline
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  owl:ObjectProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Baseline


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** cbim:baselineObject



## Cbim:baseline object

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** owl:ObjectProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Baseline


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CbimObject


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)** cbim:baseline



## Cbim:catalogue part

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  owl:ObjectProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	 cbim:Amount


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:CataloguePart


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:propertyType


## Cbim:child

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  owl:TransitiveProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)** cbim:FunctionFulfiller


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:FunctionFulfiller


**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  cbim:parent	



## Cbim:contains

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** owl:ObjectProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:FunctionFulfiller or cbim:CataloguePart or cbim:State


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)** cbim:Amount


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)** cbim:propertyValue


## Cbim:creator

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  owl:ObjectProperty	


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  cbim:PersonOrOrganisation 


## Cbim:current state
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:document
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:document URI
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:female terminal
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:first parameter
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:fulfills
**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:is affected by

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:is fulfilled by

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:is situated in

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:locator

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:male terminal

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:max bounding box

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:min bounding box

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:modifier

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:next parameter

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:next version

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:parent

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:performance

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:performance of

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:physical child

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:physical parent

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:previous state

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:primary orientation

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:property type

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:property value

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:requirement

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:requirement of

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:secondary orientation

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:shape

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:situates

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:spatial child

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:spatial parent

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:state of

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:supertype

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:task type

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:terminal

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:terminal of

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:translation

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:value domain

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:value domain resource

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:verification function fulfiller

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**


## Cbim:verification performer

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**

## Cbim:verification requirement

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** 

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**