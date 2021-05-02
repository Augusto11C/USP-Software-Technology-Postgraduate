Clean Architecture
Visão Geral
TODO Escrever uma motivação, contextualização do problema.

The construction and the long-term maintenance of robust software architecture is a demanding task. Software architects often face the problem to ensure the extensibility of systems so that new components can be added and existing ones can be removed or replaced easily. Linearly with software growth, these aspects of software engineering are getting more and more difficult because oftentimes the separation of concerns and the decoupling of components are not considered in the beginning of the development.

Every software system provides two different values to the stakeholders: behavior and architecture [1] (cap.2, pag.: 13). The second of these is the greater of the two because it is this value that makes software “soft” (in other words, change behavior easily). The first value of software is its behavior that refers to what the software does, what it delivers for the users, and what generates value. Programmers write the code to satisfy stakeholder’s requirements. [1]

Linearly with the growth of the code base of a software project, its complexity and cost of change increases [1] (estudo de caso, pag.: 5)

To build a system with a design and an architecture that minimize effort and maximize productivity, you need to know which attributes of system architecture lead to that end. [1] (cap. 1, pag.: 12)

The difficulty in making such a change should be proportional only to the scope of the change, and not to the shape of the change.

[1] (cap.2, pag.: 18)

The primary cost of maintenance is in spelunking and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect.  [1] (cap. 15, pag.: 139)

The goal of software architecture is to minimize the human resources required
to build and maintain the required system.  [1] (cap.1, pag.: 5)

O que é Arquitetura?
Usually “architecture” means structure at a high-level, and “design” means structure at a low-level. But Low-level details (design) and the high-level structure (architecture) are all part of the software design.

The architecture of a software system is the shape given to that system by those who build it. The form of that shape is in the division of that system into components, the arrangement of those components, and the ways in which those components communicate with each other. (cap. 15, pag.: 137)

The architecture of a system has very little bearing on whether that system works. [1] (cap. 15, pag.: 137)

The primary purpose of architecture is to support the life cycle of the system. [1] (cap. 15, pag.: 137)

The ultimate goal is to minimize the lifetime cost of the system and to maximize programmer productivity. [1] (cap. 15, pag.: 137)

A carefully thought-through architecture vastly mitigates these costs. By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage. [1] (cap. 15, pag.: 139)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139)

The way you keep software soft is to leave as many options open as possible,
for as long as possible. What are the options that we need to leave open? They
are the details that don’t matter [1] (cap. 15, pag.: 140).

All software systems can be decomposed into two major elements: policy and details. The policy element embodies all the business rules and procedures. The policy is where the true value of the system lives.

The details are those things that are necessary to enable humans, other systems, and programmers to communicate with the policy, but that do not impact the behavior of the policy at all (e.g. IO devices and databases) [1] (cap. 15, pag.: 140).

The goal of the architect is to create a shape for the system that recognizes policy as the most essential element of the system while making the details irrelevant to that policy. This allows decisions about those details to be delayed and deferred [1] (cap. 15, pag.: 140).

One of the benefits of developing the high-level policy without committing to the details that surround it, is that when the time for the decision arrives it can be made in a better way (taking in account all of the high-level policies that already were developed [1] (AUG) (cap. 15, pag.: 140).

If you can develop the high-level policy without committing to the details that surround it, you can delay and defer decisions about those details for a long time. And the longer you wait to make those decisions, the more information you have with which to make them properly [1] (cap. 15, pag.: 141).

Architecture’s Concern Aspects

Use Cases

The most important thing a good architecture can do to support behavior is to clarify and expose that behavior so that the intent of the system is visible at the architectural level. The use cases of that system will be plainly visible within the structure of that system.  [1] (cap. 16, pag.: 148). 

Operation

Development
A system that must be developed by an organization with many teams and many concerns must have an architecture that facilitates independent actions by those teams, so that the teams do not interfere with each other during development. This is accomplished by properly partitioning the system into well-isolated, independently developable components. Those components can then be allocated to teams that can work independently of each other [1] (cap. 16, pag.: 150). 

Deployment


A good architecture balances all of these concerns (use cases, operation, development, deployment) with a component structure that mutually satisfies them all [1] (cap. 16, pag.: 150). This is hard because all the use cases are not known, nor do we know operational constraints, the team structure, or the deployment requirements. And to turn things worse, they will inevitably change as the system moves through its life cycle. 

Princípios de Design Fundamentais
Comentar do SOLID, Component Principles e Princípios de Arquitetura (Dependency Rule, Boundaries)

The SOLID principles tell us how to arrange our functions and data structures into classes, and how those classes should be interconnected. [1] (part. 3, pag.: 58)

The goal of the principles is the creation of mid-level (module level, about the level of the code) software structures that:
• Tolerate change,
• Are easy to understand, and
• Are the basis of components that can be used in many software systems. [1] (part. 3, pag.: 58)

• SRP: The Single Responsibility Principle
An active corollary to Conway’s law: The best structure for a software system is heavily influenced by the social structure of the organization that uses it so that each software module has one, and only one, reason to change.

• OCP: The Open-Closed Principle
Bertrand Meyer made this principle famous in the 1980s. The gist is that for software systems to be easy to change, they must be designed to allow the behavior of those systems to be changed by adding new code, rather than changing existing code.

• LSP: The Liskov Substitution Principle
Barbara Liskov’s famous definition of subtypes, from 1988. In short, this principle says that to build software systems from interchangeable parts, those parts must adhere to a contract that allows those parts to be substituted one for another.

• ISP: The Interface Segregation Principle
This principle advises software designers to avoid depending on things that they don’t use.

• DIP: The Dependency Inversion Principle
The code that implements high-level policy should not depend on the code that implements low-level details. Rather, details should depend on policies

Component Cohesion
Component Coupling deals with the question “how to group classes together?”.

• REP: The Reuse/Release Equivalence Principle
• CCP: The Common Closure Principle
• CRP: The Common Reuse Principle

Component Coupling
Component Coupling deals with the relationships between components [1] (cap. 14, pag.: 111).

• Acyclic dependencies principle: no cycle in the dependency graph. Cycles couple components and, among other things, force them to be released together. Use the dependency inversion principle to break cycles.
•  The stable dependency principle: less stable components should depend on more stable components. Depend in the direction of stability.
• Stable abstractions principle: stable components should be abstract, and vice versa. An example of an abstract stable component is a high-level policy which is changed by extension following the open-closed principle [1] (cap. 17, pag.: 173).


Addressing Architecture’s Concern Aspects

Decoupling Layers

Architecture does not know all necessary use cases that the system must support, but do know the basic intent of the system. 
Some principles can be applied in order to facilitate the inclusion and maintainability of the system such as Single Responsibility Principle and the Common Closure Principle to separate those things that change for different reasons, and to collect those things that change for the same reasons—given the context of the intent of the system [1] (cap. 16, pag.: 151). User interfaces change for reasons that have nothing to do with business rules, then  a good architect will want to separate the UI portions of a use case from the business rule portions in such a way that they can be changed independently of each other. [1] (cap. 16, pag.: 151). 

Another thing that changes for different reasons are the use cases themselves. So, as we are dividing the system into horizontal layers (ex: model, view, control), we also must divide the system into thin vertical use cases that cut through those layers. By using this approach, decouple the elements of the system that change for different reasons, then you can continue to add new use cases without interfering with old ones.

Decoupling also helps the architecture with operational concerns. If the different aspects of the use cases are separated, then those that must run at a high throughput are likely already separated from those that must run at a low throughput [1] (cap. 16, pag.: 152). Then we can take for each one of them different approaches to help with the operational constraints, such as replicate those use cases with high bandwidth throughput in many servers [1] (cap. 16, pag.: 153).

Decoupling use cases contributes with the independent develop-ability, because now we can divide them by feature teams, or component teams, or even layer teams.

Decoupling use cases contributes with the independent deployability, because as we have now modularization, adding a new use case could be a simple as adding a few new jar files or services to the system while leaving the rest alone

The SOLID principles are a general guide to drive application development; however, they are just that – guides, not architectures.
Clean Architecture
How an architecture should be and what it does? 
Clean Architecture, as coined by Robert C. Martin, is an architectural standard for structuring and organising code to adhere to the desirable outcomes that were outlined in the previous sessions.

The main concept that Clean Architecture relies on is the Dependency rule that describes the idea that the source code dependencies can only point inwards, to the center of the architecture.

Other approaches adopted by Clean Architecture are clean separation of concerns, finding the right abstractions on every level of the software projects, the minimal number of internal dependencies and finding the right flow of control [4].

As R. C. Martin points out [2]: ”The outer circles are mechanisms. The inner circles are policies”.

Clean architecture has an “onion-like” layered structure that makes an application have low-coupling. These layers move from an abstract level to general level [4].
Plugin Architecture
Plugin Architecture, The core business rules are kept separate from, and independent of, those components that are either optional or that can be implemented in many different forms [1] (cap. 17, pag.: 170). Main Principles that can be applied here are Dependency Inversion Principle and the Stable Abstractions Principle.  Dependency arrows are arranged to point from lower-level details to higher-level abstractions.

Dependency arrows are arranged to point from lower-level details to higher-level abstractions.

Clean Architecture isn't about using 'use cases', it's about defining hard and soft boundaries in your application. You want to protect stuff that doesn't change as often (entities) from stuff that does change often (UI), or unstable components (Android). By providing clear boundaries between different layers you protect the higher level policies from the lower level policies. One way to do this is to define entity, use case and presentation layers [0] (AUG).

5.1.1 Entities
Entities are the Enterprise business rules within an organization. They encapsulate the most general and high-level rules, and they are notably the least likely to change and can span across multiple applications.

For example, a medical organisation, may have the Entities Doctor and Patient. There could be many separate applications to handle referrals, billing and appointments however the Doctor and Patient Entities stay the same regardless.

5.1.2 Use Cases
Use cases are application specific core business rules. They must not have any dependencies on external agents and are intended to explicitly define what the application does. They orchestrate the flow of data to and from the entities, and direct those entities to use their enterprise wide business rules to achieve the goals of the use case.

Changes in this layer should not interfere with the entities layer (inner layer), and changes in outer layers should not affect the use cases.


5.1.3 Interface Adapters
In this layer there are a set of adapters that convert data from the format most convenient for the use cases and entities, to the format most convenient for some external agency such as the database or the web and vice-versa [1] (cap. 22, pag.: 205).

In this layer, the Adapter design pattern is used as a one-way conversion from the format within the use cases to the format used in the external agents. This layer could entirely contain an MVC GUI including the views, controllers etc. This would also, for example, be the layer whereby SQL queries would be put for a SQL Database.

5.1.4 External Interfaces
These are the interfaces that are external to the application but still necessary. These might be, for instance, the database itself, an accounting package interfaced with through an API etc. [12] 

5.1.5 Other Layers
The above layers are mostly just guide layers and the actual application maybe require more if it is quite
large.

Every layer has one task to cover and each holds the property of being possible to remove and replace by another component that has similar behavior but different internal logic. This kind of isolation embraces layers to be plugin to each other and therefore easy to modify, extend or even replace during future development.[4]
Vantagens e desvantagens
Vantagens
Developing the high-level policy first (agnostic to any low-level details) is to allow the test of which "details", such as databases, works better with the architecture [0] (AUG). 

A good architect maximizes the number of decisions not made. [1] (cap. 15, pag.: 140)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139). [TODO Discutir como o clean architecture faz isso]

Developers will not have to hunt for behaviors, because those behaviors will be first-class elements visible at the top level of the system. Those elements will be classes or functions or modules that have prominent positions within the architecture, and they will have names that clearly describe their function [1] (cap. 21, pag.: 148).


The primary cost of maintenance is in spelunking and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect [1] (cap. 15, pag.: 139). A carefully thought-through architecture vastly mitigates these costs. By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage. [1] (cap. 15, pag.: 139)

Desvantagens
Indirect – there will be a lot more interfaces than one might expect (I don’t see it as necessarily bad, but I’ve seen people pointing this out)
Heavy – in the sense that you might end up with a lot more classes than you currently have in your projects (again, the extra classes are not necessarily bad)

Processos Relacionados à ISO 12207

[TODO: relacionar com aquela questão de atributos não funcionais da ISO] Developing the high-level policy first leaves you the option to try different experiments. If you have a portion of the high-level policy working, and it is agnostic about the database, you could try connecting it to several different databases to check applicability and performance. The same is true with web systems, web frameworks, or even the web itself. [1] (cap. 15, pag.: 140)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139). [TODO Discutir como o clean architecture faz isso]





Referências
[2]  R. C. Martin. (2021, Abril. 11) The Clean Architecture [Online]. Disponível: https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html

[1]  R. C. Martin. The Clean Architecture: A Craftsman's Guide to Software Structure and Design, 1. ed. Boston, MA, Pearson Education, Inc. 2017.

[3] R. C. Martin. Clean Code: A Handbook of Agile Software Craftsmanship,
1. ed. Boston, MA, Pearson Education, Inc. 2008.

[A] SOBRENOME, Nome Abreviado. Título: subtítulo (se houver). Nome do site, ano. Disponível em: (link). Acesso em: (data).

[B] SOBRENOME, nome. Título: subtítulo. Ano de apresentação. Número de folhas ou volumes. (Categoria e área de concentração) – Instituição, Local, ano da defesa.

[C] SOBRENOME, Nome Abreviado. et al. Título: subtítulo (se houver). Edição (se houver). Local de publicação: Editora, data de publicação da obra.

[D] SOBRENOME, Nome Abreviado. Título: subtítulo (se houver). Edição (se houver). Local de publicação: Editora, data de publicação da obra.

https://clevercoder.net/2018/09/08/clean-architecture-summary-review/

[4]https://pivanics.users.cs.helsinki.fi/portfolio/docs/publications/Peter_Ivanics-Clean_Software_Architecture.pdf

[5] https://jeffreypalermo.com/2008/07/the-onion-architecture-part-1/

[6] https://alistair.cockburn.us/hexagonal-architecture/
