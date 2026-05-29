# GerenciamentoPessoal

API REST para gerenciamento de tarefas pessoais desenvolvida com Spring Boot.

---

# Tecnologias Utilizadas

* Java
* Spring Boot
* Spring Web
* Spring Data JPA
* PostgreSQL
* Lombok
* Bean Validation

---

# Funcionalidades

A API permite:

* Listar tarefas
* Buscar tarefa por ID
* Criar tarefa
* Atualizar tarefa
* Deletar tarefa
* Validar dados enviados pelo cliente
* Tratar erros de forma personalizada

---

# URL Base da API

```http
http://localhost:8080
```

---

# Estrutura dos Endpoints

## Listar todas as tarefas

### GET

```http
GET /api/tarefas
```

### Resposta

```json
[
  {
    "id": 1,
    "titulo": "Estudar Spring Boot",
    "descricao": "Criar API REST",
    "concluida": false
  }
]
```

### Status HTTP

* 200 OK

---

## Buscar tarefa por ID

### GET

```http
GET /api/tarefas/{id}
```

### Exemplo

```http
GET /api/tarefas/1
```

### Status HTTP

* 200 OK
* 404 NOT FOUND

---

## Criar nova tarefa

### POST

```http
POST /api/tarefas
```

### Body JSON

```json
{
  "titulo": "Fazer compras",
  "descricao": "Comprar mantimentos para todo o mês",
  "concluida": false
}
```

### Status HTTP

* 201 CREATED
* 400 BAD REQUEST

---

## Atualizar tarefa

### PUT

```http
PUT /api/tarefas/{id}
```

### Exemplo

```http
PUT /api/tarefas/1
```

### Body JSON

```json
{
  "titulo": "Fazer compras atualizado",
  "descricao": "Comprar somente o que falta",
  "concluida": true
}
```

### Status HTTP

* 200 OK
* 400 BAD REQUEST
* 404 NOT FOUND

---

## Deletar tarefa

### DELETE

```http
DELETE /api/tarefas/{id}
```

### Exemplo

```http
DELETE /api/tarefas/1
```

### Status HTTP

* 204 NO CONTENT
* 404 NOT FOUND

---

# Tratamento de Erros

A API possui tratamento global de exceções para retornar mensagens mais amigáveis.

## Exemplo — Tarefa não encontrada

```json
{
  "mensagem": "Tarefa não encontrada"
}
```

## Exemplo — Validação

```json
{
  "mensagem": "O título é obrigatório"
}
```

---

# Validações Implementadas

Os seguintes campos são obrigatórios:

* titulo
* descricao
* concluida

---

# Testes da API

Os testes da API foram realizados utilizando:

* Postman

---

# Códigos HTTP Utilizados

| Código | Descrição             |
| ------ | --------------------- |
| 200    | OK                    |
| 201    | Created               |
| 204    | No Content            |
| 400    | Bad Request           |
| 404    | Not Found             |
| 500    | Internal Server Error |

---

# Arquitetura do Projeto

O projeto foi organizado utilizando arquitetura em camadas:

```text
controller
service
repository
model
dto
exception
```

---

# Autor

Marcelo Borges
