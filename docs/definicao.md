# Catálogo de Entidades e Serviços
No sentido de melhor agregar num ponto único (e sob um conceito comum) todos os serviços
disponíveis ao cidadão e à empresa, a AMA desenvolveu a aplicação “Catálogo de Entidades e
Serviços” (CES) disponível em modelo Software as a Service (SaaS), na qual serão parametrizados
todos os serviços públicos disponibilizados.

## Definições
[Consultar as definições](definicao)

## Modelo de Dados
[Consultar o modelo de dados](modelo)

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

## Legislação do Serviço
Refere-se à legislação específica, ou regulamento, que caracteriza o serviço, como por exemplo o diploma que dá origem à criação do serviço.
A legislação do serviço pode ser definida ao nível:
- Do próprio serviço;
- De uma especialização do serviço.

Exemplos:
 -Decreto-Lei n.º 128/2014 – que estabelece o regime jurídico da exploração dos estabelecimentos de alojamento local

## Regras do Serviço
A legislação aplicável a um serviço pode, geralmente, ser decomposta (ou implementada) por um conjunto de regras bem definidas, a verificar no âmbito da realização do serviço.

As regras do serviço podem ser definidas ao nível:
- Do próprio serviço;
- De uma especialização do serviço.

Exemplos de regras do serviço:
- A vitrina não pode exceder 0,10 m de balanço em relação ao plano da fachada do edifício
- Os estabelecimentos de alojamento local devem dispor de livro de reclamações

## Taxas do Serviço
Representam as taxas legais ou outros custos a cobrar pela realização do serviço.
Um serviço pode definir um número ilimitado de taxas. Cada taxa define uma condição para que seja, aplicada, um valor base, e uma fórmula de cálculo do valor final a aplicar, com base nos dados específicos de cada pedido.

As taxas do serviço podem ser definidos ao nível:
- Do próprio serviço;
- De uma especialização do serviço;
- De um canal do serviço.

Exemplos de taxas:

- Custo mensal para instalação de floreira por metro quadrado – 2,72 €
- Custo mensal para instalação de estrado por metro quadrado – 1,15 €
- Cartão de Cidadão – Pedido normal com entrega em território nacional – 15,00 €
- Cartão de Cidadão – Pedido normal com entrega no estrangeiro – 20,00 €


## Canal do Serviço

O Canal de Serviço representa a relação entre um ponto de atendimento e um serviço. Isto é, representa um meio disponível para realização do serviço, ou para obtenção de informação sobre o mesmo. Cabe aos pontos de atendimento definirem os serviços que prestam, e caracterizar essa relação. Analisando a relação inversa, ou seja, do ponto de vista de um serviço – um serviço pode estar disponível em vários canais, correspondendo cada um deles a um ponto de atendimento específico. O canal de serviço pode ser de dois tipos:

- Transacional – Permite a realização do serviço;
- Informativo – Presta informações sobre o serviço;

O canal de serviço pode redefinir ou acrescentar informação ao serviço como por exemplo taxas -a aplicar, requisitos ou até resultados específicos quando o serviço é realizado pelo canal em causa.

## Especialização do Serviço
As especializações de serviços representam as particularidades aplicadas por cada entidade competente local, no âmbito de serviços regulados pela administração central.
A entidade dona de uma especialização do serviço deve obrigatoriamente constar da lista de entidades competentes do serviço central.
No âmbito de uma especialização de serviço é possível redefinir ou acrescentar requisitos, resultados, regulamentos ou taxas ao serviço central.

Exemplos de especializações de serviço:
- Ocupação de Espaço Público – Câmara Municipal de Lisboa
- Ocupação de Espaço Público – Câmara Municipal de Porto
- Ocupação de Espaço Público – Câmara Municipal de Faro

## Documento
Representam os documentos produzidos ou requeridos pelos serviços do catálogo.
Um aspeto fundamental do catálogo de documentos é que, através da sua relação com o catálogo de serviços, é possível inferir relações de dependência entre os serviços que requerem ou produzem um determinado documento (referido nos requisitos e resultados dos serviços). Este tipo de informação pode ser extremamente útil na forma como são apresentados os serviços aos utilizadores no Portal do Cidadão, por exemplo. Ou na definição de pacotes de serviços interdependentes.
Exemplos de Documentos:
- Cartão do Cidadão
- Carta de Condução
- Caderneta do Registo Predial
- Certidão Permanente de Registos
- Certificado do Registo Criminal

## eService (ou Serviço Eletrónico)
Representam os serviços eletrónicos que suportam a realização de serviços públicos. Os eServices podem corresponder a WebServices, APIs JSON ou a qualquer componente tecnológica de alto nível com responsabilidades bem definidas no âmbito da realização de serviços.
Exemplos de eServices:

- WebService da Câmara Municipal de Lisboa para envio de informações relacionadas com os pedidos de serviços pelos quais a entidade é responsável;

- eForms – Componente da AMA responsável pela apresentação e recolha de dados dos formulários dos serviços;
- BPM – Componente da AMA responsável pela configuração e execução do processo de negócio que suporta a realização dos pedidos de um serviço;
- FA – Componente da AMA responsável pela configuração e autenticação de utilizadores no âmbito da realização de serviços;
- SIGA – Sistema de Informação para Gestão do Atendimento
