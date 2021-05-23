# Summary Draft
## Temas sugeridos
**Como o DevOps Pode Apoiar o Processo de Desenvolvimento de Software em Times Ágeis?**  DevOps é uma nova instância do agile software Development?

- **Contextualização do processo de desenvolvimento de software**
  - Atual vs Antigo 
  - O que mudou?

The software process involves the steps necessary to produce a software product. Understanding the requirements for that software product, including regulatory, industry, and safety requirements, is fundamental before choosing a particular process. Such requirements may dictate the methods required within the software process.

Meados da década de 1990, a duração do design, desenvolvimento e suporte do produto era previsível o suficiente para que as empresas e seus funcionários fizessem planos para novos projetos em torno da data de release do produto em desenvolvimento.

Da perspectiva de uma equipe de desenvolvimento, a release do produto representou um processo de ciclo fechado que era repetível e padronizado.

Caso existisse eventuais bugs, partes dos desenvolvedores era alocado para arrumá-lo, mas os demais eram alocados para a próxima versão

Advento da Internet, evolução do hardware, computadores mais potentes, smartphones,  aplicativos e IoT.

To succeed in a world where technologies, requirements, ideas, tools, and timelines are constantly changing, information must be accurate, readily available, easily found, and ideally delivered constantly, in real-time, to all team members.

O modelo usado até então, não é o suficiente para existir na nova realidade. Quando um produto é lançado, agora, não há mais planos para suspender a funcionalidades, mas sim para dar o suporte contínuo.  A engenharia de software, agora, foca na longevidade e na escalabilidade quando se discute requisitos do produto. 

- **Comentar sobre os princípios dos métodos ágeis no desenvolvimento de software**


Agile development methodologies team to adapt to rapid and often significant change while maintaining project momentum, is predicated on the fact that ever-changing requirements, constraints, and customer needs will continually impact all areas of a project throughout its life cycle

Agile methodologies are software development methods that focus on iterative and incremental development methods that focus on iterative and incremental development, often emphasizing direct and constant communication with stakeholders, adaptive planning, and ever-evolving requirements 

Modern processes have gravitated towards Agile methodologies, embracing iterative development and expecting constant change throughout the project life cycle.

- **Comentar sobre o fenômeno DevOps**


DevOps busca estender a colaboração de desenvolvimento para operações, que é responsável por implantar, gerenciar e apoiar o desempenho dos sistemas [2].

DevOps means a culture shift  toward collaboration between development, quality assurance, and operations (PS: operations staff are those in charge of quality control, packaging, and release products).

Devops helps deliver value faster and continuously, reducing problems due to miscommunication between team members and accelerating problem resolution.

Continuous delivery will improve time to market and allows agile practices with rapid consumer feedback.

In today’s age continuous integration and deployment, automated testing, and remote updates are not just nice to have. These methods are necessary for survival in the market. 

- **Correlacionar DevOps e Métodos Ágeis**


Com a ampla adoção das metodologias ágeis nos processos de desenvolvimento de software das empresas a forma tradicional de desenvolvimento de software mudou, novas tarefas e procedimentos foram introduzidos.
Como as mudanças contínuas e “impactantes” previstas pelo desenvolvimento de software ágil são impactadas pela implantação das práticas propostas pelo DevOps?
Scientific articles framed DevOps as a type or part of agile software development [20–22].

DevOps builds upon agile software development practices, especially continuous integration in [22,26,30–33]. Also, DevOps practices enhance existing agile practices and roles by also taking account of operations activities. 


**Links dos artigos**

https://sci-hub.se/10.1109/MS.2016.68
https://sci-hub.se/https://doi.org/10.1007/978-3-319-49094-6_44
https://sci-hub.se/https://doi.org/10.1007/978-3-030-00623-5_1
https://sci-hub.se/https://doi.org/10.1007/978-3-319-18612-2_19
https://sci-hub.se/https://doi.org/10.1007/978-3-319-49094-6_27
https://sci-hub.se/https://doi.org/10.1007/s10796-019-09905-1



### **Software Development Process by M. Kraeling and L. Tania**

The software process involves the steps necessary to produce a software product. Understanding the requirements for that software product, including regulatory, industry, and safety requirements, is fundamental before choosing a particular process. Such requirements may dictate the methods required within the software process.

### **DevOps by Christof Ebert**

DevOps means a culture shift  toward collaboration between development, quality assurance, and operations (PS: operations staff are those in charge of quality control, packaging, and release products).

Devops helps deliver value faster and continuously, reducing problems due to miscommunication between team members and accelerating problem resolution.

Continuous delivery will improve time to market and allows agile practices with rapid consumer feedback.

In today’s age continuous integration and deployment, automated testing, and remote updates are not just nice to have. These methods are necessary for survival in the market. 

#### **Build, Continuous-Integration, Deployment, Operations (Monitoring)**

Build: Achieve fast iteration, managing software development and life cycle by compiling code, managing dependencies, generating documentation, running tests.
Continuous-Integration: Integrate developers’s work as early as often as possible in a way that the system is constantly tested.
Deployment: Treat infrastructure as code so that it can be versioned, replicable and testable. Also, it can reduce provisioning and configuration time compared with manual infrastructure.
Operation: maintain your infrastructure’s stability, performance and resolve IT infrastructure problems before they affect critical business processes.

#### **Challenges for Culture Shift**

Breaking complex architectures and features sets into small chunks that can be produced and deployed independently.
Maintaining a configuration and build environment that provides constant visibility of what is deployed (which versions and dependencies).
introducing a purpose-built development and production environment derived from legacy application life-cycle management or product life-cycle management environments.
bridging the traditionally siloed cultures of development (which operations folk perceive as cumbersome and expensive because of its thoroughness) and operations (which developers perceive as quick and dirty).
	

### **Modern DevOps: Optimizing Software Development Through Effective System Interactions by C. Cois, J. Yankel and A. Connel**

A causa raiz para o sucesso de um produto de software é a transmissão de informação de forma rápida, precisa e acessível entre os atores participantes do SDLC.

Agile development methodologies team to adapt to rapid and often significant change while maintaining project momentum, is predicated on the fact that ever-changing requirements, constraints, and customer needs will continually impact all areas of a project throughout its life cycle

Agile methodologies are software development methods that focus on iterative and incremental development methods that focus on iterative and incremental development, often emphasizing direct and constant communication with stakeholders, adaptive planning, and ever-evolving requirements 

Modern processes have gravitated towards Agile methodologies, embracing iterative development and expecting constant change throughout the project life cycle.
A automação proporcionada pelo DevOps trás melhorias para o processo de desenvolvimento de software no que se diz respeito ao gerenciamento e transmissão de determinadas informações.

A adição de sistemas automatizados permite a transferência responsabilidade da execução e controle tarefas de atores humanos para computadores, liberando, assim, os atores humanos para se concentrarem em tarefas especializadas como desenvolvimento de software.

Portanto, o principal objetivo é maximizar a quantidade de esforço que os atores humanos têm disponível para realizar essas tarefas especializadas.

#### **Tarefas que podem ser automatizadas**
- Source Code por meio do Source Control System
- Tasks e issues por meio do Issue/Task Tracking System
- Corretude e qualidade do source code por meio do Code Review System
- Compilation, build e testes por meio do Build/Continuous Integration System (CI)
- Monitoring por meio de do Monitoring System
- Documentation System, Integration Environment e Communications Systems
