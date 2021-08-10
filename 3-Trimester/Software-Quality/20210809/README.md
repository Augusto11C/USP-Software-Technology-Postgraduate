# Aula 3 - 20210809
## Qualidade x Produtividade
TODO get graphic

## Qualidade do Produtividade
- Conformidade com necessidades (requisitos explícitos) do cliente
- Conformidade com padrões de desenvolvimento
- Conformidade com requisitos implícitos (boas práticas)
- Conformidade com prazos e custos (estimativas)

## Qualidade do Processo
> Como listar atributos de um processo de/com qualidade?
- Atividades definidas
	> Atividades explicitas/definidas, os participantes do projeto sabem sobres as atividades, estas atividades podem ser consultadas.

- Repetição
	> Processo repetido, bom para ganhar aprendizado sobre ele. Isso nos leva a criar/idendificar oportunidades de melhoria.

- Gerenciamento
	> Se um processo tem atividades que precisam ser executadas, o gerenciamento precisa cuidar para que ela seja bem executada. Caso a atividade não esteja sendo bem executada, o gerenciamento do processo precisa identificar o motivo dessa "má execução".
	
	> "Corre" dentro de um projeto assim como o gerenciamento de projeto.
	> Scrum master dentro do scrum.

- Dados de Processo
	> Ter apontamentos/informações/monitorações 
	> Utilizar os dados para realizar comparações entre as repetições do projeto para encontrar possíveis pontos de melhoria.

## Por que usamos Processos?
- Melhoria do desempenho das organizações de software
	> Para melhora a maneira como fazemos software

- **O que é um Processo?**
	- Conjunto de passos para realizar uma tarefa
	- Cada fase tem critérios específicos de entrada e saída
	- As fases definem as tarefas e como devem ser realizadas

### TODO GET TITLE
- Melhorar continuamente os processos através do aprendizado de novos métodos;
- construir sistemas mais complexos e maiores no futuro; e
- estruturar uma base histórica de projetos.

### Gerência de Configuração
> Gerencia de versionamento de artefatos
- Controle de mudanças
- Baselines ("linha de base")
	> - Marca de tempo de algum documento
	> - Referencia para condução gradativa
	> - Estabelece as versões do artefato que são verdade para se "construir" aqui em cima (**ponto de partida do projeto**)
	> - Definição de algumas características basicas para se iniciar um projeto?
	> - A gerencia de configuração vai para um base line

### Manutenção de Software
> O conceito de manutenção começa quando o software for entregue em produção (estar em operação)
- Rastreabilidade
	> "Quais foram as manutenções anteriores que me fizeram chegar nesse ponto?"

- Previsibilidade
	> "Quais são as implicações dessa manutenção que eu vou fazer? O que ela vai impactar?"

- Qualidade da mudança

### Testes
- Planos e especificações de testes
- Ambientes de teste
	- Para cada tipo de teste pode ter/existir um ambiente de teste específico
- Grupos de testes

### Fator crítico de Sucesso para Qualidade
- Pessoas + **processos** + Tecnologia `=====>` **Qualidade**

### Tipos de Processos
- Processos ligados ao desenvolvimento
- Processos ligados à aquisição (da especificação até a instalação)
- Processos ligados ao gerenciamento de processos

## Processos ligados ao desenvolvimento
- Definição
- Implementação
- Manutenção (optional)

#### Modelos de Clico de Vida
- **Cascatas**
	- **Prós**
		- Projetos Pequenos
	- **Cons**
		- Em grandes projetos 
		- Muito dificil ter certeza da definição final dos requisitos
		- Inflexivel a mudança de requisitos
		- Pouco contato com o usuário
- **Modelo V**
	- Derivação do cascata
- **Prototipação**
	- "Contém o Cascata"
	- Requisito funcional foi refinado e colocado no protótipo. Isso melhora a qualidade em relação ao cascata
	- Como o protótipo é incremental, quando paramos? Quando isso converge com o conjunto de requisitos que o cliente tem na cabeça?
- **Modelo Espiral**
	- Enquanto na prototipação é "jogado fora", o modelo espiral incrementa
- **Modelo SCRUM**
	- Controle do que pode ser alterado ou não (uma vez estando dentro da sprint, nada mais pode ser alterado)
	- Entrega incremental.

## Processos Ligados à Manutenção
- Modificação de um produto de software após a sua implantação para corrigir defeitos, melhorar o desempenho e outros atributos, ou adaptá-lo a novos ambientes. (IEEE, 1983)

### Problemas de Manutenção
- Pouca informação em relação ao processo de desenvolvimento
- Pouca informação em relação às manutenções anteriores
- Dificuldade de entender os programas feitos por outras pessoas
- Baixa qualidade de documentação
- Software não projetado para sofrer mudanças
- A manutenção não traz satisfação pessoal

### Fatores de Manutenibilidade
- Disponibilidade de pessoal qualificado
- Estrutura compreensível do sistema
- Operabilidade do sistema (conseguir reproduzir comportamento sobre aquilo que sofrerá manutenção)
- Uso de linguagens de programação padronizadas (c/ regras de boa programação)
- Uso de sistemas operacionais padronizados
- Estrutura padronizada de documentação
- Disponibilidade de casos de testes

### Distribuição de Esforços
- evolução: 50%
- adaptativa: 25%
- corretiva: 21%
- preventiva: 4%

### Modelo de Boehm
- entendimento do sow existente
- ...
- ...

### Modelo de Osborne
- Determinação da necessidade de mudança (cliente determina)
- Submissão do pedido de mudança
- Análise de requisitos
- Aprovação/rejeição do pedido de mudança
- Programação da atividade
- Projeto
- Codificiação
- Revisão de código
- Teste
- Atualização da doc
- auditoria (meio que o teste)
- ...
- ...
- ...

### Modelo Orientado a Pedido
- Controle de Pedidos
	- Classificação dos pedidos
	- Análise de custo/benefício
	- Priorização
- Controle de mudança
	- Seleção e reprodução do problema
	- Análise ...
	- ....
	- ....
- Controle de Versões
	- Determinação da versão
	- construção da nova versão (edição