# Caso de uso 

## Cenário
-  **Representa um exemplo concreto** de como satisfazer ou falhar a satisfação de uma meta
	-  Ou um conjunto delas
-  Podem ser cenários positivos ou negativos
	-  Cenários negativos
		-  O que não fazer com o sistema / ataques ao sistema
-  **Cenário não é um requisito**
	-  **Mas representa um conjunto deles**

## Caso de Uso
- **Uma representação de requisitos em cenários**
- Representa a interação entre Atores e o Sistema
- **Ator:** `Alguém ou algo fora do software que interage com o software`
- **Descreve como o sistema e seus atores colaboram para atender a pelo menos uma meta dos atores**
- #!#!#!#!#!#!#!#!# **Foco nos requisitos funcionais** #!#!#!#!#!#!#!#!#
- É um **conjunto de ações** do sistema que **gera um resultado de valor** a um *ator*
	- O **resultado** deve ser algo **observável**
	- O **caso de uso deve ser algo útil** para o *ator*
		- **Não** é uma **mera função** do sistema
		- O ator primário precisa ficar **satisfeito** após a execução do caso de uso
		- Ex: 
			- Procurar produtos
			- Faz compra
			- Acompanhar status da compra
- **Representa-se ações do sistema e do ator** 
	- Tipicamente **intercala-se ações do ator com do sistema**

<br>

- #!#!#!#!#!#!#!#!#  **Caso de uso não é uma função do sistema** #!#!#!#!#!#!#!#!# 
	- Decomposição funcional
		- Perde-se a noção do que o sistema faz
	- Foco deve ser no **OBJETIVO** do *ator*
- Casos de Uso **SEM** sentido:
	- Ex: "hoje estou afim de fazer um pagamento"
	- Ex: "hoje estou afim de colocar um produto no carrinho de compra"
- Agrupando conceitos que no fim farão sentido para o cliente
	- (Adicionar produto + realizar pagamento + escolhe frete) + (Alterar quantidade de produtos + remove produto)
			- **Resultado:** Procura Produtos & Faz Compra
- Mais Exemplos:
	- Uber 
		- `Fazer corrida` vs  ~~Iniciar corrida, terminar corrida~~
	- Instagram
		- `Fazer publicação` vs ~~Dar um like, comentar~~ 

<br>

- Pode ser usado para requisitos do sistema, software ou de stakehodlers
	- Escopo
		- Processo de negócios, sistema, software ou função (técnico)
		- Nivel de abstração
			- Nível sumário [nível das nuvens]: várias metas de usuários (**Alto nível de abstração**)
			- Metas do usuário [nível do mar]: usuário primário fazendo algo importante para ele, **um meta específica para um usuário específico**
			- Subfunção [nível concha]: detalhes de uma meta do usuário

## Diagrama de Casos de Uso
### Vantagens
- Facilicade de ler e escrever, pois usa linguagem natural
- Escrito na linguagem/perspectiva do usuário
- Permite relacionar as atividades de requisitos às atividades de projeto e implementação
	- Rastreabilidade
- Facilidade para gerar um caso de teste
- Organiza os requisitos em grupos

### Desvantages 
- Não representa adequadamente:
	- Algoritmos e fórmulas matemáticas
	- Requisitos não funcionais
	- Restrições
	- Imprecisão (linguagem natural)
- **Observação: o caso de uso deve ser apenas parte de um documento de especificação de requisitos**

### Representação
- Casos de uso podem ser representados usanso diferentes formatos
	- Diagramas
		- Diagrama de caso de uso
		- Diagrama para representar o comportamento
	- Texto
		- Narrativo ou estruturado
		- Uso de tabelas para representar a interação
		- Observação: não há um padrão para representação textual

### Dicas - Ator
- **Nem todo stakeholder é ator**
	- **Precisa interagir com o sistema para ser ator**
- Atores não são necessariamente pessoas
	- Podem ser outros sistemas ou
	- Hardware (impressora, leitora, etc.)
- O **nome do ator representa o papel dele** ao usar o sistema
	- **Não** é o cargo da pessoa
		- ~~Gerente de Vendas / Diretor comercial~~ → Gerente
- **Não** é o nome da pessoa
	- ~~Fábio~~ → Administrador

### Dicas - Caso de Uso
- Use nomes no presente / infinitivo para nomear o caso de uso
	- Algo que o ator faz no sistema (**ação**)
	- Representa o objetivo do ator
- Pense no que o ator precisa fazer
	- **Caso de uso é algo de valor ao ator**
- Se pergunte: `Fazer simplesmente isso é útil para o ator? Ele fica satisfeito?` 

### Conclusão Diagrama
- O diagrama não tem os detalhes do caso de uso
	- só diz: **nome e ator envolvido**
	- Quais são as ações?
	- Como funciona o caso de uso?
	- **É só um sumário**
- Existem outros detalhes
	- Extensão (extends)
- Generalização de casos de uso
	- (Não é mais permitida na UML 2.5.1)

## Representação textual de caso de uso
- Permite detalhar a sequência de ações
	- **Descrever o que o sistema faz, *sem especificar como***
		- O "como" é detalhado na atividade de projeto (design)
		- **Não detalhar interface homem-computador**
- Existem diversas abordagens
	- Diferentes formatos, regras e técnicas de redação
	- Foco em caso de uso representando requisito de software
		- Aqui será baseada em (COCKBURN, 2000) e (LEFFINGWELL; WIDRIG, 2003)

### Elemetos Típicos
- **Nome**: Nome do Caso de Uso (frase curta)
- **Descrição**: Texto breve (1 paragrafo ou 2 frases que apresenta o propósito do caso de uso)
- **Atores**: Atores envolvidos no Caso de Uso
- **Pré-Condição**: Condição do **sistema** que precisa ser verdadeira para que o caso de uso **inicie** (é a condição do SW que precisa ser verdadeira para o caso de uso iniciar  - não é condição do ator!!!)
- **Fluxo básico**:  **Sequência de ações** mais comum e/ou de maior valor (fluxo que da mais atenção, temos que tomar mais cuidado com ele)
- **Pós-condição**: "Condição do sistema que precisa ser verdadeira ao fim da execução do fluxo básico
- **Fluxos Alternativos**: Sequência de ações que trata de desvios de um fluxo (básico ou alternativo) desvios do fluxo básico
- **Requisitos Especiais**

#### Exemplo
```
UC1. Processa venda
- Descreve o processamento da venda de produtos escolhidos por um cliente em um ponto de atendimento do supermercado, por um caixa.

Atores
- Caixa
- Operadora do cartão
- Cliente

Pré-condição
- Atendente logado e sem venda aberta

Fluxo básico
1. Para cada produto da venda:
	a. O caixa informa o código do produto
	b. o software apresenta a descrição e o preço do produto corrente
	c. o caixa confirma o produto
2. o caixa finaliza a vendda
3. o software apresenta o total e solicita a forma de pagamento
4. o caixa informa que será pagamento em dinheiro e informa o valor pago
5. o software apresenta o troco, imprime o recibo e finaliza a venda

Fluxos Alternativos
FA1: Caso haja mais de uma unidade do mesmo produto (passo 1.c)
1. o caixa informa a qtd do produto
2. o software apresenta a descrição e o preço unitário do produto, a qtd e o valor total para o produto
3. o caixa confirma o produto (e volta para o passo 1 do fluxo básico)

FA2: : O Caixa informa que o pagamento é em cartão (Passo 4):
1. O Software solicita o número.
2. O Caixa informa o número do cartão.
3. O Software solicita a senha.
4. O Cliente informa a senha.
5. O Sistema informa a Operadora de cartão o número e a senha.
6. A Operadora de cartão confirma o pagamento.
7. O Sistema confirma o pagamento e imprime o recibo

Pós-condição: venda fechada
```

### Pré-condição
- **Condições do sistema**
	- Não ser algo externo do sistema, pois não tenho controle
		- Caso haja sistema externo, é possivel colocar o seguinte: `Comunicação com sistema externo está funcionando`
	- O sistema precisa ser capaz de avaliar antes de o caso de uso iniciar
	- Se forem falsas, o caso de uso nem se inicia
		- Você pode usar **E (and)** e **OU (or)** para especificar a lógica
	- **Podem ser resultados de outros casos de uso**
		- Exemplo: compra efetuada
	 
### Pós-Condição
- **Ajuda o leitor a entender o resultado da execução do caso de uso**
	-  **#!#!#!#!#!#!#!#!#** Condições do sistema  **#!#!#!#!#!#!#!#!#**
	- **Não pode colocar como pós condição, cenários que envolvam o ator, pois ator é externo e não é possível avaliar.**
		- Exemplo: ~~usuário satisfeito~~ (não é possível avaliar)
- Várias semânticas possíveis
	- válida para qualquer fluxo
	- válida apenas para o fluxo básico ( #!#!#!#!#!#!#!#!# **professor adotou essa daqui** #!#!#!#!#!#!#!#!#)

### Ações em fluxos
- Numere as ações
- Represente o agente que executa a ação
	- Exemplo: O **Funcionário** confirma... / O **Sistema** informa...
- Detalhe as informações necessárias
	- Exemplo: O Gerente deve informar o nome e o CPF do cliente
		- Se não estiver especificado, seria necessário conversar com alguém para definir o que
		precisa informar...
		- Se forem muitos, pode-se colocar uma lista na forma de itens
			- Exemplo: O usuário informa:
			- Nome
			- Telefone
			- Endereço
- Siga boas práticas de redação de requisitos
	- Não use adjetivos/advérbios/comparações
		- Exemplo: O Cliente deve selecionar facilmente os produtos
	- Evite pronomes vagos
		- Exemplo: O Sistema envia um e-mail ao Gerente com isso
	- Evite linguagem subjetiva
		- Exemplo: O Gerente deve informar os dados
	- Não use negações
		- Exemplo: O Cliente não deve selecionar um produto indisponível
	- Não apresente detalhes de interface 
		- Exemplo: O Usuário clica na janela...
	- Evite detalhes de implementação 
		- Exemplo: O Sistema salva no banco de dados as informações...
	- Evite sinônimos para conceitos usados
		- Exemplo:
			1. O sistema apresenta a descrição do produto
			2. O Funcionário informa o texto explicativo do produto

### Fluxo Alternativo
- Também chamado de **extensão** (pode ser confuso)
-  Especifique claramente a condição e o passo
	- Exemplo: Caso o produto esteja em falta (passo 3)
- Considere que o passo do fluxo original não será executado devido à condição
	- Exemplo
	```
		1.c. O Caixa confirma o produto.
		...
		FA1: Caso haja mais de uma unidade do mesmo produto (Passo 1.c):
	```

- Pode haver um **fluxo alternativo de um fluxo alternativo**
	- Numere o fluxo alternativo
	- Exemplo
		- FA2: O Caixa informa que o pagamento é em cartão (Passo 4)
		- FA3: O Cartão é inválido (Passo FA2.6)
-  **O fluxo alternativo pode terminar o UC ou retornar ao fluxo original**
	- Indique claramente isso
	- Exemplo
		- O caso de uso termina.
		- ...e volta para o passo 1 do fluxo básico


## Exemplo 1 - Use Case - Capture Trade-in
- Description:
	- the shopper has a shopping cart containing products and wants to add a trade-in to see how it will affect costs
- Actors
	- Shopper
- Preconditions
	- the shopping cart must contain products

- Basic Scenario
	1. Shopper selects to capture a trade-in
	2. system determines the value of trade-in by presenting information to the shopper and asking a series of questions to determine the value of the trade-in. The series of questions and information presented depend on the answers the shopper gives along the way. The path of questions and information is predetermined, in order to highlight probable business practices arround trade-ins
	3.  Shopper reviews the trade-in summary and value, considers it.
	4. Shopper adds it to the shopping cart.
	5. System adds to the shopping cart the trade-in and the navigation information
	6. System presents a view of the shopping cart with all the products and trade-ins contained in it, as well as re-calculating the total cost taking into consideration the trade-in(s)

Shopper repeats the above steps as many times as desired to capture and value different trade-ins, adding them to the shopping cart as desired.

- **Alternatives Flows**
2a. At any time prior to adding the trade-in to the cart, the shopper can go back and modify any previous answer.
4a. Shopper decides not to add the trade-in to the shopping cart: System retains the navigation information for later.
4b. Shopper wants the trade-in to be applied to a specific item in the shopping cart: Shopper specifies a product contained in the shopping cart they wish the trade-in to be applied against

- Post-condition
	- The trade-in has been valued, added to the shopping cart, and has reduced the cost of the items contained in the shopping cart.

## Exemplo 2 - Use Case - Order Goods, Generate Invoice
- Description
	- customer places order for goods, and invoice is generated and sent out with the ordered items.
- Actor
	- Customer

- Main success scenario
	1. Customer selects items and quantities.
	2. System allocates required quantities to customer.
	3. System obtains authenticated invoicing authorization.
	4. Customer specifies shipping destination.
	5. System send picking instructions to distribution.

- **Alternatives Flows**
	2a. Insufficient stock to meet required quantity for item:
	2a1. Customer cancels order.
	2b. Out of stock on item:
	2b1. Customer cancels order.
	3a. Customer is bad credit risk (link to acceptance test case for this exception).
	4a. Invalid shipping destination: ??

- Post-condition
	- Goods will have been allocated to the Customer.
	- Invoice will have been created (Customer Invoicing Rule applies).
	- Picking list will have been sent to distribution.
Use Case 21, 22, 32(CRUD) ,, 37-



## Dicas
- **Cada caso de uso precisa ter valor para um ator (pelo menos)**
- Quando fazer caso de uso, focar em um único ator
	- Exemplo de inagação - "Com o que o ator médico ficaria satisfeito?"
- **Caso de uso é detalhado o suficiente para um desenvolvedor implementar**
- O médico está fazendo mais do que atualizar um prontuário, ele está atendendo e durante o atendimento as operações do sistema podem ser mais complexas que CRUD
