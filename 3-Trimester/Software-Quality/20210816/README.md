# Aula 4 - 20210816

## Software Quality Assurance (SQA)
Definições 
- Um padrão planejado e sistematizado de todas as ações necessárias para fornecer confiança adequada a um item ou produto de acordo com os requisitos especificados 
- Um conjunto de atividades projetadas para avaliar o processo pelo qual os produtos são desenvolvidos

### Abrangência de SQA
- Métodos e ferramentas (análise, projeto, codificação, teste)
- Revisões técnicas formais (em todas as fases)
- Estratégias de teste (várias fases)
- Controle de documentação de software (geração e alteração)
	- Muito ligado ao controle de versão - Versionamento dos docs e artefatos
- Procedimentos para garantir a adequação aos padrões de desenvolvimento de software
- Mecanismos de medição e divulgação (métricas de qualidade)

## Software Configuration Management (SCM)
- É um conjunto de atividades desenvolvido para administrar as mudanças em todo o cliclo de vida do software
	- Foca no gerenciamento das mudanças
	- Gerenciamento das versões
	
### Ciclo de SCM
- Identificar a mudança
- Controlar a mudança
- Garantir que a mudança esteja sendo implementada adequadamente
- Relatar a mudança às pessas interessadas 

## Configuração de Software
- Programas (fonte e executável)
- Estrutura de dados (internos, externos)
- Documentos 

## Baseline
> Plano do projeto congelado = retrato congelado do cronograma = baseline
> marca de referencia no tempo

- É definida como um marco de referência no desenvolvimento de software, caracterizado pela entrega e aprovação de Itens de Configuração de Software (SCI).
- Os SCI podem sofrer mudanças, mas serão feitas através de um procedimento específico e formal para avaliar e verificar cada mudança.

- Contexto: existe um conjunto de artefatos que são possíveis que se verificar e estão OK. 
	- Dado esse contexto, só assim podemos definir um baseline

## Itens de Configuração de Software
> da sustenção para aquilo que roda em produção
- Manuais (operação, sistema, manutenção, treinamento, instalação) 
- Programa Executável 
- Relatórios (operação, testes, manutenção, etc.) 
- Padrões e Procedimentos (Eng. Software)

## Processo de Controle de Mudanças
- A necessidade de mudança é reconhecida
- O usuário submete um pedido de mudança
- O desenvolvedor avalia
- É gerado um relatório de mudança
- O gerente de configuração toma decisão
- Pedido de mudança é rejeitado
	- o usuário é informado
- Pedido de mudança é aceito
	- Uma ordem de mudança de engenharia é gerada
	- Pessoas são designadas aos objetos de configuração (partes constituintes dos SCI)

## Auditoria de Configuração
- A mudança especificada na Ordem de Mudança de Engenharia foi feita ?
- Modificações adicionais foram incorporadas ?
- Uma Revisão Técnica Formal foi realizada ?
- Os padrões de Eng. de Software foram seguidos ?
- Os procedimentos de SCM para anotar, registrar e relatar a mudança foram seguidos ?
- Todos os SCI relacionados foram atualizados ?

## Ferramentas CASE
- Computer Aided Software Engineering
- As ferramentas CASE envolvem 
	- Cada etapa do processo de engenharia de software
	- Atividades quesão aplicadas em todo o processo

### Tipos de CASE
- administrativos
	- planejamento de sstemas comerciais
	- gerenciamento de projetos
	- planejamento de projetos (ajuda na estimativa de esforço, custo e prazo)
- técnicas
	- análise, projeto, codifcação, teste
	- integração, prototipação
	- manutenção (eng. reversa e reengenharia)

### Caracterśticas Geras dos CASE
- francionamento da complexidade
- adequação a um publico diversificado
- mais baratas que a construção em si
- verificáveis (rastreabilidade)
- de fácil manutenção
- orientação gráfica

## Métricas de Software
- definição
	- **Métrica** - 
		- **Caracterização quantitativa** do software baseada na teoria de medições (descrição matemática de escalas, medidas e métodos de medições). Tal teoria deve esclarecer se uma medida específica é apropriada em cada situação. (Henderson-Sellers, B. “Object-Oriented Metrics - Measures of Complexity” - Prentice Hall, 1996.)
			- "Definição de uma medida ou valor que será colhido em algum lugar."
			- "Conceitual / define a forma de obteção, unidade"
			- "Especificação do que eu quero medir"
	- **Medidas** - measure
		- "Valor numérico"
		- Grandeza determinada que serve de padrão para avaliação de outras grandezas
		- Fornece uma indicação quantitativa de algum atributo de um produto ou processo - valor. (Pressman)
	- **Medição** - measurement
		- "procedimento para se obter o valor"
		- Ato ou efeito de medir (Dicionário)
		- Ato de determinar uma medida 

## Medidas do Software
- O software é medido para
	- indicar a qualidade do produto
	- Avaliar a produtividade das pessoas
	- Avaliar os benefícios (produtividade e qualidade) derivados de novos métodos e ferramentas de software
	- formar uma linha básica de estimativas
	- ajudar a justificar os pedidos de novas ferramentas ou treinamento adicional 

### Medidas Diretas e Medidas Indiretas
#### Medidas diretas
- custo esforço despendido
- linhas de código
- velocidade de execução
- tamanho de memória
- número de defeitos

#### Medidas indiretas

- funcionalidade
	- medida direta para atribuir a uma medida indireta
- complexidade
- eficiência
- confiabilidade
- manutenibilidade
- qualidade

### Métricas Orientadas ao tamanho
- kloc: numero de linhas * 1000
	- 12KLOC = 12000
	- linhas de código não é uma boa medida sozinha, para complementa-la precisamos ter um dado extra, como "linguagem de programação"

- Medidas indiretas
	- Produtividade = KLOC/Esforço
	- Qualidade = Defeitos/KLOC
	- Custo = $/LOC
	- Documentação = Página de documentação/KLOC
	- **Comentários**

### Métricas Orientadas à função (Function point)
- Function point: como é que o ambiente vai demandar serviços para o software
	- cada serviço é um ponto de função
- Pode ser uma metrica para medir funcionalidade

<br>

- Nro. de entradas usuário (produz alteração na base de dados do sistema)
- Nro de saídas usuário
- Nro. de consultas usuário
- Nro. de arquivos
- Nro. de Interfaces externas

---
---
---
---

## Métrica de Complexidade de McCabe - 1976
- é uma metrica que dá uma medida quantitativa da complexidade lógica de um programa
- Baseia-se na complexidade ciclomática dado por um grafo de programa. (N de caminhos através de um programa) - Baseado na contagem de pontos de decisão
- O grafo descreve o fluxo de controle
- Definição
	- V(G) de um grafo G é dado por
	- V(G) = e - n + 2p, onde
		- e - ramos
		- n - vértices
		- p - # de componentes conectados
	- Em um grafo G fortemente conectado, V(G) é igual ao numero máximo de caminhos linearmente independentes
	- V (G) = 10 (limite mpaximo na prática)
 
### Propriedades
- V (G) >= 1
- V (G) é o número máximo de caminhos linearmente independentes em G; é o tamanho de um conjunto básico de caminhos
- Inserindo ou retirando statements funcionais em G não afeta V(G)
- G tem somente um caminho se V(G) = 1
- Inserindo um novo ramo em G ...
- ...
- ...
