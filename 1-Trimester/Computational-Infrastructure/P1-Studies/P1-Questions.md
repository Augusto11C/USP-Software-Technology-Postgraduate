**1. (1) Apresente algumas características essenciais do conceito de nuvem.**

A computação em nuvem é um modelo de terceirização, no qual os serviços de TI são fornecidos e pagos com base no uso sob demanda dos recursos.
Entre as características essenciais do conceito de nuvem estão:
1. Escalabilidade e elasticidade: é possível alocar mais ou menos recursos em momentos de necessidade/demanda com agilidade.
2. Autoatendimento sob demanda: Como resultado da automação e orquestração dos recursos disponíveis na nuvem, é necessário um esforço mínimo de gerenciamento de sistemas para implantar sistemas ou aplicativos em um ambiente de nuvem.
3. pool de recursos: Em vez de fornecer a cada aplicativo uma quantidade fixa de poder de processamento e armazenamento, a computação em nuvem fornece aplicativos com recursos de um pool fragmentado (feito usando tecnologias de virtualização).
4. serviços mensuráveis: Em um ambiente de nuvem, o uso real de recursos é medido e cobrado. não há despesas de capital, apenas despesas operacionais. Este é o contraste com o investimento necessário para construir uma infraestrutura tradicional.

**2. (1) Qual a relação entre nuvem e virtualização?**
Pode-se dizer que a principal relação entre nuvem e virtualização é que a nuvem utiliza a tecnologia de virtualização, não se limitando apenas a esta tecnologia, para prover serviços e recursos.
Virtualização fornece provisionamento de recursos lógicos e, ao contrário das técnicas de provisionamento de recursos físicos, proporciona recursos/funções poderosas que auxiliam no objetivo da computação em nuvem de criar um conjunto dinâmico de recursos a serem utilizados por vários usuários.

**3. (1) Quais as principais vantagens da virtualização de servidores?**
Entre as vantagens da virtualização de computadores está o desacoplamento e isolamento das máquinas virtuais da máquina física e de outras máquinas virtuais por meio de uma camada de virtualização.
A máquina virtual é uma representação lógica de um computador físico em software. Tendo isto em vista, novas máquinas virtuais podem ser provisionadas conforme necessário, sem a necessidade de compra de hardware.
Com a utilização de máquinas virtuais, é possível economizar custos em hardware, energia e resfriamento, pois como menos máquinas físicas são necessárias, os custos de manutenção podem ser reduzidos e o risco de falha de hardware também é reduzido.

**4,5. Considere um sistema com dois componentes que apresentam disponibilidade individual de 99%. Qual é a disponibilidade do sistema, se os dispositivos operarem**
**(1) em série**
Para calcular a disponibilidade de um sistema ou dispositivo onde seus componentes estão em série, multiplique a disponibilidade de todas as suas peças.
0,99 x 0,99 = 0,9801

**(1) em paralelo**
Para calcular a disponibilidade de um sistema ou dispositivo onde seus componentes estão em paralelo, utiliza-se a fórmula abaixo:
A = 1 - ( 1 – A1)^n
A = Disponibilidade
n = número de sistema em paralelo
A1 = disponibilidade de um único sistema
1 – (1-0,99)^2 = 0,9999

**6. (1) Qual é a vantagem da comunicação por pacotes para aplicações de comunicação de dados?**
A grande vantagem da comunicação por pacotes é a sua tolerância a falhas. Fazendo um comparativo com comunicação por comutação de circuitos, se um switch ficar indisponível, todos os circuitos que o utilizam são afetados e nenhum tráfego pode ser enviado em qualquer um deles. Com a comutação de pacotes, os pacotes podem ser roteados em torno desses switches indisponíveis .

**7. (1) Quais as principais vantagens dos cabos de fibra óptica em relação aos cabos elétricos?**
A primeira vantagem que podemos citar sobre os cabos de fibra é a largura de banda muito superior à largura de banda da dos cabos elétricos, podendo-se, dessa forma, realizar a transmissão de um volume maior de dados.
A segunda vantagem relaciona-se com a atenuação do sinal. No caso das fibras, a atenuação de um sinal que se propaga nesse meio é menor quando comparado com cabos elétricos, exigindo menos repetidores ao longo do caminho para restaurar o sinal. Isso permite gerar economia com um número menor de equipamentos necessários.
A terceira vantagem que podemos citar é o custo da fibra em relação aos cabos elétricos que utilizam cobre, um material relativamente caro, em sua confecção. A fibra é mais barata, portanto sua utilização na construção de redes de sistemas é mais vantajosa quando pensamos em custo.

**8. (1) O que caracteriza os sistemas VSAT em relação aos outros sistemas de comunicação via satélite?**
O sistema de satélites VSAT é caracterizado por conjunto de antenas pequenas, uma antena mestra com uma área consideravelmente maior e um satélite de comunicação. Normalmente, a antena mestra se comunica com o satélite, este último, por sua vez, encaminha os sinais para as antenas VSAT.
O sistema de satélites VSAT o ganho de conjunto das antenas é a soma das áreas das antenas.
Como os canais são compartilhados, caso uma estação fique transmitindo sinal ininterruptamente durante várias horas, pode ser que ela deixe as demais inoperantes.
As antenas VSAT são mais baratas e pequenas e consomem menos energia

9. (1) O que significa um endereço formado totalmente por bits 1 em um pacote ethernet?
O endereço formado totalmente por bits 1 no pacote ethernet significa que a informação deve ser transmitida via Broadcast.

**10. (1) Descreva o funcionamento de uma ponte transparente após sua ligação.**
Após a inicialização de uma ponte transparente em uma rede ethernet, a estrutura da topologia da rede é aprendida por meio do tráfego dos pacotes na rede. À medida que chegam e saem, a ponte toma conhecimento dos diversos componentes conectados na rede.
Esse conhecimento, por sua vez, é temporário, e após um período de tempo ele é esquecido pela ponte. Isto acontece para que, caso tenha ocorrido alguma alteração na topologia da rede, as pontes tenham a capacidade de “reaprender” a nova estrutura.


