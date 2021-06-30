## Hadoop 
- Software open source coordenado pela apache
- armazenamento e processamento distribuido de grandes conjuntos de dados em clusters de computadores "communs"
- Framework para ambientes distribuídos usado principalmente para análise de grandes volumes de dados
- HDFS (Hadoop Distributed File System) - Armazenamento de dados confiável (redundante e com alta disponibilidade)
	- suporta qualquer tipo de dados
	- gerencia o conjunto de servidores
	- armazenamento de grandes conkuntos de dados de forma distribuida
- MapReduce - Computação paralela de alto desempenho Processamento de conjuntos de dados, reduzindo o volume da saída de dados
	- dados são divididos em porcções
	- porções são processados em paralelo
	- geram resultados intermediários
	- resuldado final agrega tais resultados intermediários
- Common Utilities: conjunto de bibliotecas e utilitários comuns que auxiliam outros módulos Hadoop

## DW vs Hadoop
- Distribuição (distribuição do processamento e dos dados) é o principal diferencial entre DW e Hadoop.
- Modelagem utilizada 
	- DW utiliza modelo multi-dimensional
	- Modelagem NoSQL

DW: Arquitetura para armazenamento e consulta de dados
BigData: Tecnologia para tratar e consutar grandes conjuntos de dados

<br>

DW: processamento centralizado
BigData: Processamento distribuído

DW: Dados Estruturados
BigData: Dados estruturados e semi-estruturados

DW: Bases de dados relacionais
BigData: Base de dados relacionais e NoSQL

DW e BigData: Análise de questões importantes das atividades da empresa/organização



## Hadoop Arquitetura
- TODO get image slide 87
- Cliente
- Master
- Slave

### Tarefas Executadas - Cliente
- Escrever um arquivo no HDFS
	- Comunica-se com o NameNode para obter os metadados
		- NameNode responde com o número de blockos e sua localização
			- O Cliente divide o arquivo em blocos e os envia ao primeiro DataNode
				- Esse DataNode replica o bloco a mais dois DataNodes e envia uma confirmação ao NameNode

<br>

- Solicitar uma tarefa ao Job Tracker
	- JobTracker distribui a tarefa aos Task Trackers - Fase Map
		- Task Trackers executam a Fase Map
			- Job Tracker distribui a tarefa aos Task Trackers - Fase Reduce
				- Task Tracker Executam a Fase Reduce

<br>

- Ler um arquivo do HDFS
	- Interage com o NameNode para obter a localização dos blocos
		- Interage com os DataNodes indicados, havendo troca de mensagens e verificação de autorização

<br>

- Armazenam os blocos de dados originais
- processam grandes volumes de dados de forma paralela, dividindo o trabalho em frações independentes
- executado as tarefas Map e/ou Reduce - modelo de programação, não uma linguagem
- Se a comunicação com a master atingir um limite de tempo sem resposta -> assume-se falha

### Tarefas Executadas - Master
- Recebe um serviço solicitado pelo Cliente
- Cria um plano de execução: determina quais Slaves serão acionados
- Gerencia a execução das tarefas (conhece os recursos consumidos e os disponíveis)
- Gerencia arquivos armazenados e sua divisão em blocos (arquivos de 128MB)
- Controla replica dos dados (3 réplicas de cada arquivo)

<br>

- Verifica o processamento e intervalos pré-definidos
- modifica as atribuições em caso de falha
- Namenode armazena os metadados necessários: nome e tamanho dos arquivos, localização dos bloos, datas de criação e modificação
- novos dados/arquivos são frequentes -> NameNode guarda as informações sobre a localização dos arquivos em memória


## Data Lake
Data Lake é um repositório enorme que acolhe todos os tipos de dados em seus formatos nativos, sendo que, em algum momento será utilizado por alguém da organização.

### Esquema On Read e On Write
#### On Write
- Antes dos dados serem gravados no disco, precisamos realizar os seguintes passos
	- A estrutura dos dados deve ser totalmente definida antes da escrita de qualquer dado: tabelas, colunas, chaves
	- Incluir tipos de dados e tamanhos
	- Estrutura otimizada para consultas mais rápidas
	- Dificuldade de se implementar mudanças nessa estrutura

#### On Read
- Não é necessário definir a priori a estrutura dos dados
- o esquema é definido quando os dados são lidos, mas não quando são armazenados
- no momento da leitura define-se quais serão os dados necessários a caa objetivo
- dados não são alterados ou descartados no momento do armazenamento
- sem o etl, os dados devem ser tratados no momento da leitura -> conultas mais lentas

### Data Lake - Etapas
1. Ingstão de dados
2. Seleção dos dados a serem analisados
3. Aplicação de ferramenta analítica de dados
4. Utilização dos resultados da análise

### Arquitetura
- Dados estruturados, semi-estruturados e não estruturados
	- Ferramenas de extração e carga de dados (hadoop, etc)
		- Data Lake
			- ferramentas de extração de dados
				- Big Data
				- DW 
#### Outras Nomeclaturas Arquitetura
- Landing Zone ~ ingestão
- Standardiztion zone ~ armazenamento de dados padronizados
- Analytics SandBox ~ ferramentas de análise dos dados

### Metadados
- Metadados: etiquetar todos os dados brutos
- tem um mpeamento dos dados
- conhecer o contexto/origem dos dados
- ter, a priori, uma indicação de como tratar os dados

### Riscos do Data Lake
- Armazenar dados sem uso ("one way")
	- Guardar só por guardar
	- Pode se tornar um grande acumulador de dados
- Não há relacionamento entre os dados: dificulta a etapa de análise
- dados uteis podem ficar ocultos
- Pelo fato de armazenar o dado sem tratamento prévio há uma dificuldade em se ter boa qualidade de dados
- sem metados pode não ser possivel um uso adequado dos dados
- questões de segurança: os dados devem ter restrições de acesso que o Data lake não implementa
- Necessidade de grande capacidade de armazenamento

### Data Lake vs DW
DW: Arquitetura para armazenamento e consulta de dados 
DL: Tecnologia para tratar e consultar grandes conjuntos de dados

DW: Processamento centralizado
DL: Processamento distribuído

DW: Dados estruturados 
DL: Dados estruturados, semiestruturados e não estruturados

DW: Esquema de dados de difícil alteração 
DL: Sem esquema 

DW: Consistência alta
DL: Consistência baixa

DW: Esquema on write: processa os dados antes de armazenar -> “dados limpos” 
DL: Esquema on read: armazena os dados antes de processar ->  “dados brutos”

DW: Baixa Granularidade
DL: Alta granularidade

DW: Expectativa de uso de todos os dados
DL: Expectativa de uso de parte dos dados
