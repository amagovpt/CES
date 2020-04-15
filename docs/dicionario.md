## Public Service
Servi�o P�blico

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome do servi�o|
|description|	Descri��o do servi�o|
|keyword|	Palavras-chave do servi�o|
|sector	|Atividades econ�micas (CAE)|
|type|	Tipo de servi�o (COFOG)|
|serviceStatus|	Estado do servi�o|
|isGroupedBy|	Eventos de Vida e Eventos de Neg�cio|
|requires|	Servi�os relacionados com tipo de rela��o �Servi�o Necess�rio� |
|related|	Servi�os relacionados com tipo de rela��o �Servi�o Relacionado�|
|hasCriterion|	Destinat�rios do servi�o|

## Business Event	
Evento de Neg�cio 

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome do evento de neg�cio|
|description|	Descri��o do evento de neg�cio|


## Life Event	
Evento de Vida

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome do evento de vida|
|description|	Descri��o do evento de vida|

## Participation	
Entidade do Servi�o 

|Nome do Atributo|Descri��o|
|------------ | ------------|	
|description|	Descri��o da entidade|
|role|	Fun��o da entidade no �mbito do servi�o|


## Criterion Requirement	
Mapeia com o conceito de Destinat�rio do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|	
|name|	Nome do destinat�rio do servi�o|
|type|	Tipo de destinat�rio do CES|

## Evidence	
Mapeia com o conceito de Requisito do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|	
|name|	Nome do requisito do servi�o|
|description|	Descri��o do requisito do servi�o|
|type|	Documento associado ao requisito do servi�o|
|relatedDocumentation|Documenta��o relacionada do requisito do servi�o|



## Output	
Mapeia com o conceito de Resultado do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|	
|name |	Nome do resultado do servi�o|
|description|Descri��o do resultado do servi�o|
|type|	Documento associado ao resultado do servi�o|
	
## Cost	
Mapeia com os conceitos de Taxa do Servi�o, Taxa da Especializa��o do Servi�o e Taxa do Canal do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|	
|name |	Nome da taxa do servi�o|
|description|	Descri��o da taxa do servi�o|
|value|	Valor da taxa do servi�o|
|currency|	�EUR�|
|isDefinedBy|	Entidade dona do servi�o; entidade dona da especializa��o do servi�o; ou entidade dona do ponto de atendimento associado ao canal do servi�o � consoante o tipo de taxa
|ifAccessedThrough|	Canal do servi�o � no caso das taxas do canal do servi�o|
	
## Channel	
Mapeia com o conceito de Canal do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name	Nome do ponto de atendimento associado ao canal do servi�o|
|description|	Informa��o adicional do canal do servi�o|
|ownedBy|	Entidade dona do ponto de atendimento associado ao canal do servi�o|
|type	|Tipo de ponto de atendimento|
|hasInput|	Requisitos do canal do servi�o|
|openingHours	|Hor�rio de atendimento do canal do servi�o|
|availabilityRestriction|	Restri��es de atendimento do canal do servi�o|
|hasEmail|	Contatos do tipo �Email� do ponto de atendimento|
|hasTelephone|	Contatos do tipo �Telefone� do ponto de atendimento|
|hasCost	|Taxas do canal do servi�o|
	
## Opening Hours Specification	
Mapeia com o conceito de Restri��es de Atendimento do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|
|dayOfWeek|	Dia da semana|
|opens|	Hor�rio de abertura|
|closes|	Hor�rio de fecho|
|validFrom	|V�lido de|
|validThrough	|V�lido at�|
	
## Rule	
Mapeia com os conceitos de Regra do Servi�o e Regra da Especializa��o do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome da regra do servi�o|
|description|	Descri��o da regra do servi�o|
|implementFormalFramework|Legisla��o associada � regra do servi�o|
	

## Formal Framework	
Mapeia com os conceitos de Legisla��o do Servi�o e Legisla��o da Especializa��o do Servi�o do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome da legisla��o|
|description	Descri��o da legisla��o|
|relatedDocumentation	Documenta��o relacionada da legisla��o (link para DRE)|
	

## Public Organization	
	
Mapeia com o conceito de Entidade do CES	
|Nome do Atributo|Descri��o|
|------------ | ------------|
|name|	Nome da entidade|
|description|	Descri��o da entidade|
|preferedLabel|	Sigla ou abreviatura|
|spatial	|�mbito territorial da entidade|
|purpose	|Atividade econ�mica principal|
|classification	|Tipo de entidade|
|homepage	|Contatos da entidade do tipo �URL�|
|subOrganizationOf|	Entidade pai|
|contactPoint	|Contatos da entidade|
|address|	Morada Principal / Sede|
	
## Contact Point	
	
Mapeia com o conceito de Contactos da Entidade do CES	

|Nome do Atributo|Descri��o|
|------------ | ------------|
|hasEmail|	Contatos do tipo �Email�|
|hashTelephone|	Contatos do tipo �Telefone�|















