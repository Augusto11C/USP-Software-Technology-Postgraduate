# Análise e Projeto Orientado a Objetos - Visão Geral

## Avaliação
M = (Exercícios + 2*Projeto + 3*Prova)/6

- Exercícios
  - Feitos nas aulas com parte prática
  - Segue o Projeto Integrado
- Projeto
  - Modelo de análise: TDB
  - Modelo de projeto: TDB
- Prova
  - Individual e com consulta a materiais impressos

## Desenvolvimento de Software
Desenvolver software não é só levantar os requisitos e implementar. Existem diversos fatores e problemas que devem ser levados em conta, como:
  - Complexidade do software
  - Tamanho da equipe
  - Retrabalho
  - Reutilização
  - Mudança
  - Manutenção
  - (e outras questões normais de projetos)

- Atividades Clássicas
  - Definição e análse de requesitos
    - Levantar os requisitos do software
    - Refinar e estruturar os requisitos
  - Projeto
    - Projetar como o software deve fazer o que foi requisitado
  - Implementação
    - Criar o software
    - Criar e executar os testes 
  - Teste
    - Executar o software criando em busca de defeitos
  - Implementação
    - colocar o software no ambiente real

## Paradigma de Programação
- O paradigma de programação influencia diversos desses aspectos.
> Forma de conceituar o que significa realizar computação e como tarefas executadas no computador devem ser estruturadas e organizadas. (Budd, 2001)

### Alguns Paradigmas
- Imperativo
	- Estado e comandos e de mudanças do estado global
	- Linguagens: Pascal, C e Cobol
	- Tem uma função e altera um estado global
- Funcional
	- Algoritmos (ponto de vista matemático)
	- Linguagens: Lisp, scala
	- Uma linguagem funcional pura dificulta a "mudança" de estado, pois o conceito de estado não existe
- Lógico
	- Metas e lógica de predicados
	- Linguagem: Prolog
- **Orientado a objetos**

### Qual o melhor paradigma?
- depende do problema
- a solução de um problema computacional é influenciado pelo paradigma seguido
	- facilidade/dificuldade de representação
- Algumas linguagens são multiparadigma


### Paradigma de Desenvolvimento
- O paradigma de programação influencia diretamente as atividades de desenolvimento


### Atividades de Desenvolvimentos vs Influencia Paradigma
1. Definição e análise de requisitos
2. projeto
3. implementação
4. teste
5. implantação

- definição e análise de requisitos(1) / implantação(5) **não** são afetados diretamente pelo paradigma, mas o resto SIM!!
  - A análise de requisitos é tradicionalmente executada independente de paradigma 
    - Foco no problema e não na solução

- Na prática: representação de requisitos são ligadas a um paradigma pelo processo
	- Facilita a execução das demais atividades
	- Exemplo
		- Histórias -> orientação a objetos
		- Casos de uso -> Orientaão a objetos (UP)
		- Diagrama de fluxo de dados -> imperativo (APE)
		- Modelo de metas -> Orientação a agentes (Tropos)

## Orientação a Objetos
- Combina os dados e as funções que os manipulam em uma unidade: objeto
  - Cada objeto tem um conjunto de responsabilidades
  - Métodos do objeto são, normalmente, a única forma de acessar os seus dados
- O Sofware é organizado pelos **conceitos de domínio**
  - abstração do mundo real
- Substantivo == Objeto
	- O pattern command ao invés de criar um substantivo-objeto ele cria um verbo-objetivo

### Classe e Objeto
- Classe: Representa as características comuns a um conjunto de objetos
- Objeto: Objeto é uma instância de uma classe
- Atributo: Propriedade de uma classe, permite representar o **estado**
- Operação: Representa o comportamento
  - Método: A implementação de um operação

### Acoplamento
- Medida de quanto um elemento **depende** de outros elementos
  - "Ser conectado, saber da existência ou confia"
  - Ao alterar a parte visível da classe é necessário analisar, no mínimo, as classes que dependem dela
- Algumas formas de acoplamento
  - Atributo
  - Parâmentro de uma operação
  - Variável local
  - Retorno do método
  - "qualquer necessidade de import"

<br>

- **Problemas do alto acoplamento**
  - Mudanças em classes relacionadas causam mudanças na classe
  - Dificuldade de entender a classe isoladamente
  - Dificuldade de reuso

<br>

- **Considerações sobre acoplamento**
  - Deve-se **minimizar o acoplamento**
    - Mínimo necessário e suficiente de dependências entre as classes
    - O necessário para uma classe realizar suas responsabilidades

### Coesão
- Medida de quão **relacionadas e focadas são as responsabilidades** de um elemento
- "O quanto os atributos e operações da classe estão relacionados"

<br>

- **Problemas da baixa coesão**
  - Dificuldade de entender a classe
  - Dificuldade de reusar a classe
  - Dificuldade de manutenção
  - Necessidade de alterações mais frequentes na classe


<br>

- Deve-se maximizar a coesão
  - Atributo/operação deve ficar na classe adequada
- Características de classes com **alta coesão**
  - Representa apenas 1 conceito do domínio de aplicação
    - Relacionado ao princípio da responsabilidade única
      - **Apenas 1 razão para mudar uma classe**
    - Responsabilidades claras

