# Notes-References-Resources 2

## Hyperthreading
- Hyperthreading is the hardware solution to increasing processor throughputby decreasing resource idle time.
- the hyperthreadedprocessor, in effect, acts like two CPUs in one.
- Allows multiple concurrent threads to be executed. Threads are interleaved so that resources not being used by one thread are used by others.
- fillexecution slots, thereby making more efficient use of available execution resources by keeping the execution core busier. 

### Hyperthreading References
- [](http://meseec.ce.rit.edu/551-projects/spring2016/2-3.pdf)
- [](http://alvarestech.com/temp/smar/www.delt.ufmg.br/seixas/PaginaATR/Download/DownloadFiles/Introduction%20to%20Multithreading.pdf)

## Evolução da Arquitetura Memória-Processador

1. Acesso por interconexões dedicadas
![](./resources/acesso-interconecoes-dedicadas.png)

2. Acesso por interconexões **QuickPath**
![](./resources/acesso-interconexoes-quickpath.png)
![](./resources/acesso-interconexoes-quickpath-arquitetura-processador.png)

## Memórias
### Tipos de Memórias
- Conteúdo Fixo: ROM, PROM
- Conteúdo Quase Fixo: FLASH
- Conteúdo variável: M. estática, M. dinâmica, M. flash
   - Conteúdo Fixo: ROM, PROM
- Conteúdo Quase Fixo: FLASH
- Conteúdo variável: M. estática, M. dinâmica, M. flash

### Conteúdo Fixo
- São memórias cujo conteúdo é fixo e não pode ser alterado.

#### ROM
- ROM é uma memória cujo conteúdo é fixo e não pode ser alterado.
- Há vários tipos de ROMs: todos são não-voláteis, i.e. não requerem energia para manter o seu conteúdo.
- Um importante uso de ROM é em processador CISC para armazenar o microprograma.
- ROM pode ser fabricado com portas NOR ou NAND, com um layout denso.
- Como ROM não pode ser alterada, erro de um bit pode acarretar em discartar um lote inteiro.

### Conteúdo Variável
#### Memória RAM
- Pode ser de dois tipos: DRAM e SRAM, ambos voláteis (o conteúdo se perde quando o computador é desligado e depois religado).
- A unidade básica de armazenamento é uma célula contendo um bit

##### DRAM (Dynamic RAM)
- usada na memória principal.
- O capacitor armazena ou não carga elétrica, representando 1 e 0, resp.
- Quando carregado, o capacitor pode perder carga por vazamento.
- Para manter um capacitor que representa 1 sempre carregado, um pulso de
- refrescamento é aplicado periodicamente. Daí o nome dinâmico.

```
DRAM stores the binary information in the form of electric charges that applied to capacitors. The stored information on the capacitors tend to lose over a period of time and thus the capacitors must be periodically recharged to retain their usage. The main memory is generally made up of DRAM chips.

it is cheaper than SDRAM, because requirer 1 capacitor and one transistor while sram requirers several transistors

reduced power consumption due to the fact that the information is stored in the capacitor.
```

- Leitura destrutiva
  - Assim, o conteúdo deve ser restaurado após cada leitura, levando à existência de dois tempos:
    - tempo de acesso - o necessário para obter o valor desejado
    - tempo de ciclo - o total para leitura e restauração, até que uma nova operação possa ser iniciado.

- A  memoria é organizada como uma matriz bidimensional (linhas vs colunas)
- a leitura afeta toda uma linha
- a coluna é selecionada após a leitura da linha

##### SRAM (Static RAM)
- A memória estática mantém o dado inalterado, **desde que haja energia**. É usada na memória cache, sendo menos densa, mais rápida e mais custosa do que DRAM.
- SRAM 6 transistores por bit vs DRAM1 transsitor por bit.
- Retém o valor indefinidamente, até o equipamento ser desligado.
- Capacidade  << DRAM
- Custo >> DRAM
- Tempo de acesso << que as DRAMs
- 

##### DRAM vs SRAM
- Ambas são voláteis.
- A célula DRAM é mais simples e ocupa menos espaço que uma célula SRAM.
- Portanto DRAM é mais densa (mais células por unidade de área) e mais barata.
- Por outro lado, DRAM requer uma circuitaria de refrescamento. Para memórias grandes, esse custo fixo é mais que compensado pelo menor custo.
- Daí DRAM é preferida para memórias grandes e SRAM (que é um pouco mais rápida) é mais usada em memória cache.

   