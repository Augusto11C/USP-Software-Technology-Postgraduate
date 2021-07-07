## DW - Passos para Implantação

1. surge a ideia/necessidade para o dw
2. realização da especificação
	- definir objetivo
	- graus de desempenho
	- quais relatorios a se gerar?
	- preocupação c/ segurança de acesso
3. consultas
	- quais tipos de consultas deixarei disp para users
4. cargas de dados
	- de quanto em quanto tempo haverá carga?
	- averá descarte dos dados? ou colocaremos em fita magnética
5. Bancos de dados de origem
	- onde estão? 
6. Inclusão de metadados
7. Criar modelo multidimensional
	- inicialmente podemos criar a matriz de barramento
8. apartir do (7) montar os modelos estrelas
9. definir atributos fato/dimensão
10. definir a granularidade
11. detalhamento das consultas
	- consultas no passado, presente, futuro
12. especificar, se necessario, data mars
13. definir qual gerenciador de banco de dados devemos utilizar
14. definir o hardware (servidores, onde será feito backups, etc)
15. desenvolvimento do ETL
16. definir os cubos que serão usados
17. definir a ferramenta olap e outros sw necessários
18. definir a equipe
19. testes considerando 1-18
20. criar monitorações de uso e desempenho
21. realização de manutenções
22. cada uma das etapas o orçamento deve estar bem definido

## BigData - Passos para Implantação

1. surge a ideia/necessidade para o dw
2. realização da especificação
	- definir objetivo
	- graus de desempenho
	- quais relatorios a se gerar?
	- preocupação c/ segurança de acesso
3. consultas
	- quais tipos de consultas deixarei disp para users
4. cargas de dados
	- de quanto em quanto tempo haverá carga?
	- averá descarte dos dados? ou colocaremos em fita magnética
5. Bancos de dados de origem
	- onde estão? midias sociais
6. metadados
7.  V's
8. definir a granularidade
9. Usar o Hadoop MapRedulce
10. [semelhante ao dw]

## Data lake - Passos para Implantação 

1. surge a ideia/necessidade para o dw
2. realização da especificação
	- definir objetivo
	- graus de desempenho
	- quais relatorios a se gerar?
	- preocupação c/ segurança de acesso
3. consultas
	- quais tipos de consultas deixarei disp para users
4. cargas de dados
	- de quanto em quanto tempo haverá carga?
	- averá descarte dos dados? ou colocaremos em fita magnética
5. Bancos de dados de origem
	- onde estão? midias sociais
6. metadados
7. Extração e Carga de Dados
8. Gerar datalake ou Hadoop/MapReduce (este gerará BigData)