API
retorna a estrutura de dados conforme o cliente solicita;

Metodos HTTP

- GET - busca algo
- POST - cria algo
- PUT/PATH - atualiza algo put(varios dados) path(unico dado)
- DELETE - deleta algo

Benefícios

- Múltiplos clientes (front-end e back-end)
- Protocolo de comunicação padronizado
- Mesma estrutura web e mobile
- Comunicação com serviços externos

Params / Query Params / Body

GET - http://api.com/company/1/users?page=2

1 - Route Params
?page=2 - Query Params

###

{
"USER": {

      "name": "Fulano de Tal"
       }

}

{ } = Body

Http codes

- 1xx - Informational
- 2xx - Success

  - 200: success
  - 201: created

- 3xx Redirection

  - 301: moved permanently
  - 302: moed

- 4xx Client Error

  - 400: bad request
  - 401: unauthorized
  - 404: not found

- 5xx Server error
  - 500 internal server error

---

Query params: Filtros e paginação

insomnia - http://localhost:3333/projects?title=React&owner=Diego

backend - const { title, owner } = request.query

Route Params: Identificador de recursos

insomnia = http://localhost:3333/projects/:id

backend - const { id } = request.params

Request Body - Conteudo para criar ou editar um recurso (JSON)

insomnia - {
"title": "aplicativo",
"description": "descricao do app"
}

backend - const { title, description } = request.body;
