# Notes-References-Resources - 

Arquitetura de um computador é o conjunto de atributos de um sistema de computação, como é visto pelo programador, isto é, a estrutura conceitual e o comportamento funcional, sem considerar a organização dos fluxos de dados e de controle, nem a implementação física.

## Fabricação CPU
- Lingote de silício monocristalino ultra puro é cortado em fatias, e estas polidas.
- Aplica-se uma camada de material fotossensível, e a seguir a placa é exposta à luz ultravioleta.
- A parte não atingida pela luz é removida com um solvente.
- A parte exposta é corrida por um processo químico, e o restante do material fotossensível é removido.
- O processo é repetido até que todas as operações sobre o silício estejam
completas.
- Aplica-se uma fina camada de cobre. Repete-se as técnicas anteriores para remover as partes desnecessárias.
- O processo é repetido para produzir todas as interconexões necessárias. Os chips são testados ainda no wafer
- Os componentes são cortados e em seguida emcapsulados.

## Velocidade e Dissipação
Quanto mais rápido um circuito opera, maior é a quantidade de energia que consome (e portanto precisa dissipar, sob forma de calor).

## Lei de Amdahl
Aumento de velocidade devido ao melhoramento E:

```
aumt vel (e) = (temp exec sem e) / (temp exec com e)
```

- Se E for pequeno, não há uma diferença significativa no resultado
- O importante é melhorar as parte do processo que consomem um percentual significativo do tempo total


## Mainframes
Mainframes razões para utilização:
- Cultura instituição
- Software Legado
- Segurança

## Servidores
- "Baixa diversidade" fatores relevantes:
  - Compatibilidade com aplicações existentes
  - Tipo de suporte existente
  - Coerência com projeto de evolução

- Múltiplos tipos de servidores implicam em problemas
  - suporte
  - compatibilidade
  - diálogo

### Servidores Desktops vs Servidores x86

- Servidores x86 e desktops não apresentam diferenças em arquitetura e implementação

- A diferença reside na execução:
  - Desktops - menor custo
  - Servidores - maior confiabilidadeservidores desktops vs servidores x86

### Servidores em Blades
- Designa uma execução compacta de servidores.

- Cada blade contém um servidor completo, com:
  - Processador
  - Memória
  - Disco para SO
  - Outras interfaces, pelo menos Ethernet

### Servidores "Open Compute Project"
Projeto de arquitetura aberta, desenvolvido por Facebook, e posteriormente outras grandes empresas, como Microsoft e Intel Objetivos eficiência energética e economia.

## Processadores
### Modelos Conceituais de Processadores
- Harvard: Programas e dados residem em memórias diferentes e específicas.
- von Neumann: programas e dados compartilham a mesma memória.
- PS: Os processadores modernos apresentam aspectos das duas arquiteturas.

### Fluxo de Dados e de Controle
Fluxo de Dados e de Controle

- O fluxo de dados (datapath) representa os caminhosque os dados podem percorrer em um sistema digital.

- O fluxo de controle representa os sinais de controlenecessários para que o fluxo de dados funcione como desejado.

### Componentes Básicos de um Computador
- unidade de processamento: realiza operações
- memória: armazena dados e instruções
- controle: controla a operação de todas as unidades (geralmente não é representado)

