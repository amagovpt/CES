# Government Core Vocabularies


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/CoreVocabularies1.png)
## Person


|Nome do Atributo|Tipo|
|------------ | ------------|
|fullName|string|
|familyName|string|
|givenName|string|
|patronymicName|string|
|alternativeName|string|
|gender|string|
|birthName|string|
|dateOfBirth|string|
|dateOfDeath|string|
|countryOfBirth| Location|
|placeOfBirth  | Location|
|countryOfDeath| Location|
placeOfDeath    Location
identifier   Identifier

## Agent

|Nome do Atributo|Tipo|
|------------ | ------------|

## Identifier

|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier
|identifierType
|dateOfIssue
|issuingAuthority
|issuingAuthorityUri

## Jurisdiction
|name|string|
|id |URI|


## Location

|Nome do Atributo|Tipo|
|------------ | ------------|
|geographicName|string|
|geographicIdentifier|URI|
|geometry|Geometry|
|address |Location|  

## Geometry

|Nome do Atributo|Tipo|
|------------ | ------------|
|coordinates| list|
|crs||
|geometryType||

## Address

|Nome do Atributo|Tipo|
|------------ | ------------|
|fullAddress||
|poBox||
|thoroughfare||
|locatorDesignator|
|locatorName|
|addressArea|
|postName||
|adminUnitL2|
|adminUnitL1||
|postCode||
|addressID||

## Legal Entity~

|Nome do Atributo|Tipo|
|------------ | ------------|
|legalName|String|
|alternativeName|String|
|activity| Code List|
|status  | Code List|
|type  |Code List|

## Code

|Nome do Atributo|Tipo|
|------------ | ------------|
|content||
|list||
|agency||


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/CoreVocabularies2.png)
## FormalFramework


## Criterion


|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|criterionType||
|name||
|description||
|fullfilledIndicator||
|weight||

## RequirementGroup

|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|description||

# CriterionRequirement

|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|name||
|description||
|expectedDataType||
|expectedValue||
|maximumValue||
|minimumValue||
|typeOfTranslation||
|levelOfCertification||
|typeOfCopyQuality||

## Evidence


|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|evidenceType||
|name||
|description|
|language||
|issuedBy Organization||

## PeriodOfTime


|Nome do Atributo|Tipo|
|------------ | ------------|
|startTime||
|endTime||

## DocumentReference

|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|url||
|description||
|type||

## RequirementRespnse

|Nome do Atributo|Tipo|
|------------ | ------------|
|identifier||
|name||
|description||
|value||
