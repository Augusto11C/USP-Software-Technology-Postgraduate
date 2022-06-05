<!-- Output copied to clipboard! -->

<!-----

You have some errors, warnings, or alerts. If you are using reckless mode, turn it off to see inline alerts.
* ERRORs: 0
* WARNINGs: 0
* ALERTS: 1

Conversion time: 1.142 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β33
* Sun Aug 14 2022 09:17:59 GMT-0700 (PDT)
* Source doc: EX-7-GRUPO_4_Plano-de-Teste
* Tables are currently converted to HTML tables.
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!

----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 1.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>




<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


**Projeto Integrado - TSW-014/2022- 1**

**Exercício - 7**

**Augusto Calado Bueno**

**Thaís Assunção Silva**

**São Paulo**

**2022**


## Introdução

Este exercício visa entregar todo o plano de testes dos casos de uso e fluxo do usuário na aplicação, a fim de garantir uma melhor qualidade e o conjunto completo das diversas funcionalidades requisitadas.


## Teste de Validação

Validação é uma disciplina de engenharia de software que visa ajudar na qualidade da aplicação. Juntamente com a disciplina de verificação, se torna uma coleção de atividades de análises e testes que ocorrem durante todo o ciclo de vida de um projeto [2].


## Recursos Necessários



* **Recursos Humanos**
    * Quality Assurance Engineer (Realiza a criação e execução dos testes)
    * Product Manager (auxilia na validação dos critérios de aceite)
    * Product Owner (auxiliar na validação/criação dos testes)
* **Recursos Materiais**
    * Tablets (iOS e Android); 
    * Celular (iOS e Android);
    * Notebook;
    * Impressora;
    * Internet.


## Plano de Teste


<table>
  <tr>
   <td colspan="2" ><strong>Use Case 1 - Preenchimento do Prontuário</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 1.1
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Cadastro do paciente existe previamente na unidade de saúde e retorna dados ao ser usado para acessar o prontuário.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que um paciente com cadastro informou seu <span style="text-decoration:underline;">número de carteira de saúde</span> ou <span style="text-decoration:underline;">CPF</span>
<p>
<strong>E</strong> há a adição do dado no <span style="text-decoration:underline;">campo correspondente</span> na funcionalidade de preenchimento de <span style="text-decoration:underline;">prontuários.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver o <span style="text-decoration:underline;">preenchimento parcial automático</span> dos dados pessoais do paciente devido a existência retroativa.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 1 - Preenchimento do Prontuário</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 1.2
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Cadastro do paciente não existe previamente na unidade de saúde e um prontuário em branco é retornado na funcionalidade de preenchimento de prontuários.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que um paciente sem cadastro informou seu<span style="text-decoration:underline;"> número de carteira de saúde</span> ou <span style="text-decoration:underline;">CPF</span>
<p>
<strong>E</strong> há a adição do dado no <span style="text-decoration:underline;">campo correspondente</span> na funcionalidade de preenchimento de <span style="text-decoration:underline;">prontuários.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver a exibição de um <span style="text-decoration:underline;">prontuário em branco</span> a fim de permitir o preenchimento dos dados. 
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 2 - Registro internações e transferências com controle de vagas</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 2.1
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Nenhuma unidade hospitalar possui leitos disponíveis para internação ou recebimento de transferências.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o médico atendente <span style="text-decoration:underline;">solicitou a internação</span> do paciente correspondente
<p>
<strong>E</strong> há o aviso do sistema referente a <span style="text-decoration:underline;">falta de leitos vagos</span> nos hospitais com os devidos níveis de gravidade.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver o cadastro do paciente na <span style="text-decoration:underline;">fila de espera</span> de leitos e a <span style="text-decoration:underline;">sinalização</span> desse cadastro ao médico solicitante.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 2 - Registro internações e transferências com controle de vagas</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 2.2
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>A unidade hospitalar referente a internação recusa a solicitação do médico atendente.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o médico atendente <span style="text-decoration:underline;">solicitou a internação</span> do paciente correspondente
<p>
<strong>E</strong> há o aviso ao sistema referente a <span style="text-decoration:underline;">recusa da internação.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver a <span style="text-decoration:underline;">sinalização</span> dessa recusa ao médico solicitante <span style="text-decoration:underline;">por meio de mensagem.</span>
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 2 - Registro internações e transferências com controle de vagas</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 2.3
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>A unidade hospitalar referente a internação não atende o nível de gravidade requerido pelo paciente.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o médico atendente <span style="text-decoration:underline;">solicitou a internação</span> do paciente correspondente
<p>
<strong>E</strong> há o aviso do sistema referente ao <span style="text-decoration:underline;">nível de gravidade alternativo ao necessário.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver uma <span style="text-decoration:underline;">nova escolha de localidade</span> que atenda o nível de gravidade solicitado.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 2 - Registro internações e transferências com controle de vagas</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 2.4
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>A unidade hospitalar interna o paciente no leito reservado.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o médico atendente <span style="text-decoration:underline;">solicitou a internação</span> do paciente correspondente
<p>
<strong>E</strong> há a <span style="text-decoration:underline;">reserva do leito</span> pelo sistema na unidade hospitalar com <span style="text-decoration:underline;">nível de gravidade necessário.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> deverá haver uma <span style="text-decoration:underline;">mensagem</span> no sistema informando o leito ao médico chefe de internação a fim de preparar a chegada do paciente.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 3 - Atualização do prontuário (estado e evolução do paciente)</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 3.1
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Busca do prontuário médico de um paciente diagnosticado com COVID-19 por médico atendente para inclusão de diagnóstico e tratamento.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> um <span style="text-decoration:underline;">CPF</span> de um paciente que já passou pelo processo de triagem (<span style="text-decoration:underline;">possui</span> um <span style="text-decoration:underline;">prontuário médico criado</span> com informações de saúde básicas)
<p>
<strong>Quando</strong> o médico atendente buscar pelo <span style="text-decoration:underline;">prontuário utilizando o CPF.</span>
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então, </strong>o sistema deve indicar que há <span style="text-decoration:underline;">prontuários médico cadastrado para o CPF</span> do paciente informado.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 3 - Atualização do prontuário (estado e evolução do paciente)</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 3.2
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Busca do prontuário médico de um paciente paciente sem prontuário médico cadastrado/criado.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> um <span style="text-decoration:underline;">CPF</span> de um paciente que não passou pelo processo de triagem  (<span style="text-decoration:underline;">não possui</span> um <span style="text-decoration:underline;">prontuário médico criado</span> com informações de saúde básicas) 
<p>
<strong>E</strong> <span style="text-decoration:underline;">não possui informações médicas</span> antigas cadastradas no sistema,
<p>
<strong>Quando</strong> o médico <span style="text-decoration:underline;">buscar o prontuário</span> utilizando o <span style="text-decoration:underline;">CPF</span> do paciente.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então, </strong>o sistema deve indicar que <span style="text-decoration:underline;">não há nenhum prontuário médico</span> cadastrado para o CPF do paciente informado.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 3 - Atualização do prontuário (estado e evolução do paciente)</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 3.3
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Acesso ao prontuário médico de um paciente diagnosticado com COVID-19 por médico atendente para inclusão de diagnóstico e tratamento.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> um <span style="text-decoration:underline;">CPF</span> de um paciente que já passou pelo processo de triagem (<span style="text-decoration:underline;">possui</span> um <span style="text-decoration:underline;">prontuário médico criado</span> com informações de saúde básicas)
<p>
<strong>Quando</strong> o médico busca pelo <span style="text-decoration:underline;">prontuário médico</span> do paciente
<p>
<strong>E</strong> inserir as informações sobre o <span style="text-decoration:underline;">diagnóstico e tratamento</span> no prontuário encontrado. 
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então, </strong>as informações inseridas pelo médico devem ser <span style="text-decoration:underline;">salvas pelo sistema e exibidas para os usuários</span> quando realiza-se uma nova busca.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 3 - Atualização do prontuário (estado e evolução do paciente)</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 3.4
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Acesso ao prontuário médico de um paciente por enfermeiro para atualização/inclusão de diagnóstico e tratamento.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> um <span style="text-decoration:underline;">CPF</span> de um paciente que já passou pelo processo de triagem (<span style="text-decoration:underline;">possui</span> um <span style="text-decoration:underline;">prontuário médico criado</span> com informações de saúde básicas)  
<p>
<strong>Quando</strong> o enfermeiro ou técnico de enfermagem busca pelo <span style="text-decoration:underline;">prontuário médico</span> do paciente
<p>
<strong>E</strong> tentar inserir as informações sobre o <span style="text-decoration:underline;">diagnóstico e tratamento</span> no prontuário encontrado. 
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> o sistema <span style="text-decoration:underline;">não permitirá as atualizações</span> no diagnóstico e tratamento (são campos “atualizáveis” apenas por médicos).
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 3 - Atualização do prontuário (estado e evolução do paciente)</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 3.5
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Impressão do prontuário médico de um paciente por profissional da saúde (ex: médico ou enfermeiro).
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> um <span style="text-decoration:underline;">CPF</span> de um paciente que já passou pelo processo de triagem (<span style="text-decoration:underline;">possui</span> um <span style="text-decoration:underline;">prontuário médico criado</span> com informações de saúde básicas) 
<p>
<strong>Quando</strong> o profissional da saúde busca pelo <span style="text-decoration:underline;">prontuário médico</span> do paciente 
<p>
<strong>E</strong> iniciar a operação de impressão do prontuário desejado.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> o sistema <span style="text-decoration:underline;">ira colocar o PDF </span>do prontuário na fila de impressão e o imprimirá<span style="text-decoration:underline;">.</span>
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 4 - Gerar Relatórios</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 4.1
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Geração do relatório de registros de pacientes (contando com infectados, re-infectados e óbitos).
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o sistema possui <span style="text-decoration:underline;">informações</span> sobre <span style="text-decoration:underline;">paciente</span> (infectados, curados, re-infectados)
<p>
<strong>Quando </strong>um usuário (ex: funcionários da secretaria da saúde com as devidas permissões) iniciar a função de extração de relatório de registro de pacientes para o <em>range </em>de datas informado pelo usuário.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> o sistema compilará as informações disponíveis no <em>range </em>de tempo desejado e gerará o relatório de registro de pacientes.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 4 - Gerar Relatórios</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 4.2
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Geração do relatório de balanço de vagas nos hospitais.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o sistema possui <span style="text-decoration:underline;">informações</span> sobre <span style="text-decoration:underline;">internações</span> e <span style="text-decoration:underline;">condição dos hospitais</span>
<p>
<strong>Quando </strong>um usuário (ex: funcionários da secretaria da saúde com as devidas permissões) iniciar a função de extração de relatório de balanço de vagas nos hospitais para o <em>range </em>de datas informado pelo usuário.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> o sistema compilará as informações disponíveis dentro do <em>range </em>de tempo desejado e gerará o relatório de relatório de balanço de vagas nos hospitais.
   </td>
  </tr>
</table>



<table>
  <tr>
   <td colspan="2" ><strong>Use Case 4 - Gerar Relatórios</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Identificador Caso de Teste</strong>
   </td>
   <td>Caso de Teste 4.3
   </td>
  </tr>
  <tr>
   <td><strong>Descrição do Caso de Teste</strong>
   </td>
   <td>Geração do relatório das fases de cada regiões do estado (verde, amarela ou vermelha) sobre a pandemia.
   </td>
  </tr>
  <tr>
   <td><strong>Dados de Entrada</strong>
   </td>
   <td><strong>Dado</strong> que o sistema possui <span style="text-decoration:underline;">informações</span> sobre cidadãos <span style="text-decoration:underline;">infectados com COVID-19</span>, <span style="text-decoration:underline;">internações</span> e <span style="text-decoration:underline;">condição dos hospitais</span>
<p>
<strong>Quando </strong>um usuário (ex: funcionários da secretaria da saúde com as devidas permissões) iniciar a função de extração de relatório das fases de cada regiões do estado para o <em>range </em>de datas informado pelo usuário.
   </td>
  </tr>
  <tr>
   <td><strong>Resultados Esperados</strong>
   </td>
   <td><strong>Então,</strong> o sistema compilará as informações disponíveis dentro do <em>range </em>de tempo desejado e gerará o relatório de relatório das fases de cada regiões do estado.
   </td>
  </tr>
</table>



## Referências

[1] CALADO, Augusto; ASSUNÇÃO, Thais. Projeto Integrado - TSW-014/2022- 1: Exercício 3 - Casos de Uso. Versão 4. 2022. Acesso disponível: [https://cutt.ly/MF8jMct](https://cutt.ly/MF8jMct).

[2] D.R. Wallace; R.U. Fujii. Software Verification and Validation: An Overview. IEEE, Maio, 1989. Acesso disponível: [https://ieeexplore.ieee.org/abstract/document/28119](https://ieeexplore.ieee.org/abstract/document/28119)
