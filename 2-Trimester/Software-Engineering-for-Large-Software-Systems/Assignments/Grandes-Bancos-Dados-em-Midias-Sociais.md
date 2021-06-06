## Resumo - Grandes Bancos de Dados em Mídias Sociais
Augusto Calado Bueno

Em 2020, no Facebook, haviam 10,5 milhões de vídeos postados, 147 mil fotos compartilhadas a cada minuto. 150 mil mensagens foram enviadas a cada minuto e foram gerados quatro petabytes de dados todos os dias no Facebook.  No instagram 300 mil posts foram feitos a cada minuto, no Twitter quinhentos milhões de novos Tweets foram postados todos os dias, e no aplicativo de mensagens Whatsapp 41 milhões de mensagens foram compartilhadas a cada minuto[7][6][5].

É evidente o volume massivo de dados gerados pelas redes sociais todos os dias, gerenciar essa quantidade não é uma tarefa simples e demanda muitos recursos, tanto de software quanto de hardware [1]. 

Devido a característica das redes sociais produzirem muito volume de dados, o tradicional modelo RDBMS não é o suficiente para manipular, orquestrar e gerenciar a quantidade de dados e operações que acontecem a cada segundo. Novas soluções  relacionadas a armazenamento e banco de dados como banco de dados NoSQL foram desenvolvidas para tratar este problema.

As grandes redes sociais como Facebook, Instagram, Whatsapp e Twitter utilizam uma arquitetura híbrida entre banco de dados SQL e NoSQL para atender a demanda de dados produzidos e consumidos.

O Twitter para atender a demanda e os dados produzidos diariamente utiliza uma arquitetura híbrida de sistemas de armazenamento contando com bancos SQL, NoSQL e In-memory DBs. O banco de dados relacional MySQL é utilizado para gerenciamento de campanhas de anúncios e troca de anúncios. Já o banco Redis é usado para armazenar as sessões dos usuários, timelines e tweets e o Framework Hadoop é usado para manipular mais de 500 PB de dados distribuídos e cold storage (armazenamento de dados inativos) [2][3].

O Facebook, por sua vez, faz uso, também, de uma arquitetura de banco de dados híbrida, utilizando soluções de armazenamento SQL e NoSQL. Como solução SQL, há a utilização do MySQL que armazena os grafos social de rastreio e gerenciamento de eventos dos usuários da rede social. Como solução NoSQL e cache, utiliza-se o Memcache e Beringei CircleCI. Este último é um no mecanismo de armazenamento de série temporal de memória desenvolvido pelo próprio Facebook. O Memcache é um sistema de armazenamento que localiza-se na frente do MySQL para melhorar a performance de latência [4].

## Referências
[1] Analysis of Data Management and Query Handling in Social Networks using NoSQL Databases 

[2] THE INFRASTRUCTURE Behind Twitter: Scale. [S. l.], 19 jan. 2017. Disponível em: https://blog.twitter.com/engineering/en_us/topics/infrastructure/2017/the-infrastructure-behind-twitter-scale.html. Acesso em: 9 jun. 2021.

[3] HOW Twitter Uses Redis To Scale - 105TB RAM, 39MM QPS, 10,000+ Instances. [S. l.], 8 set. 2014. Disponível em: http://highscalability.com/blog/2014/9/8/how-twitter-uses-redis-to-scale-105tb-ram-39mm-qps-10000-ins.html. Acesso em: 9 jun. 2021.

[4] FACEBOOK Database [Updated] – A Thorough Insight Into The Databases Used @Facebook. Disponível em: https://www.8bitmen.com/what-database-does-facebook-use-a-1000-feet-deep-dive/. Acesso em: 9 jun. 2021.

[5] HOW Much Data Is Created Every Day in 2021. [S. l.], 18 maio 2021. Disponível em: https://techjury.net/blog/how-much-data-is-created-every-day/. Acesso em: 9 jun. 2021.

[6] DATA Never Sleeps 8.0. [S. l.], 2021. Disponível em: https://www.domo.com/learn/infographic/data-never-sleeps-8. Acesso em: 9 jun. 2021.

[7] HOW Much Data Do We Create Every Day? The Mind-Blowing Stats Everyone Should Read. [S. l.], 21 maio 2018. Disponível em: https://www.forbes.com/sites/bernardmarr/2018/05/21/how-much-data-do-we-create-every-day-the-mind-blowing-stats-everyone-should-read/?sh=352c3dae60ba. Acesso em: 9 jun. 2021.

[8] HOW Much Data Is Created Every Day? [27 Staggering Stats]. [S. l.], 28 jan. 2021. Disponível em: https://seedscientific.com/how-much-data-is-created-every-day/. Acesso em: 9 jun. 2021.



