# Government Core Vocabularies


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/CoreVocabularies1.png)
## Person
fullName
familyName
givenName
patronymicName
alternativeName
gender
birthName
dateOfBirth
dateOfDeath
countryOfBirth  Location
placeOfBirth    Location
countryOfDeath  Location
placeOfDeath    Location
identifier   Identifier

## Agent


## Identifier
identifier
identifierType
dateOfIssue
issuingAuthority
issuingAuthorityUri

## Jurisdiction
name
id URI


## Location
geographicName
geographicIdentifier URI
geometry  Geometry
address Location  

## Geometry
coordinates CoordinatesList
crs 
geometryType

## Address
fullAddress
poBox
thoroughfare
locatorDesignator
locatorName
addressArea
postName
adminUnitL2
adminUnitL1
postCode
addressID

## Legal Entity
legalName
AlternativeName
activity Code List
status   Code List
type  Code List

## Code
content
list 
agency


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/CoreVocabularies2.png)
## FormalFramework


## Criterion
identifier
criterionType
name
description
fullfilledIndicator
weight

## RequirementGroup
identifier
description

# CriterionRequirement
identifier
name
description
expectedDataType
expectedValue
maximumValue
minimumValue
typeOfTranslation
levelOfCertification
typeOfCopyQuality

## Evidence
identifier
evidenceType
name
description
language
issuedBy Organization

## PeriodOfTime
startTime
endTime

## DocumentReference
identifier
url
description
type



