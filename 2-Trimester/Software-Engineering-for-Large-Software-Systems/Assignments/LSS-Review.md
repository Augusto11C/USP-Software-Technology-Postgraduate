# Review

## Introdução
- Motivações
	- Entender os Clientes
	- Valor dos dados
	- Competitividade 
	- Predizer tendências
	- Otimização (planejamento, processos)

> Data Gravity is a theory around which data has mass. As data (mass) accumulates, it begins to have gravity. **This Data Gravity pulls services and applications closer to the data**. This attraction (gravitational force) is caused by the need for services and applications to have higher bandwidth and/or lower latency access to the data

- Com maior quantidade de dados aumenta a responsabilidade e dificuldade em movimentar ee dar acesso a tais dados, bem como protege-los

- **Sistema de Base de Dados**
	- Sistema computadorizado de armazenamento de coleções de registros/fichas
    - funções basicas: armazenar/recuperar/atualizar/excluir dados  **Dados vs Informações**
    - Dados ---> (significado) ---> informação ---> (análise) ---> conhecimento ---> (tomar decisões) ---> "Sabedoria"

```
- Dados
    - Processamento
        - Armazenamento
            - Controle Geral
                - Decisões Estratégicas

```

- **Sistemas de informação**
	- **Definição**: Conjunto de componentes computacionais inter-relacionados que coletam, processam, armazenam e distribuem informação para apoiar o processo de tomada de decisões e o controle de uma organização
		- Contêm informações sobre pessoas, lugares e coisas significativas à organização e ao ambiente ao seu redor

- **Sistema de Banco de Dados**
	- Dados uniformes
	- Grande número de registros "pequenos"
	- Dados alfanuméricos
	- Transações curtas

## Data Warehouse vs Data Mining vs Big Data vs Data Lake
### Intro Data Warehouse
- **Obter melhor desempenho nos negócios**

```
Explorar dados -> obter informações -> tomar decisões acertadas
```
-   Tipos de dados
    -   Registros Tradicionais
    -   Documentos completos
    -   Planilhas
    -   Figuras, gráficos, desenhos técnicos, etc
   
-   Por que DW?    
    -   Ambiente distinto
    -   dados historicos
    -   decisões: levar em conta todas informações disponíveis
    -   Rapidez

- Suporte à Tomada de Decisões
	-   Tendência de consumo
	-   Aumento/redução produção
	-   Regulação de estoques
	-   simulação de aalterações
	-   estratégia de vendas

### Intro Data Mining
```
Data Warehouse ----> (estatísticas/IA) ----> conhecimento (regras/padrões)
```

### Intro Big Data
- visa extrair valor a partir de bases de dados muito grandes, com grande variedade de origens, com grande velocidade de captura e análise
- “Big” no Big Data não é somente o tamanho da base de dados
	- Não se refere a nenhum patamar de volume de dados
	- Os dados são “big” quando seu tamanho se torna elemento ativo do problema

### Intro Data Lake
- armazenar dados sem se preocupar como vai ser seu uso
	- armazenar também os metadados
- Dados estruturados, semiestruturados e não estruturados, todos armazenados na forma “nativa
- “Ingestão” de dados em qualquer formato
- Disponibilidade imediata dos dados
- O trabalho fica para o momento da análise

### Métricas
-   medir o valor dos dados
-   medir o custo do gerenciamento de dados
-   medir número de profissionais envolvidos
-   medir cumprimento dos objetivos
-   medir Maturidade do processo de gerenciamento dos dados

### Causa da Baixa Qualidade de Dados
-   Digitação
-   Degradação ---> obsolescência
-   Uso incorreto - não conhecimento do significado/má interpretação
-   Reestruturação frequente, troca de SGBDs/BDs, SOs, Servidores
-   Baixo acompanhamento/monitoração do desempenho da base de dados (isso faz com que os problemas não sejam detectados)

## Data Warehouse
> Data Warehouse é uma coleção de dados orientados por assuntos, integrados, variáveis com o tempo e não voláteis, para dar suporte ao processo gerencial de tomada de decisões. - (Inmon)

> Data Warehouse é um processo em andamento que  **aglutina dados de fontes heterogêneas**, incluindo dados históricos e dados externos  **para atender à necessidade de consultas**  estruturadas (consultas já criadas mas parametrizadas) e ad-hoc (através de ferramenta criar a consulta ao vivo), relatórios analíticos e de suporte à decisão. (Harjinder)

> **Data Warehouse é o  _processo de integração_  dos dados corporativos de uma empresa em um único repositório**, a partir do qual os usuários podem facilmente executar consultas, gerar relatórios e fazer análises. (Singh)

> Data Warehouse é o um sistema que extrai, limpa, trata e entrega dados de várias fontes em um modelo dimensional e suporta/implementa consultas e análises para o processo de tomada de decisão. (Kimball)

- Prazo para armazenamento dos dados em bancos transacionais
	-   Conforme tabelas crescem, as consultas realizadas crescem proporcionalmente
    -   Não da para ficar armazenando nos bancos transacionais uma quantidade de dados muito grande, por isso o "prazo de validade'
-   Dados não Padronizados

![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/estrutura-dw.png)

-   ETL: Extration Transformation Load
-   DM: Data Marts "mini dw"    
    -   podemos ter vários níveis de DM
        -   Ex: DW do brasil todos e DM representando regiões (Sul, Suldeste, Nordeste, etc)
    -   abrange dados novos e antigos
    -   dados completos e resumidos
    -   dados convertidos ou não

### Arquiteturas do DW e DM
- Data Marts Independentes
	![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/data-marts-independentes.png)

- Jub and Spoke
	![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/data-marts-conformidade.png)

- Hub and Spoke
	![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/hubs-and-spoke.png)

- DW distribuído
	![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/dw-distribuido.png)


### DW vs Data Marts
- Dados da corporação x dados de um grupo ou
departamento
- Assuntos gerais x assuntos específicos
- Decisões estratégicas x Decisões táticas
- Modelo dimensional em ambos

### DW vs DB Transacional
-   Objetivo
    -   BDT
        -   Rodar o negócio
        -   Operações diárias
    -   DW
        -   análise do negócio
        -   decisões estratégicas de longo prazo
-   Tipo de informação
    -   BDT
        -   Operacional
    -   DW
        -   Informativo/analítico
-   Unidade de trabalho
    -   BDT
        -   Consulta, Inserção, Alteração, Exclusão
    -   DW
        -   Carga e consulta
-   Granularidade
    -   BDT
        -   Dados detalhados
    -   DW
        -   Dados detalhados e resumidos
-   Dados
    -   BDT
        -   Atuais/Operacionais
    -   DW
        -   Históricos

### Ciclo de Desenvolvimento
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/ciclo-desenvolvimento-dw.png)

### Back Room e Front Room DW
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210518/resources/back-end-front-end-dw.png)

### Quais são os principais aspectos positivos decorrentes da implantação de um Data Warehouse? E os aspectos negativos?
Uma dos grandes aspectos positivos decorrente da implantação do Data Warehouse, de acordo com Bill Inmon, é o suporte adicional dado ao processo gerencial de tomada de decisões, pois, através do Data Warehouse, análises e informações estratégicas para o negócio podem ser produzidas.

As informações contidas dentro do DW são provenientes de fontes diversas e o DW permite a centralização destas informações em um local.

Antes de se armazenar os dados, ocorre um processo transformação, o que permite armazenar dados mais "limpos" e padronizados. Outro aspecto positivo da utilização do DW, é o  **não**  impacto nos sistemas transacionais, pois, por se tratar de um sistema apartado, consultas e interações com o DW não degradam o desempenho do ambiente, sistemas e serviços do transacional da companhia.

Podemos citar como aspectos negativos a dificuldade de capturar, **transformar e padronizar os dados** que são proveniente de diversas fontes em dados significativos para o DW. Devido ao aumento constante do volume, os dados podem ficar **obsoletos** e o sistema de consulta do DW degradado. Por conter informações sensíveis deve-se implementar e gerenciar políticas de segurança elaboradas para evitar acesso indevido aos dados.

#### Positivos e Negativos Tópicos
```
Positivos
-   Integração de diversas fontes de dados
-   Acesso facilitado a dados históricos
-   Possibilidade de analisar diferentes janelas de tempo
-   Separar operações de operações convencionais e de tomada de decisão
-   Acesso a relatorios estruturados ad-hoc
-   redução do tempo total para análise
-   Análises e informações estratégias para o negócio podem ser produzidas
-   Armazenar dados mais limpos e padronizados

Negativos
- amplia possíveis problemas com garantia de segurança 
- dificilmente implementação de alterações na implementação dos modelos 
- custos de projeto, instalação e manutenção
- curva acentuada de aprendizado e aceitação
- Não suporta dados não estruturados
```

### Modelagem Dimensional
-   Estrutura de dados  **Medições**  e  **Dimensões**
    -   **Medições:**  Dados numéricos: **Tabela Fato**
    -   **Dimensões:**
        -   Parâmentro do negócio
        -   Tabela satélites vinculadas à tabela fato central:  **Tabelas Dimensão**

#### Tabela Fato
-   Chaves estrangeiras
-   Valores  **Fato**  que representam a medição do item que está sob foco.
    -   Valores numéricos (medições)
    -   **Cada valor tem Interseção de todas dimensões**
    -   **Exparso**: Não há dados em todas interseções
-   contém indicadores importantes para uma área de negócio

####  Tabelas dimensão    
-   Chaves primarias ficam aqui
-   Atributos descritivos
-   definem propriedades da dimensão
-   Campo numérico: fato ou atributo?
	-   Se varia a cada amostragem -> fato
	-   Se é uma descrição praticamente constante de um item -> atributo

#### Cubo de dados
-   Cubo de Dados: denominação de uma estrutura dimensional produzida por uma consulta
-   Dimensões originais: produto, loja e tempo
-   Cube. Another term for a  **fact table**. It can be represented "n" dimensions, rather than just three (as may be implied by the name).

#### Modelo Roll Up/Drill Down/ Drill Across
- Slice (left) & Dice (right)
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210525/resources/slice-dice.png)

### Estruturação dos Dados
- Cumulativo
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210525/resources/estruturacao-dados-dw-granularidade-cumulativo.png)
- Rotativo

![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210525/resources/estruturacao-dados-dw-granularidade-rotativo.png)

### Ferramentas OLAP
> Tecnologia de software que permite que analistas, gerentes e executivos obtenham, de maneira rápida, consistente e interativa, acesso a uma ampla variedade de visualizações possíveis de informações que reflita a dimensão real do empreendimento do ponto de vista do usuário

#### O que é OLAP?
-   Suportar análises e Consultas AD Hoc
-   Acesso às informações no modelo multidimensional
-   Informações: visualizadas por gráficos / relatórios / tabelas
-   Visão Multidimensional: visualizar cubos de informação sob **diferentes ângulos** (slice/dice) e **níveis de agregação** (drill/down)

#### Características Ferramentas OLAP
- Paging: apresentação em várias páginas
- Filtering: filtragem de dados
- Rotacionamento: rotação do cubo
- Breaks: separar grupos de informações
- Sorts: ordenamento de informações
- Exceções: restringir grupos de valores
- Visualização de limites: diferenciação de cores/fontes

#### ROLAP vs MOLAP vs DOLAP
- **ROLAP** - Relational OnLine Analytic Processing
	- Extrair dados diretamente do esquema dimensional
	- Acesso a todos os dados (sumarizados/detalhados)
	- Maior tempo de acesso em relação ao MOLAP e ao DOLAP
- **MOLAP** - Multidimensional OnLine Anaytic Processing
	- Cubos pré-montados armazenados no servidor
	- Tempo de acesso reduzido
	- Restrição a consultas (cubo pré-montado)
- **DOLAP** - Desktop OnLine Analytic Processing
	- Cubos pré-montados armazenados no cliente
	- Tempo de acesso reduzido
	- Restrição a consultas (cubo pré-montado)
	- Transmissão do cubo pela rede de comunicação

### Variantes do Modelo Dimensional Star
#### Star Completo
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210601/resources/star-completo.png)

#### Star Particionado da Tabela Fata
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210601/resources/star-particao-tab-fato.png)

#### Star Particionado das Tabelas Dimensão![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210601/resources/star-particao-tab-dimensao.png)

#### Snowflake Chain
- "É tipo uma normalização"
- Normalizar tabelas dimensão

- Snowflake chain 
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210601/resources/snowflake-chain.png)

- Snowflake Lookup 
![](https://github.com/AugustoCalado/USP-Software-Technology-Postgraduate/raw/main/2-Trimester/Software-Engineering-for-Large-Software-Systems/20210601/resources/snowflake-lookup.png)

