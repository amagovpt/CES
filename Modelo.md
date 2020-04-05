
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
