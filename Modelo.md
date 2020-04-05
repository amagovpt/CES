
|Atributo| Tipo | Obrigatório|Descrição|
|------------ | ------------|
|id	|Bigint|	Chave|	Identificador principal da entidade|
|version|	Bigint|	Chave|	Versão do registo da entidade|
|vstatus|	Varchar(45)|	Sim|	Estado da versão do registo|
|vstart	|Datetime	|Sim|	Data e hora de criação da versão|
|vapproval|	Datetime|	Não|	Data e hora de aprovação da versão|
|vend	|Datetime|	Não|	Data e hora de fim de validade da versão|
|vcomment|	Varchar(255)|	Sim|	Comentários da versão do registo|
|code	\Varchar(45)|	Sim |	Código da entidade|
|val_start|	Datetime|	Não|	Data de início de vigência|
|val_en|	Datetime|	Não|	Data de fim de vigência|
|territorial_scope_id|	Bigint|	Sim|	ID do âmbito territorial da entidade|
|logo_id|	Bigint|	Não|	ID do logotipo da entidade|
|location_ID | Bigint|	Sim|	ID da morada principal da entidade|
|parent_org_id|	Bigint	|Não|	ID da organização pai|
|parent_org_version\|	Bigint|	Não| Versão da organização pai|
|org_type_id	| Bigint|	Não|	ID do tipo de organização|
|economic_activity_id|	Bigint|	Não|	ID da CAE principal|
|nipc	|Varchar(9)|	\Não| 	Número de Identificação de Pessoa Coletiva|
|last_updated|	Datetime|	Não |	Data e hora da última atualização|
|last_validated|	Datetime|	Não|	Data e hora da última validação|
|created_by	| varchar(45)|	Não|	Utilizador ou conector que criou a versão|
\last_updated_by|	varchar(45)|	Não|	Utilizador ou conector que atualizou a versão|
