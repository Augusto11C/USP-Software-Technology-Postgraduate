# Instructions

## Regras (como em TSW-019): 

- A falta na apresentação acarreta a perda de 100% da nota da participação individual do aluno. Atenção para a distribuição da participação dos membros dos grupos pois há nota individual. 

- Cada grupo que vai apresentar deve enviar ao professor, por e-mail (paulo.muniz@usp.br), uma cópia da apresentação ATÉ 15:00h do dia da apresentação para que receba os primeiros comentários. O não atendimento desta regra implica uma penalidade de 20% na avaliação da apresentação do grupo. 

- Tempo máximo por grupo: 30 minutos. 

## Objetivos da Apresentação #1

1. Subdomínios e contextos delimitados.
    - A. Identificar os Contextos Delimitados do projeto integrado, classificando-os nos tipos de (sub)domínio (nuclear,...).
    - B. Em cada Contexto Delimitado, identificar seus conceitoschave. Basta identificá-los, com uma breve descrição.
    - C. Apresentar um esboço inicial do Mapa de Contexto. [NB. Não será preciso apresentar o esboço de uma arquitetura hexagonal, como no Exercício #1]
2. Apresentar a última versão do diagrama de classes completo de APOO.
3. Apresentar o modelo de classes desse diagrama em um novo diagrama com Entidades e Objetos de Valor identificados com seus estereótipos. 
    - Notem que nem todas as classes representadas no diagrama do item 1 são Entidades ou Objetos de Valor. Tais classes devem manter a sua representação original. O diagrama deve ter o máximo possível de associações unidirecionais.
4. Modularização
    - Particionar o diagrama do item 3 nos Contextos Delimitados definidos como nucleares (core). Em ada Contexto Delimitado Nuclear:
        - Dividir o diagrama em Módulos, identificando os Módulos. Apresentar as dependências das classes dos Módulos dos Contextos Delimitados Nucleares. Vamos desconsiderar aqui, por enquanto, considerações arquitetônicas (camadas, hexagonal,...). 

5. Agregados e Eventos de Domínio
    - A. Revisar os Módulos do item 4 para conterem Agregados. Apresentar o(s) modelo(s) de classes resultante(s).
    - B. Selecionar o módulo do Agregado “mais complexo”. Se necessário, revisá-lo para manter a consistência transacional. Justificar.
        - Identificar candidatos a Evento de Domínio desse Agregado. Modelá-los em classes e apresentá-los no diagrama desse módulo.
        - Mostrar em diagramas de sequência a publicação e o tratamento desses eventos por clientes interessados. 

6. Completando o projeto tático
- Completar todos os Módulos do item 5, incluindo o Módulo do Agregado “mais complexo”, com candidatos a Serviços de Aplicação, Fábrica, Repositório e Serviços de Domínio.
    - Os nomes dos Módulos devem ter qualificadores que identifiquem o Contexto Delimitado e a camada arquitetônica: Aplicação e Domínio, opcionalmente a de Infraestrutura.
    - Os Repositórios podem ser representados apenas por suas interfaces, denotadas por «repositorio», sem sua implementação na Infraestrutura.
- Resultado esperado: candidatos a modelos de classes completos dos Módulos contendo todos os padrões táticos do DDD vistos até aqui.