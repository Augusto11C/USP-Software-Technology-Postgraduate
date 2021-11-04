
# Aula 5 - 20211103
- TODO: ler sobre fábrica abstrata
- [Aula 4] Agregado: encapsula a estrutura interna de objetos com associações complexas, mantendo a integridade desta estrutura.
- Fábrica – cria e reconstitui objetos não triviais (tipicamente builda agregados)
- Repositório – opera na metade e no fim do ciclo de vida: fornece meios para encontrar e recuperar Agregados, enquanto
encapsula toda a infraestrutura envolvida.
- "Uso canônico == uso pretendido"
- TODO Get Image slide 04/30
    - Os **serviços de aplicação** somente orquestram os objetos, não contendo nenhuma lógiva de negócio
        - serviço pode usar diretamente o repositório (usa o repositório para persistir/recuperar agregados)
        - serviço pode usar diretamente a fábrica (criar agregados com alguma complexidade)
        - atualiza o modelo de domínio pela raiz do agregado
        - serviço pode usar diretamente serviços de domínio para certas transações que envolvem mais de um agregado
    
    - Os **serviços de domínio**
        - "dois agregados precisam interagir em uma mesma transação" -> serviço de domínio orquestra/articula essa interação em uma única transação

### Fábrica
"Transfira a responsabilidade de criar instâncias de **objetos complexos e Agregados** para um objeto separado, que por si mesmo não tem nenhuma responsabilidade no modelo de domínio, embora faça parte do projeto [design] do domínio. Forneça uma interface que encapsule toda a montagem complexa, não exigindo que o cliente refencie classes concretas dos objetos que estão sendo instanciados. **Crie Agregados inteiros como uma única peça, aplicando seus invariantes**.” (Evans, E., p. 138)

<br>

- "joga a bola pra um terceiro para resolver o problema da criação de agregado"

- Separar a criação de um objeto de seu uso: uma regra fundamental do design (não necessariamente do DDD). 
- O objeto cliente deve ignorar como os objetos dependentes foram criados => SRP com respeito ao **uso**.
- Apesar de **pertencer ao modelo de domínio**, **não faz parte de sua linguagem onipresente**. É uma necessidade do design/implementação do modelo de domínio.
- Encapsula o conhecimento necessário à criação de objetos complexos e, sobretudo, de Agregados. A fábrica deve aplicar os invariantes ao criar os objetos.
- Em ocasiões simples, basta o objeto cliente invocar um construtor ou pode-se aplicar a Injeção da Dependência.
