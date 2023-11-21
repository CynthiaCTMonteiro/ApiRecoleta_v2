# ApiRecoleta_v2

## Descrição

ReColeta é uma API RESTful desenvolvida em Java com o framework Spring Boot, focada em sustentabilidade e reciclagem. Este projeto visa facilitar a conexão entre geradores de resíduos e recicladores, promovendo práticas sustentáveis e o correto descarte de resíduos para mitigar os impactos ambientais.

## Funcionalidades

- **Registro e Autenticação de Usuários**: Permite que usuários se registrem e autentiquem no sistema.
- **Gerenciamento de Usuários**: Inclui operações de CRUD (Create, Read, Update, Delete) para gerenciar usuários, seus tipos e papéis no sistema.

## Entidades

- **User**: Representa um usuário, com atributos como nome, sobrenome, email e senha.
- **Role**: Define os papéis dos usuários, como `ROLE_USER` ou `ROLE_ADMIN`.
- **UserType**: Categoriza tipos de usuários, como `PRODUCES_WASTE` ou `COLLECTS_WASTE`.

## Dependências

- Spring Boot
- Spring Security
- Spring Data JPA
- BCryptPasswordEncoder
- Lombok
- Java Persistence API (JPA)
- Hibernate
- PostgreSQL

## Configuração de Segurança

- Configurações de segurança com Spring Security, incluindo regras de acesso e autenticação.
- Configurações CORS com WebConfig.

## Mapeamento ORM e Segurança

- Anotações JPA para mapeamento ORM.
- BCryptPasswordEncoder para codificação de senhas.

## Inicialização

- Inicialização com `@PostConstruct` para criar um usuário administrador padrão.

## Principais Métodos

- `User.save(UserRegistrationDto registrationDto)`: Salva um novo usuário.
- `UserService.loadUserByUsername(String username)`: Carrega um usuário para autenticação.
- `UserController.registerUserAccount(UserRegistrationDto registrationDto)`: Registra um novo usuário.
- `UserController.editUser(Long id, User user)`: Edita um usuário existente.
- `UserController.delete(Long id)`: Exclui um usuário.

## Configuração e Execução

### Pré-requisitos

Antes de iniciar, verifique se você tem o seguinte software instalado:

- **Java JDK (versão 11 ou superior)**: É necessário ter o Java Development Kit para compilar e executar aplicações Java. Você pode baixá-lo do [site oficial da Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- **Maven (versão 3.6 ou superior)**: Maven é uma ferramenta de automação de build para projetos Java. Faça o download do Maven no [site oficial](https://maven.apache.org/download.cgi) e siga as [instruções de instalação](https://maven.apache.org/install.html).
- **PostgreSQL (com um banco de dados configurado conforme especificado no arquivo `application.properties`)**: PostgreSQL é um sistema de gerenciamento de banco de dados. Instale-o seguindo as instruções no [site oficial](https://www.postgresql.org/download/).

### Configurando o Banco de Dados

1. **Criar um Banco de Dados**: Inicie o PostgreSQL e crie um novo banco de dados para a aplicação.
2. **Atualizar Configurações**: Localize o arquivo `src/main/resources/application.properties` no projeto. Abra-o em um editor de texto e atualize as configurações de banco de dados (URL, nome de usuário e senha) para corresponder às do banco de dados que você criou.

### Executando a Aplicação

1. **Abrir Terminal**: Navegue até a pasta raiz do projeto usando um terminal.
2. **Construir o Projeto com Maven**: Execute `mvn clean install`. Este comando limpa os arquivos de compilação anteriores (se houver) e constrói o projeto. Se a construção for bem-sucedida, você verá uma mensagem de 'BUILD SUCCESS'.
3. **Iniciar a Aplicação**: Execute `mvn spring-boot:run`. Este comando inicia a aplicação. Você saberá que a aplicação está rodando se não houver erros no terminal e se ver mensagens indicando que o servidor iniciou.
4. **Acessar a Aplicação**: Abra um navegador e acesse `localhost:8080`. Se tudo estiver configurado corretamente, a aplicação deve estar rodando nesta URL.

### Executando Testes

1. **Abrir Terminal**: Volte para o terminal na pasta raiz do projeto.
2. **Executar Testes com Maven**: Digite `mvn test` e pressione Enter. Isso iniciará os testes automatizados.
3. **Visualizar Resultados**: Após a execução dos testes, os resultados serão exibidos no terminal. Procure por 'BUILD SUCCESS' para saber que todos os testes passaram.

## Sobre o Projeto

Este projeto é parte de um esforço colaborativo dos alunos da Faculdade de Tecnologia de Cotia (FATEC) para abordar questões ambientais urgentes, promovendo a sustentabilidade e a economia circular.

