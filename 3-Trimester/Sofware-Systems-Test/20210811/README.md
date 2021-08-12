# Aula 2 - 20210811

- **domínio de entrada:** exemplos como inteiro, string, etc

-  espaço de entrada é a união dos domínios da entrada

- modelo do espaço de entrada: 
	- composto por
			- _caracteristicas_:
			- _blocos_: partição de um domínio da entrada 
			- Exemplo: 
				- Característica Elemento está na primeira posição da lista? 
				- **Bloco true** e **Bloco false**

- **modelo do domínio da entrada**
	- deve ser basear em alguma características distintiva das entradas do programa ou de seu comportamento, ou de seu ambiente

- **propriedade de completude**

- particionamento do espaço da entrada


---

## Refinando o Modelo do Espaço de Entrada
**Cobertura do espaço de entrada**
- **Critério 1: Cobertura de todos as combinações (CTC)**
	- Usa todas as combinações de blocos de todas as características, e deve haver pelo menos um caso de teste para cada combinação.
	- Um conjunto de casos de teste para satisfazer CTC deve ter pelo menos um caso para cada combinação.
- **Critério 2: Cobertura de cada escolha (CCE)**
	- Um valor de cada bloco para cada característica deve ser usado em pelo menos um caso de teste.
- **Critério 3: Cobertura em pares (CEP)**
	- Um valor de cada bloco para cada partição combina-se com um valor de todos os blocos de cada outra partição.
- **Critério 4: Cobertura da escolha de base (CEB)** 
	- Escolhe-se um bloco de base para cada partição, e um teste de base é formado usando esta escolha para cada partição. Os demais testes são escolhidos fixando-se todos os blocos da base exceto um, e usando escolhas não de base das demais partições.

## Teste baseado tabela de decisão
- regra de decisão do dominio da entrada