# Software Product Line (SPL)
SPL ou linha de produto de software corresponed a um paradigma para desenvolver software aplicativo (sistemas e produtos de software) usando plataforma e customização em massa


## Software Product Line Engineering (SPLE)
Motivações para adotar a abordagem de Software Product Line Engineering (SPLE)
- Reduction of Development Costs 
- Enhancement of Quality 
- Reduction of Time to Market

```
questão de 28/6/21: quais são os conceitos básicos de SPLE?
```

1. Customização em massa (mass customization) – corresponde a produção em massa de bens de consumo (aplicações) customizada para atender às necessidades individuais.
2. Plataformas (platform) – qualquer base tecnológica em que se constrói outros processos ou tecnologias (sub produtos ou funções/funcionalidade que atendam um conjunto de requisitos do usuário).

<br>

- **Platforms are prerequisites for mass customization**

<br>

- Plataforma de software (software platform) – conjunto de subsistemas de software e interfaces que formam uma estrutura comum onde podem ser desenvolvidos e produzidos os derivativos de software.

### Variabilidade (ou Flexibilidade)
A variabilidade é sinônimo de flexibilidade 
- Variabilidade – é um item variável do mundo real ou uma propriedade variável do item. 
- Permite a escolha dentre diferentes opções
- Variabilidade objeto – é uma instância particular da variabilidade
- Ponto de variação – é a representação da variabilidade no domínio dos artefatos enriquecidos por informação contextualizada. 
- Variante – corresponde a representação do objeto da variabilidade dentro do domínio de artefatos. Uma das possíveis opções a ser escolhida.

### Grupos de Processos
1. Engenharia de Dominio - Define a **uniformidade** (visões ou interfaces uniformes) e **variabilidade** da linha de produto de software
2. Engenharia de Aplicação -  corresponde ao desenvolvimento das aplicações por meio de **reuso de artefatos do domínio** e exploração variabilidade

## Engineering customized products
### Criação da Plataforma 
- fase de preparação para a customização 
	- **Primeiro - pontos comuns** 
	- em seguida, a diferenciação

### Introdução de flexibilidade (Variabilidade) 
- os artefatos a serem usados pelos diferentes produtos devem ser suficientemente adaptáveis aos diferentes produtos a serem produzidos em linhas de produção 
- base para a customização em massa

### Reorganização
- Migrar de produção single-system engineering para uma abordagem de product line engineering tem algumas consequências: 
	- Uma unidade responsável pela Plataforma 
	- Outra responsável pelos produtos derivados (customizados)

### Diagrama Domain Engineering & Application Engineering
- Desenvolvimento de artefatos – é o resultado da engenharia de domínio ou de aplicação 
- Artefatos de domínio – são os artefatos criados sob a engenharia de domínio para posterior reuso
- Artefatos de aplicação – correspondem aos artefatos desenvolvidos para uma linha específica de aplicação
- Sub-processos da Engenharia de Domínio
	- Gerenciamento do Produto
	- Engenharia de Requisitos de Domínio
	- Desenho do Domínio
	- Realização (Implementação) do Domínio 
	- Testes do Domínio
- Sub-processos da Engenharia de Aplicação 
	- Engenharia de Requisitos de Aplicação 
	- Desenho da Aplicação 
	- Realização (Implementação) da Aplicação 
	- Testes da Aplicação

## APLE Methodology ASD and SPL
### ASD Agile Software Development
- Proposed methodology is based on agile method scrum, its activities, artifacts and phases, as it is most widely used agile method.
- **Variability** → adding and/or removing the components from PL architecture
- The proposed approach also addresses the variability inside the component
- The proposal meth. Is using both, the external variability (adding and deleting components) and, internal variability (variations inside component).

### APLE Methodology
- Aplication Engineering Team (AE) will work in 4-week iteration (sprint). AE team will adopt PL architecture to create the product specific architecture. This product specific architecture is then evaluated in order to define whether or not it satisfies the specific product requirements and quality attributes.
- Domain Engineering Team (DE) will also work in 4- week iteration. The main tasks performed by DE team
are that the DE team will build the core assets and agile product line architecture
- Feature catalog is collection of initial user stories and acceptance tests. These user stories (i.e. ATs) are used as input to perform search operation in the central repository named as Info Base. 
- SPL backlog → similar to product backlog. It contains the requirements for the implementation of core assets (i.e. non-existing). It may also contain the requirements that move from product backlog to SPL backlog.
- Info base is like a central repository that contains the reusable artifacts such as requirements, acceptance tests, source code, etc. The features backlog items (i.e. ATs) are used as input to search items from this repository