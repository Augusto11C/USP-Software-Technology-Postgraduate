# Manutenção

20/04 - Get Slides

- Processo que muda o software após a entrega
- Objetivo (ISO 14764, 2006, p.5)
	> Modificar o produto de software existente enquanto preserva sua integridade.
	
- Motivos para se fazer manutenção
	- Prover continuidade do serviço
	- Apoiar atualizações obrigatórias (ex.: leis)
	- Apoiar solicitações de melhoria
	- Facilitar o trabalho de manutenção
- Não recebe tanta atenção...
	- ...mas é igualmente (se não mais) importante que o desenvolvimento..

- **Alto custo** (Grubb e takang, 2003)
	- 49% a 75% do custo do software é manutenção
	- TODO get in video slide 3 info
	- 50% do custo de manutenção é entender o software

## Tipos de Manutenção
- Existem diferentes tipos de manutenção: Correção e Melhoria
- TODO get image slide 4
- As manutenções podem ser **reativas** ou **proativas**
	- Antes ou depois de o problema se manifestar

### Manutenção  & Correção
- Manutenção corretiva
	- corrige erros (reativo)
	- envolve a manutenção emergencial
- Manutenção preventiva
	- Modificação necessária ao detectar possiveis falhas (proativa)
	- Ex: Bug do milênio

### Manutenção & Melhoria
- Manutenção adaptativa
	- necessária para lidar com mudanças no ambiente (reativo)
		- Ex: mudanças nas interfaces com outros sistemas
- Manutenção perfectiva
	- detecta e corrige falhas latentes (proativo)
	- Ex: melhorar a manutenibilidade do software

### Tipos de Manutenção
- Uma mudança pode envolver diversos tipos
	- Ex: Para adaptar o software a um novo SO pode ser necessário corrigir alguns defeitos
	- Ainda assim a classificação é importante  - **Priorização**

## Processo
- Começa durante o desenvolvimento e termina com a aposentadoria do software.
- TODO get image in slide 8
> "durante o desenvolvimento a manutenção é o planejamento para se fazer a manutenção"
> Professor Fábio em sala de aula

- Importante planejar a manutenção
	- Durante o desenvolvimento
	- (plano de manutenção)
- se possível, o mantenedor deve participar do desenvolvimento
	- basicamente em atividades de garantia da qualidade, verificação e validação.
- TODO get image in slide 10

## Análise
- Analisar os problemas e as solicitações
- requisição de mudança
	- propõe uma mudança ao software
	- nem sempre uma solicitação se torna uma mudança
		- apesar de estranho, pode ser o funcionamento esperado
			- "Não é um bug, mas sim uma **feature**"
- TODO get image slide 11


```
migração de monolito para microserviço
	- não se desenvolve do zero
	- manutenção perfectiva

manutenção é infinita e o desenvolvimento é finito
- pode sobrar funcionalidade, e isso será manutenção

prazo vs funcionalidade
- após realizado a entrega e datas depois do prazo é manutenção

- depois que chegar na manutenção, não se volta para desenvolvimento.
```
