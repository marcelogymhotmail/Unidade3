# GerenciamentoPessoal

A API permite:

- Listar tarefas
- Buscar tarefa por ID
- Criar tarefa
- Atualizar tarefa
- Deletar tarefa


http://localhost:8080


---

# Endpoints da API

## Listar todas as tarefas

### GET

http
GET /api/tarefas


---

## Buscar tarefa por ID

### GET

http
GET /api/tarefas/{id}


---

## Criar nova tarefa

### POST

http
POST /api/tarefas


### Body JSON

json
{
  "titulo": "Fazer compras",
  "descricao": "Comprar mantimentos para todo o mes",
  "concluida": false
}


---

## Atualizar tarefa

### PUT

http
PUT /api/tarefas/{id}


### Body JSON

json
{
  "titulo": "",Fazer compras atualizado
  "descricao": "Comprar somente o que falta",
  "concluida": true
}


---

## Deletar tarefa

### DELETE

http
DELETE /api/tarefas/{id}


---

# Testes

Os testes da API foram realizados utilizando:

- Postman

## Status HTTP utilizados

| Código | Descrição |
| 200 | OK |
| 201 | Created |
| 204 | No Content |
| 404 | Not Found |

---

# Autor

Marcelo Borges
