![alt_text](images/image1.png "image_tooltip")


**Projeto Integrado - TSW-014/2022- 1**

**Exercício - 3**

**Augusto Calado Bueno**

**Thaís Assunção Silva**

**São Paulo**

**2022**


## 
        Casos de Uso



1. Preenchimento do Prontuário

            Descreve o preenchimento do prontuário durante o atendimento de um paciente com COVID-19 ou com suspeita de COVID-19.


        **Atores:**


            - Técnico de Enfermagem.


            **Pré-condição: **


            - N/A.


            **Fluxo Básico: **

1. O técnico de enfermagem inicializa a função de preenchimento de prontuários do sistema;
2. O técnico de enfermagem informa o número da carteira de saúde ou o CPF do paciente;
3. O sistema exibe os campos de dados pessoais do paciente;
4. O técnico de enfermagem registra os dados pessoais do paciente (nome, idade, sexo, alergias);
5. O sistema registra os dados pessoais;
6. O técnico de enfermagem faz o registro do atendimento inserindo as queixas principais, sintomas e sinais vitais;
7. O sistema registra os dados gerados durante o atendimento; 
8. O técnico de enfermagem finaliza o atendimento;
9. O sistema finaliza a função;
10. Fim do caso de uso.

            **FA1: **Paciente já possui cadastro anterior (FB.3):

1. O sistema informa que já existe cadastro do paciente registrado e segue para o **Use Case 3 - Atualização de prontuário**.

            **Pós-Condição:**


            - Dados do atendimento do paciente são registrados no sistema.



### 


### 
        2. Registro internações e transferências com controle de vagas (vaga mais próxima) 


            Descreve o fluxo da solicitação de internações de pacientes com COVID-19, a sua transferência (caso seja necessário), e o controle de vagas.


        **Atores:**


            - Médico atendente; 


            - Médico chefe de internação do hospital;


            - Equipe da ambulância 


            **Pré-condição: **


            - Ter leitos disponíveis para internação.


            **Fluxo Básico: **



1. Médico atendente faz a realização da solicitação para internação do paciente informado o prontuário médico do atendimento; 
2. O sistema busca um leito e realiza a reserva na unidade de origem da solicitação levando em conta a gravidade do caso e os níveis de gravidade atendidos pelo hospital;
3. O sistema encaminha ordem de internação para o médico chefe de internação da unidade contendo as seguintes informações para preparação do leito:
    1. Informações pessoais do paciente (nome, CPF, data de nascimento e número do SUS);
    2. Doença do paciente;
    3. Condições atuais.
4. O sistema exibe uma mensagem na tela do médico solicitante da internação as informações:
    4. Reserva de Leito Realizada com sucesso;
    5. Local de internação;
    6. Preparativos necessários para transferir o paciente.
5. O médico atendente finaliza a operação de solicitação de internação;
6. O sistema finaliza a operação;
7. Fim do caso de uso. 

            **FA1: **Solicitação de internação é recusada (FB.4):

1. O sistema de controle de internações analisa a solicitação e a **recusa**; 
2. O sistema exibe uma mensagem na tela do médico solicitante da internação a informação da recusa da internação;
3. O médico atendente finaliza a operação de solicitação de internação;
4. O sistema finaliza a operação;
5. Fim do caso de uso. 

            **FA2: **Unidade de saúde de origem da solicitação atende o nível de gravidade do paciente, **mas** **não possui leitos** ou **não tem infraestrutura para realizar internações**.(FB.2):

1. O sistema verifica que** não é possível** realizar a internação na **unidade de saúde de origem da solicitação de internação** e busca por outras unidades com leitos disponíveis levando em conta os seguintes critérios:
    1. Proximidade do paciente com o local de internação;
    2. Níveis de gravidade do paciente para fazer o match de gravidade do caso atendido pelo hospital.
2. O sistema reserva leito na unidade selecionada, encaminha ordem de internação para o médico chefe de internação da unidade e encaminha ordem de transferência para o SAMU. A ordem de transferência possui os seguintes dados:
    3. Local de origem;
    4. Local de destino;
    5. Informações pessoais do paciente (nome, CPF, data de nascimento e número do SUS);
    6. Doença do paciente;
    7. Condições atuais 
    8. Recomendações médicas para o transporte.
3. O sistema exibe uma mensagem na tela do médico solicitante da internação as informações:
    9. Reserva de Leito Realizada com sucesso;
    10. Local de internação;
    11. Preparativos necessários para transferir o paciente.
4. O médico atendente finaliza a operação de solicitação de internação;
5. O sistema finaliza a operação;
6. Fim do caso de uso. 

            


            **FA3: **Nenhuma unidade hospitalar possui leitos (FB.2):

1. O sistema verifica que há indisponibilidade de leitos** em todos os hospitais cadastrados**, coloca o paciente em fila de espera para leitos, salva os dados do atendimento (queixas principais, sintomas, exames solicitados e diagnóstico) e sinaliza ao médico solicitante sobre inclusão do paciente na lista de espera;
2. Fim do caso de uso. 

            **FA4: Unidade de saúde de origem da solicitação** não atende o nível de gravidade do paciente (FB.2):

1. O sistema verifica que a unidade de origem da solicitação não atende o nível de gravidade do paciente que necessita internação e busca por hospitais que podem aceitá-lo levando em conta os seguintes critérios:
    1. Proximidade do paciente com o local de internação;
    2. Níveis de gravidade do paciente para fazer o match de gravidade do caso atendido pelo hospital.
2. O sistema reserva leito na unidade encontrada, encaminha ordem de internação para o médico coordenador de internação da unidade, sinaliza ao médico solicitante da internação sobre a alocação do leito para o paciente e encaminha ordem de transferência para o SAMU. A ordem de transferência possui os seguintes dados:
    3. Local de origem;
    4. Local de destino;
    5. Informações pessoais do paciente (Nome, CPF, data de nascimento e número do SUS);
    6. Doença do paciente;
    7. Condições atuais 
    8. Recomendações médicas para o transporte.
3. O sistema exibe uma mensagem na tela do médico solicitante da internação as informações:
    9. Reserva de Leito Realizada com sucesso;
    10. Local de internação;
    11. Preparativos necessários para transferir o paciente.
4. O médico atendente finaliza a operação de solicitação de internação;
5. O sistema finaliza a operação;
6. Fim do caso de uso. 

            **Pós-Condição: **


            - Dados da solicitação da reserva do leito são registrado no sistema; 


            - Vaga de leito paciente é reservada.


### 
        3. Atualização do prontuário (estado e evolução do paciente)


            Descreve o acesso aos prontuários médicos dos pacientes por profissionais da saúde para a realização de atualizações sobre o estado e evolução do paciente.


        **Atores:**

* Profissional da saúde
    * Médico
    * Enfermeiro

                **Observação: **Ao longo do formulário estes atores serão referenciados por **profissional da saúde. **


            **Pré Condição: **

* Ter um prontuário médico do paciente previamente registrado.

            **Fluxo Básico: **

1. O profissional da saúde inicializa a função de update de prontuários do sistema;
2. O sistema solicita o número de identificação do paciente (CPF ou número do SUS);
3. O profissional da saúde informa a identificação do paciente; 
4. O sistema faz a checagem de permissão para o acesso à informação; 
5. O sistema apresenta o histórico do paciente com as seguintes informações:
    1. Doenças crónicas; 
    2. Principais alergias; 
    3. Atendimentos médicos passados.
6. O profissional da saúde realiza a inclusão de informações sobre o paciente (estado atual e evolução do quadro de saúde do paciente):
    4. Sintomas (desaparecimento sintomas ou surgimento de novos sintomas);
    5. Sinais vitais (temperatura, pressão arterial, batimentos por minutos);
    6. exames solicitados e resultados (caso haja);
    7. diagnóstico (caso já seja possível concluir sobre a condição do paciente).
7. O sistema registra os dados inseridos;
8. O profissional da saúde finaliza a operação de atualização;
9. O sistema finaliza a função;
10. Fim do caso de uso.

            **FA1: **O número de identificação informado do paciente não existe (FB.2):

1. O sistema sinaliza que o paciente não foi encontrado;
2. Retorna para o passo 2 do fluxo básico. 

            **FA2:** Solicita a impressão do histórico médio (FB.5):

1. O profissional da saúde requisita a impressão dos dados médicos do paciente;
2. O sistema envia para a fila de impressão os dados requisitados; 
3. O sistema finaliza a função;
4. Fim do caso de uso.

            **Pós-Condição: **


            - Prontuário atualizado


### 
        4. Gerar Relatórios


            Produção de relatórios sobre a evolução do COVID-19 no estado levando em conta dados como registros de pacientes (casos recuperados, casos em acompanhamento, casos confirmados, óbitos confirmados), balanço de vagas nos hospitais (taxa de ocupação dos leitos), e mapa colorido de fase da doença (média móvel de novos casos, óbitos, internações).


        **Atores:**


            - Secretário de saúde do estado.


            - Analista da secretaria de saúde do estado.


            **Observação:** Ao longo do caso de uso estes atores serão referenciados por funcionário da secretaria do estado.


            **Pré-condição: **


            - N/A


            **Fluxo Básico: **

1. O funcionário da secretaria do estado inicializa a função de geração de relatórios do sistema;
2. O funcionário da secretaria do estado seleciona qual tipo de relatório deseja extrair, como: relatório de registros de pacientes (contando com infectados, re-infectados e óbitos), ou relatório de balanço de vagas nos hospitais, ou relatório do mapa colorido de fase da doença e informa o intervalo de datas do qual deseja que os dados sejam agrupados;
3. O sistema apresenta o relatório em um arquivo disponível para _download_;
4. O funcionário da secretaria do estado efetua o _download _do arquivo;
5. O funcionário da secretaria do estado finaliza a função;
6. O sistema finaliza a função;
7. Fim do caso de uso.

            **FA1: **O relatório não possui dados no intervalo de datas inserido (FB.3)

1. O sistema informa a falta de dados no intervalo inserido;
2. O sistema solicita um novo intervalo de datas;
3. O funcionário da secretaria do estado informa o novo intervalo de datas do qual deseja que os dados sejam agrupados;
4. O fluxo volta para o passo 4 do fluxo básico. 

            **FA2: **O relatório disponível para _download _está corrompido (FB.6)

1. O funcionário da secretaria do estado finaliza a função;
2. O fluxo volta para o passo 1 do fluxo básico.

            **FA3: **O _download _do arquivo falha (FB.7)

1. O funcionário da secretaria do estado efetua o _download _dos arquivos novamente;
2. O fluxo volta para o passo 8 do fluxo básico.

            **FA4: **O funcionário da secretaria do estado deseja obter relatório de registros de pacientes (contando com infectados, re-infectados e óbitos) (FB.2)

1. O funcionário da secretaria do estado seleciona o relatório do tipo registros de pacientes e informa o intervalo de datas do qual deseja que os dados sejam agrupados;
2. O sistema apresenta o relatório em um arquivo disponível para _download_;
3. O funcionário da secretaria do estado efetua o _download _do arquivo;
4. O funcionário da secretaria do estado finaliza a função;
5. O sistema finaliza a função;
6. Fim do caso de uso.

            **FA5: **O funcionário da secretaria do estado deseja obter relatório de balanço de vagas nos hospitais, ou (FB.2)

1. O funcionário da secretaria do estado seleciona o relatório do tipo registros de pacientes e informa o intervalo de datas do qual deseja que os dados sejam agrupados;
2. O sistema apresenta o relatório em um arquivo disponível para download;
3. O funcionário da secretaria do estado efetua o download do arquivo;
4. O funcionário da secretaria do estado finaliza a função;
5. O sistema finaliza a função;
6. Fim do caso de uso.

            **FA6: **O funcionário da secretaria do estado deseja obter relatório do mapa colorido de fase da doença(FB.2)

1. O funcionário da secretaria do estado seleciona o relatório do tipo registros de pacientes e informa o intervalo de datas do qual deseja que os dados sejam agrupados;
2. O sistema apresenta o relatório em um arquivo disponível para download;
3. O funcionário da secretaria do estado efetua o download do arquivo;
4. O funcionário da secretaria do estado finaliza a função;
5. O sistema finaliza a função;
6. Fim do caso de uso.

            **Pós-Condição **


            - O download dos relatórios solicitados é concluído com sucesso.
