# TaskFlow API

RESTful task management API built with **Node.js, Express and MongoDB (Mongoose)**, with unit and integration tests (**Jest, Supertest**) and a **GitHub Actions** CI pipeline.

## Run locally
```bash
npm install
# needs MongoDB running locally, or set MONGODB_URI
npm start
```

## Endpoints
| Method | Route | Description |
|---|---|---|
| GET | /health | Health check |
| GET | /api/tasks?status=&priority=&page=&limit= | List tasks (filter + pagination) |
| GET | /api/tasks/:id | Get one task |
| POST | /api/tasks | Create a task (validated) |
| PUT | /api/tasks/:id | Update a task |
| DELETE | /api/tasks/:id | Delete a task |

## Tests
```bash
npm test
```
Unit tests cover the validation logic; integration tests exercise every route through Supertest with the Mongoose model mocked, so no database is needed in CI.
