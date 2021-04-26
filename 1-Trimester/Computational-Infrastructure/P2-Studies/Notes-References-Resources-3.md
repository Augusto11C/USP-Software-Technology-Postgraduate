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