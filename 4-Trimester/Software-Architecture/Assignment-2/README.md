# Viewpoints modeling and the RM-ODP

- Due to the extensive system specifications, it is extremelly difficult for a single individual comprehend all aspects of the system specs. Furthermore, there are different interest for each stackeholder of a given system and different reasons for examining the system's spec.
- RM-ODP plays a big role in provide separate viewpoits into the spec of a given complex system
	- These views each satisfy an audience with a particular interest in a set of aspects of the system.

- Viewpoint is a subdivision of the spec of a system. They are separately specified, but not completely independent. They are just sufficiently independent to simplify reasoning about the complete specification.

- Enterprise viewpoint: 
	- Purpose, scope and policies of the system
	- It describes business requirements and how to meet them
	- Aspectos de consideração:
		- Identificação e descrição do negócio, incluindo responsáveis, regras, ações, propósitos, uso e políticas da empresa
		- Identificação da visão estrutural do negócio
	- Atividade
		- Descrever as comunidades e os objetivos de cada uma
		- Descrever o comportamento necessário para cumprir os objetivos das comunidades

- Information viewpoint
	- semantics of the information 
	- information processing performed
	- It describes information managed by tge system
	- Also, it describes the structure and content type of the supporting data
	- Aspectos de consideração:
		- Identificação e descrição das informações que fluem através do processo de negócio
			- informações que fluem pelo processo
		- Identificação e descrição das informações que são utilizadas na visão estrutural de negócio
			- informações da visão estrutural do negócio

- Computational viewpoint
	- it describes functionality provides by the system and its functional decomposition
	- the functional decomposition shows the "objects" present within the system and how they iteract thorough interfaces
	- Baseado nos seguintes objetos:
		- objetos que encapsulam dados e processamento
		- objetos que oferecem interfaces para interação com outros objetos
		- objetos que podem oferecer interfaces multiplas
	- Visão define os objetos dentro do sistema, as atividades dentro desses objetos e as interações que ocorrem entre os objetos.
	- Maioria dos objetos nessa spec descrevem funcionalidades da aplicação e estes objetos são unidos por ligações pelas quais as interações acontecem.
	- Aspectos de consideração:
		- Infra que fornece suporte ao negócio
			- ex: para identificar as infos sobre crédito do cliente, a instituição já possui infra pronta para tal realização
		- Sistemas existentes que já apóiam o negócio
			- ex: já existia o sistema de conta-corrente e pagamento. Para o IB é necessário implementar a interação entre o cliete na internet e esses sistemas através de um ambiente seguro e controlado

- Engineering viewpoint
	- It describes the distribution of processing performed by the system to manage info and provide funcionality
	- focuses on the mechanisms and functions required to support distributed interactions between objects in the system
	-  focado no modo como é alcançada a interação dos objetos no ambiente distribuíd
	- Aspectos de consideração:
		- especificar a distribuição de sistemas e repositórios corporativos já existentes na empresa
		- comparar com os serviços de negócio identificados e com a localização fisica das unidades de negócio

- Technology viewpoint
	- focuses on the choice of technology of the system
	- It describes the technologies chosen to provide the processing, functionality and presentation of information.
	- Aspectos de consideração:
		- validar e verificar a aderência dos serviços de neǵocio com frameworks tecnológicos candidatos
		- verificar a necessidade de aquisição de outras tecnologias
