# ProductClientHub

ProductClientHub é uma aplicação ASP.NET Core para gerenciar clientes e produtos. Esta aplicação fornece uma API para registrar, atualizar, obter e deletar clientes e produtos.

Este projeto foi desenvolvido no minicurso de Introdução ao C# da Rocketseat.

## Estrutura do Projeto

- **ProductClientHub.API**: Contém a API principal do projeto.
- **ProductClientHub.Communication**: Contém classes de comunicação, como requests e responses.
- **ProductClientHub.Exceptions**: Contém classes de exceções personalizadas.

## Configuração

### Pré-requisitos

- .NET 8.0 SDK
- Visual Studio 2022 ou superior

### Configuração do Banco de Dados

Este projeto utiliza SQLite como banco de dados. O caminho do banco de dados está configurado no arquivo `ProductClientHub.API/Infrastructure/ProductClientHubDbContext.cs`.

### Configuração do Ambiente

Existem três arquivos de configuração de ambiente:

- `appsettings.json`: Configurações gerais.
- `appsettings.Development.json`: Configurações específicas para o ambiente de desenvolvimento.
- `appsettings.Production.json`: Configurações específicas para o ambiente de produção.

## Executando o Projeto

1. Clone o repositório:

   ```sh
   git clone https://github.com/seu-usuario/ProductClientHub.git
   cd ProductClientHub
   ```

2. Restaure as dependências:

   ```sh
   dotnet restore
   ```

3. Execute a aplicação:
   ```sh
   dotnet run --project ProductClientHub.API
   ```

A aplicação estará disponível em `http://localhost:5184`.

## Endpoints da API

### Clientes

- **POST /api/clients**: Registra um novo cliente.
- **PUT /api/clients/{id}**: Atualiza um cliente existente.
- **GET /api/clients**: Obtém todos os clientes.
- **GET /api/clients/{id}**: Obtém um cliente pelo ID.
- **DELETE /api/clients/{id}**: Deleta um cliente pelo ID.

### Produtos

- **POST /api/products/{clientId}**: Registra um novo produto para um cliente.
- **DELETE /api/products/{id}**: Deleta um produto pelo ID.
