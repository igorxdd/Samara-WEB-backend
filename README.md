# MyTasks Web

Projeto de gerenciamento de tarefas com backend em Node.js e frontend React.

## Visao geral

- API REST com autenticacao JWT
- API GraphQL com `Schema`, `Query` e `Mutation`
- Persistencia em MongoDB
- Relacionamento entre entidades `User` e `Task`

## Estrutura

- `backend/`: API, regras de negocio, models, rotas REST e GraphQL
- `frontend/`: aplicacao web

## Tecnologias

- Node.js + Express
- MongoDB + Mongoose
- JWT + bcryptjs
- GraphQL + Apollo Server
- React

## Como rodar

### Backend

```bash
cd backend
npm install
```

Crie o arquivo `backend/backend.env` com:

```env
MONGODB_URI=mongodb://localhost:27017/mytasks
JWT_SECRET=seu_segredo_forte_com_32_ou_mais_caracteres
PORT=5000
NODE_ENV=development
```

Inicie:

```bash
npm run dev
```

### Frontend

```bash
cd frontend
npm install
npm start
```

## Endpoints principais

### REST

- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/me`
- `GET /api/tasks`
- `POST /api/tasks`
- `PUT /api/tasks/:id`
- `PATCH /api/tasks/:id/complete`
- `PATCH /api/tasks/:id/reopen`
- `DELETE /api/tasks/:id`

### GraphQL

- `POST /graphql`

Exemplo:

```json
{
  "query": "query { me { id name email } }"
}
```

## Colecao Postman

Colecao pronta para apresentacao:

- `backend/postman/Colecao-Apresentacao-Samara.postman_collection.json`

## Objetivo academico

Atender os requisitos de backend da disciplina com:

- CRUD REST completo
- seguranca com JWT
- validacao de dados
- simplificacao com GraphQL
