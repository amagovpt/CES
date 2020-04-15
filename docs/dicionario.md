## Public Service
Serviço Público

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do serviço|
|description|	Descrição do serviço|
|keyword|	Palavras-chave do serviço|
|sector	|Atividades económicas (CAE)|
|type|	Tipo de serviço (COFOG)|
|serviceStatus|	Estado do serviço|
|isGroupedBy|	Eventos de Vida e Eventos de Negócio|
|requires|	Serviços relacionados com tipo de relação Serviço Necessário |
|related|	Serviços relacionados com tipo de relação Serviço Relacionado|
|hasCriterion|	Destinatários do serviço|

## Business Event
Evento de Negócio

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do evento de negócio|
|description|	Descrição do evento de negócio|


## Life Event
Evento de Vida

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do evento de vida|
|description|	Descrição do evento de vida|

## Participation
Entidade do Serviço

|Nome do Atributo|Descriço|
|------------ | ------------|
|description|	Descrição da entidade|
|role|	Função da entidade no âmbito do serviço|


## Criterion Requirement
Mapeia com o conceito de Destinatário do Serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do destinatário do serviço|
|type|	Tipo de destinatário do CES|

## Evidence
Mapeia com o conceito de Requisito do Serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do requisito do serviço|
|description|	Descriço do requisito do serviço|
|type|	Documento associado ao requisito do serviço|
|relatedDocumentation|Documentação relacionada do requisito do serviço|



## Output
Mapeia com o conceito de Resultado do Serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name |	Nome do resultado do serviço|
|description|Descrição do resultado do serviço|
|type|	Documento associado ao resultado do serviço|

## Cost
Mapeia com os conceitos de Taxa do serviço, Taxa da Especialização do serviço e Taxa do Canal do serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name |	Nome da taxa do serviço|
|description|	Descrição da taxa do serviço|
|value|	Valor da taxa do serviço|
|currency|	"EUR"|
|isDefinedBy|	Entidade dona do serviço; entidade dona da Especialização do serviço; ou entidade dona do ponto de atendimento associado ao canal do serviço , consoante o tipo de taxa
|ifAccessedThrough|	Canal do serviço - no caso das taxas do canal do serviço|

## Channel
Mapeia com o conceito de Canal do serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome do ponto de atendimento associado ao canal do serviço|
|description|	Informação adicional do canal do serviço|
|ownedBy|	Entidade dona do ponto de atendimento associado ao canal do serviço|
|type	|Tipo de ponto de atendimento|
|hasInput|	Requisitos do canal do serviço|
|openingHours	|Horário de atendimento do canal do serviço|
|availabilityRestriction|	Restrições de atendimento do canal do serviço|
|hasEmail|	Contatos do tipo "Email" do ponto de atendimento|
|hasTelephone|	Contatos do tipo "Telefone" do ponto de atendimento|
|hasCost	|Taxas do canal do serviço|

## Opening Hours Specification
Mapeia com o conceito de Restrições de Atendimento do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|dayOfWeek|	Dia da semana|
|opens|	Horário de abertura|
|closes|	Horário de fecho|
|validFrom	|Válido de|
|validThrough	|Vàlido até|

## Rule
Mapeia com os conceitos de Regra do serviço e Regra da Especialização do serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome da regra do serviço|
|description|	Descrição da regra do serviço|
|implementFormalFramework|Legislação associada à regra do serviço|


## Formal Framework
Mapeia com os conceitos de Legislação do serviço e Legislação da Especialização do serviço do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome da legislação|
|description	Descrição da legislação|
|relatedDocumentation	Documentação relacionada da legislação (link para DRE)|


## Public Organization

Mapeia com o conceito de Entidade do CES
|Nome do Atributo|Descrição|
|------------ | ------------|
|name|	Nome da entidade|
|description|	Descrição da entidade|
|preferedLabel|	Sigla ou abreviatura|
|spatial	|Âmbito territorial da entidade|
|purpose	|Atividade económica principal|
|classification	|Tipo de entidade|
|homepage	|Contatos da entidade do tipo "URL"|
|subOrganizationOf|	Entidade pai|
|contactPoint	|Contatos da entidade|
|address|	Morada Principal / Sede|

## Contact Point

Mapeia com o conceito de Contactos da Entidade do CES

|Nome do Atributo|Descrição|
|------------ | ------------|
|hasEmail|	Contatos do tipo "Email"|
|hashTelephone|	Contatos do tipo "Telefone"|
