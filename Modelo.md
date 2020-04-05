
## Organization
Tabela principal das entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id	|Bigint|	Chave|	Identificador principal da entidade|
|version|	Bigint|	Chave|	Versão do registo da entidade|
|vstatus|	Varchar(45)|	Sim|	Estado da versão do registo|
|vstart	|Datetime	|Sim|	Data e hora de criação da versão|
|vapproval|	Datetime|	Não|	Data e hora de aprovação da versão|
|vend	|Datetime|	Não|	Data e hora de fim de validade da versão|
|vcomment|	Varchar(255)|	Sim|	Comentários da versão do registo|
|code|\Varchar(45)|	Sim |	Código da entidade|
|val_start|	Datetime|	Não|	Data de início de vigência|
|val_en|	Datetime|	Não|	Data de fim de vigência|
|territorial_scope_id|	Bigint|	Sim|	ID do âmbito territorial da entidade|
|logo_id|	Bigint|	Não|	ID do logotipo da entidade|
|location_ID | Bigint|	Sim|	ID da morada principal da entidade|
|parent_org_id|	Bigint	|Não|	ID da organização pai|
|parent_org_version|	Bigint|	Não| Versão da organização pai|
|org_type_id	| Bigint|	Não|	ID do tipo de organização|
|economic_activity_id|	Bigint|	Não|	ID da CAE principal|
|nipc	|Varchar(9)|	\Não| 	Número de Identificação de Pessoa Coletiva|
|last_updated|	Datetime|	Não |	Data e hora da última atualização|
|last_validated|	Datetime|	Não|	Data e hora da última validação|
|created_by	| varchar(45)|	Não|	Utilizador ou conector que criou a versão|
|last_updated_by|	varchar(45)|	Não|	Utilizador ou conector que atualizou a versão|

## Location
Tabela de moradas das entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|	Bigint|	Chave|	ID da localização|
|address|	Varchar(1024)|	Não	|Endereço|
|parish_id|	Bigint|	Não|	ID da freguesia|
|postal_code_4|	Varchar(4)|	Não	|Primeiros 4 dígitos do código postal|
|postal_code_3|	Varchar(3)|	Não|	Últimos 3 dígitos do código postal|
|postal_code_local|	Varchar(255)|	Não	|Localidade do código postal|
|latitude|	decimal(10,8)|	Não|	Latitude em formato decimal|
|longitude|	Decimal(11,8)|	Não|	Longitude em formato decimal|


## Organization_text			
Tabela de traduções das entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|	Bigin|	Chave|	Identificador principal da entidade|
|version|	Bigint|	Chave|	Versão do registo da entidade|
|language_code|	Varchar(2)|	Chave|	Código do idioma|
|desc_owner_id|	Bigint|	Sim|	ID da entidade dona da descrição|
|desc_owner_version|	Bigint|	Sim|	Versão da entidade dona da descrição|
|name	|text|	Sim|	Nome da entidade|
|abbreviation|	Varchar(45)	|Não|	Sigla ou abreviatura|
|keywords|	Longtext|	Não|	Palavras-chave|
|description|	Longtext|	Não|	Missão ou descrição da entidade|
|legislation|Longtext|	Não|	Legislação específica da entidade|


## Organization_type_text			
Tabela de traduções dos tipos de entidade.			

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|org_type_id|	Bigint|	Chave	id do tipo de entidade|
|language_code|	Varchar(2)|	Chave	Código do idioma|
|name	text|	Sim|	Nome do tipo de entidade|



## Related_org			
Tabela de entidades relacionadas.			

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|from_org_id|	Bigint|	Chave|	ID da entidade origem|
|from_org_version|	Bigint|	Chave|	Versão da entidade de origem|
|to_org_id| Bigint|	Chave	|ID da entidade de destino|


## Org_group
Tabela de relação das entidades com os grupos de entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|org_id	|Bigint|	Chave	|ID da entidade|
|org_version|	Bigint	|Chave|	Versão da Entidade|
|group_id|	Bigint|	Chave	|ID do grupo|


## Core_entity_group
Tabela principal dos grupos de entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do grupo|
|parent_id|Bigint|Chave|ID do grupo pai|
|root_id|Bigint|Chave|ID do grupo raiz|
|code|Varchar(45)|Sim|Código do grupo|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|

## Core_entity_group_text
Tabela de traduções dos grupos de entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|group_id|Bigint|Chave|ID do grupo|
|language_code|Varchar(2)|Sim|Código do idioma|
|name|Varchar(255)|Sim|Nome do grupo|
|description|Text|Não|Descrição do grupo|


## Point_of_care
Tabela principal dos pontos de atendimento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID principal do ponto de atendimento|
|version|Bigint|Chave|Versão do registo do ponto de atendimento|
|vstatus|Varchar(45)|Sim|Estado da versão do registo|
|vstart|Datetime|Sim|Data e hora de criação da versão|
|vapproval|Datetime|Não|Data e hora de aprovação da versão|
|vend|Datetime|Não|Data e hora de fim de validade da versão|
|vcomments|Varchar(255)|Sim|Comentários da versão do registo|
|code|Varchar(45)|Sim|Código da entidade|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|
|territorial_scope_id|Bigint|Sim|ID do âmbito territorial da entidade|
|owner_org_id|Bigint|Sim|ID da organização dona|
|owner_org_version|Bigint|Sim|Versão da organização dona|
|addr_org_id|Bigint|Não|ID da organização hospedeira|
|addr_org_version|Bigint|Não|Versão da organização hospedeira|
|poc_type|Varchar(45)|Não|Tipo de ponto de atendimento|
|poc_address|Varchar(255)|Não|Endereço do ponto de atendimento|
|logo_id|Bigint|Não|ID do logotipo da entidade|
|last_updated|Datetime|Não|Data e hora da última atualização|
|last_validated|Datetime|Não|Data e hora da última validação|
|created_by|varchar(45)|Não|Utilizador ou conector que criou a versão|
|last_updated_by|varchar(45)|Não|Utilizador ou conector que atualizou a versão|

## Point_of_care_text
Tabela de traduções das entidades.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do ponto de atendimento|
|version|Bigint|Chave|Versão do ponto de atendimento|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|

## Poc_contact
Tabela de contactos do ponto de atendimento.
|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do contacto|
|poc_id|Bigint|Sim|ID do ponto de atendimento|
|poc_version|Bigint|Sim|Versão do ponto de atendimento|
|type|Varchar(45)|Sim|Tipo de contacto|




## Poc_opening_hours
Tabela de horários de atendimento.

|poc_id|Bigint|Chave|ID do ponto de atendimento|
|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|poc_version|Bigint|Chave|Versão do ponto de atendimento|
|row_idx|int|Chave|Índice do horário de atendimento|
|opening_hours|Varchar(255)|Sim|Horário de atendimento|


## Poc_availability_restriction
Tabela de restrições de atendimento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|poc_id|Bigint|Chave|ID do ponto de atendimento|
|poc_version|Bigint|Chave|Versão do ponto de atendimento|
|row_idx|Int|Chave|Índice da restrição de atendimento|
|valid_from|Datetime|Não|Data de início de validade|


## Poc_division
Tabela principal das divisões de atendimento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|poc_id|Bigint|Chave|ID do ponto de atendimento|
|poc_version|Bigint|Chave|Versão do ponto de atendimento|
|code|Varchar(45)|Chave|Código da divisão de atendimento|
|val_start|Datetime|Não|Data de início de vigência|

## Poc_division_text
Tabela de traduções das divisões de atendimento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|poc_id|Bigint|Chave|ID do ponto de atendimento|
|poc_version|Bigint|Chave|Versão do ponto de atendimento|
|code|Varchar(45)|Chave|Código da divisão de atendimento|
|language_code|Varchar(2)|Chave|Código do idioma|

## Service_channel
Tabela principal dos canais de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do canal de serviço|
|poc_id|Bigint|Sim|ID do ponto de atendimento|
|poc_version|Bigint|Sim|Versão do ponto de atendimento|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|address|Varchar(1024)|Não|Endereço específico do serviço|
|channel_scope|Varchar(45)|Não|Âmbito do canal|
|division_code|Varchar(45)|Não|Código da divisão de atendimento|

## Service_channel_text
Tabela de traduções dos canais de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|service_channel_id|Bigint|Chave|ID do canal de serviço|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|addicional_info|Longtext|Não|Informação específica do canal do serviço|


## Channel_input
Tabela principal do requisito de canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do requisito do canal de serviço|
|channel_id|Bigint|Sim|ID do canal de serviço|
|code|Varchar(45)|Sim|Código do requisito|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|
|replaces_code|Varchar(45)|Não|Código do requisito do serviço|
