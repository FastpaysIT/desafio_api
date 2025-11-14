#  Desafio Backend Júnior - FastPays

O objetivo deste teste é avaliar seu domínio em construção de APIs, Docker, modelagem de banco de dados e qualidade de código (testes e validações).

---

##  O Cenário

Você deve criar uma API RESTful para gerenciar o cadastro de **Empresas** e **Pessoas**.

A regra de negócio fundamental é:
> **Uma Empresa pode ter várias Pessoas vinculadas a ela, mas uma Pessoa só pode trabalhar em uma única Empresa.**

Você é livre para escolher a tecnologia (Node.js, Python, Java, Go, C#, PHP, etc), desde que cumpra os requisitos abaixo.

---

## Requisitos Técnicos Obrigatórios

1.  **Docker:** A aplicação e o banco de dados devem subir com um único comando `docker-compose up`.
2.  **Banco de Dados:** Obrigatório uso de banco Relacional (PostgreSQL ou MySQL).
3.  **Testes Unitários:** Você deve implementar testes unitários focados nas **regras de negócio/validações** (ex: validar se o CPF está correto, se a limpeza de strings funciona, etc). Não é obrigatório testar a camada de banco de dados ou controllers.

---


## Contrato da API (Entrada e Saída)

Sua API deve aceitar payloads JSON. Atente-se às discrepâncias entre o formato de entrada (com formatação) e o formato do banco (apenas números).

### 1. Criar Empresa (`POST /empresas`)
**Exemplo de Entrada:**
```json
{
  "nome": "FastPays Tecnologia",
  "cnpj": "12.345.678/0001-90",
  "endereco": "Av. Paulista, 1000"
}
```

### 2. Criar Pessoa (`POST /pessoa`)
**Exemplo de Entrada:**
```json
{
  "nome": "Flavio Serafim",
  "cpf": "111.222.333-44",
  "email": "flavio.serafim@email.com",
  "empresaId": ____
}
```


### 3. Buscar Empresa por ID (`GET /empresas/{id}`)
**Objetivo:** Retornar os dados de uma empresa específica.
* **Saída Esperada:** Um array JSON com os objetos de empresa.

### 4. Listar Pessoas (`GET /pessoas`)
**Objetivo:** Listar todas as pessoas cadastradas no sistema.
* **Saída Esperada:** Um array JSON com os objetos de pessoa.

### 5. Listar Pessoas de uma Empresa (`GET /empresas/{id}/pessoas`)
**Objetivo:** Listar todos os colaboradores vinculados a uma empresa específica.
* **Saída Esperada:**
    * Receber o ID da empresa na URL.
    * Retornar a lista de pessoas que possuem o `empresaId` correspondente.


## 📦 Como Entregar

1.  Faça um **Fork** deste repositório.
2.  Desenvolva a solução no seu perfil do GitHub (o repositório deve ser **Público**).
3.  Envie o link do projeto finalizado para **[EMAIL DA EMPRESA]**.

> **Importante:** Não esqueça de atualizar o arquivo `README.md` do seu projeto explicando como rodar a aplicação.

    
