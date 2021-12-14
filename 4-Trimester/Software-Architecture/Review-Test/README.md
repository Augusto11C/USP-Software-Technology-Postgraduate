# Review Test
- Existem três elementos importantes nos sistemas computacionais
Hardware, software, dados
- A arquitetura de um sistema intensive-software é a estrutura ou as estruturas do sistema composta pelos elementos de software, as propriedades externas e visíveis destes elementos e os relacionamentos entre estes elementos

## Analogia com Casa
- Por que desenhar a casa no software e não construir ela de uma vez?
    - Propósito de uso
    - Possui finalidade
    - Agregar valor
    - Verificar se concretizou de uma forma menos custosa os requisitos de quem está envolvida no projeto

- Ambiente onde a casa está inserido afeta a experiencia de seu uso

- Requisito funcional: Aquilo que o software deve fazer
- Requisito não funcional: são os requisitos relacionados ao uso da aplicação em termos de desempenho, usabilidade, confiabilidade, segurança, disponibilidade, manutenção e tecnologias envolvidas

## Arquitetura de Software
- Definição I: Forma, elementos, fundamentação (o "por quê" da forma o motivo)
- Definição II: Conceitos ou propriedades fundamentais de um sistema em seu ambiente incorporados em seus elementos,relacionamentos e os **princípios de seu design** e evolução” (ISO/IEC/IEEE, 2011).

<br>

- Três elementos importantes
    - Hardware, software e dados

<br>

- A arquitetura de um sistema **intensive-software** (sistema de software intensivo) é a estrutura ou as estruturas do sistema composta pelos elementos de software, as propriedades externas e visíveis destes elementos e os relacionamentos entre estes elementos.

- microserviço:
    - unidade autonoma de execução independente.
    - elemento de processamento
    - definição também depende da escola de pensamento

## Elementos do sistema e seus relacionamentos
- Qualquer sistema é composto por partes
    - Módulos, componentes, partições ou subsistemas
    - Terminologia neutra elementos
        - partes que constituem um sistema

- **Estrutura de um sistema**
    - Elementos que constituem o sistema e o relacionamento entre eles

- **Estrutura estática de um sistema**
    - Define seus elementos internos e sua disposição em "design-time"

- **Estrutura dinâmica**
    - Elementos ("runtime") e suas iterações
        - Como o sistema trabalho, que acontece "runtime" e como responde aos estímulos externos ou internos
      - **exemplo**: fluxo de informações entre elementos
## Propriedades Externas
- Comportamento externamente visível
    - iterações funcionais entre o sistema e o seu ambiente.
    - fluxo de informação de entrada e saída, como o sistema responde aos estímulos externos, o contrato publicado ou API que a arquitetura tem com o mundo exterior.
    - O comportamento externo deve ser modelado observando o sistema como caixa preta.
- Propriedade de qualidade
    - Propriedades não funcionais, externas e visíveis
        - Desempenho, segurança, outros.
        - Como o sistema se comporta do ponto de vista de um observador externo.


## Princípio de Design e Evolução
- Declaração fundamental de convicção, abordagem ou intenção que orienta a definição de sua arquitetura.

- Uma forma de estabelecer uma estrutura de tomada de decisão para um arquitetura consistente e bem estruturada.

## Elementos Arquiteturais
- é o elemento ou elementos básicos que se **utilizam para construir o sistema**.

- a natureza do elemento arquitetural depende do tipo de sistema e de seu contexto.
    - Bibliotecas de programas, subsistemas, unidades distribuídas aplicações.

- Deve possuir um conjunto de atributos principais
    - Conjunto de responsabilidades
    - Restrições
    - Interfaces
    - Define os serviços que oferece aos outros elementos arquiteturais

## Visões Arquiteturais
Uma visão é uma representação de um ou vários aspectos de uma arquitetura, ilustra como arquitetura trata um ou várias preocupações de um ou vários stakeholder

![](./resource/visoes-arquiteturais.png)

## Propriedades de Qualidade
- Muitas decisões arquiteturais visam requisitos que são comuns a algumas ou todas as visões
    - Em muitos casos os r**equisitos estão mais ligadas a propriedades de qualidade que numa função particular**

### Exemplo - Segurança
- Ponto de vista funcional
    - O sistema precisa identificar e autenticar seus usuários. Os processos de segurança devem evitar qualquer ataque externo
- Ponto de vista da informação
    - O sistema deve  controlar diferentes classes de acesso à informação. 
    - O sistema deve aplicar esses controles em diferentes níveis de granularidade
        - Segurança no nível de objetos dentro de uma base de dados
- Ponto de vista operacional
    - O sistema deve manter e distribuir informações  confidenciais(senhas) 
    - O sistema deve-se atualizar com os mesmos níveis de segurança
- A segurança deve ser analisada nos outros pontos de vistas 
- “O sistema deve ser seguro” deve ser analisado através de todos os pontos de vista

## Perspectiva Arquitetural
Coleção de atividades, táticas e diretrizes de arquitetura que são u**sadas para garantir que um sistema exiba um conjunto específico de propriedades de qualidade relacionadas** e que por sua vez precisam de consideração em várias visões da arquitetura do sistema.

### Estrutura da Perspectiva
- Requisito
    - Define a propriedade de qualidade 
- Aplicabilidade
    - Explica a dimensão da relação com as visões
- Atividades
    - Passos para aplicar a perspectiva nas visões. Decisões arquiteturais de projeto para modificar ou melhorar as visões
- Táticas arquiteturais
    - Soluções gerais e típicas que podem ser utilizadas para tratar o atributo de qualidade

## Representação de uma Arquitetura
- Como se identifica o Ambiente que sistema está inserido?
- Quem são os stakeholders? Como atuam no Ambiente? O que fazem? Como são representados?
- Qual é negócio? Quais são ações e os agentes que realizam?
- Como se identificam os elementos do sistema?
- Como se identificam as iterações entre as partes do software?
- Quais são as funcionalidades do sistema? Como estão distribuídas nos elementos?
- Como se representa os aspectos dinâmicos?
- Como se representa as propriedades de qualidade?
- Quais são as tecnologias utilizadas e como se identificam na arquitetura

## Análise de uma Arquitetura
- Pré-Condição: Saber conceito de Arquitetura e de visões, Contexto/Ambiente
- At- ividades
    - Entender o ambiente, os agentes, os elementos e atividades que fazem parte, como atuam, como interagem
    - Identificar as camadas e a finalidade de cada uma
    - Analise a camada que tem interação com o ambiente e identifique quais são os agentes /elementos de interação e as atividades de negócio que podem realizar por meio de tecnológica
    - Identificar e analisar o tipo de informação que geram e consomem
    - Analise as camadas subsequentes da arquitetura, identifiquem os elementos de processamento da informação, o tipo de processamento que realizam e o valor que agregam ao negócio
    - Identifique a colaboração entre os elemento de processamento em cada camada e reflita sobre a infraestrutura de comunicação
    - Analise e pesquisa sobre as tecnologias existem para viabilizar a implementação da arquitetura

## Processos centrados em Arquitetura de Software
![](./resource/gap-business-e-ti.png)

### Práticas de Engenharia Centradas em Arquitetura
![](./resource/praticas-eng-centradas-arq.png)

![](./resource/centrado-arquitetura.png)