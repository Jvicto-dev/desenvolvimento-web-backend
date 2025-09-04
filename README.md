# desenvolvimento-web-backend

API RESTful para gerenciamento de tarefas em Java com Spring Boot, utilizando MySQL e Spring Data JPA. Permite cadastrar, consultar, atualizar e remover tarefas.

## Sobre o Projeto

Este projeto consiste em uma **API RESTful** para gerenciamento de tarefas, desenvolvida em **Java com Spring Boot**. Cada tarefa possui:

- Nome da tarefa
- Data de entrega
- Responsável pela tarefa

## Funcionalidades

- Criar uma nova tarefa
- Consultar todas as tarefas cadastradas
- Consultar uma tarefa específica pelo ID
- Atualizar uma tarefa existente
- Remover uma tarefa

## Tecnologias Utilizadas

- **Java 17** e **Spring Boot**
- **Spring Data JPA**
- **MySQL**
- **Postman** ou **Insomnia** para testes
- Padrões REST

## Como Executar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/desenvolvimento-web-backend.git
   cd desenvolvimento-web-backend
   ```

2. **Configure o banco de dados MySQL:**
   - Crie um banco chamado `trabalho_uninter`:
     ```sql
     CREATE DATABASE trabalho_uninter;
     ```
   - O arquivo de configuração `application.properties` já está pronto para uso:
     ```
     spring.application.name=TrabalhoUninter
     spring.datasource.url=jdbc:mysql://localhost:3306/trabalho_uninter
     spring.datasource.username=root
     spring.datasource.password=
     spring.jpa.hibernate.ddl-auto=update
     spring.jpa.show-sql=true
     spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
     ```
   - Ajuste o usuário e senha conforme sua instalação do MySQL.

3. **Execute a aplicação:**
   - Via terminal:
     ```bash
     ./mvnw spring-boot:run
     ```
   - Ou rode a classe principal pelo seu IDE.

## Testando a API

Você pode testar usando Postman, Insomnia ou até o navegador:

- **Listar tarefas**
  ```
  GET http://localhost:8080/tarefas
  ```
- **Criar tarefa**
  ```
  POST http://localhost:8080/tarefas
  ```
  Exemplo de body (JSON):
  ```json
  {
    "nome": "Estudar Spring Boot",
    "dataEntrega": "2025-09-10",
    "responsavel": "Victo"
  }
  ```
- **Buscar tarefa por ID**
  ```
  GET http://localhost:8080/tarefas/{id}
  ```
- **Atualizar tarefa**
  ```
  PUT http://localhost:8080/tarefas/{id}
  ```
  Body igual ao de criação.

- **Remover tarefa**
  ```
  DELETE http://localhost:8080/tarefas/{id}
  ```

## Observações

- O banco de dados MySQL deve estar rodando localmente.
O arquivo de banco de dados `trabalho_uninter.sql` está na raiz do projeto.
---

Projeto desenvolvido para a disciplina de **Desenvolvimento Web Back-
