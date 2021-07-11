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

### Metadados
Dados sobre os dados
-“Sombra” de dados
-“DNA” dos dados
-Em períodos longos de tempo
	- Significado dos dados pode se alterar
	- Controle do histórico de alterações
-Dados que descrevem
	- Estrutura dos dados
	- Algoritmos de extração/ sumarização
	- Mapeamento ambiente operacional ---> DW (fontes de informação)
- Origem/Destino dos dados

### ETL
- **Extrair Dados**
	- Data Profiling: análise técnica dos dados para descrever seu conteúdo, consistência e estrutura
	- Change Data Capture : identificar os dados que sofreram alterações desde a última carga
	- Extract: eventuais descompressão e decriptação dos dados
- **Limpar e processar dados**
	- Data Cleansing: corrigir dados “defeituosos”, descrição de erros, métricas de QD
	- Deduplication: eliminar replicações do mesmo dado
	- considerações
		- Mesmos dados com nomes diferentes
		- dados diferentes com mesmo nome
		- valores impossíveis
- **Entregar os dados**
	- Gerenciador de Dimensões de Modificação Lenta
	- Gerador de Surrogate Keys

- Tipos de carga 
	- Carga inicial
	- Cargas periódicas de dados

- ETL Fontes de dados Externos
	- Jornais/revistas
	- Boletins informativos
	- Relatórios
	- Características
		- Periodicidade não é fixa
		- Formato variável

### DW - Passos para o Projeto
- Especificação do DW
- Projeto da Matriz de barramento
- Projeto da tabela fato
- Definição dos fatos
- Granularidade da tabela fato
- Definição das dimensões
- Dimensões de Modf. Lenta
- Amplitude tempo
- Intervalo de Extração

## Big Data
- Dados contêm informação/conhecimento significativo e que pelo seu custo e tempo de obtenção merecem tratamento adequado
- Compreensão: análise, captura, tratamento, armazenamento, compartilhamento, consulta e visualização
- Problema: tomar grandes e complexos conjuntos de dados que os aplicativos tradicionais não consigam processar em tempo adequado

> When data sets do not fit in main memory (in core), or when they do not fit even on local disk, the most common solution is to acquirer more resources

- Os dados são “big” quando seu tamanho, variedade e velocidade de geração tornam-se elementos ativos do problema

> Big data consists of extensive datasets, primarily in the characteristics of volume, variety, velocity, and/or variability - that require a scalable architecture for efficient storage, manipulation, and analysis

> The Big Data paradigm consists of the distribution of data systems acreoss horizontally coupled, independent resources to achieve the scalability needed for the efficient processing of extensive datasets

> Big Data is a term applied to data sets whose size is beyond the ability of commonly used software tools to capture, manage, and process the data within a tolerable elapsed time. Big Data sizes are a constantly moving target currently ranging from a few dozen terabytes to many petabytes of data in a single data set.

- Dados
- Volume, variedade, velocidade, variabilidade, veracidade, visualização, valor

### Os V's do Big Data
- Volume
- Variedade
	-  Múltiplos repositórios de origem
	- Múltiplos formatos  Estruturados, Não Estruturados, Semi Estruturados
	-  Textos, vídeos, redes sociais, tabelas, imagens, sensores
- Velocidade
	- Geração de dados cada vez mais acelerada
	- Necessidade de processamento mais rápido
- Veracidade
	- Origem conhecida e confiável
	- Confiança no significado e no conteúdo dos dados
	- Qualidade dos dados: completeza, acurácia
- Valor
	- Grau de utilidade
- Variabilidade
	- Alteração ou inserção de novos significados dos dados
- Visualização
	- utilizar a formas gráficas mais úteis e acessíveis
- Validade/Volatilidade
	- qual o período de utilidade dos dados

### Aplicações
- Instituições financeiras: entender e aumentar satisfação de clientes; minimizar riscos e fraudes
- Governo: gestão de serviços públicos, questões de defesa nacional, . . . .
- Saúde: análise de registros de pacientes para predição/reação a eventos clínicos ---> tratamentos melhores e mais rápidos
- Comércio: Análise de Fidelidade, Análise da Concorrência e de Risco de Clientes (Pão de Açucar, Vivo, Amazon, . . . .)
- Análise do clima: dados de centrais meteorológicas
- Manutenção de equipamentos: previsão de panes 
- Educação: identificar alunos com dificuldades, implementar melhores sistemas de avaliação

### Camadas da Arquitetura Big Data
1. Obtenção dos dados
	- Obtenção de dados estruturados, semiestruturados e não estruturados  --> Variedade
	- Formatos variáveis
	- Velocidade
	- Frequência de obtenção dos dados: sob demanda, contínua, real-time
2. Armazenamento dos Dados
	- Armazenar e/ou processar esses dados -> cluster master/slave
3. Análise dos dados
	- Utilizar ferramentas apropriadas (**data mining**, IA, estatśtica)
	- Gerar os documentos necessários
	- entregar aos profissionais adequados
	- analisar: métodos descritivos, diagnóstico, preditivo, prescritivo
4. Consumo dos Resultados da Análise
	- Humanos ou aplicativos
	- Utilização adequada desses resultados `->` tomada de decisões e de ações `->` visa melhorar a tomada de decisões nos negócios

A. Integração dos dados
- Definir as ferramentas de software para as camadas lógicas
- Definir os tipos de bancos de dados a serem formados

B. Governança de Big Data
- Gerenciar grandes volumes de dados
- Definir as políticas de uso, armazenamento e remoção de dados

C. Qualidade de Serviços
- Disponibilizar os dados em tempos adequados
- Verificar a correção e precisão dos dados
- Respeitar a política de privacidade

### Big Data Analítico - Técnicas
- Processo de examinar grandes conjuntos de dados para obter padrões, correlações, tendências “ocultas"
- Ferramentas: data mining, text analytics, análise estatística e preditiva
- Aprendizado de máquina: uso de algoritmos para reconhecer padrões complexos 
- Processamento de Linguagem Natural - IA e linguística: algoritmos para analisar a linguagem humana 
- Reconhecimento de Padrões: técnicas de aprendizado de máquina

### Big Data Analítico - Tipos de análise
- descritiva
	- identificar e avaliar os atributos
	- estimar a contribuição dos atributos no resultado
- diagnóstica
	- Extrair padrões a partir dos dados
- Preditiva
	- Determinar a probabilidade de possíveis resultados
- Prescritiva
	- Ações indicadas para obter os resultados desejados

### Hadoop
- Hadoop: software open source coordenado pela Apache Software Foundation. 
- Armazenamento e processamento distribuído de grandes conjuntos de dados em clusters de computadores “comuns” 
- Framework para ambientes distribuídos usado principalmente para análise de grandes volumes de dados 
- HDFS (Hadoop Distributed File System) Armazenamento de dados confiável (redundante e com alta disponibilidade) 
- MapReduce: Computação paralela de alto desempenho Processamento de conjuntos de dados, reduzindo o volume da saída de dados 
- Common Utilities: conjunto de bibliotecas e utilitários comuns que auxiliam outros módulos Hadoop

#### Serviços Principais
- Map Reduce (Computação distribuído)
	- Dados são divididos em porções 
	- Porções são processadas em paralelo 
	- Geram resultados intermediários 
	- Resultado final agrega tais resultados intermediários
- HDFS (Armazenamento Distribuído)
	- Suporta qualquer tipo de dados 
	- Gerencia o conjunto de servidores 
	- Armazenamento de grandes conjuntos de dados de forma distribuída
- Common Utilities

### Fato vs Mito
- Mito: Hadoop tem a preocupação exclusiva com grandes volumes de dados
	- Fato: Hadoop também tem como foco a diversidade de dados - pode gerenciar o acesso a qualquer tipo de dados, armazenando-os no HDFS
- Mito: o HDFS é o gerenciador de dados do Hadoop 
	- Fato: O HDFS é um sistema de arquivos e não um gerenciador de bases de dados - podem ser usados como gerenciadores o Hbase ou o Hive
- Mito: O MapReduce faz parte do HDFS 
	- Fato: HDFS e MapReduce fazem uma boa parceria, mas um pode ser usado sem o outro
- Mito: Hadoop é uma alternativa/substituto do Data Warehouse 
	- Fato: Hadoop pode auxiliar um Data Warehouse, mas não substituir

### DW vs Big Data
```
DW: Arquitetura para armazenamento e consulta de dados
BgD: Tecnologia para tratar e consultar grandes conjuntos de dados

DW: Processamento centralizado 
BgD: Processamento distribuído

DW e BgD: Análise de questões importantes das atividades da empresa / organização

DW: Dados estruturados 
BgD: Dados estruturados e semiestruturados 

DW: Bases de dados relacionais 
BgD: Bases de dados relacionais e NoSQL
``` 

## Data Lake
> Data Lake é um repositório enorme que acolhe todos os tipos de dados em seus formatos nativos, sendo que, em algum momento será utilizado por alguém da organização

### Esquema On Write
- A estrutura dos dados deve ser totalmente definida antes da escrita de qualquer dado: tabelas, colunas, chaves, ...
- Inclui tipos de dados e tamanhos
- Estrutura otimizada para consultas mais rápidas
- Dificuldade de se implementar mudanças nessa estrutura

### Esqema On Read
- Não é necessário definir a priori a estrutura dos dados
- **O esquema é definido quando os dados são lidos, mas não quando são armazenados** 
- No momento da leitura define-se quais serão os dados necessários a cada objetivo 
- Dados não são alterados ou descartados no momento do armazenamento 
- Sem o ETL, os dados devem ser tratados no momento da leitura `->` consultas mais lentas

### Riscos do Data Lake
- Armazenar dados sem uso (“one way”) 
- Pode se tornar um grande “acumulador” de dados 
- Não há relacionamento entre os dados: dificulta a etapa de análise 
- Dados úteis podem ficar ocultos / escondidos 
- Eventualmente o usuário deve ser expert nos dados
- Dificuldade em se ter boa qualidade dos dados 
- Sem metadados pode não ser possível um uso adequado dos dados 
- Questões de segurança: os dados devem ter restrições de acesso que o Data Lake não implementa 
- Necessidade de grande capacidade de armazenamento

### Transformar o Data Lake na “Mina de Ouro”
 - Hadoop 
 - Amazon Web Services (AWS) 
 - Microsoft Azure 
 - Google Cloud Platform

### DW x Data Lake
```
DW: Arquitetura para armazenamento e consulta de dados
DL: Tecnologia para tratar e consultar grandes conjuntos de dados

DW: Processamento centralizado 
DL: Processamento distribuído

DW e DL: Análise de questões importantes das atividades da empresa / organização

DW: Dados estruturados 
DL: Dados estruturados e semiestruturados 

DW: Esquema de dados de difícil alteração
DL: Sem esquema

DW: Consistência alta
DL: Consistência baixa
``` 

## Data Mining
- Aplicação de técnicas de descoberta do conhecimento  Estatística e Inteligência Artificia para identificação de regras, padrões, restrições e distinções (outliers).
- Extração não trivial de conhecimento implícito, previamente desconhecido e potencialmente útil
- Exploração e análise por meios automáticos / semiautomáticos de gdes qdades de dados para obter padrões com significado
- Ferramenta utilizada para descobrir novas corrrelações, padrões e tendências entre as informações de uma empresa, através da análise de grandes quantidades de dados armazenados em Data Warehouse usando técnicas de reconhecimento de padrões, estatísticas e matemáticas.”

### Desafios 
- Escalabilidade: capacidade de processar volumes crescentes de dados
- Dimensionalidade: gde nº de atributos e/ou variáveis 
- Dados complexos e heterogêneos 
- Qualidade dos dados
- Preservação da privacidade/propriedade dos dados

### Paths
- `[[treinar][testar]]`
	- Modelo
		- Resultados

### 80/20
- Princípio de pareto: 80% da informação útil está localizada em 20% dos dados

### KDD-Knowledge Discovery in Database
- KDD: processo completo de aquisição de conhecimento 
	- Tarefa multidisciplinar
	- Técnicas utilizadas em várias áreas  BD, DW, IA, Estatística 
- Data Mining: componente do processo

### Algoritmos de Data Mining
- Predição
	- Identificar/predizer classe/ valor de novos dados a partir de dados conhecidos 
	- Treinamento, teste, avaliação e classificação 
		- Classificação 
		- Regressão
	- Classes previamente determinadas
- Descrição
	- Identificação de padrões de comportamento comuns
	- Clustering 
	- Sumarização 
	- Regras de Associação
	- Caracterização
	- Discriminação
	- Evolução /Análises Sequenciais
	- Desvio
- Predição -> Classificação
	- Finalidade: predizer o comportamento 
	- Os atributos são divididos em classes/categorias já pré-definidas
	- Objetivo: obter uma função que mapeie um valor no conjunto de classes
	- Valores discretos
	- Métodos: mínima distância, hiperparalelepípedos, árvores de decisão, vizinhos mais próximos, redes neurais
- Predição -> Regressão
	- Similar à classificação, porém com valores contínuos 
	- Também visa predizer o comportamento / valores
	- Prever valor de gasto de clientes, com base no sexo, faixa de renda, ...
- Clustering
- Descrição -> Clustering
	- Os grupos devem ser formados a partir de propriedades comuns
	- Novos elementos são inseridos nos grupos
	- Agrupar objetos que possuem alto grau de similaridade em classes
	- Exemplos: agrupar clientes com comportamentos de compra similares, agrupar documentos relacionados, análise de cesta de mercado
- Sumarização
	- Descrição compacta para um subconjunto de dado
	- Ex.: resumos mensais variados
- Regras de Associação
	- Detecção de associações / conexões entre objetos 
	- Se X ocorre, então Y também ocorre 
	- Regra de associação: buscar itens que ocorrem simultaneamente
- Evolução / Análise Sequencial
	- Inclusão do fator tempo
	- Detecção e avaliação na evolução dos dados ao longo do tempo 
	- Ex.: obter padrão de evolução de vendas em 12 meses
- Desvios / Anomalias / Outliers
	- Identificação de elementos do conjunto de dados cujos valores diferem de um padrão ou da maioria dos valores
	- Comportamento “normal”: geralmente fornecido com base em alguma suposição (média, crescimentos lineares, ...) 
	- Ex.: desvio em relação a vendas médias ou com relação à altura média das pessoas