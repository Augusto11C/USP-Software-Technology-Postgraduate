## Casos de uso CRUD
- CRUD: Create, Read, Update e Delete
	- Gerenciam algum **dados**
- Chame de "gerencia X" / "manipula X"
	- Coloque o Read como fluxo principal
	- Deixe os demais como fluxos alternativos
		- Nem sempre haverá todos os fluxos (ex: pode não ser possível remover)
		- Pode haver outros fluxos
			- Exemplo: ativar/desativar

```
UC2. Gerencia usuários
Descreve a listagem, cadastro, atualização e remoção de usuários do software.
**Atores**
	Administrador
Pré-condição: não há.
**Fluxo básico**
	1. O software apresenta a lista dos usuários, informando o nome e o e-mail de cada um.
	2. O administrador seleciona um usuário
	3. O software apresenta o nome, e-mail, telefone e endereço do usuário
**Fluxo alternativo**
	FA1. O administrador solicita a remoção de um usuário (passo 2)
		1. O software remove o usuário do sistema e retorna ao passo 1 do fluxo básico.
	FA2. O usuário removido é o próprio administrador (passo FA.1)
		1. O software informa que não é possível remover o usuário e termina o caso de uso.
```

## Tempo
- Como lidar com tarefas periódicas do software?
	- Exemplo
		- Backup automático
		- Remover pedidos não concluídos
- Tempo pode ser um ator
	- Idealmente não deveria ser o único ator
		- O valor desse caso de uso é para quem?
- Exemplo: 
	```
	UC - Fazer backup dos pedidos
	Descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição descrição.
	**Atores**
		Tempo
	```

## Login
- Deve-se fazer um UC para login?
	- é algo de valor para o cliente logar no sistema?
- Tipicamente o login será pré-condição para os UCs
	- Pode-se assumir que se é daquele tipo de ator, então **tem que** estar logado!
		- Exemplo: Usuário e Cliente (Usuário <------ Cliente)
- O login precisará ser implementado. Representá-lo pode ser útil para a priorização

## Problemas Comuns
- Detalhamento de como o sistema executa os casos de uso
	- Exemplos: consulta de pedidos
		- ~~Os sistema consulta o banco de dados e encontra todos os pedidos do cliente. Osistema então apresenta uma nova janela apresentando pedido por pedido~~
- Foco exagerado nos casos de uso CRUD
	- CRUD deve ser apenas para cadastramento de dados
	- Separe um item se ele for importante para o ator
		- **valor**

## Problemas Comuns
- Interação de ator com ator
	- Detalhes de negócio
		- não está na intersecção do ambiente e o software
			- é só ambiente
	- exemplo
		1. o sistema solicita o nome do cliente
		2. ~~o funcionario pergunta ao cliente o nome~~
		3. ~~o cliente informa o nome~~
		4. o funcionário informa o nome do cliente
- Interação do sistema com o sistema
	- representação de **detalhes** do sistema

## Processos
- A criação do caso de uso pode ser iterativa
	1. identificar os atores
	2. identificar os casos de uso
		1. definir apenas o nome e a descrição
			- para que o ator usará o sistema?
			- o ator precisa informar algo ao sistema?
			- o ator precisa ser informado de algo pelo sistema?
	3. Detalhar os casos de uso ( e relacionar com os outros casos de uso)
		 -  Pode-se começar pelo fluxo principal
		 - fluxos alternativos podem ser detalhados depois
- Quando detalhar um caso de uso?
	- alguma iteração anterior
		- risco de mudança quando for implementado
		- esforço desnecessário: caso de uso pode não ser implementado
		- exemplo
			- iteração 1
				- 10 casos de uso identificados,
				- 5 detalhados
				- 3 implementados
			- iteração 2
				- 1 novo caso de uso identificado
				- 3 detalhados
				- 2 implementados
		- Estratégia usada pelo UP -  detalhar mais do que for implementar
<br>

	- Início da iteração em que ele será implementado
		- Aumenta a duração do planejamento
		- Exige disponibilidade do PO/stakeholders no início da iteração
		- Exemplo
			- Iteração 1
				- 10 casos de uso identificados
				- 3 detalhados/implementados
			- Iteração 2
				- 1 novo caso de uso identificado
				- 2 detalhados/implementados

## Caso de Uso vs História de Usuário
- Na prática, a história pode ser vista como um **fragmento** de um caso de uso.