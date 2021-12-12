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