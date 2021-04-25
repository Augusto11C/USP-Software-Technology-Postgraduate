# Clean Architecture - Projecto Engenharia de Software


## Visão Geral
TODO Escrever uma motivação, contextualização do problema.

Every software system provides two different values to the stakeholders: behavior and architecture.[1] (cap.2, pag.: 13). The second of these is the greater of the two because it is this value that makes software “soft” (in other words, change behavior easily). The first value of software is its behavior that refers to what the software does, what it delivers for the users, and what generates value. Programmers write the code to satisfy stakeholder’s requirements. [1]

Linearly with the growth of the code base of a software project, its complexity and cost of change increases [1] (estudo de caso, pag.: 5)

To build a system with a design and an architecture that minimize effort and maximize productivity, you need to know which attributes of system architecture lead to that end. [1] (cap. 1, pag.: 12)

The difficulty in making such a change should be proportional only to the scope of the change, and not to the shape of the change.

If architecture comes last, then the system will become ever more costly to develop, and eventually change will become practically impossible for part or all of the system. [1] (cap.2, pag.: 18)

The primary cost of maintenance is in spelunking and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect.  [1] (cap. 15, pag.: 139)

The goal of software architecture is to minimize the human resources required
to build and maintain the required system.  [1] (cap.1, pag.: 5)

## O que é Arquitetura?
Usually “architecture” means structure at a high-level, and “design” means structure at a low-level. But Low-level details (design) and the high-level structure (architecture) are all part of the software design.

The architecture of a software system is the shape given to that system by those who build it. The form of that shape is in the division of that system into components, the arrangement of those components, and the ways in which those components communicate with each other. (cap. 15, pag.: 137)

The architecture of a system has very little bearing on whether that system works. [1] (cap. 15, pag.: 137)

The primary purpose of architecture is to support the life cycle of the system. [1] (cap. 15, pag.: 137)

The ultimate goal is to minimize the lifetime cost of the system and to maximize programmer productivity. [1] (cap. 15, pag.: 137)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139)

A carefully thought-through architecture vastly mitigates these costs. By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage. [1] (cap. 15, pag.: 139)

The way you keep software soft is to leave as many options open as possible,
for as long as possible. What are the options that we need to leave open? They
are the details that don’t matter [1] (cap. 15, pag.: 140).

All software systems can be decomposed into two major elements: policy and details. The policy element embodies all the business rules and procedures. The policy is where the true value of the system lives.

The details are those things that are necessary to enable humans, other systems, and programmers to communicate with the policy, but that do not impact the behavior of the policy at all (e.g. IO devices and databases) [1] (cap. 15, pag.: 140).

The goal of the architect is to create a shape for the system that recognizes policy as the most essential element of the system while making the details irrelevant to that policy. This allows decisions about those details to be delayed and deferred [1] (cap. 15, pag.: 140).

One of the benefits of developing the high-level policy without committing to the details that surround it, is that when the time for the decision arrives it can be made in a better way (taking in account all of the high-level policies that already were developed [1] (AUG) (cap. 15, pag.: 140).

## Princípios de Design Fundamentais
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

### Component Cohesion
Component Coupling deals with the question “how to group classes together?”.

• REP: The Reuse/Release Equivalence Principle
• CCP: The Common Closure Principle
• CRP: The Common Reuse Principle

### Component Coupling
Component Coupling deals with the relationships between components [1] (cap. 14, pag.: 111).

• Acyclic dependencies principle: no cycle in the dependency graph. Cycles couple components and, among other things, force them to be released together. Use the dependency inversion principle to break cycles.
•  The stable dependency principle: less stable components should depend on more stable components. Depend in the direction of stability.
• Stable abstractions principle: stable components should be abstract, and vice versa. An example of an abstract stable component is a high-level policy which is changed by extension following the open-closed principle [1] (cap. 17, pag.: 173).

## Clean Architecture
Plugin Architecture, The core business rules are kept separate from, and independent of, those components that are either optional or that can be implemented in many different forms [1] (cap. 17, pag.: 170).

Dependency arrows are arranged to point from lower-level details to higher-level abstractions.


Clean Architecture isn't about using 'use cases', it's about defining hard and soft boundaries in your application. You want to protect stuff that doesn't change as often (entities) from stuff that does change often (UI), or unstable components (Android). By providing clear boundaries between different layers you protect the higher level policies from the lower level policies. One way to do this is to define entity, use case and presentation layers [0] (AUG).

##Vantagens e desvantagens

### Vantagens
Developing the high-level policy first (agnostic to any low-level details) is to allow the test of which "details", such as databases, works better with the architecture [0] (AUG). 

A good architect maximizes the number of decisions not made. [1] (cap. 15, pag.: 140)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139). [TODO Discutir como o clean architecture faz isso]

The primary cost of maintenance is in spelunking and risk. Spelunking is the cost of digging through the existing software, trying to determine the best place and the best strategy to add a new feature or to repair a defect [1] (cap. 15, pag.: 139). A carefully thought-through architecture vastly mitigates these costs. By separating the system into components, and isolating those components through stable interfaces, it is possible to illuminate the pathways for future features and greatly reduce the risk of inadvertent breakage. [1] (cap. 15, pag.: 139)


### Desvantagens
Indirect – there will be a lot more interfaces than one might expect (I don’t see it as necessarily bad, but I’ve seen people pointing this out)
Heavy – in the sense that you might end up with a lot more classes than you currently have in your projects (again, the extra classes are not necessarily bad)

## Processos Relacionados à ISO 12207

[TODO: relacionar com aquela questão de atributos não funcionais da ISO] Developing the high-level policy first leaves you the option to try different experiments. If you have a portion of the high-level policy working, and it is agnostic about the database, you could try connecting it to several different databases to check applicability and performance. The same is true with web systems, web frameworks, or even the web itself. [1] (cap. 15, pag.: 140)

[Operational] A good software architecture communicates the operational needs of the system. Architecture should reveal operation. The architecture of the system should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for the developers. This simplifies the understanding of the system and, therefore, greatly aids in development and maintenance. [1] (cap. 15, pag.: 139). [TODO Discutir como o clean architecture faz isso]





Referências
[1]  R. C. Martin. (2021, Abril. 11) The Clean Architecture [Online]. Disponível: https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html

[2]  R. C. Martin. The Clean Architecture: A Craftsman's Guide to Software Structure and Design, 1. ed. Boston, MA, Pearson Education, Inc. 2017.

[3] R. C. Martin. Clean Code: A Handbook of Agile Software Craftsmanship,
1. ed. Boston, MA, Pearson Education, Inc. 2008.

[A] SOBRENOME, Nome Abreviado. Título: subtítulo (se houver). Nome do site, ano. Disponível em: (link). Acesso em: (data).

[B] SOBRENOME, nome. Título: subtítulo. Ano de apresentação. Número de folhas ou volumes. (Categoria e área de concentração) – Instituição, Local, ano da defesa.

[C] SOBRENOME, Nome Abreviado. et al. Título: subtítulo (se houver). Edição (se houver). Local de publicação: Editora, data de publicação da obra.

[D] SOBRENOME, Nome Abreviado. Título: subtítulo (se houver). Edição (se houver). Local de publicação: Editora, data de publicação da obra.

https://clevercoder.net/2018/09/08/clean-architecture-summary-review/
