# Criterion and Evidence Type Rule Base



## Criterion

5.2. Class: Criterion
The Criterion class represents the rule or principle used to judge, evaluate or assess
something. The Criterion class has the properties described below.
Core Criterion and Core Evidence Vocabulary

5.2.1. Property: identifier
This property provides a formally issued identifier for the Criterion. A Criterion must
have an identifier.
5.2.2. Property: criterion type
A Criterion must be defined in terms of a coded type in order to allow for
classification and automatic translation. The types of criterion shall be based on
controlled vocabularies.
5.2.3. Property: name
A Criterion must have a name. It can be used as a short descriptive text.
5.2.4. Property: description
A Criterion may be textually described using this property. The description can be
used to add details and further explanation about the Criterion.
5.2.5. Property: fulfilled indicator
This property is used when the Criterion class is informed as a response and the
submitter wants to specify whether the Criterion is considered to be fulfilled (true)
or not (false).
5.2.6. Property: weight
A Criterion may have a weight to provide for automatic scoring of the Criterion
responses. It implies that there are multiple criteria, and the weight represents the
importance of one criterion among the whole set of criteria.
5.2.7. Property: is defined in Formal framework
A legal text or any other Formal framework defines the legal basis for the criterion.
5.2.8. Property: fulfilled by Requirement group
A Criterion shall be fulfilled by means of one or more groups of options. Each one of
these options is defined as a Requirements group.
There might be different ways to validate a single criterion, therefore there can be
multiple Requirement groups associated with a criterion. Each Requirement group
contains all the requirement criteria that must be fulfilled in order to fulfil the whole
criterion.

## Formal framework

5.3. Class: Formal framework
This class and its properties are defined in the Core Public Service Vocabulary11
Application Profile and may represent legislation, policy, or policies lying behind the
rules that govern a criterion.



## Requirement group

5.4. Class: Requirement group
Criterion requirement group is the set of requirements that must be fulfilled
together to validate a criterion.
A Criterion can be satisfied using different options. The Requirement group class is
used to wrap the set of criteria requirements that validate a criterion.
All criteria requirements belonging to a requirement group shall be valid for the
requirement group to be considered valid.
When there is more than one Requirement group for a Criterion, at least one of
them has to be positively validated for the Criterion to be considered fulfilled.
5.4.1. Property: identifier
A Requirement group must be identified.
5.4.2. Property: description
A Requirement group may be textually described using this property. The
description can be used to add details and explanation about the Requirement
group.
5.4.3. Property: has Criterion requirement
A Requirement group is a collection of Criterion requirements. At least, a
Requirement group shall contain one Criterion requirement.


## Criterion requirement
A Criterion can be expressed as a set of requirements where every requirement
must be valid. A Criterion requirement is an atomic requirement. This can be better
explained with the examples in section 6.1, where the criterion is "to be eligible to
enter into the cinema to watch a movie", and there are several options to meet this
criterion. One option has two Criterion requirements:
 Holding a ticket
 Being older than eighteen
Some criteria can be expressed with several atomic requirements. A Criterion
requirement can specify the expected value that the Criterion response has to
contain, or a range of threshold values within which the Criterion response has to fit
in.
The Criterion requirement may apply to a certain period of time. It also can provide
a list of candidate evidences that the responder can use to prove the Criterion
requirement. 




5.5.2. Property: identifier
A Criterion requirement must have an identifier.
Core Criterion and Core Evidence Vocabulary
5.5.2. Property: name
A Criterion requirement may have a name by which it can be referred to.
5.5.3. Property: description
A Criterion requirement may have an explanatory description.
5.5.4. Property: expected data type
Each Criterion requirement shall describe the expected data type that the response
has to provide.
5.5.5. Property: expected value
This property is used to define the expected value that the responder has to
provide in the Criterion response.
5.5.6. Property: maximum value
When the value of the Criterion response must fall into a range or it shall be lesser
than a threshold, this property is used to define the maximum expected value.
5.5.7. Property: minimum value
When the value of the Criterion response must fall into a range or it shall be larger
than a specific threshold, this property is used to define the minimum expected
value.
5.5.8. Property: type of translation
A Criterion requirement may specify whether the evidence proving that this
Criterion requirement shall be translated and what type of translation shall apply,
for instance, certified translation.
5.5.9. Property: level of certification
A Criterion requirement may specify whether the Evidence proving this Criterion
requirement shall belong to a specific level of certification, for instance, legalisation.
5.5.10. Property: type of copy quality
A Criterion requirement may specify whether the Evidence proving this Criterion
requirement shall be of a specific type of copy, for instance, certified copy.
5.5.11. Property: applicable in Period of time
If the Criterion requirement shall apply to a specific time period, this class is used
to describe it.
5.5.12. Property: met by Evidence
A Criterion Requirement may point to a list of candidate Evidences that can be used
by the responder to prove the Criterion requirement is fulfilled.


## Requirement response

5.6. Class: Requirement response
Requirement response is an assertion that responds to a criterion requirement.
Core Criterion and Core Evidence Vocabulary
Requirement Response is the class used to define the actual response to a Criterion
requirement. It provides the value for the specific requirement and the period to
which it applies. It refers to the Criterion requirement that validates.
5.6.1. Property: identifier
A Requirement response must have an identifier.
5.6.2. Property: name
A Requirement response may have a name by which it is referred to.
5.6.3. Property: description
A Requirement response may have an explanatory description.
5.6.4. Property: value
The Requirement response must contain the value that responds to the Criterion
requirement. In order to fulfil the Criterion requirement, when there is an expected
value or an expected threshold, the value should be equal to the expected value or
within the range established by the thresholds.
5.6.5. Property: applies to Period of time
If the Requirement response applies to a specific period, this class is used to
establish it.
5.6.6. Property: validates Criterion requirement
The Requirement response must refer to the Criterion requirement it is replying to.
5.6.7. Property: proven by Evidence
The Requirement response may provide the Evidence that proves the response, and
thus the Criterion requirement.
5.7. Class: Period of time
An interval of time that is named or defined by its start and end times.
5.7.1. Property: start time
The date and time on which the period of time starts.
5.7.2. Property: end time
The date and time on which the period of time finalizes.

## Evidence

5.8. Class: Evidence
Evidence is any resource that can document or support a Requirement response.
The Evidence class contains information that proves that a Criterion requirement
exists or is true, in particular Evidences are used to prove that a specific Criterion is
met.
Core Criterion and Core Evidence Vocabulary

An Evidence can have the following properties.
5.8.1. Property: identifier
An Evidence must have an identifier.
5.8.2. Property: evidence type
The Evidences contain a property type to categorize Evidences and to allow for the
creation of controlled vocabularies that can facilitate automatic translation.
5.8.3. Property: name
An Evidence may have a name by which it is referred to.
5.8.4. Property: description
An Evidence may have an explanatory description.
5.8.5. Property: language
An Evidence may define the language the attestation of evidentiary document is
written in.
5.8.6. Property: issued by Organisation
An Evidence may refer to the organisation that issued the attestation or evidentiary
document.
5.8.7. Property: is supported by Document reference
An Evidence may refer to the attestation, to the evidentiary document or to the URL
where the proof from a third party can be found.
5.8.8. Property: belongs to Agent
An Evidence shall belong to an Agent. A Criterion may affect several Agents;
therefore the evidences shall define to which Agent they belong. For instance, a
criterion of non-conviction applied to an Organisation requires evidences of nonconviction for the organisation responsible persons. Each of those evidences shall
indicate to which person within the organisation they belong.

## Agent

5.9. Class: Agent
An Organisation or Natural person providing a Requirement response that satisfies
a Criterion. The Agent class is a generalisation of the Person and Organisation
classes defined in the Core Person Vocabulary and the Organisation Ontology
respectively.
5.9.1. Property: satisfies Criterion
An Agent satisfies a Criterion. It shall satisfy the Criterion by providing Requirement
responses that validate the Criterion requirements of the Criterion.
5.9.2. Property: provides Requirement response
An Agent provides Requirement responses to validate the Criterion requirements
defined in the Criterion.
Core Criterion and Core Evidence Vocabulary
Page 21 of 38
5.10. Class: Organisation
This is a subclass of the class Agent. This subclass contains the properties defined
in the class Agent above plus the properties defined in the Organisation Ontology12
.
The modelling of the Legal Entities must follow the Core Business Vocabulary (Legal
Entity is a subclass of Organisation) and the modelling of Public Organisations must
follow the Core Public Organisation Vocabulary (Public Organisation is a subclass of
Formal Organisation)

## Organisation

5.10. Class: Organisation
This is a subclass of the class Agent. This subclass contains the properties defined
in the class Agent above plus the properties defined in the Organisation Ontology12
.
The modelling of the Legal Entities must follow the Core Business Vocabulary (Legal
Entity is a subclass of Organisation) and the modelling of Public Organisations must
follow the Core Public Organisation Vocabulary (Public Organisation is a subclass of
Formal Organisation)
5.11. Class: Person
This is a subclass of the class Agent. This subclass contains the properties defined
in the class Agent above plus the properties defined in the Core Person
Vocabulary

## Document reference
5.12. Class: Document reference
A reference to the document, attestation or data, usually provided by a party
different from the one providing the response, that proves the response.
5.12.1. Property: identifier
A Document reference shall contain an identifier.
5.12.2. Property: URL
The Uniform Resource Locator where the document or attestation can be found.
5.12.3. Property: description
A Document reference may contain the description of the attestation or evidentiary
document.
5.12.4. Property: type
The Document reference may contain the type that categorizes the attestation or
evidentiary document.


6.2.3. Requirement group
The requirement group class contains an identifier and a set of criterion
requirements.
The requirement group represents an option. In our example, there are two
different option and their properties will be an identifier and a set of Criterion
requirements that describe each option:

Identifier 7c637c0c-7703-4389-ba52-02997a055bd7
Criterion requirement See 6.1.4. 

file:///C:/Users/marco.p.pedro/Downloads/core_evidence_and_core_criterion_vocabulary_-_draft_1.pdf


6.2.4. Criterion requirement
Each requirement group has a set of criterion requirements. In this example, the
first requirement group contains only one single requirement.
This first Requirement Group is the option that has to be chosen by the parties that
have never been convicted. In this case, replying "true" to this criterion is enough
to fulfil the main criterion.
Property Value
Identifier 4157c56b-754b-4f92-b4b1-0256b9a472d2
Description
The economic operator itself or any person who is a member of its
administrative, management, or supervisory board or has powers of
representation, decision or control therein has not been the subject
of a conviction by final judgement for participation in a criminal
organisation, by a conviction rendered at the most five years ago or in
which an exclusion period set out directly in the conviction continues
to be applicable as defined in Article 2 of Council Framework Decision
2008/841/JHA of 24 October 2008 on the fight against organised
crime (OJ L 300, 11.11.2008, p. 42)
Expected
data type Boolean
The second requirement group contains a set of six different criterion requirements
that may also be used to make the whole criterion valid. Those parties that having
been convicted, have been clearing it up shall use this option.
Most of the requirements are provided textually, which means that it will not be
possible to automatically assess the responses.
Core Criterion and Core Evidence Vocabulary
15/03/2016 Page 20 of 30
Property Value
Identifier 4157c56b-754b-4f92-b4b1-0256b9a472d1
Description:
The economic operator itself or any person who is a member of its
administrative, management, or supervisory board or has powers of
representation, decision or control therein has been the subject of a
conviction by final judgement for participation in a criminal
organisation, by a conviction rendered at the most five years ago or
in which an exclusion period set out directly in the conviction
continues to be applicable as defined in Article 2 of Council
Framework Decision 2008/841/JHA of 24 October 2008 on the fight
against organised crime (OJ L 300, 11.11.2008, p. 42)
Expected
data type Boolean


Property Value
Identifier ecf40999-7b64-4e10-b960-7f8ff8674cf6
Description Provide the date of conviction
Expected
data type text

Property Value
Identifier 7d35fb7c-da5b-4830-b598-4f347a04dceb
Description Provide the reason of the conviction
Expected
data type text


identifieddentifier c5012430-14da-454c-9d01-34cedc6a7ded
Description Provide the name of the convicted persons.
Expected
data type text


Description Length of the period of conviction
Expected
data type text


identifier 7b07904f-e080-401a-a3a1-9a3efeeda54b
Description Description of the measures taken to demonstrate "self-cleaning".
Expected
data type text

