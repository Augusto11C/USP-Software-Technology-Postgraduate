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

## 20211117
- Ambiente de Produção de Software Centrada em Arquitetura
- A partir de uma arquitetura de referencia, orienta-se a criação da arquitetura "base"

## Processo Centrado em Arquitetura de Software
- Question (A) Como começamos o desenvolvimento de software?
    - Como chegamos na história de usuário?
        - como levantamos requisitos? 
            - tiramos os requisitos de onde?
- Answer (A) USER EXPERIENCE
    - Jornada do usuário -> processo que tem uma sequência de diversas atividades (um fim pode ser objetivad)
    - Empatia

- Muitas vezes existe uma distância entre o negocio e o sistema
    - Negócio
        - Processo de Negócio
        - Requisitos de Negócio
        - Gerenciamento do Negócio
        [[[[[gap]]]]]
    - Sistema TI
        - Requisitos sistema
        - arquitetura
        - projeto e implementação
        - equipes TI

- Como resolver esse GAP?
    - Planejamento do desenvolvimento e evolução. [objetivos, metas e negócios] --> [sistema]
        - Design --> arquitetura --> implementação    
    - avaliação.  [sistema] ---> [objetivos, metas e negócios]
        - conformidade --> arquitetura --> avaliação
