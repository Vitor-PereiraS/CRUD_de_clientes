# API base para Cadastro de Clientes

Este projeto consiste em uma **API REST para gerenciamento de clientes**, desenvolvida com Spring Boot e seguindo boas práticas de arquitetura, validação de dados e tratamento de exceções.  
O foco principal é garantir **integridade, consistência e qualidade dos dados**, além de uma experiência clara para quem consome a API.

---

## 🚀 Tecnologias Utilizadas

- Java 17  
- Spring Boot 3  
- Spring Data JPA (Persistência de dados)  
- H2 Database (Banco de dados em memória para testes)  
- Maven (Gerenciamento de dependências)  
- Bean Validation (Validações e regras de negócio)

---

## 📋 Funcionalidades

A API expõe um recurso de **Clientes**, com as seguintes operações:

- **Busca Paginada**  
  Listagem eficiente de clientes com paginação, visando melhor performance.

- **Busca por ID**  
  Recuperação detalhada de um cliente específico.

- **Criação de Cliente**  
  Cadastro de novos clientes com validação de campos obrigatórios.

- **Atualização de Cliente**  
  Alteração de dados existentes com verificação de erros e inconsistências.

- **Remoção de Cliente**  
  Exclusão segura de registros a partir do identificador.

---

## ⚙️ Regras de Negócio e Validações

Para assegurar a qualidade dos dados (**Data Quality**), o projeto implementa:

- **Nome**  
  Campo obrigatório, não pode ser vazio ou nulo.

- **Data de Nascimento**  
  Validada para impedir datas futuras (`@PastOrPresent`).

- **Mapeamento de Banco de Dados**  
  Conversão automática de `camelCase` para `snake_case`  
  Exemplo: `birthDate` → `birth_date`.

- **Seed de Dados**  
  A aplicação já inicia com um script SQL contendo **mais de 10 registros**, facilitando testes imediatos das rotas da API.

---

## ⚠️ Tratamento de Exceções

A API retorna respostas padronizadas seguindo boas práticas REST:

- **404 – Not Found**  
  Quando o ID solicitado não existe no banco de dados.

- **422 – Unprocessable Entity**  
  Quando ocorre falha de validação, retornando mensagens claras e específicas para cada campo inválido.

---

## 🛠️ Como Executar o Projeto

### Pré-requisitos

- Java 17  
- Maven  

### Passos para execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
2. Acesse a pasta do projeto e execute:
  ```bash
  ./mvnw spring-boot:run
  ```
3. A API estará disponível em:
  ```text
  http://localhost:8080
  ```
4.O console do banco H2 pode ser acessado em:
  ```text
  http://localhost:8080/h2-console
  ```
👤 Autor
Vitor Pereira de Souza
