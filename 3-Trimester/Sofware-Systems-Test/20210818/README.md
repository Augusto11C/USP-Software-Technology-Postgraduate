# Aula 3 - 20210818
## Observações sobre o que vimos até aqui
- Sobre as técnicas básicas de teste
	- Como foi dito, o assunto é bem vasto. Demos mais atenção a poucas técnicas básicas centradas em especificação; no caso, **as que particionam o espaço de entrada do SUT**.
		- São técnicas de teste de caixa-preta
		- Os métodos vistos também são chamados de métodos de Partição em Categorias (Category-Partition
	- Tabelas de Decisão e Máquinas de estadoso usadas em testes são técnicas de Teste Baseado em Modelo (MBT)


## Aceitação - Quadrantes de Teste

- Primeiro e segundo quadrantes são mais voltados para o negócio
- Terceiro e quarto quadrantes são mais voltados para a tecnologia
- Segundo e terceiro quadrantes guiam o desenvolvimento (Prevenção de defeitos antes e durante a codificação)
- Primeiro e quarto quadrantes avaliam o produto (Busca de defeitos e descoberta de características faltantes)

<br>

- **Terceiro Quadrante (step 1)**
	- *Testes de Unidade, componentes ou integração*, Implantação, API, Formatos de dados
- **Segundo Quadrante (step 2)**
	- *Teste de história de usuários*, casos de uso, especificação por exemplos, *aceitação de sistemas*, experiência de usuário, protótipos e simulações
- **Primeiro Quadrante (step 3)**
	- Testes exploratórios, usuabilidade, aceitação de usuário 
- **Quarto Quadrante (step 4)**
	- Testes de desempenho, carga, segurança, outros atributos de qualidade

### Pirâmida de Teste
**(base)**

- Teste de unidade
	- Abrangencia menor
	- Quantidade de testes maior
	- Devem ser rápidos para se ter feedback rápido e preciso, com detalhes dos *bugs*
	- Versáteis
	- Incompleto, pois testa apenas partes específicas
	- **Automatizar** no nível de tarefas
- Teste de integração ou de componentes
	- Integração interna do sw
	-  abrangencia um pouco mair que a dos testes de unidade
	- quantidade de testes um pouco menor do que a dos testes de unidade
	- Testa a conectividade do software, independentemente da IU
	- API, web services, controladores
	- Feedback não muito preciso
	- **Automatizar** no nível de histórias de usuário
- Testes de IU
	- abrangencia um pouco mair que a dos testes de integração
	- quantidade de testes um pouco menor do que a dos testes de integração
	- Testa o software desde a IU - Testes de ponta a ponta (end-to-end)
	- Mostram o que o usuário deveria ver
	- tendem a ser frágeis e instáveis
	- são lentos e mais caros => feedback lento e sem precisão
	- **Automatizar** no nível de IU para histórias de usuário

**(top)**


#### Sobre a Pirâmide de teste, o que a prática mostrou no dia-a-dia?
- Regras de ouro
	- priorizar os testes de unidade
	- cobrir as lacunas dos testes de unidade com testes de integração => entre partes do software
	- usar com parcmônia os testes de ponta a ponta
	- ...


### Critério de Aceitação e Teste de Aceitação
#### Definições
- **Critérios (condições) de aceitação (satisfação)**
	- Os critérios que um sistema ou componente deve satisfazer para ser aceito por um usuário, cliente ou outra entidade autorizada. Um conjunto de condições que é exigido para ser atendido antes de os produtps entregues serem aceitos
	- Características de qualidade externas especificadas pelo PO da perspectiva de um negócio ou stakeholder. Definem o comportamento desejado e são usados para determinar se um item do product backlog foi desenvolvido com sucesso. (Rubin, K., 2013)
	- Suposições e decisões chaves feitas pela equipe do cliente para definir o comportamento desejado do código entregue para uma determinada história do usuário.
		- A discussão das condições de aceitação ajuda a identificar as suposições de risco e **aumenta a confiança da equipe em escrever e estimar todas as tarefas para completar a história**. (Crispin, L.; Gregory, J., 2009)
	- Critérios que serão usados para calibrar (ou medir) o sucesso de um projeto. (Cohn, M., 2005)
	- Uma **condição de satisfação** é, simplesmente, um **teste de aceitação de alto-nível** que deverá ser verdadeiro depois que a história estiver completa. (Cohn, M., 2010)

> Três paths definição:
> critérios
> teste
> confirmação e teste

- **Teste de Aceitação**
	- Teste conduzido para determinar se um sistema satisfaz seus critéiros de aceitação e para permitir que o cliente determine a aceitação de um sistema
	- Teste realizado para verificar se os critérios de aceitação foram atingidos. Teste que define o valor de negócio que cada item do product backlog deve entregar. (Rubin, K., 2013)
	- É um termo mais amplo que pode incluir tanto os testes voltados para o negócio como os voltados para a tecnologia. (Crispin, L.;Gregory, J., 2009)