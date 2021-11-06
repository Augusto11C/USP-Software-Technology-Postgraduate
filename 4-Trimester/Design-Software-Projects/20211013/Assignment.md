1. Subdomínios e contextos delimitados

    A. Identificar os **Contextos Delimitados** do projeto integrado,**classificando-os** nos tipos de (sub)domínio (nuclear,...).

    - Atendimento/Consulta
      - Paciente
      - Médico
      - Instituição atendimento
      - Remédios
      - Serviços
    - Institucional
      - hospital, clinicas e postos
    - Users
      - Paciente
      - Médico
      - Analista
    - Transporte
      - Ambulancia, etc
    - Serviços Hospitalares
    - Suprimentos
      - remédios
      - equipamentos epis
      - Máquinas (raio-x, ultrasom)
    - Monitorimento Pandemia (Planejamento/Controle/Acompanhamento (Pandemia))

    B. Para cada Contexto Delimitado, **identificar seus conceitos chave** (breve descrição).

    C. Criar um Mapa de Contexto

2. Definir esboço inicial arquitetura hexagonal
   - Identificar as Portas pelos protocolos das interações que devem ser tratados por elas
     - Portas de Grupo Persistência
       - Banco de dados Relacional (PostgreSQL)
       - Banco de dados em Memória (Redis)
    
     - Portas de Grupo Message Broker / Message Queue / Event bus / Message Bus (a mediator that transfers a message from a sender to a receiver)
       - Kafka
       - RabbitMQ

     - Porta de Notificação
       - SMS
       - Email

     - Portas de Grupo HTTP
       - API REST

   - Definir as principais **interações processadas pelas Portas**.
     -  Portas de Grupo Persistência
        -  Salva prontuários médicos
        -  