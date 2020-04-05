# Catálogo de Entidades e Serviços

# Organização (ou Entidade)
Representam um organismo público ou entidade privada. As entidades podem ter subentidades (ou depender de uma entidade hierarquicamente acima). Cada entidade define a sua morada principal ou sede. Não existem outras moradas no catálogo.
## Exemplos de entidades:
* Agência para a Modernização Administrativa
* Loja do Cidadão das Laranjeiras (subentidade da entidade AMA)
* Direção Geral das Atividades Económicas
* CTT
* Loja dos CTT de Arroios (subentidade da entidade CTT)

## Divisão de Atendimento
Um ponto de atendimento pode definir divisões e associar serviços a cada divisão de atendimento. Este conceito pode ser utilizado para representar a divisão interna de serviços de um ponto de atendimento. Nos casos em que se aplique, as divisões podem ser utilizadas para representar as senhas de um ponto de atendimento presencial.
Exemplos de Divisões de Pontos de Atendimento:
* Atendimento Presencial da Loja de Alcântara da Câmara Municipal de Lisboa 1
* Atendimento Geral
* Apoio à Integração do Imigrante
* Habitação Municipal
* Urbanismo e Obras
* Balcão do IRN da Loja do Cidadão das Laranjeiras 2
* Senha A – Piso 0 – Cartão de Cidadão – Pedido de Alteração de Morada
* Senha B – Piso 1 – Cartão de Cidadão – Levantamento/Cancelamento/Confirmação de Morada/2º Via
* Carta PIN
* Senha C – Piso 1 – Passaporte – Levantamento
* Senha D – Piso 1 – Passaporte – Pedido

## Serviço Público (ou simplesmente Serviço)
Representa os serviços propriamente ditos. Nem sempre é fácil definir de forma clara o conceito de serviço público ou distinguir serviços de outros conceitos do catálogo (como pontos de atendimento, serviços eletrónicos ou até etapas do procedimento de um dado serviço). Até porque nem sempre existe uma única forma de representar os mesmos conceitos. Assim utilizamos aqui o conceito de serviço tal como foi definido no âmbito do Core Public Service Vocabulary1 (e que esteve na base da modelação de dados do CES):

 Um Serviço Público é um conjunto obrigatório ou discricionário de atos executados ou que podem ser realizados por ou em nome de uma organização pública. Os serviços podem ser em benefício de um indivíduo, empresa ou outra autoridade pública, ou grupos de qualquer um destes. A capacidade de agir existe quer seja (o serviço) usado ou não, e o termo "benefício" pode ser aplicado no sentido de permitir o cumprimento de uma obrigação. Conforme definido na versão revista do Quadro Europeu de Interoperabilidade, o serviço público europeu compreende todos os serviços prestados pelas administrações públicas da Europa, ou por outras organizações em seu nome, a empresas, cidadãos ou outras administrações públicas.
Com base na definição acima, e no conhecimento da equipa envolvida na construção do CES, deixamos algumas regras que podem ajudar na correta identificação e caracterização de serviços:


### Um serviço deve ter sempre um objetivo claro e bem definido;
### Deve ser relativamente simples identificar e descrever de forma clara:
### A quem se destina o serviço;
- Quais são os requisitos necessários para a realização do serviço;
-  Qual o procedimento genérico envolvido na realização do serviço;
-  Qual é o tempo de processamento médio estimado para a realização do serviço (desde o pedido até à sua finalização);
- Quais são os resultados produzidos pelo serviço;
- Que taxas se aplicam à realização do serviço.

### Um serviço deve produzir sempre, pelo menos, um resultado.
- Se não é claro definir qual é o resultado da realização de um serviço, há uma grande probabilidade de não se tratar de fato de um serviço.


Posto isto, nem sempre é fácil definir as fronteiras de um serviço ou a granularidade utilizada na definição de serviços.
### Exemplo:
- Alteração da morada do cartão de cidadão:
- Pode ser descrito como um único serviço – que resulta na alteração da morada;
Ou como dois serviços distintos:
- Pedido de alteração de morada – que resulta na receção de uma carta com os códigos de confirmação;
- Confirmação de morada – que requer os códigos de confirmação e resulta na confirmação efetiva da morada;

### Ocupação de Espaço Público
- Pode ser descrito como um único serviço – com critérios ou taxas distintas conforme o tipo de instalação;
- Ou como N serviços, um por cada tipo de instalação;

Qualquer uma das soluções apresentadas nos exemplos acima pode ser defendida como uma interpretação válida do conceito de serviço. A decisão sobre a opção a escolher deve ter em conta aspetos como a simplificação e a clareza na apresentação dos serviços aos seus destinatários ou a facilidade na gestão da informação do serviço ou conjunto de serviços.

## Destinatários do Serviço
Representam o público-alvo a quem se destina o serviço, bem como eventuais critérios de elegibilidade necessários à sua realização. A descrição de um destinatário de um serviço é interna ao próprio serviço. Isto é, específica de cada serviço. Cada destinatário pode no entanto estar associado a um determinado “Tipo de Consumidor”. Os “tipos de consumidor”, por sua vez, estão pré-definidos numa das taxonomias ou vocabulários controlados do catálogo.

Exemplos de Destinatários de Serviço:
- Cidadãos residentes na Área Metropolitana de Lisboa
- Cidadãos maiores de idade
- Proprietário do estabelecimento comercial
- Representante legal do proprietário do estabelecimento comercial

## Requisitos do Serviço
Representam as evidências necessárias à realização do serviço. Estas evidências podem, por sua vez, corresponder a documentos descritos no catálogo de documentos do CES.
Os requisitos do serviço podem ser definidos ao nível:
- Do próprio serviço;
- De uma especialização do serviço;
- De um canal do serviço.

Exemplos de requisitos de serviço (e a sua relação com eventuais documentos):
- Identificação do titular do estabelecimento – Cartão do Cidadão
- Cópia simples da caderneta predial urbana – Caderneta Predial Urbana
- Termo de responsabilidade, subscrito pelo titular do estabelecimento
-Comprovativo de morada

## Resultados do Serviço
Por definição, um serviço deve sempre produzir um resultado qualquer. Ou não faria sentido realizar o serviço. O resultado de um serviço pode ser um determinado documento, uma autorização, ou qualquer outro tipo de resultado menos tangível.

Os resultados do serviço podem ser definidos ao nível:
- Do próprio serviço;
- De uma especialização do serviço;
- De um canal do serviço.

Exemplos de resultados de serviço:
- Emissão do cartão do cidadão – Cartão do Cidadão
- Confirmação da alteração de morada do cartão do cidadão (não produz qualquer documento, simplesmente altera a morada associada ao documento existente)
- Resposta formal ao pedido do serviço “A minha rua” com a indicação de eventuais ações a tomar pelas entidades competentes
