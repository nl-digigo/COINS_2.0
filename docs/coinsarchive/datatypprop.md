# Datatype Properties

## Cbim:BaselineStatus

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The status (true＝open or false＝closed) of the baseline.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)


**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Baseline

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean)


## Cbim:Changelog

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The changelog of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:ChecksumFile

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  Checksum hash of the attached file.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)
  

## Cbim:ChecksumFileAlgorithm

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The checksum algorithm (e.g. SHA1, MD5, ...) that was used to generate the checksum of the attached file.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)

## Cbim:ChecksumUri

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  Checksum hash of the URI linked document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:ChecksumUriAlgorithm

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The checksum algorithm (e.g. SHA1, MD5, ...) that was used to generate the checksum of the URI linked document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:CreationDate 

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The creation date/time of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:dateTime](http://www.w3.org/2001/XMLSchema#dateTime)



## Cbim:DefaultValue

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The default value of the parameter.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		Parameter

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)

## Cbim:Description

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The description of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:DocumentAliasFilePath

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The locally stored copy of the document. The property cbim:documentAliasFilePath contains the filename of a document, if the file is stored in the directory 'bim' of a COINS container. The property cbim:documentAliasFilePath prevails above the property cbim:documentUri.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:DocumentFragment

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The fragment addresses a specific location in the document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:DocumentType

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The type of the document.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Document

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)


## Cbim:EndDate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The abstract typed property end date.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:date](http://www.w3.org/2001/XMLSchema#date)


## Cbim:EndDateActual

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The actual end date of the task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:date](http://www.w3.org/2001/XMLSchema#date)


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  	cbim:endDate

## Cbim:EndDatePlanned

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The planned end date of the task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	Cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:date](http://www.w3.org/2001/XMLSchema#date)


**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  	cbim:endDate


## Cbim:Expired

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The expiration status of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean)


## Cbim:LayerIndex

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The layer index number of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:int](http://www.w3.org/2001/XMLSchema#int)

 

## Cbim:ModificationDate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The last modification date/time of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  [xsd:datetime](http://www.w3.org/2001/XMLSchema#dateTime) 	

 

## Cbim:Name

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The name of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Object

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string) 

## Cbim:ReleaseDate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The release date/time of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:CbimObject	

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  [xsd:datetime](http://www.w3.org/2001/XMLSchema#dateTime) 


## Cbim:ReleaseStatus

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The release status of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Object

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string) 


## Cbim:StartDate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)** The abstract typed property start date.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:date](http://www.w3.org/2001/XMLSchema#date)

## Cbim:StartDateActual

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The actual start date of the task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  xsd:date	

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:startDate


## Cbim:StartDatePlanned

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The planned start date of the task.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Task

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  xsd:date	

**[rdfs:subPropertyOf](http://www.w3.org/2000/01/rdf-schema#subPropertyOf)**  cbim:startDate

## Cbim:Unit

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The unit of the property type.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PropertyType

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string) 
 

## Cbim:UserID

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**   The user defined ID of the C-BIM object.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Object

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string) 


## Cbim:Value

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The actual value of the property value.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:PropertyValue

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:anySimpleType](http://www.w3.org/2001/XMLSchema#anySimpleType)


## verification date

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  Cbim:VerificationDate

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)**  [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	value domain Verification_1.1_Class|cbim:Verification


**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:datetime](http://www.w3.org/2001/XMLSchema#dateTime) 	



## Cbim:VerificationMethod

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The test method of the verification.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Verification

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  	[xsd:string](http://www.w3.org/2001/XMLSchema#string)  


## Cbim:VerificationResult

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The result of the verification.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**		cbim:Verification

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  		[xsd:boolean](http://www.w3.org/2001/XMLSchema#boolean)



## Cbim:XCoordinate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The x coordinate of the vector.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  [xsd:float](http://www.w3.org/2001/XMLSchema#float)	

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  


## Cbim:YCoordinate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The y coordinate of the vector.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  [xsd:float](http://www.w3.org/2001/XMLSchema#float)	

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  

## Cbim:ZCoordinate

**[rdfs:comment](http://www.w3.org/2000/01/rdf-schema#comment)**  The z coordinate of the vector.

**[rdf:type](http://www.w3.org/1999/02/22-rdf-syntax-ns#type)** [owl:FunctionalProperty](http://www.w3.org/2002/07/owl#FunctionalProperty)

**[rdfs:domain](http://www.w3.org/2000/01/rdf-schema#domain)**	cbim:Vector

**[rdfs:range](http://www.w3.org/2000/01/rdf-schema#range)**  [xsd:float](http://www.w3.org/2001/XMLSchema#float)	

**[owl:inbverseOf](http://www.w3.org/2000/01/rdf-schema#inverseOf)**  


