# Dívida Técnica

04/05 - Get Slides

- Atalhos que os desenvolvedores tomam durante o desenvolvimento.
- Artefatos incompletos, imaturos e inadequados que aumentam o custo e diminuem a qualidade
- Ajuda a comunicar para pessoas não técnicas
-
> Entregar código imaturo é como assumir uma dívida. Um pouco de dívida aumenta a velocidade do desenvolvimento o quanto ela é paga rapidamente ao reescrever. (...)
> O perigo é quando a dívida não é paga. Cada minuto gasto com um código não muito certo conta como juros da dívida. 
> \- (Cunningham, 1992)

- Conceitos
	- Principal: esforço necessário para corrigir
	- Juros: custo de não se corrigir a dívida 
		- Esforço maior e menor produtividade 
	- Probabilidade dos juros: probabilidade de se ver consequências da dívida

## Tipos Dívida Técnica
- Teste
	- Exemplo: cobertura inadequada, testes manuais 
-  Defeito 
	-  Exemplo: defeitos conhecidos não corrigidos 
- Documentação 
	- Exemplo: falta de documentação (manual ou arquitetura) 
- Design / Arquitetura 
	- Exemplo: design / arquitetura inadequada, necessidade de refatoração 
- Código 
	- Exemplo: más práticas, dificuldade de entendimento, duplicação de código

## Taxonomia
- Quadrante de dívida técnica 
TODO get image slide 6

## Causas da dívida técnica
- Desconhecimento técnico
- Pressão para atender uma deadline
- Tentativa de aumentar artificialmente a velocidade
- Não correção de dívidas antigas
	- Dívidas crescem sobre dívidas
	- Tenta-se evitar a correção de uma dívida

## Consequências
TODO get image from slack

## Gerência
- Atividades
	- Identificar
	- Medir
	- Monitorar

### Identificar
- Feito pelo time de desenvolvimento
	- Desenvolvedores, mantenedores e gerentes
	- Definição de histórias
- Descrição
	- Localização
	- Porque precisa ser feito
	- Estimativa do principal e dos juros (custo e probabilidade de se deparar com o problema novamente)
		- (Atividade de Medir)

### Medir
- Estimar princial e juros
	- dados históricos
	- conhecimento de especialista

- Algumas ferramentas identificam e calculam automaticamente
	- SonarQube (https://www.sonarqube.org)

### Monitorar
- decisão do que fazer com a dívida
		- pagar ou postergar
- Em geral há um backlog específico
- Toda dívida deve ser paga?
	- Fim da vida do produto
	- Protótipo

### Formas de Pagar
-	Pagar a dívída quando se deparar com ela
	-	nem sempre é a melhor forma: custo/benefício
-	Pagar dívida incrementalmente
	-	aos poucos X Sprint de Refatoração
-	Pagar a dívida de maior juros primeiro
-	Pagar a dívida enquanto se faz atividades de desenvolvimento
	-	Alocar pontos de história para tratar de dívida técnica
Fabio Levy Siqueira

22:06

[https://www.springer.com/gp/book/9783642290435](https://www.springer.com/gp/book/9783642290435)

Survey Research Methods - Floyd J. Fowler

Yin Study case research

Case Study Research

Design Science Methodology for Information Systems and Software Engineering