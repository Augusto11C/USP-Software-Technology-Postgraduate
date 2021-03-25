# Implementação e Teste

## To Study
- Problema da Parada 
	- Teoria onde se diz que não é possivel determinar se um programa termina ou não
- Agile Software Development, Principles, Patterns, and Practices by Robert C. Martin 
- [Mocks Aren't Stubs by Martin Fowler](https://martinfowler.com/articles/mocksArentStubs.html)
- [TestDouble by Martin Fowler](https://martinfowler.com/bliki/TestDouble.html)

## Implementação
Responsabilidades:
- Gerar o código fonte
	- algoritmo adequado/detalhes tecnológicos
	- pode envolver diversas linguagens
- executar alguns níveis de teste
- Integração
- gerar executáveis, bibliotecas e componentes

TODO Image from slide 2

### Preocupações
minimizar complexibilidade
-	correção, eficiencia e elegância (legível)

Antecipar mudanças 
- desperdício X retrabalho
- (na prática é a arquitetura que acaba tendo maior nessa parte de retrabalho e mudanças futuras)

Permitir a verificação 
- Facilitar as atividades de Verificação e Validação 
- Facilitar a depuração

Reuso
- usar libs, frameworks, códigos e componentes
- criar elementos reusáveis -> planejamento

padronização
- padrões de código
	- uso de recursos
	- comunicação entre elementos de software
	- acesso a plataformas
- documentação
- ferramentas

## Test-Driven Development (TDD)
- Testes de unidade são feitos antes do código
- abordagem usada pelo `Extreme Programming`
Criar os testes como se o código já existisse ----> faz os testes compilarem ----> executar os testes (que devem falhar) ----> programar a solução ----> executar o teste `->....->` Criar os testes como se o código já existisse `->....->` 

## Integração
Juntar o trabalho dos programadores 
- Gera uma versão "completa" do software 
- Baseado na versão atual de cada item 
- Verifica o trabalho dos desenvolvedores 
- As partes do software funcionam em conjunto

Juntar o software a outros elementos 
- Software e hardware

Importância da **gerência de configuração**

O ideal é integrar com alta frequência
- mas a integração tem um custo envolvido.
- Algumas questões a considerar
	- Complexidade do software (e de seus módulos)
	- Complexidade da integração
		- Equipes distribuídas
	- Duração das iterações 

## Testes
- Atividade de controle da qualidade do produto
TODO: Imagem slide 8

- Parte do processo de Verificação e Validação
	- Forma mais comum V&V

**O que é teste ?**
> Teste é o processo de executar um programa com o objetivo de encontrar erros
> \- (MYERS, 2012, p.6)

**Então por que não testar tudo?**

## Estratégia de Teste
- Ajudam a escolher conjuntos de dados que têm maior probabilidade de existência de erros

**Duas estratégias principais** 
	- Estrutural: caixa branca
	- Funcional: caixa preta

### Teste Caixa Preta
- Alvo do teste como uma caixa preta
	- Não se usa nenhum detalhe interno
TODO: Image slide 14
- Foco na especificação
	- A saída obtida para uma determinada entrada é a esperada?

### Teste Caixa Branca
- O teste é feito considerando o conhecimento da estrutura interna do código
TODO: Image slide 14
- Foco nos caminhos 
	- Condições, laços e comandos

### Estratégia de Testes
Alguns tipos de defeitos só são encontrados aplicando uma das
estratégias
- Caixa branca: não se percebe a falta de caminhos
	- Exemplo: faltou considerar alguma condição

- Caixa preta: não se percebe alguns tipos de falhas da lógica interna
	- Exemplo: considerou-se um caso a mais

## Níveis de Teste
- A forma de realizar os testes depende do processo
- Normalmente o teste é realizado em vário níveis
- **Teste em V**
	- Cada teste considera aspectos de uma atividade de desenvolvimento

### Teste em V
TODO: Image slide 19

### Teste de unidade
- Testa cada módulo do software
	- Menor elemento do software
	- Comparar sua função à interface definida
- Tradicionalmente feito pelo desenvolvedor
- Algumas questões
	- Qual é a cobertura ideal? É 100%?
	- Deve ser funcional ou estrutural?
	- Quando criar o teste de unidade?
		- Antes de programar a classe **(TDD)**
		- Depois de programar a classe


- Podem ser necessários drivers e stubs
	- Driver: elemento que aceita dados de entrada e os passa para o elemento a
ser testado
	- Stub: substitui um elemento que é chamado
	- Implementação simples, apenas para testar
	- O termo mais genérico é dublê

### Teste de Integração
- Testa as partes trabalhando em conjunto
	- Trata de problemas com as interfaces dos elementos
	- Considera outros componentes / serviços
	- Também chamado de teste de serviço
- Duas estratégias principais
	- Big bang
		- As partes são integradas de uma vez
		- Problema: identificar a origem de um defeito
	- Incremental
		- As partes são integradas aos poucos
		- Top-Down ou Bottom-Up

#### Top-Down
TODO: Imagem slide 24

#### Bottom-up
TODO: Imagem slide 24

#### Existem estratégias específicas para OO
- Teste baseado em Thread
	- Integra as classes que tratam de uma "thread de funcionalidade" / evento específico do
sistema 
	- (Teste de serviço)
- Teste baseado em Uso 
	- Testa primeiro as classes independentes e adiciona as classes dependentes
	- Similar à integração Bottom-Up

### Teste funcional
- "Teste da especificação"
	- Procura por diferenças entre o software e seu comportamento externo
	- Testa o software como um todo
	- Normalmente realizado como um teste caixa-preta
	- Também chamado de teste de UI

### Teste de Sistema
- Testa o software frente aos seus "objetivos"
- Atendimento aos requisitos do sistema
- Software como parte do sistema

- Sistemas intensivos de software
	- Exemplo: sistema web
	- Diversos navegadores e SOs
	- Tradicionalmente aborda os requisitos não funcionais

Alguns tipos de teste:
- Teste de stress
- Teste de usabilidade
- Teste de segurança
- Teste de desempenho
- Teste de documentação

### Teste de Aceitação
- verifica a espectativa dos stakeholder

