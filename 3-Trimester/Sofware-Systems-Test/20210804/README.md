# Aula 2 - 20210804
## Estabelecendo um Vocabulário Inicial
- Defeito, erro e falha de software na disciplina
	- **Falha (failure) de software**
		- Comportamento externo incorreto com respeito aos requisitos ou a outra descrição do comportamento esperando. Um sintoma.
	- **Defeito (fault)**
		- Um defeito estático no software, como por exemplo a instrodução de equívocos no design ou no programa. A causa raiz das falhas.
	- **Erro de software**
		- Um estado interno incorreto de um programa é a manifestação de algum defeito em tempo de execução.
	- Bug de software
		- Um termo informal que acaba se referindo aos três conceitos de modo equivalente.

- **Teste**
	- 1. Uma atividade na qual um sistema ou componente é executado sob condições especificadas, os resultados são observados ou registrados, e uma avaliação é feita de algum aspecto do sistema ou componente.
	- 2.
	- 3. conjunto de um ou mais casos de testes e procedimentos
	- O processo de avaliar um produto pelo aprendizado dele através da exploração e experimentação, que inclui de algumo: questionamento, estudo, modelagem, observação, inferência, etc

- **Checagem**
	- Checagem é o processo de fazer avaliações pela aplicação de regras de decisão algorítimicas em observações específicas de um produto.
	- **Uma** **checagem** é uma concretização da checagem

- **Teste x Checagem -  algumas implicações**
	- A checagem pode ser realizada por uma ferramenta, enquanto o teste poder ser só apoiado por ferramentas.
	- O **teste** é uma **investigação em aberto**, enquanto a **checagem focaliza fatos específicos** e regras relacionadas a estes fatos.
	- O Teste enbloba a Checagem - Checagem é uma parte do teste

- **Testabilidade de Software**
	- Testabilidade - um atributo de qualidade do software:
		- O grau com que um sistema ou componente **facilita o estabelecimento de critérios para realização e o desempenho de testes**, para determinar se estes critérios foram atendidos.
		- Determinada principalmente por dois aspectos
			- *Observabilidade do software*: O quão fácil é observar o comportamento de um programa em termos de suas saídas, efeitos no ambiente ou em outros elementos.
			- *Controlabilidade do software*: O quão fácil é prover um programa com as entradas necessárias, em termos de valores operações e comportamentos.

- **Caso de teste**
	- Valores do caso de teste: Valores de entrada para realizar execução do software sob teste (SUT).
	- Valores do prefixo: Entradas necessárias para colocar o software no estado apropriado para receber os valores do caso de teste.
	- *Valores do sufixo*: Entradas que precisam ser enviadas ao software após o envio dos valores do caso de teste
		- *Valores de verificação*: Valores necessários para observar os resultados dos valores do caso de teste.
		- *Valores de saída*: Valores ou comandos necessários para terminar a execução do teste ou retorná-lo a um estado estável
	- Resultados esperados: O Resultado que deveria ser produzido pelo caso de teste se o software se comporta como esperado.

- **Classificação dos testes**
	- Tipicamente: **Nível de teste** e **Tipo de teste**
	- **Nível de teste**
		- Expressa a proximidade do teste com o código fonte.
		- *Teste de unidade*: um teste que verifica uma "pequena parte" (uma "unidade") do código, de moro "rápido" (com suporte de automatização), e de modo "isolado".
		- *Teste de integração*: `Há uma variedade de interpretações`
			- "A ligação progressiva e o teste de programas ou módulos para assegurar seu funcionamento apropriado no sistema completo" (ISO)
			- Deve avaliar se as interfaces entre unidades ou módulos têm premissas consistentes e se comunicam corretamente. Assumem que as unidades ou módulos estejam operando como esperado ("corretamente").
		- *Teste de Sistema*: Conjunto de testes que verifica se o sistema inteiro funciona. Seu alvo é a funcionalidade global do sistema sob teste (SUT).
		- *Teste de aceitação*: Conjunto de testes que validam se o SUT está conforme às expectativas dos stakeholders adquirentes e usuários, e está pronto para o uso.
			- *Teste de Aceitação de Usuário* (UAT)
	- **Tipo de Teste**
		- Refere-se à finalidade do teste
		- *Teste funcional*: O ato de executar o software e verificar se seu comportamento corresponde às expectativas explícitas, provendoo-o com diferentes entradas e comparando os resultados com as expectativas; explora-o também para ver se ele viola quaisquer expectativas implícitas.
		- *Teste não funcional*: Seus alvos são os atributos de qualidade, tais como usabilidade, confiabilidade, desempenho, etc.
		- *Teste de Regressão*:  TODO

-  **Estilos de teste**
	- *Tradicional*
		- O teste é uma fase que ocorre após uma fase de construção
		- Assume que haja uma esoecificação prévia que guia todos os aspectos da construção, dando sentido à ocorrência de uma verificação depois da construção
		- O papel do testador é reativo, estando ancorado na visão tradicional de QA que dissocia o teste do desenvolvimento
	- *Ágil* 
		- O desenvolvedor continua escrevendo testes de unidade, mas conta como o testador para responder a "Como testar isso?", etc.
		- O papel do testador é proativo: é parte integrante da equipe de desenvolvimento, ajudando-a, de modo colaborativo, na elaboração e na automatização dos testes - testes em pares (pair testing) 

- **Requisito de Teste**: Um elemento específico de um artefato de software que deve ser coberto por um caso de teste; 


comportamento especificado: vem da especificação
comportamento programado: vem da implementação
## TODO get title
### Particionamento do espaço da entrada
- Dividir o espaço de entrada do SUT em partições lógicas
		- Particionar a entrada em regiões nas quais se assume conter valores igualmente úteis para o teste
		- Os testes baseiam-se apenas nas descrições das entradas
- A partição de um domínio da entrada define um conjunto de classes de equivalência, que por comodidade chamaremos de **_blocos_**.
	- Para esta técnica, todos os valores de um bloco são considerados equivalentes: conceitualmente, basta um único valor por bloco
		- todos os blocos são disjuntos em pares
		- .....
		- .....
		- .....
- Modelo do domínio da entrada (MDE)
	- Como realizar o particionamento? Ele deve ser basear em alguma características distintiva das entradas do programa ou de seu comportamento, ou de seu ambiente.
		- Exemplos de característica: Ordem dos preços de um produto, distância que separa um restaurante de certa localização.
		- Cada característica é particionada em blocos (classes de equivalência)
	- No mínimo, o teste da entrada usa um bloco de cada característica. Melhora-se em ...............
- **Exemplo ilustrativo simples**
	- Dado um conjunto classificado de preço de produtos de uma categoria de produto, identificar a ordem da classificação.
		- **Domínio da entrada:** preço classificados de produtos
		- ......
		- ......
		- ......
		- ......
	- Qual é o problema?
		- As noções de classificação em ordem ascendente e em ordem descendente estão agrupadas na mesma característica: ordem dos preços.


---

- Qual o modelo da entrada
	- o modelo me permite dizer os valores da entrada.
	- 

--- 

dominio da entrada baseada na funcionalidade dela



- Comportamento é algo que você define em uma interação dinãmica
- Função 
