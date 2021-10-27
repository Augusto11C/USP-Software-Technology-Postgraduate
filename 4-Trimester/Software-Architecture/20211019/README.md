# Aula 2 - 20211019 

## Analogia com Casa

- Por que desenhar a casa no software e não construir ela de uma vez?
    - Propósito de uso
    - Possui finalidade
    - Agregar valor
    - Verificar se concretizou de uma forma menos custosa os requisitos de quem está envolvida no projeto

- Ambiente onde a casa está inserido afeta a experiencia de seu uso


- Requisito funcional: Aquilo que o software deve fazer
- Requisito não funcional: 

## Arquitetura de Software
- Definição I: Forma, elementos, fundamentação (o "por quê" da forma o motivo)
- Definição II: Conceitos ou propriedades fundamentais de um sistema em seu ambiente incorporado em seus elementos,relacionamentos e nos **princípios de seu design** e evolução” (ISO/IEC/IEEE, 2011).

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

- Estrutura de um sistema
    - Elementos que constituem o sistema e o relacionamento entre eles

- Estrutura estática de um sistema
    - Define seus elementos internos e sua disposição em "design-time"

- Estrutura dinâmica
    - Elementos ("runtime") e suas iterações
        - Como o sistema trabalho, que acontece "runtime" e como responde aos estímulos externos ou internos
      - **exemplo**: fluxo de informações entre elementos

## Propriedades Externas
- Comportamento externamente visível
    - iterações funcionais entre o sistema e o seu ambiente
    - fluxo de informação de entrada e saída, como o sistema responde aos estímulos externos, o contrato publicado ou API que a arquitetura tem com o mundo exterior
    - O comportamento externo deve ser modelado observando o sistema como caixa preta
- Propriedade de qualidade
    - Propriedades não funcionais, externas


## Princípio de Design e Evolução
- Declaração fundamental de convicção, abordagem ou intenção que orienta a definição de sua arquitetura

- Uma forma de estabelecer uma estrutura de tomada de decisão para um arquitetura consistente e bem estruturada

## Elementos Arquiteturais
- é o elemento ou elementos básicos que se utilizam para construir o sistema
- a natureza do elemento arquitetural depende do tipo de sistema e de seu contexto
    - Bibliotecas de programas

  - Deve possuir um conjunto de atributos principais

# Aula 3 - 20211026

- Elemento arquitetural
- Instanciação da arquitetura
- Abstração de uma Arquitetura

## Visões Arquiteturais
- Problematização de representar um sistema sob diferente aspectos.
- Uma **visão** é uma representação de **um ou vários aspectos de uma arquitetura**, ilustra como arquitetura **trata um ou várias preocupações de um ou vários stakeholder**.

- A partir da visão do negócio é possível identificar informações e seus ciclos de vida que serão usados para representar o sistema.

### Cinco Visões de Arquitetura
- Visão Tecnologia: Elementos de hardware & software

- Visão Engenharia: Infraestrutura requerida para suportar a distribuição
    - midleware que permite a interoperabilidade entre as aplicações do sistema

- Visão Empresa: O objetivo, escopo e políticas para a organização que será proprietária do sistema de informação (enxergar os processos de negócio)
    - Objetivo | Políticas | Escopo | Papeis

- Visão Informação: Informação manipulada pelo sistema e restrições sobre o uso e interpretação daquela informação
    - Semântica: significado, ciclo de vida, regras da informação ()

- Visão Computacional: Decomposição funcional do sistema em objetos adequados para distribuição
    - Aplicação | Interfaces
    - Onde estão as funcionalidades
