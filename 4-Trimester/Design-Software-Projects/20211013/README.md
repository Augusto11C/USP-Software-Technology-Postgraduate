# Aula 2 - 20211013
## Objetivos
- noções preliminares do projeto dirigido pelo domínio (DDD)

## DDD - Noções Fundamentais
### DDD - Motivação
- muitas vezes as **discussões** com os especialistas do domínio estão totalmente **desconectadas** da **interpretação embutida na base de código**.
- o DDD utiliza uma **linguagem comum** que deve **permitir a expressão do modelo conceitual do domínio** em todas as comunicações entre as duas partes: a Linguagem Ubíqua ou Onipresente.
- Os especialistas do domínio e os desenvolvedores devem entender o modelo conceitual do domínio que evolui ao longo do projeto (project) em termos da linguagem onipresente.

### DDD - O que é Domínio?
- em termos pragmáticos, é o que uma organização faz numa parte do mundo dos negócios.
- nesse domínio há várias áreas e funções específicas, stakeholders com interesses distintos e idiomas específicos.

<br>

- consequência 1: um **Domínio** de negócio é **composto** por **vários Subdomínios**.
- consequência 2: em vez de se ter um único modelo de design inclusivo, tem-se vários modelos de design específicos.
- no DDD, os **_modelos de design_ são desenvolvidos em Contextos Delimitados** (Bounded Contexts).

### DDD - Projeto Estratégico - Contexto Delimitado (Bounded Contexts)
- idealmente, cada Subdomínio é mapeado em um **Contexto Delimitado**.
- cada Contexto Delimitado:
	- **define** uma **fronteira conceitual** em um Domínio, definindo/criando um **Espaço de Solução** do sistema que **apoia o domínio do negócio** em questão.
	- tem sua **própria Linguagem Onipresente** que fundamenta e orienta um modelo de design.
	- fornece uma **implementação técnica** que reforça as fronteiras do espaço de solução, **definindo os modelos de design deste espaço**.