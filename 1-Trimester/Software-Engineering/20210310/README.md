# Engenharia de Requisitos

## Definição - Engenharia de Requisitos
função interdisciplinar que mediaa entre os domínios do adquirente e fornecedor para **estabelecer e manter** os requisitos a serem atendidos pelos sistemas, software ou serviço de interesse (ISO, 2018)

## Motivação
- defeitos de requisitos são caros
	- custo relativo para corrigir defeitos

- descobrir defeitos durante a fase de levantamento de requisitos diminui o custo a longo prazo do projeto

- Algumas razões para projeto de software falharem
	- nao entender as necessidades do negocio
	- falta de habilidade de chegar a um consenso de prioridades
	- não começar com o cliente final
	- etc

TODO imagem slide:2

## Problemas que geram defeitos no levantamento dos requisitos
- Envolvimento baixo do usuário insuficiente
- planejamento impreciso
	- planejamento feito com poucas informações
- aumento incontrolável dos requisitos
- ambiguidade dos requisitos
- requisitos desnecessários
	- funcionalidade que "usuário vai adorar"
- stakeholders menosprezados
- dificuldade de o stakeholder expressar o que quer
- dificuldade de o Engenhaia de Requisitos entender o stakeholder

## "O cliente não sabe o que quer"
o cliente sabe o que ele quer, mas o problema é que o cliente não sabe expressar/explicar o que ele quer.

- dificuldade de o stakeholder expressar o que quer
- dificuldade de o Eng. Req. entender o stakeholder

- ... as vezes eles não sabem bem o que querem
	- processo criativo -> Eng. Req. e stakeholders
	- mas eles sabem **porquê** querem

## Definição - Stakeholder
- pessoas ou organizações que tem um interesse no sistema a ser desenvolvido (Pohl,2021)
- pode ser considerada fonte de requisitos
- **desenvolvedor é stakeholder?** Sim, ele leva opções de solução que podem influenciar requisitos, necessidades etc.
- agencias reguladoras são stakeholders

## Definição - Requisito
- uma afirmação que traduz ou exprerssa uma **necessidade** e suas **restrições** e condições associadas.

### Por que devemos evitar colocar detalhes de implementação nos requisitos?
- porque dessa forma você está restringindo o leque de opções que pode ser utilizado para a implementação.

## Requisitos Funcionais vs. Não Funcionais vs. Restrições
### Requisitos Funcionais
- especificam a funcionalidade que os sistema deve prover aos usuários
	- Resultados de operações a serem automatizadas
	- condições sob as quais as operações devem ser aplicadas
	- exemplos
		- validações das entradas
		- sequência exatas de operações
		- respostas para a situações anormais
		- relações entre saídas e entradas

- **ex:** 
	- O software deve permitir a busca de produtos por palavra chave
	- Um usuário pode adicionar um produto disponível ao carrinho de compras

### Requisitos não funcionais
- definem propriedades de qualidade para sistemas
	- restringem os requisitos funcionais
	- também chamados de requisitos de qualidade
- **ex:** 
	- A verificação do cadastro do usuário deve demorar no máximo 5s
	- Apenas um técnico com privilégios de Administrador deve ter acesso aos logs do sistema

TODO imagem slide:14

### Retrições
- Restrição organizacional ou tecnológica que afeta como o software deve ser desenvolvido
	- Orçamento, plataformas, linguagens, leis, soluções tecnológicas etc.
	- Muitas vezes considerada como requisitos não funcionais
- **ex:**
	- A interface web deve usar o framework React
	- O software deve ser entregue até dia 02/06
	- O projeto deve usar Scrum

## Requisitos
- TODO

- importante perguntar o "porquê" -> metas
	- provêm um racional para o requisito
	- TODO
### Metas
- Objetivos que o software deve atingir
- Em geral são apresentadas de forma vaga
- exemplos:
	- TODO

## Atividades de ER
### Elicitação
- Objetivo: Elicitar todos os requisitos no nível adequado para o sistema a ser desenvolvido
- Necessário Documentar
- Quais são as fontes de requisitos?
	- Stakeholders
	- Documentos existentes
	- Sistemas existentes

### Documentação

### Negociação
- Stakeholders tem diferentes interesses e necessidades
	- Contradições e dificuldades de atender a todos
- Tipos de conflitos:
	- DE INTERESSE: diferentes metas/requisitos
	- DE VALOR: Importância dos requisitos
	- DE DADOS: interpretação diferente
### Verificação e Validação
- Garantir que os requisitos são adequados
	- Validação com os stakeholders
		- protótipos
		- revisão
		- simulação

- Verificar Propriedades dos modelos
	- Métodos formais
	- revisões ténicas
	- argumentação

### Gestão de Requisitos
- Principal atividade é a gestão dos artefatos
- Priorização dos requisitos
- Rastreabilidade 
	- TODO get Image:25

## Caso de Uso
- Representação de requisitos em **cenários**
- Cenário: representa um exemplo concreto de como satisfazer ou falhar a satisfação de uma meta
- Representa a interação entre Atores e o Sistema

-> o que o ator faz --> o que o sistema faz

## História Usuário
TODO


