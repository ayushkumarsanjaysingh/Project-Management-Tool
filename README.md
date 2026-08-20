# Project Pocket

A small project management tool for learning full-stack basics. Users can sign up, log in, create projects, add tasks, mark tasks as done, and add comments.

## Requirements

- Node.js 18 or newer
- MongoDB running locally, or a MongoDB Atlas connection string

## Run it

1. Copy `backend/.env.example` to `backend/.env` and set `MONGO_URI` and `JWT_SECRET`.
2. Install dependencies from the project root:

```bash
npm install
npm run install-all
```

3. Start both servers:

```bash
npm run dev
```

Open `http://localhost:5173` in your browser. The API runs on `http://localhost:5000`.

## Main folders

- `backend/models`: simple MongoDB schemas
- `backend/routes`: login, projects, tasks, and comments endpoints
- `backend/server.js`: Express server setup
- `frontend/src/pages`: login and dashboard screens
- `frontend/src/components`: reusable project and task UI

## API notes

Protected endpoints expect `Authorization: Bearer <token>`. The frontend adds this token automatically after login.
