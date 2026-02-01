CRUD de Clientes - Spring Boot API
Este projeto é uma API REST robusta desenvolvida para o gerenciamento de clientes, com foco em integridade de dados, validações estruturadas e tratamento de exceções. O sistema permite o armazenamento e manipulação de informações essenciais, garantindo que a base de dados permaneça consistente e performática.

🚀 Tecnologias Utilizadas
Java 17

Spring Boot 3

Spring Data JPA (Persistência de dados)

H2 Database (Banco de dados em memória para testes)

Maven (Gerenciamento de dependências)

Bean Validation (Regras de negócio e integridade)

📋 Funcionalidades
A API expõe um recurso de clientes com as seguintes operações:

Busca Paginada: Listagem eficiente de recursos para otimização de performance.

Busca por ID: Recuperação detalhada de um registro específico.

Inserção de Novo Recurso: Cadastro de clientes com validação de campos.

Atualização de Recurso: Edição de dados existentes com tratamento de erro.

Deleção de Recurso: Remoção segura de registros por identificador.

⚙️ Regras de Negócio e Validações
Para garantir a qualidade dos dados (Data Quality), o projeto implementa:

Nome: Campo obrigatório (não pode ser vazio).

Data de Nascimento: Validada para impedir datas futuras (@PastOrPresent).

Mapeamento de Banco: Conversão automática de camelCase para snake_case (ex: birthDate -> birth_date).

Seed de Dados: O projeto já inicia com um script SQL contendo mais de 10 registros significativos para facilitar o teste imediato das rotas.

⚠️ Tratamento de Exceções
A API retorna códigos de status HTTP padronizados:

404 Not Found: Retornado quando um ID solicitado não existe no banco.

422 Unprocessable Entity: Retornado em falhas de validação, acompanhado de uma mensagem customizada detalhando o erro em cada campo.

🛠️ Como Executar o Projeto
Certifique-se de ter o Java 17 e o Maven instalados.

Clone o repositório:

Bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
Acesse a pasta do projeto e execute:

Bash
./mvnw spring-boot:run
A API estará disponível em http://localhost:8080.

O console do Banco H2 pode ser acessado em http://localhost:8080/h2-console.

👤 Autor
Vitor Pereira de Souza
