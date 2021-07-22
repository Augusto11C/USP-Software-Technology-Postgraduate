# Mineração de Processos
## Control-flow Perspective
- "encontrar o caminho do processo"
	- "processo não tem uma caracterização definida a priori"
- Foca na ordenação lógica das atividades
- Busca encontrar uma boa caracterização de todos os possíveis caminhos de um processo
- Os dados são organizados com alguma forma de notação, como:
	- **Redes de Petri Net**, BPMN e UML

## Organizational Perspective
- "tentar identificar quais atores estão envolvidos no processo"
- Reconhecida como perspectiva do recurso (resource perspective)
- Foca em dados relacionados aos atores envolvidos em cada atividade que podem ser pessoas, sistemas, departamentos ou cargos.
- Busca apresentar a rede social envolvida no processo para estruturar a organização em termos de unidades organizacionais e cargos

## Time Perspective
- Foca nas datas e horários atribuídos ao início e fim de cada atividade do processo 
- Fornece informações detalhadas da localização dos problemas de performance por meio da combinação de um modelo de processo – seja ele um modelo formal pré-definido ou um modelo minerado – e os períodos identificados nos eventos de logs.

## Informational Perspective
- Conhecida como **perspectiva do caso (case perspective)** 
- Foca em aspectos específicos de casos individuais gerados na execução de um processo 
- Uma **instância ou caso de processo** pode ser caracterizada pelo seu **percurso no processo**, pelos recursos que a executam, ou por valores descritos nos dados dos eventos.

## Modelo de Processo de Software
- O modelo de processo de software gerado neste fluxo tradicional (slide anterior) é prescritivo, ou seja, o modelo não necessariamente reflete o trabalho que está sendo realizado nas rotinas diárias.
- a detecção das discrepâncias entre o modelo de processos sugerido e o modelo que é realmente praticado é difícil de ser evidenciada manualmente, ou até mesmo utilizando ferramentas como planilhas Excel
- Os praticantes do modelo, neste caso os Engenheiros de Software, não são envolvidos na modelagem do processo, e eles podem ser considerados os melhores especialistas em partes específicas que atuam.

<br>

- Os logs de eventos – ou trilhas de auditoria – das ferramentas utilizadas no  desenvolvimento de software pelos Engenheiros de Software são submetidos aos algoritmos de mineração de processos para identificar o processo real   sendo executado.
- As técnicas de mineração de processos podem indicar possíveis inconformidades do processo em execução em relação ao processo modelado e também indicar possíveis pontos de gargalo. (compara o processo descoberto através da mineração com o processo executado/representado)
- Permite que o Engenheiro de Processos analise estes dados e realize as otimizações que sejam mais efetivas. 