# Task Manager

A full-stack task manager app with user authentication and task CRUD.
## Features

* JWT Authentication
* MongoDB Atlas Cloud Database
* Create, Update, Delete Tasks
* Mark Tasks as Completed/Pending
* Real-Time Task Search
* User-Specific Task Management

## Project Structure

```text
taskmanager/
  backend/    Express API, MongoDB models, auth middleware
  frontend/   React app
```
  ## Prerequisites

* Node.js and npm
* MongoDB Atlas account
* MongoDB Atlas cluster
* MongoDB Atlas database user
* MongoDB Atlas connection string


## Backend Setup

1. Open a terminal in the backend folder:

```bash
cd backend
```

2. Install dependencies:

```bash
npm install
```

3. Create `backend/.env`:

```env
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/taskmanager?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret
PORT=5000
```

> This project uses MongoDB Atlas (Cloud Database). Create a cluster, database user, and whitelist your IP address before running the backend.


4. Start the API server:

```bash
npm start
```

The backend runs on `http://localhost:5000`.

## Frontend Setup

1. Open another terminal in the frontend folder:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the React app:

```bash
npm start
```

The frontend runs on `http://localhost:3000`.

## API Routes

Auth:

- `POST /api/auth/register`
- `POST /api/auth/login`

Tasks:

- `GET /api/tasks`
- `POST /api/tasks`
- `PUT /api/tasks/:id`
- `DELETE /api/tasks/:id`

Task routes require an `Authorization: Bearer <token>` header.

## Useful Commands

Backend:

```bash
cd backend
npm start
```

Frontend:

```bash
cd frontend
npm start
npm run build
```

## Notes

- Keep real `.env` values private and do not commit them.
- The frontend currently calls the API at `http://localhost:5000`.
- The backend `dev` script uses `nodemon`; install it before running `npm run dev`.
