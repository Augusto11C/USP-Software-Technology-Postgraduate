



**Projeto Integrado - TSW-014/2022- 1**

**Exercício - 1**

**Augusto Calado Bueno**

**Thaís Assunção Silva**

**São Paulo**

**2022**


### Features do Projeto Integrado



* Cadastro dos funcionários envolvidos;
* Prontuário médico digital específico para COVID-19;
    * Trata-se de uma feature que engloba consulta, preenchimento e atualização. Feature que trabalha com o domínio Prontuário médico.
* Consulta do histórico médico do paciente;
    * O texto de definição do sistema CovidNet exige que mantenhamos o controle dos retornos do paciente nos hospitais cadastrados, os resultados de melhora, piora, reinfecção etc. Portanto, o histórico médico é indispensável para manter essa rastreabilidade, controle e gerenciamento.
* Definição de critérios de gravidade por tipo de hospital;
    * Os analistas da secretaria de saúde devem poder definir os critérios para dizer qual o tipo de gravidade de condição de um paciente é atendida por um hospital ou instituição de saúde.
* Indicação automática do local de internação (envolvendo transferências);
* Acompanhamento das vagas de hospitais, considerando os tipos de vagas;
* Transferência;
    * Conexão com sistema externo de solicitação de ambulância
    * A feature de transferência leva em conta o resultado da feature de reserva (booking) de leitos e o resultado da gravidade atribuída ao paciente pelo médico atendente.
* Geração de relatórios para acompanhamento da evolução da COVID-19 no Estado;
* Cálculo da fase que a região do Estado se encontra;
    * O cálculo da fase da região está dentro do relatório, portanto a feature que publica o relatório usa como insumo o resultado da feature que realiza o cálculo da fase da região.


### Histórias


#### 1 - Cadastro de usuário


    **1. História**



* Como um(a) operador(a) da central de combate ao COVID;
* Eu quero **cadastrar** funcionários da área da saúde;
* Para que esses funcionários possam atuar no combate à pandemia;
* Critérios de aceite:
    * Verificar se cadastro do funcionário existe antes de realizar operações no sistema;
    * Verificar emissão de mensagem de sucesso ao finalizar cadastro de funcionário;
    * Verificar submissão de formulário de cadastro incompleto (com dados faltando);

    **2. História**

* Como um(a) operador(a) da central de combate ao COVID;
* Eu quero visualizar os funcionários cadastrados da área da saúde, agrupados pelo local de atuação a qual foram atribuídos (UBS, AMA, Hospital público, Hospital do Servidor, Hospital de campanha);
* Para verificar quais locais de atuação estão carecendo de profissionais;
* Critérios de aceite:
    * Verificar listagem sem funcionários cadastrados;
    * Verificar listagem com todos funcionários atribuídos para apenas um local de atuação;
    * Verificar listagem com pelo menos um funcionário atribuído para cada local de atuação (UBS, AMA, Hospital público, Hospital do Servidor, Hospital de campanha);


#### 2 - Prontuário médico digital específico para COVID-19


    **3. História**



* Como enfermeiro de triagem;
* Eu quero preencher o prontuário médico digital do paciente durante o meu atendimento (anamnese inicial);
* Para registrar e exibir informações do quadro de saúde do paciente, como existência de diabetes, hipertensão, doenças respiratórias;
* Critérios de aceite:
    * Verificar registro das informações referentes ao quadro de saúde do paciente que está usando pela primeira vez o sistema de saúde público;
    * Verificar registro das informações referentes ao quadro de saúde do paciente com pelo menos uma visita aos hospitais cadastrados no sistema;
    * Verificar no término do preenchimento a visualização dos dados preenchidos durante o atendimento;

    **4. História**

* Como um funcionário de atendimento beira-leito;
* Eu quero visualizar um prontuário específico ao COVID-19;
* Para que eu possa acompanhar a evolução do quadro de saúde dos pacientes (ex: visualização e atualização de sinais vitais do paciente);
* Critérios de aceite:
    * Verificar prontuário para paciente variando as seguintes características: entubado, UTI, estável, instável;
    * Verificar indicação de sinais vitais do paciente;

    **5. História** 

* Como médico;
* Eu quero atualizar um prontuário específico ao COVID-19;
* Para que eu possa registrar um novo caso no quadro de saúde dos pacientes (ex: curas, óbitos e reinfecções);
* Critérios de aceite:
    * Verificar registro das informações referentes ao quadro de saúde do paciente com pelo menos uma visita aos hospitais cadastrados no sistema;
    * Verificar no término do preenchimento a visualização do quadro atualizado;


#### 3 - Consulta do histórico médico do paciente


    **6. História **



* Como médico;
* Eu quero um histórico médico do paciente;
* Para que eu possa consultá-lo e assim fazer um atendimento mais assertivo;
* Critérios de aceite:
    * Verificar histórico de pacientes conforme seu estado (entubado, UTI, estável, instável ou óbito);
    * Verificar condições do paciente no momento do último atendimento;

    **7. Histórico**

* Como enfermeiro de triagem;
* Eu quero acesso ao histórico médico dos pacientes que atendo;
* Para confirmar as informações reportadas pelo paciente durante a anamnese e também para entender melhor a evolução da sua saúde;
* Critérios de aceite:
    * Verificar paciente que veio a óbito;
    * Verificar paciente que já teve COVID-19;
    * Verificar paciente recém-nascido;


#### 4 - Definição de critérios de gravidade por tipo de hospital


    **8. História**



* Como um analista do centro de controle do COVID-19;
* Eu quero visualizar cada hospital baseado em tipos (hospital de campanha, hospital geral, hospital/dia-isolado, etc);
* Para que eu possa definir qual o tipo de gravidade de casos de COVID-19 a instituição deve ser atribuído a partir desses dados;
* Critérios de aceite:
    * Verificar por tipo “hospital de campanha”;
    * Verificar por tipo “hospital de geral”;
    * Verificar por tipo “hospital/dia-isolado”;
    * Verificar acesso dos funcionários que são analistas;
    * Verificar acesso dos funcionários que não são analistas;


#### 5 - Indicação automática do local de internação (envolvendo transferências) 


    **9. História**



* Como médico atendente de um pronto socorro público
* Eu quero ser capaz de solicitar um local de internação
* Para que eu possa encontrar uma instituição hospitalar de forma rápida que consiga prover o atendimento demandado pela condição do paciente 
* Critérios de aceite:
    * Verificar duplicidade de vaga ao solicitar simultaneamente;
    * O tempo de resposta da indicação deve ser instantâneo;

    **10. História**

* Como médico atendente da equipe de transporte de pacientes;
* Eu quero receber as informações do quadro de saúde do paciente (ex.: sintomas);
* Para que eu possa deixar sua condição de saúde estável (sem piorar)durante o trajeto da ambulância até seu local de internação;
* Critérios de aceite:
    * Verificar paciente sem cadastro no sistema;
    * Verificar paciente com resultado positivo para covid-19;


#### 6 - Acompanhamento das vagas de hospitais, considerando os tipos de vagas


    **11. História**



* Como médico coordenador de internação da central de Regulação de Ofertas e Serviços de Saúde que cuida do gerenciamento dos leitos disponíveis;
* Eu quero conseguir realizar o acompanhamento/monitoração dos leitos por tipo (Leitos de UTI, Leitos de unidade de terapia semi-intensivo, Leito indiferenciado, Leito infantil, etc) e status (leito disponível, ocupados e em criação);
* Para que eu possa gerenciar os recursos demandados pela instituição onde trabalho para manter os leitos operando de forma satisfatória;
* Critérios de aceite:
    * Verificar quando um leito é recém liberado;
    * Verificar quando um leito é alocado/reservado;

    **12. História **

* Como uma enfermeira responsável por limpeza e alocação de leitos para (de) pacientes;
* Eu quero ser informada das novas internações que reservaram leitos na instituição onde trabalho;
* Para que eu possa agir de forma rápida na preparação do paciente para o paciente;
* Critérios de aceite:
    * Verificar quando um leito é recém liberado;
    * Verificar quando um leito é alocado/reservado;

    **13. História **

* Como médico coordenador de internação da central de Regulação de Ofertas e Serviços de Saúde que cuida do gerenciamento dos leitos disponíveis;
* Eu quero conseguir visualizar e monitorar a capacidade de vagas de cada hospital;
* Para que eu possa medir e analisar as ocorrências de leitos disponíveis em caso de superlotação;
* Critérios de aceite:
    * Verificar quando não possui leitos disponíveis em nenhum hospital;
    * Verificar quando não possui leitos disponíveis em um hospital específico;
    * Verificar quando há a liberação de leitos em um hospital lotado;
    * Verificar quando há a liberação de leitos em um hospital não lotado;


#### 8 - Transferência


    **14. História **



* Como secretário de saúde do estado de São Paulo;
* Eu quero obter indicações de hospitais disponíveis para receber transferências (ex: hospitais de campanha e hospitais de referência);
* Para que eu possa melhor alocar pacientes de acordo com a gravidade do caso;
* Critérios de aceite:
    * Verificar disponibilidade de leitos no hospital indicado;
    * Verificar gravidade requerida pelo hospital indicado;
    * Verificar a gravidade do caso do paciente.

    **15. História**

* Como secretário de saúde do estado de São Paulo;
* Eu quero visualizar o critério atual dos hospitais disponíveis para receber transferências (ex: hospitais de campanha e hospitais de referência);
* Para que eu possa acompanhar as mudanças que ocorrem de tempos em tempos;
* Critérios de aceite:
    * Verificar os hospitais disponíveis;
    * Verificar alteração de critério dos hospitais disponíveis.


#### 9 - Geração de relatórios para acompanhamento da evolução da COVID-19


    **16. História **



* Como um analista de contágio;
* Eu quero um meio para acompanhar a evolução da COVID-19 (número de novos casos, número de reinfecções, número de vacinados (primeira e segunda dose), número de variantes descobertas, etc) no Estado; 
* Para que eu possa acompanhar/estudar a progressão da pandemia e gerar relatórios informativos sobre o contágio com base nesses dados;
* Critérios de aceite:
    * Verificar quando há o registro de casos de infecção com nova variante;
    * Verificar quando há registro de casos de reinfecção;
    * Verificar quando há registro de casos de infecção/reinfecção para pessoas vacinadas;

    **17. História ** 

* Como secretário de saúde do estado de São Paulo;
* Eu quero poder obter relatórios detalhado levando em conta os dados obtidos no cálculo da fase de cada região;
* Para que eu possa melhor informar a população do estado ao aplicar medidas restritivas;
* Critérios de aceite:
    * Verificar produção do relatório quando o cálculo resultante da fase de restrição da região é vermelho, amarelo e verde;


#### 10 - Cálculo da fase que a região do Estado se encontra


    **18. História  **



* Como secretário de saúde do estado de São Paulo;
* Eu quero o resultado do cálculo da fase de restrição das cidades (roxa, vermelha, amarela, verde), levando em conta os dados referentes à população (faixa etária, sexo, ocupação profissional, se tem ou não doenças crônicas etc), vacinação, taxa de ocupação dos leitos, número de infectados, número de óbitos, recursos hospitalares disponíveis (epi);
* Para que eu possa tomar decisões quanto a aplicação de medidas restritivas;
* Critérios de aceite:
    * Verificar quando se a aumento pequeno, médio e grande de casos de infecção;
    * Verificar quando há uma pequena, média e grande diminuição dos leitos de internação disponíveis;