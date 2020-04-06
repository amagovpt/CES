
![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/organization.png)
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

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/organizationtype.png)

## Organization_type
Tabela base dos tipos de entidade.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|id do tipo de entidade|
|code|Varchar(45)|Sim|Código do tipo de entidade|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|


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


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/relatedorg.png)

## Related_org			
Tabela de entidades relacionadas.			

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|from_org_id|	Bigint|	Chave|	ID da entidade origem|
|from_org_version|	Bigint|	Chave|	Versão da entidade de origem|
|to_org_id| Bigint|	Chave	|ID da entidade de destino|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/orggroup.png)
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

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/poc.png)

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

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|poc_id|Bigint|Chave|ID do ponto de atendimento|
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

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/division.png)
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

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/servicechannel.png)
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

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/requirement.png)

## Channel_input_cr
Tabela de destinatários do requisito do canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|channel_input_id|Bigint|Chave|ID do requisito do canal de serviço|
|criterion_requirement_id|Bigint|Chave|ID do destinatário|


## Channel_input_text
Tabela de traduções do requisito do canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|channel_input_id|Bigint|Sim|ID do requisito do canal de serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do requisito|
|description|Longtext|Não|Descrição do requisito|
|related_doc_url|varchar(255)|Não|URL para documentação relacionada|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/channeloutput.png)

## Channel_output
Tabela principal do resultado de canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do resultado do canal de serviço|
|channel_id|Bigint|Sim|ID do canal de serviço|
|code|Varchar(45)|Sim|Código do resultado|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|
|replaces_code|Varchar(45)|Não|Código do resultado do serviço|

## Channel_output_text
Tabela de traduções do resultado do canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|channel_ouput_id|Bigint|Sim|ID do resultado do canal de serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do resultado|
|description|Longtext|Não|Descrição do resultado|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/channelcost.png)

## Channel_cost
Tabela principal da taxa do canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da taxa do canal de serviço|
|channel_id|Bigint|Sim|ID do canal de serviço|
|code|Varchar(45)|Sim|Código da taxa|
|cost_value|Double|Sim|Valor base da taxa em euro (€)|
|cost_condition|Text|Sim|Condição de aplicação da taxa|
|cost_formula|Text|Sim|Fórmula de cálculo do valor total|
|rounding_mode|Varchar(45)|Sim|Tipo de arredondamento|
|rounding_decimal|Int|Sim|Nº de casas decimais|
|replaces_code|Varchar(45)|Não|Código da taxa do serviço|


## Channel_cost_text
Tabela de traduções da taxa do canal de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|channel_cost_id|Bigint|Sim|ID da taxa do canal de serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da taxa|
|description|Longtext|Não|Descrição da taxa|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/service.png)

## Service
Tabela principal dos serviços.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do serviço|
|version|Bigint|Chave|Versão do serviço|
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
|logo_id|Bigint|Não|ID do logotipo da entidade|
|last_updated|Datetime|Não|Data e hora da última atualização|
|last_validated|Datetime|Não|Data e hora da última validação|
|service_status|Varchar(45)|Não|Estado do serviço (CPSV)|
|processing_time|Varchar(1024)|Não|Tempo de processamento|
|created_by|varchar(45)|Não|Utilizador ou conector que criou a versão|
|last_updated_by|varchar(45)|Não|Utilizador ou conector que atualizou a versão|

# Service_text
Tabela de traduções dos serviços.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do serviço|
|version|Bigint|Chave|Versão do serviço|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome|
|abbreviation|Varchar(45)|Não|Sigla ou abreviatura|
|keywords|Longtext|Não|Palavras-chave|
|description|Longtext|Não|Descrição|
|procedure|Longtext|Não|Descrição do procedimento|
|proc_diagram_id|Bigint|Não|ID do diagrama do procedimento|


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/servicetype.png)

## Service_service_type
Tabela de relação dos tipos de serviço associados a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|service_type_id|Bigint|Chave|ID do tipo de serviço|


## Service_type
Tabela base dos tipos de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do tipo de serviço|
|parent_id|Bigint|Não|ID do tipo de serviço pai|
|root_id|Bigint|Não|ID do tipo de serviço raiz|

## Service_type_text
Tabela de traduções dos tipos de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_type_id|Bigint|Chave|id do tipo de serviço|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome do tipo de serviço|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/businessevent.png)

## Service_business_event
Tabela de relação dos eventos de negócio associados a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|service_category_id|Bigint|Chave|ID do evento de negócio|


## Service_life_event
Tabela de relação dos eventos de vida associados a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|service_category_id|Bigint|Chave|ID do evento de vida|


## Service_service_category
Tabela de relação das categorias de serviço associadas a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|service_category_id|Bigint|Chave|ID da categoria de serviço|


## Service_category
Tabela base das categorias de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da categoria de serviço|
|parent_id|Bigint|Não|ID da categoria de serviço pai|
|root_id|Bigint|Não|ID da categoria de serviço raiz|
|code|Varchar(45)|Sim|Código da categoria de serviço|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|

## Service_category_text
Tabela de traduções das categorias de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_type_id|Bigint|Chave|ID da categoria de serviço|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome da categoria de serviço|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/economicactivity.png)

## Service_economic_activity
Tabela de relação das atividades económicas associadas a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|economic_activity_id|Bigint|Chave|ID da atividade económica|


## Economic_activity
Tabela base das atividades económicas.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da atividade económica|
|parent_id|Bigint|Não|ID da atividade económica pai|
|root_id|Bigint|Não|ID da atividade económica raiz|
|code|Varchar(45)|Sim|Código da atividade económica|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|


## Economic_activity_text
Tabela de traduções das atividades económicas.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|economic_activity_id|Bigint|Chave|ID da atividade económica|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome da atividade económica|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/serviceorg.png)

## Service_org
Tabela de relação das entidades associadas a um serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_id|Bigint|Chave|ID do serviço|
|service_version|Bigint|Chave|Versão do serviço|
|org_id|Bigint|Chave|ID da entidade|
|org_version|Bigint|Chave|Versão da entidade|
|role|Varchar(45)|Sim|Função da entidade no âmbito do serviço|


## Criterion_requirement
Tabela base dos destinatários do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do destinatário do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código do destinatário|
|consumer_type_id|Bigint|Não|ID do tipo de consumidor|


## criterion_requirement_text
Tabela de traduções dos destinatários do serviço

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|criterion_requirement_id|Bigint|Sim|ID do destinatário do serviço|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome do destinatário do serviço|
|description|Longtext|Não|Descrição do destinatário do serviço|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/consumertype.png)

## consumer_type
Tabela base dos tipos de consumidor.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do tipo de consumidor|
|parent_id|Bigint|Não|ID do tipo de consumidor pai|
|root_id|Bigint|Não|ID do tipo de consumidor raiz|
|code|Varchar(45)|Sim|Código do tipo de consumidor|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|

## consumer_type_text
Tabela de traduções dos tipos de consumidor.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|consumer_type_id|Bigint|Chave|ID do tipo de consumidor|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome do tipo de consumidor|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/serviceinput.png)

## Service_input
Tabela principal do requisito do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do requisito do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código do requisito|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|

## Service_input_cr
Tabela de destinatários do requisito do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_input_id|Bigint|Chave|ID do requisito do serviço|
|criterion_requirement_id|Bigint|Chave|ID do destinatário|


## Service_input_text
Tabela de traduções do requisito do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|service_input_id|Bigint|Sim|ID do requisito do serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do requisito|
|description|Longtext|Não|Descrição do requisito|
|related_doc_url|varchar(255)|Não|URL para documentação relacionada|


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/serviceoutput.png)

## Service_output
Tabela principal do resultado de serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do resultado do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código do resultado|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|


## Service_output_text
Tabela de traduções do resultado do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|service_ouput_id|Bigint|Sim|ID do resultado do serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do resultado|
|description|Longtext|Não|Descrição do resultado|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/servicelegislation.png)

## Service_legislation
Tabela principal da legislação do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da legislação do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código da legislação|


## Service_legislation_text
Tabela de traduções da legislação do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|service_legislation_id|Bigint|Sim|ID da legislação do serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da legislação|
|description|Longtext|Não|Descrição da legislação|
|related_doc_url|varchar(255)|Não|URL para pagina externa (ex: dre.pt)|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/servicerule.png)

## Service_rule
Tabela principal da regra do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da regra do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código da regra|


## Service_rule_legislation
Tabela de legislação aplicável à regra do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|service_rule_id|Bigint|Chave|ID da regra do serviço|
|service_legislation_id|Bigint|Chave|ID da legislação do serviço|


## Service_rule_text
Tabela de traduções da regra do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|service_rule_id|Bigint|Sim|ID da regra do serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da regra|
|description|Longtext|Não|Descrição da regra|

## Service_cost_var
Tabela de referência das variáveis de cálculo das taxas do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da variável|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código da variável|
|description|Text|Sim|Descrição da varável|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/servicecost.png)

## Service_cost
Tabela principal da taxa do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da taxa do serviço|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código da taxa|
|cost_value|Double|Sim|Valor base da taxa em euro (€)|
|cost_condition|Text|Sim|Condição de aplicação da taxa|
|cost_formula|Text|Sim|Fórmula de cálculo do valor total|
|rounding_mode|Varchar(45)|Sim|Tipo de arredondamento|
|rounding_decimal|Int|Sim|Nº de casas decimais|

## Service_cost_text
Tabela de traduções da taxa do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|channel_cost_id|Bigint|Sim|ID da taxa do serviço|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da taxa|
|description|Longtext|Não|Descrição da taxa|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/relatedservice.png)

## Related_service
Tabela de serviços relacionados.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|from_service_id|Bigint|Chave|ID do serviço origem|
|from_ service_version|Bigint|Chave|Versão do serviço de origem|
|to_ service_id|Bigint|Chave|ID do serviço de destino|
|to_service_version|Bigint|Chave|Versão do serviço de destino|
|relation_type|Varchar(45)|Não|Tipo de relação|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/service_pecialization.png)

## Service_specialization
Tabela principal das especializações de serviços.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da especialização|

|version|Bigint|Chave|Versão da especialização|
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
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|logo_id|Bigint|Não|ID do logotipo da entidade|
|last_updated|Datetime|Não|Data e hora da última atualização|
|last_validated|Datetime|Não|Data e hora da última validação|
|service_status|Varchar(45)|Não|Estado do serviço (CPSV)|
|processing_time|Varchar(1024)|Não|Tempo de processamento|
|created_by|varchar(45)|Não|Utilizador ou conector que criou a versão|
|last_updated_by|varchar(45)|Não|Utilizador ou conector que atualizou a versão|

## Service_specialization_text
Tabela de traduções das especializações dos serviços.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do serviço|
|version|Bigint|Chave|Versão do serviço|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome|
|abbreviation|Varchar(45)|Não|Sigla ou abreviatura|
|keywords|Longtext|Não|Palavras-chave|
|description|Longtext|Não|Descrição|
|description_flag|varchar(45)|Sim|Comportamento do atributo descrição|
|procedure|Longtext|Não|Descrição do procedimento|
|procedure_flag|Varchar(45)|Sim|Comportamento do atributo procedimento|
|proc_diagram_id|Bigint|Não|ID do diagrama do procedimento|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/specializationinput.png)

## Specialization_input
Tabela principal do requisito da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do requisito da especialização|
|specialization_id|Bigint|Sim|ID do serviço|
|specialization_version|Bigint|Sim|Versão do serviço|
|code|Varchar(45)|Sim|Código do requisito|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|
|replaces_code|Varchar(45)|Não|Código do requisito do serviço|


## Specialization_input_cr
Tabela de destinatários do requisito da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|specialization_input_id|Bigint|Chave|ID do requisito da especialização|
|criterion_requirement_id|Bigint|Chave|ID do destinatário|


## Specialization_input_text
Tabela de traduções do requisito da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|specialization_input_id|Bigint|Sim|ID do requisito da especialização|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do requisito|
|description|Longtext|Não|Descrição do requisito|
|related_doc_url|varchar(255)|Não|URL para documentação relacionada|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/specializationoutput.png)

## Specialization_output
Tabela principal do resultado da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do resultado da especialização|
|specialization_id|Bigint|Sim|ID da especialização|
|specialization_version|Bigint|Sim|Versão da especialização|
|code|Varchar(45)|Sim|Código do resultado|
|document_id|Bigint|Não|ID do documento|
|document_version|Bigint|Não|Versão do documento|
|replaces_code|Varchar(45)|Não|Código do resultado do serviço|


## Specialization_output_text
Tabela de traduções do resultado da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|specialization_ouput_id|Bigint|Sim|ID do resultado da especialização|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do resultado|
|description|Longtext|Não|Descrição do resultado|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/specializationlegislation.png)

## Specialization_legislation
Tabela principal da legislação da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da legislação da especialização|
|specialization_id|Bigint|Sim|ID da especialização|
|specialization_version|Bigint|Sim|Versão da especialização|
|code|Varchar(45)|Sim|Código da legislação|
|replaces_code|Varchar(45)|Não|Código da legislação do serviço|

## Specialization_legislation_text
Tabela de traduções da legislação da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|specialization_legislation_id|Bigint|Sim|ID da legislação da especialização|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da legislação|
|description|Longtext|Não|Descrição da legislação|
|related_doc_url|varchar(255)|Não|URL para página externa (ex: dre.pt)|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/specializationrule.png)

## Specialization_rule
Tabela principal da regra da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da regra da especialização|
|specialization_id|Bigint|Sim|ID da especialização|
|specialization_version|Bigint|Sim|Versão da especialização|
|code|Varchar(45)|Sim|Código da regra|
|replaces_code|Varchar(45)|Não|Código da regra do serviço|

## Spec_rule_spec_legislation
Tabela de legislação da especialização, aplicável à regra da especialização.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|specialization_rule_id|Bigint|Chave|ID da regra da especialização|
|specialization_legislation_id|Bigint|Chave|ID da especialização|


## Spec_rule_service_legislation
Tabela de legislação do serviço, aplicável à regra da especialização.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|specialization_rule_id|Bigint|Chave|ID da regra da especialização|
|service_legislation_id|Bigint|Chave|ID da legislação do serviço|

## Specialization_rule_text
Tabela de traduções da regra da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|specialization_rule_id|Bigint|Sim|ID da regra da especialização|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da regra|
|description|Longtext|Não|Descrição da regra|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/specializationcost.png)

## Specialization_cost
Tabela principal da taxa da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da taxa do serviço|
|specialization_id|Bigint|Sim|ID da especialização|
|specialization_version|Bigint|Sim|Versão da especialização|
|code|Varchar(45)|Sim|Código da taxa|
|cost_value|Double|Sim|Valor base da taxa em euro (€)|
|cost_condition|Text|Sim|Condição de aplicação da taxa|
|cost_formula|Text|Sim|Fórmula de cálculo do valor total|
|rounding_mode|Varchar(45)|Sim|Tipo de arredondamento|
|rounding_decimal|Int|Sim|Nº de casas decimais|
|replaces_code|Varchar(45)|Não|Código da taxa do serviço|


## Specialization_cost_text
Tabela de traduções da taxa da especialização do serviço.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da tradução|
|specialization_cost_id|Bigint|Sim|ID da taxa da especialização|
|language_code|Varchar(2)|Sim|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome da taxa|
|description|Longtext|Não|Descrição da taxa|


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/document.png)

## Document
Tabela principal dos documentos.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do serviço|
|version|Bigint|Chave|Versão do serviço|
|vstatus|Varchar(45)|Sim|Estado da versão do registo|
|vstart|Datetime|Sim|Data e hora de criação da versão|
|vapproval|Datetime|Não|Data e hora de aprovação da versão|
|vend|Datetime|Não|Data e hora de fim de validade da versão|
|vcomments|Varchar(255)|Sim|Comentários da versão do registo|
|code|Varchar(45)|Sim|Código da entidade|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|
|territorial_scope_id|Bigint|Sim|ID do âmbito territorial da entidade|
|doc_type_id|Bigint|Não|ID do tipo de documento|
|owner_org_id|Bigint|Sim|ID da organização dona|
|owner_org_version|Bigint|Sim|Versão da organização dona|
|logo_id|Bigint|Não|ID do logotipo da entidade|
|last_updated|Datetime|Não|Data e hora da última atualização|
|last_validated|Datetime|Não|Data e hora da última validação|
|created_by|varchar(45)|Não|Utilizador ou conector que criou a versão|
|last_updated_by|varchar(45)|Não|Utilizador ou conector que atualizou a versão|

## Document_text
Tabela de traduções dos documentos.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do documento|
|version|Bigint|Chave|Versão do documento|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome|
|abbreviation|Varchar(45)|Não|Sigla ou abreviatura|
|keywords|Longtext|Não|Palavras-chave|
|description|Longtext|Não|Descrição|
|legislation|Longtext|Não|Legislação específica do documento|
|url|Varchar(255)|Não|URL para página externa sobre o documento|


![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/documenttype.png)

## Document_type
Tabela base dos tipos de documento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|id do tipo de documento|
|code|Varchar(45)|Sim|Código do tipo de documento|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|

## Document_type_text
Tabela de traduções dos tipos de documento.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|doc_type_id|Bigint|Chave|id do tipo de documento|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome do tipo de documento|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/eservices.png)

## eservice
Tabela principal dos eServices.


|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do eService|
|version|Bigint|Chave|Versão do eService|
|vstatus|Varchar(45)|Sim|Estado da versão do registo|
|vstart|Datetime|Sim|Data e hora de criação da versão|
|vapproval|Datetime|Não|Data e hora de aprovação da versão|
|vend|Datetime|Não|Data e hora de fim de validade da versão|
|vcomments|Varchar(255)|Sim|Comentários da versão do registo|
|code|Varchar(45)|Sim|Código da entidade|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|
|territorial_scope_id|Bigint|Sim|ID do âmbito territorial do eService|
|address|Varchar(255)|Não|Endereço|
|address_type|Varchar(45)|Não|Tipo de endereço|
|owner_org_id|Bigint|Sim|ID da organização dona|
|owner_org_version|Bigint|Sim|Versão da organização dona|
|logo_id|Bigint|Não|ID do logotipo da entidade|
|last_updated|Datetime|Não|Data e hora da última atualização|
|last_validated|Datetime|Não|Data e hora da última validação|
|created_by|varchar(45)|Não|Utilizador ou conector que criou a versão|
|last_updated_by|varchar(45)|Não|Utilizador ou conector que atualizou a versão|

## eservice_text
Tabela de traduções dos eServices.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do eService|
|version|Bigint|Chave|Versão do eService|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome|
|abbreviation|Varchar(45)|Não|Sigla ou abreviatura|
|keywords|Longtext|Não|Palavras-chave|
|description|Longtext|Não|Descrição|
|consumers|Longtext|Não|Descrição dos consumidores|
|pricing|Longtext|Não|Custos associados|
|pre_conditions|Longtext|Não|Pré-condições de utilização|
|service_level|Longtext|Não|Descrição dos níveis de serviço|
|terms_conditions|Longtext|Não|Termos e condições|
|legislation|Longtext|Não|Legislação específica do eService|
|security_desc|Longtext|Não|Normas de segurança aplicáveis|
|privacy_constraints|Longtext|Não|Privacidade|


## Eservice_eservice_type
Tabela de relação dos tipos de eService associados a um eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_id|Bigint|Chave|ID do eService|
|eservice_version|Bigint|Chave|Versão do eService|
|eservice_type_id|Bigint|Chave|ID do tipo de eService|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/eservicetype.png)

## Eservice_type
Tabela base dos tipos de eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do tipo de eService|
|parent_id|Bigint|Não|ID do tipo de eService pai|
|root_id|Bigint|Não|ID do tipo de eService raiz|
|code|Varchar(45)|Sim|Código do tipo de eService|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|


## Eservice_type_text
Tabela de traduções dos tipos de eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_type_id|Bigint|Chave|id do tipo de eService|
|language_code|Varchar(2)|Chave|Código do idioma|
|name|text|Sim|Nome do tipo de eService|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/eserviceorg.png)

## Eservice_org
Tabela de relação das entidades associadas a um eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_id|Bigint|Chave|ID do eService|
|eservice_version|Bigint|Chave|Versão do eService|
|org_id|Bigint|Chave|ID da entidade|
|org_version|Bigint|Chave|Versão da entidade|
|role|Varchar(45)|Sim|Função da entidade no âmbito do eService|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/eserviceparam.png)

## Eservice_param
Tabela principal dos parâmetros do eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_id|Bigint|Chave|ID do eService|
|eservice_version|Bigint|Chave|Versão do eService|
|code|Varchar(45)|Chave|Código do eService|
|type|Varchar(45)|Sim|Tipo de dados|
|index_type|Varchar(45)|Sim|Tipo de índice|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|


## Eservice_param_text
Tabela de traduções dos parâmetros do eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_id|Bigint|Chave|ID da eService|
|eservice_version|Bigint|Chave|Versão do eService|
|param_code|Varchar(45)|Chave|Código do parâmetro|
|language_code|Varchar(2)|Chave|Código do idioma|
|desc_owner_id|Bigint|Sim|ID da entidade dona da descrição|
|desc_owner_version|Bigint|Sim|Versão da entidade dona da descrição|
|name|text|Sim|Nome do parâmetro|
|description|Longtext|Não|Descrição do parâmetro|


## Ses
Tabela de serviços associados aos eServices.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|eservice_id|Bigint|Chave|ID do eService|
|eservice_version|Bigint|Chave|Versão do eService|


## Ses_param_value
Tabela de configuração dos parâmetros do serviço no âmbito do eService.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do valor do parâmetro|
|eservice_id|Bigint|Sim|ID do eService|
|eservice_version|Bigint|Sim|Versão do eService|
|service_id|Bigint|Sim|ID do serviço|
|service_version|Bigint|Sim|Versão do serviço|
|param_code|Varchar(45)|Sim|Código do parâmetro|
|poc_id|Bigint|Não|ID do ponto de atendimento|
|poc_version|Bigint|Não|Versão do ponto de atendimento|
|division_code|Varchar(45)|Não|Código da divisão de atendimento|
|org_id|Bigint|Não|ID da entidade|
|org_version|Bigint|Não|Versão da entidade|
|param_value|Varchar(255)|Sim|Valor do parâmetro|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/admdivision.png)

## Adm_division
Tabela de divisões administrativas.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da divisão administrativa|
|parent_id|Bigint|Não|ID da divisão administrativa pai|
|type|Varchar(45)|Sim|Tipo de divisão administrativa|
|Code|Varchar(45)|Sim|Código da divisão administrativa (DICOFRE)|
|name|Varchar(255)|Sim|Nome da divisão administrativa|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|
|nuts_id|Bigint|Não|ID da região NUTS|


## Nuts
Tabela de regiões NUTS.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID da região NUTS|
|parent_id|Bigint|Não|ID da região NUTS pai|
|level|int|Sim|Nível da região NUTS|
|Code|Varchar(45)|Sim|Código da região NUTS|
|name|Varchar(255)|Sim|Nome da região NUTS|
|val_start|Datetime|Não|Data de início de vigência|
|val_end|Datetime|Não|Data de fim de vigência|

![GSD1 phenotype]({{ BASE_PATH }}/CES/assets/images/territorialscope.png)

## territorial_scope
Tabela comum do âmbito territorial dos registos do catálogo.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|id|Bigint|Chave|ID do âmbito territorial|
|type|Varchar(45)|Sim|Tipo de elementos do âmbito Territorial|

## territorial_scope_adm_division
Tabela de relação dos elementos do âmbito territorial constituídos por divisões administrativas.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|territorial_scope_id|Bigint|Chave|ID do âmbito territorial|
|adm_division_id|Bigint|Chave|ID da divisão administrativa|


## Territorial_scope_nuts
Tabela de relação dos elementos do âmbito territorial constituídos por regiões NUTS.

|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|------------|------------|
|territorial_scope_id|Bigint|Chave|ID do âmbito territorial|
|nuts_id|Bigint|Chave|ID da região nuts|
