# Projeto Integrado

## Usuários
- Funcionários da Secretaria de Saúde
- Médicos do centro de regulação das vagas de UTI
- Médicos e enfermeiros de hospitais públicos e postos de saúde
	- inputa no sistema prontuário de pacientes que chegan aos hospitais públicos e postos de saúde com covid


## Preenchimento do Prontuário
- Dados de identificação do paciente, bem como a existência de diabetes, hipertensão, doenças respiratórias e oximetria, os quais são usados pelo sistema definir a gravidade do caso. 

- Deve-se ainda anotar a data do registro, já que o mesmo paciente pode retornado várias vezes ao serviço, e o status de vacinação contra Covid-29.

## Featurues

### Indicação do local de internação
O sistema deve indicar onde o paciente deve ser internado caso ele precise de internação. 
Para isso, o sistema deve controlar o número de vagas de internação


### Controle do número de vagas de internação por de COVID-19 dos hospitais
O sistema deve controlar o número de vagas de internação de COVID-19 dos hospitais, incluindo as vagas em leitos de enfermaria, leitos de UTI, leitos com respirador e UTI pediátrica.


### Indicar transferencias entre hospitais
Dependendo da gravidade do caso e da disponibilidade, o sistema pode indicar a transferência a hospitais de campanha ou hospitais de referência para o tratamento de COVID-19 (cada tipo de hospital tem um critério específico e que muda com o tempo).


### Registrar casos de pacientes
O sistema deve permitir o registro dos casos de pacientes curados, óbitos e reinfecções.
Isso deve ser atualizado no prontuário.


### Consultar os registros de COVID-19 + geração de relatórios 
Os analistas da Secretaria de Saúde podem consultar os registros de COVID-19 de todos os hospitais do Estado e gerar relatórios de diagnóstico de evolução da COVID-19 no Estado. 

O principal relatório é o que faz o cálculo da fase que a região do Estado se encontra (vermelho, laranja, amarelo, verde e azul). 
