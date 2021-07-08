## Negociação
- stakeholders têm diferentes interesses e necessidades
	- contradições e dificuldades de atender a todos
- alguns tipos de conflitos 
	- de interesse: diferentes metas/requisitos
	- de valor: importânce dos requisitos
	- de dados: interpretação diferente

<br>

- atividades 
	- identificar conflitos
	- identificar a causa dos conflitos
	- resolver os conflitos
	- **documentar a solução do conflito e o racional**

<br>

- como solucionar conflitos?
	- negociação
	- solução criativa
			- uma pessoa quer **a**, outra quer **b**, a solução é **c**
	- decisão

## Gestão de Requisitos
- a principal atividade é a **gestão dos artefatos**
- Priorização dos requisitos 
- Rastreabilidade dos requisitos 
	- Relação dos requisitos com outros elementos 
- Gestão de mudanças
	- Identificar e tratar das mudanças nos requisitos

### Rastreabilidade
- definição
	- habilidade de descrever e seguir a vida de umrequisito, tanto na direção para frente ou para trás
	- rastreabilidade para trás
		- requisito para seus artefatos predecessores
		- Exemplo: plano de negócio e documentos
	- Rastreabilidade para frente (ou pós rastreabilidade)
		- Requisito para seus artefatos posteriores
		- Exemplo: classes, casos de teste e código fonte
- algumas representações
	- Texto com hyperlinks
	- matrizes de rastreabilidade
	- grafos de rastreabilidade

<br>

#### Algumas vantagens
- Apoia a validação dos requisitos
- Permite identificar funcionalidades não especificadas
	- Sem justificativa para implementar
- Permite identificar requisitos não implementados
- Facilita a gestão de mudanças
- Facilita o gestão de riscos
- Permite a determinação de responsabilidade
	- (Pode ser importante em questões judiciais)

<br>
#### problemas
- custo e complexidade de rastrear
- custo de manter a rastreabilidade

---

- não é necessário ter uma rastreabilidade completa
	- ...não precisa ser bidirecional...
	- é importante planejar
	- alguns softwares precisam: software críticos
- Existem ferramentas para apoiar a rastreabilidade
- Jira + Confluence
- IBM Engineering Requirements Management DOORS Next

## Gestão de Mudanças
- Requisitos Mudam
	- falha no entendimento
	- problema mudou
	- contexto mudou
	- usuários e stakeholders mudaram de ideia
	- resultados não foi o esperado
- Outras mudanças relacionadas
	- prioridade
	- escopo
	- software/release
- Importante gerenciar as mudanças
	- avaliar se a mudança é apropriada
	- stakeholders afetados são informados
		- podem tomar decisões apropriadas
	- projeto absorve mudanças de ma forma organizada
	- ...mudanças de requisitos impactam no custo, prazo e na qualidade (RNFs)
	- é parte do processo de gestão de configuração
		- trata de mudanças em qualquer item ded configuração
- Processo formal para tratar das mudanças
	- mantêm  a integridade dos itens
- Falarei genericamente (não só para requisitos)
	- Vale para mudanças de requisitos ou outras mudanças em itens de configuração
- Detalhes
	- Cada item precisa ser identificado
		- No caso de requisitos: história, caso de uso, etc.
	- Trata de solicitações de mudança

## Solicitação de Mudança
- Documento com a requisição de mudança
	- Dados sobre a solicitação e sobre a sua análise
	- Exemplo
		- Origem da solicitação
		- Datas (solicitação, análise, aprovação etc.)
		- Descrição
		- Status da mudança (ativa, aprovada, fechada etc.)
		- Prioridade
		- Resultados da avaliação e das análises
		- Decisões tomadas
		- Comentários

## Análise
- Necessário analisar a solicitação de mudança
	- ponto de vista técnico
		- avaliação da mudança
		- análise de custo e impacto
	- ponto de vista estratégico e organizacional
- Avaliação da mudança (técnico)
	- Avaliar se a solicitação merece uma ação
		- Nem todas as solicitações são válidas...
			- Não é possível replicar o problema
			- Problema / melhoria já relatada
			- Pedido já implementado
			- Não é um problema – é como o software deve funcionar
	- Responsável: suporte ou desenvolvedor


Acceptance Criteria defines how a particular feature could be used from an end user’s perspective. t focuses on business value, establishes the boundary of the feature’s scope and guides development. These are unique to a user story and form the basis of user story acceptance testing which establishes the conditions for the success of the feature.

Acceptance criteria could establish a boundary that helps team members to understand what’s included and what’s excluded from the scope of the user story.
