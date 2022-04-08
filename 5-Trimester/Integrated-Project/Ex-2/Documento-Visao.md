**Projeto Integrado - TSW-014/2022- 1**

**Exercício - 2**

**Augusto Calado Bueno**

**Thaís Assunção Silva**

**São Paulo**

**2022**


## Requisitos de Negócio


### Oportunidade de Negócio - Definição do Problema


<table>
  <tr>
   <td>
    <strong>O Problema </strong>
   </td>
   <td>Gerenciar as ocorrências de contaminação de pessoas pela COVID-19, realizando tanto o controle da transmissão/propagação do vírus quanto o controle de disponibilidade de leitos no estado. 
   </td>
  </tr>
  <tr>
   <td>
    <strong>Afeta</strong>
   </td>
   <td>
<ul>

<li>Secretaria da saúde do estado; 

<li>Funcionários da rede de saúde:  
<ul>
 
<li>Médicos; 
 
<li>Técnicos de enfermagem;
 
<li>Enfermeiros;
 
<li>Equipe da ambulância  (motorista, médico, socorrista, etc).
</li> 
</ul>

<li>Instituições de saúde (e.g: hospitais e postos de saúde); 

<li>Pacientes.
</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>
    <strong>Tem como Impacto </strong>
   </td>
   <td>
    Compreender a evolução dos casos dentro do Estado, possibilitando assim a gestão eficiente dos recursos como materiais, leitos e profissionais de saúde.
   </td>
  </tr>
  <tr>
   <td>
    <strong>Uma Solução de sucesso seria/teria </strong>
   </td>
   <td>
    O desenvolvimento de um sistema para registro de prontuários médicos, controle e gerenciamento de leitos e internações e controle e gerenciamento das ocorrências de casos de infecções pelo COVID-19.
   </td>
  </tr>
</table>




Posicionamento do Produto


<table>
  <tr>
   <td>
    <strong>Para </strong>
   </td>
   <td>
    Funcionários envolvidos (e.g. enfermeiros / médicos) e funcionários da secretaria de saúde.
   </td>
  </tr>
  <tr>
   <td>
    <strong>Que </strong>
   </td>
   <td>
    Desejam controlar e gerenciar leitos e internações, tal qual as ocorrências de contaminação por COVID-19, acompanhando a evolução da doença.
   </td>
  </tr>
  <tr>
   <td>
    <strong>O</strong>
   </td>
   <td>
    CovidNet
   </td>
  </tr>
  <tr>
   <td>
    <strong>É </strong>
   </td>
   <td>
    Sistema de gerenciamento e registro de ocorrências de contaminação de COVID-19 e controle de leitos.
   </td>
  </tr>
  <tr>
   <td>
    <strong>Que </strong>
   </td>
   <td>
    Registra e gerencia os casos de COVID-19 de forma digital e realiza a gestão dos recursos destinados ao combate à pandemia como leitos hospitalares.
   </td>
  </tr>
  <tr>
   <td>
    <strong>Diferentemente de </strong>
   </td>
   <td>
    Fazer o gerenciamento manual através de prontuários físicos e registros isolados em diferentes sistemas da instituição hospitalar. 
   </td>
  </tr>
  <tr>
   <td>
    <strong>Nosso Produto </strong>
   </td>
   <td>
    Tem como maior diferencial a integração entre os diversos sistemas presentes em instituições de saúde (e.g. hospitais e unidades de saúde), fazendo com que se haja uma visão holística da situação da pandemia através das informações inseridas no sistema, análise estatísticas do estado de saúde dos pacientes e condições dos hospitais.
   </td>
  </tr>
</table>



## 
    


## 
    Contexto de Negócio 


### 
    Perfil dos stakeholders 



* Secretaria da saúde do estado; 
    * Analista do centro de controle do COVID-19 (contribue com insights para produção de relatório);
    * Secretário de saúde (quem solicitou o sistema);
    * Analista de contágio (contribui com insights para produção de relatório).
* Funcionários da rede de saúde (contribuem com insights): 
    * Médicos; 
    * Técnicos de enfermagem;
    * Enfermeiros;
    * Equipe da ambulância  (motorista, médico, socorrista, etc).
* Instituições de saúde (receberão a implantação do projeto) :
    * Hospitais (e.g. de campanha, particulares e públicos);
    * Clínicas;
    * Postos de saúde. 

### 
    Usuários finais 


        ● **Médicos**: Formação superior, pode trabalhar em mais de um local, tem acesso à internet, realiza os atendimentos nos hospitais, podendo ser em pronto socorro ou UTI. Toma decisões quanto à priorização de pacientes e direcionamento para outras unidades, fazem prescrição médica, avaliam exames; 


        ● **Enfermeiros**: Formação superior, pode trabalhar em mais de um local, tem acesso à internet, realizam o acompanhamento de técnicos de enfermagem, guiam a triagem de pacientes, liberam medicamentos conforme prescrição, realizam exames solicitados, checam anotações do prontuário do paciente;


        ● **Técnicos de Enfermagem**: Formação técnica, pode trabalhar em mais de um local, tem acesso à internet, realiza a triagem de pacientes, ministram medicamentos, realizam exames solicitados, medem sinais vitais e preenchem o prontuário de acordo com a evolução do paciente;

* **Operador(a) da central de combate ao COVID-19: **Formação média concluída, acesso restrito ao sistema, cadastra funcionários envolvidos, visualiza e edita cadastros, agrupa e reagrupa funcionários por instituição de saúde e checa locais com carência de profissionais;
* **Analista do centro de controle do COVID-19:** Formação superior, acesso irrestrito ao sistema, realiza análises sobre a progressão e controle da pandemia através das informações do sistema e análises dos recursos hospitalares como sua disponíveis, quais estão em utilização, quais estão em falta, etc;
* **Secretário de saúde: **Cargo político, acesso aos relatórios produzidos e hospedados no sistema. Visualizar os relatórios de progressão da pandemia, da monitoração e disponibilidade de recursos hospitalares para tomar decisões quanto a aplicação de medidas restritivas, compra e alocação de recursos (equipamentos médicos, disponibilização de mais leitos, etc).

## 
    Escopo



### Features Principais



1. Cadastro dos funcionários envolvidos;
2. Prontuário médico digital específico para COVID-19;
3. Consulta do histórico médico do paciente;
4. Definição de critérios de gravidade por tipo de hospital;
5. Indicação automática do local de internação (envolvendo transferências);
6. Acompanhamento das vagas de hospitais, considerando os tipos de vagas;
7. Geração de relatórios para acompanhamento da evolução da COVID-19 no Estado;
8. Cálculo da fase que a região do Estado se encontra;