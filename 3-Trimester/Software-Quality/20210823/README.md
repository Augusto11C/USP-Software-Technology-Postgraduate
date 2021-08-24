# SQ-20210823 
## Fatores de Qualidade de Software
- A qualidade de software é uma combinação ...
- ...
- ...
- Os fatores de qualidade se dividem em
	- os que poser ser medidos diretamente ...
	- os que poser ser medidos indiretamente ...
- Como se medem os fatores de Qualidade
	- Testes
		- informais
		- formais
	- Revisões
		- informais (bate papo técnico)
		- formais (walkthrough, inspeções, revisão técnica formal)

## Métricas para a Qualiade de Software
- O software é avaliado através de medições dos fatores para se chegar a uma indicação de qualidade
- Cálculo da qualidade (Q)
	- Q = `k1 * F1 + k2 * F2 + ... + kn*Fn`
		- onde, ki = constantes
		- Fj = fatores de qualidade
	- Q = ?

> Projeto que o professor trabalhou
>    - funcionalidade x defeitos

### Revisão Técnica Formal
- Objetivos
	- Descobrir defeitos de função, lógica ou implementação em qualquer representação do software
	- Verificar se o software que se encontra sob revisão atende aos requisitos
	- Garantir que o software tenha sido representado de acordo com padrões pré-definidos (caso não tenha sido, será considerado "DEFEITO")
	- Obter um software que seja desenvolvido uniformimente
	- Tornar os projetos mais administráveis

- **Registro de Revisão**
	- Lista de questões de revisão
		- Identifica as áreas problemáticas do produto
		- serve como um "checklist" de itens de ações que irá orientar o produtor quando as correções forem feitas
	- Relatório de revisão resumido
		- o que foi revisado?
		- quem fez a revisão?
		- quais foram as descobertas e as conclusões?
	> parece que existe uma reunião que revisa esses registros
	> o objetivo da reunião é encontrar defeitos dos artefatos

- Decisões que o Relatório do passo anterior pode gerar
	- os participantes aceitam o produto sem modificações adicionais
	- os participantes rejeitam o produto devido a defeitos graves
	- os participantes aceitam provisoriamente (defeitos menores foram encontrados e devem ser corrigidos)

- Roteiro para uma RTF
	- Lider, autor e revisores
	- Atribuições do Líder
		- preparação
		- agendamento
		- realização
		- encerramento
	- Recomendações para os Revisores
		- esteja preparado
		- seja cooperativo
		- observe a linguagem
		- seja educado
		- levante questões, não os resolva
		- evite discussões de estilo
	- Recomendações para o Lider
		- destaque os objetivos, regras e procedimentos da revisão
		- destaque os resultados da revisão anterior
		- eleja uma equipe qualificada para a revisão
		- destaque a importância da preparação prévia dos revisores
		- coordene a obtenção de infraestrutura adequada para a revisão
		- anote em separado os pontos que estejam fora do escopo da revisão
		- desencoraje comportamentos inadequados dos  revisores
		- destaque o resultado das revisões
		- distribua uma cópia do registro da revisão o mais rápido possível para os revisores

#### O que são Defeitos?
- São injetados no programa por pessoas através 

#### Onde o Defetio pode Ccorrer
- programas
- arquitetura do programa
- requisitos
- especificações
- documentações

#### Natureza do Defeito
- pode ser identificado
- pode ser descrito
- poser ser contado


## Modelo de Ampliação de Defeitos - IBM
- TODO get image
	- PS: tudo que é erro == defeito (professor copiou errado)

- Considerações da imagem
	- A eficiência de detecção de erros diminui a medida que se aumenta a quantidade de artefatos

- percentuais de detecção de defeito nos `projeto preliminar` e `projeto detalhado` é 0, pois está se desenvolvendo e não inspecionando.

...
...

## Validação e Verificação (V&V)
- a atividade de teste é um elemento dentro de um conceito mais amplo chamado V&V
	- verificação: "estamos construndo certo o produto?" (se foi feito da melhor maneira, maneira correta - maneira de conduzir - a maneira como eu fiz foi adequada?)
	- validação: "estamos construindo o produto certo?" (conforme os requisitos)
		- ex: utilizar protótipos para dar um check a totalidade dos requisitos
- Abrange muitas atividades de SQA:
	- Revisão de tecnicas formais
	- Monitoração de desempenho
	- Simulação
	- Estudo de viabilidade
	- Revisão
	- ...

### Teste
- Um bom caso de teste é aquele que tem uma elevada probabilidade de revelar um defeito ainda não descoberto
- Um teste bem-sucedido é aquele revela um defeito ainda não descoberto

O que é teste de unidade, integração e validação