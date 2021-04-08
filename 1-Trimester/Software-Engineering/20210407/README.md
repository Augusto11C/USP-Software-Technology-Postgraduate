# Gerência de Projeto
**livro**
- peopleware
- [Taxonomy-Based Risk Identification](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=11847)
- RUBIN, K. S. Essential Scrum. Addison-Wesley, 2012.
- https://scrumguides.org/
- Improving Agile Retrospectives: Helping Teams Become More Efficient
- Agile Retrospectives: Making Good Teams Great

## Conceitos I
 - Projeto
	> é um esforço ** temporário** empreendimento para criar um **produto**, serviço ou **resultado exclusivo**

- Gerenciamento de Projetos
	> É a aplicação de conhecimento, habilidades, ferramentas e técnicas às atividades do projeto para atender aos seus requisitos (PMI, 2013a, p.4)

## Projeto de Software
- Alguns diferenciais (Sommerville, 2019)
	- Software é intangível
	- Difícil ver o progresso
	- Projetos grandes são diferentes
		- Difícil reaproveitar conhecimento
		- **Processos** de software são **variáveis** e dependem da organização
- Algumas outras dificuldades (PMI, 2013b)
	- Mudanças de requisitos
	- Planejamento é complexo pela imprecisão dos requisitos
	- Evolução das tecnologias
	
- **Fatores que afetam a gerência de projetos de software (Sommerville, 2019)**
	- quantidade de envolvidos no projeto
	- complexidade do projeto
	- experiência da equipe
	- cliente (interno, externo (governo, empresa grande)
	- tamanho do software
	- cultura organizacional
	- processo de desenvolvimento de software (ágil x orientado a plano)

## PMBOK
- Subconjunto do conhecimento que é amplamente reconhecido como boa prática 
	- **Não é um método** 
		- Cada gerente e equipe definem os processos apropriados e seu rigor
	- Define os conceitos básicos
- Descreve processos
	- Entradas
	- Ferramentas e Técnicas
	- Saídas

## Atividades Gerencia de Projetos
- Atividades básicas
	- Planejamento de projeto
- Gerenciamento de riscos
- Gerenciamento de pessoas
- Geração de relatórios
- Elaboração de propostas

## Planejamento do Projeto
- Atividades (Pressman e Maxim, 2016)
1. Estabelecer o escopo do projeto
2. Determinar a viabilidade
3. Analisar os riscos
4. Definir os recursos necessários
5. Estimar o custo da mão de obra
6. Desenvolver um cronograma do projeto
	- Alocar os recursos

## Gerenciamento de Riscos
- Risco
	> É um **evento ou condição incerta** que, se ocorrer, provocará um **efeito positivo ou negativo** em um ou mais **objetivos do projeto** tais como escopo, cronograma, custo e qualidade” (PMI, 2013a, p.309 )

- Riscos podem ameaçar o projeto, o produto ou o negócio
- Exemplo
	- Projeto: perda de um desenvolvedor experiente
	- Produto: desempenho insuficiente
	- Negócio: concorrente introduzir um produto similar
- Processo de gerenciamento de riscos é iterativo

```
Identificação de riscos  --> 
	Análise de riscos   	--> 
		Planejamento de risco  --> 
			Monitoração de riscos
```
- Identificação
	- Importância de checklist ou taxonomias de risco
- Análise
	- Probabilidade e gravidade do risco
- Planejamento
	- riscos principais
		- estratégia de prevenção
		- estratégia de minimização
		- plano de contigência

## Gerenciamento de pessoas
- Importância de um grupo coeso: **time**
	- Visão alinhada
	- Padrões de qualidade próprios
		  - Seguem com mais ênfase
	 - Pessoas se apoiam e aprendem com as outras
	 - Conhecimento compartilhado
	 - Incentiva refatoração e melhorias
- Seleção dos membros
 - Equilíbrio entre habilidades e personalidades
 - Time multifuncional

## Métodos Ágeis
- algumas características (Rubin, 2013)
	- habilidades de T
	- tamanho adequado
		- scrum: menos de 10 pessoas
	- trabalho em ritmo constante
	- atitude de "mosqueteiros"
```
#### Habilidades em T ####

 ***AMPLO*** -> Habilidade em trabalhar em outras areas
      p
      r
      o
      f   -> área funcional, disciplina ou especialidade
	  u
	  d
	  o
```

## Scrum 
- Um dos métodos ágeis mais usados atualmente
	- Proposto por Ken Schwaber e Jeff Sutterland em 1993
- “Framework leve que ajuda pessoas, times e organizações a gerar valor por meio de soluções adaptativas para problemas complexos” **(Schwaber e Sutherland, 2020)**
	- (Framework para desenvolver, entregar e manter produtos complexos)
	- Grande incerteza
	- Não é um processo, método ou técnica
	- Foco na organização e gerência do trabalho
- Não é específico para projetos de software
	- Pode ser usado para outros tipos de produtos
	- Não trata de questões técnicas de desenvolvimento

### Visão
- Abordagem iterativa e incremental
	- Melhorar a previsão e controlar riscos
- Pilares (Schwaber e Sutherland, 2020)
	- **Transparência**
		- Resultados visíveis e critérios compartilhados
	- **Inspeção**
		- Artefatos gerados e progresso deve ser frequentemente inspecionado
		- Não deve atrapalhar o objetivo do trabalho
	- **Adaptação**
		- Caso haja desvios, o processo deve ser ajustado o mais rápido possível

#### Visão Geral TODO get image slide 15/29

### Time Scrum
- Auto organizáveis e multifuncionais
	- Normalmente com menos de 10 pessoas
- Papéis
	- **Product Owner** (dono do produto)
		- Responsável por gerenciar o backlog do produto
	- **Desenvolvedores**
		- Realizam o trabalho
			- Não existem sub-times ou títulos
		- Entregam um incremento “pronto” do produto
	- **Scrum master**
		- Promover e suportar o Scrum
		- Auxilia o Product Owner, o Desenvolvedores e a Organização

### Artefatos
- **Backlog** do produto
	- tudo o que é conhecido ser necessário para o produto
		- fonte dos requisitos
	- Lista ordenada de **itens**
		- possuem descrição, ordem e estimativa
			- podem ser **Histórias, casos de uso**, ou qualquer outra forma
		- em geral possuem descrições de testes para aceitação
	- responsabilidade do produto owner
	- continuamente refinado
		- product owner + desenvolvedores
- **Backlog** da Sprint
	- itens do backlog do produto selecionados para a Sprint
	- plano para entregar o incremento
		- em geral: tarefas de desenvolvimento
	- responsabilidade dos desenvolvedores
- Incremento
	- soma dos itens de backlog do produto completados ("prontos") na Sprint

### Sprint
- Evento de 1 mês ou menos (duração fixa)
	- (em geral, 2 semanas)
- Possui uma **meta** do que será construído
	- Pode ser cancelada se objetivo se tornar obsoleto
	- Promove direção para o time
- Consiste em
	- Planejamento do Sprint
	- Reuniões diárias
	- Trabalho de desenvolvimento
	- Revisão da Sprint
	- Retrospectiva da Sprint

### Planejamento da Sprint
- Planejamento do trabalho realizado
	1. Definição do valor da Sprint
		- Meta da Sprint (valor para os stakeholders)

	2. O que pode ser entregue
		- PO debate objetivo e os itens do Backlog do produto
			- Capacidade da equipe
			- Acordo com o Time Scrum

	3. Como o trabalho será realizado
		- Backlog da Sprint: itens escolhidos e plano de entrega
		- PO ajuda a tirar dúvidas

### Estimativa
- Scrum não especifica **como** estimar
- Para desenvolvimento de software é comum usar
	- história do usuário (item) e tarefa
	- estimativas
		- pontos de história (backlog da sprint)
		- horas (para tarefas)
- **planning poker** para estimar

#### Planning Poker
- variação da técnica Delphi
- características
	- baseado em consenso
		- discussão
	- usa opinião de especialistas
		- desenvolvedores
	- tamanho relativo
		- baseado em histórias anteriores
			- **acurácia ** x precisão