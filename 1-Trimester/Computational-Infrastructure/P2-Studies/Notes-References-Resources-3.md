# Notes-References-Resources 3
## Memória Principal
- A Memória Principal é constituída por DRAMs
- Desempenho da Memória Principal:
- Latência: é a penalidade por falha
  - Tempo de acesso: tempo entre uma requisição e o fornecimento de uma palavra de memória
- Tempo de ciclo: tempo entre requisições 

### Categorias de memórias
- ECC (Error correction code)
  - bits adicionais para corrigir um erro simples e detectar um erro duplo.
  - Normalmente taxa de erro é muito baixa, por isso em computadores convêncionais não se aplica essa técnica.
  - erro simples: um bit da palavra foi alterado.
  - erro duplo: dois bits da palavra foram alterados.
- DIMM (dual in-line memory module) 
- RDIMM (registered dual in-line memory module) 
- UDIMN (unregistered dual in-line memory module) 

### DRAMs
#### Synchronous DRAM
- Leitura e load do proximo dado simultaneos. Transfere os dados de forma síncrona com o clock do barramento.

#### DDR DRAMs
- Dados transferidos quando o clock sobe e quando o clock desce.Antigamente é era apenas em um dos cenários (SDRAM).
- Isso permitio dobrar a taxa de transferencia.

## Memória Virtual
- antigamente memória era cara.

- para contornar o problema, criou-se a memória virtual para "enganar" o pc sobre a abundância de memória.
- precisa ter uma quantidade de memória suficiente para essa tecnica funcionar.
- a m.v. utiliza a m.f. como uma espécie de "cache".
- A memória virtual armazena o programa em disco e apenas pedaços (páginas no caso de paginação ou segmentos no caso de segmentação) são trazidos para a memória quando necessários.
- usado para resolver o problema de multiplos processos acontecendo concorrentemente/paralelamente.
  - cada um deles precisa de memória, e ele só pode acessar sua própria memória, não podendo acessar a memória de outros processos.
  - A memória virtual permite que cada processo tenha seu própio espaço de endereçamento pré-definido.
- orienta e disciplina a execução de vários processos no mesmo processador.

### 3 Perguntas Para Memória Virtual
```
1. Onde um bloco pode ser colocado no nível superior?
R: Qualquer lugar, é feito por software 

2. Como um bloco pode ser encontrado no nível superior?
R: Realizado por meio da tabela de páginas do desenho anterior

3. O que acontece numa escrita?
R: Escreve primeiro na memória e só quando o espaço da memória for necessário, dai escreve-se em disco
```

### Cache e Memória Virtual
- cada referência à memória virtual pode acarretar em dois acessos à memória física: um para acessar entrada desejada da Tabela de Páginas, e outro para a página desejada.
  - solução: mais de um tipo de cache - translation lookaside buffer (TLB)
  

####  Translation Lookaside Buffer TLB
- O Translation Lookaside Buffer TLB é uma memória cache que contém as entradas (i.e. as linhas) da Tabela de Páginas mais recentemente usadas
- Para localizar uma dada página, TLB é consultado. Se encontrar (TLB hit), o número do bloco correspondente é obtido. Pelo princípio de localidade, há grande probabilidade de isso ocorrer
- https://www.ime.usp.br/~song/mac344/slides07-virtual-memory.pdf (20/44)

## Sistemas de E/S
TODO get image from slide 105/120
- Processador com acesso direto a memória para não atrasar o funcionamento do processador
- North Bridge: Liga o processador aos dispositivos mais rápidos que estejam conectados
- South Bridge: Liga o processador aos dispositivos mais lentos que os dispositivos da North Bridge (ex: interface de rede, usb, etc)
- O desempenho dos subsistemas de E/S eletromecânicos é limitado por restrições mecânicas

### Barramentos
- Barramento é uma ligação compartilhada entre subsistemas
- Baixo custo: um mesmo conjunto de fios é compartilhado por todos
- Pode ser um gargalo, podendo limitar o desempenho de E/S
- A velocidade de um barramento é limitada por fatores físicos (comprimento do barramento, num máx de dispositivos)

#### Tipos de Barramento
- Dois tipos de barramentos
- Barramento de E/S: normalmente podem ser longos, muitos tipos de dispositivos podem ser ligados, grande variação na capacidade de transferência de dados
- Barramento de CPU-Memória-Controladores: alta velocidade, para maximizar a transferência de dados entre CPU, memória e controladores, ou entre CPUs
- **Transação em um barramento**:  é o processo de transmitir endereços e receber ou transmitir dados.

### Barramento SCSI
- SCSI - Barramento de Entrada e Saída.
- Todos os dispositivos podem se comunicar diretamente entre si.
- Dispositivos podem ser mestres (Iniciadores) ou escravos (alvos).
- https://www.ic.unicamp.br/~ducatte/mo401/1s2008/T2/079734-t2.pdf

#### Protocolo SCSI Fases
- Bus Free: no access barramento
- Arbitration: competição para acesso barramt
- Selection: avisa disp de dest q ele participa prx op
- Command: iniciador commandos p disp dest
- Data Transfer: transf de dados
- Message pash: Transferencia msg controll (desconexao, command complet,...)

### iSCSI - Internet SCSI
- Proposta de um padrão estendendo os comandos SCSI para operação em uma rede TCP/IP.
- Torna-se prático somente com velocidades de 1 - 10 Gb/s.
- Escalabilidade e possibilidade de operação em longas distâncias
- Tecnologia conhecida e equipamentos disponíveis.

### SATA
- ** Substituição da interface **paralela** por interface **serial**
- Reduz dimensão dos cabos
- Permite velocidades mais altas



