# Minimal MERN Task Manager

Minimal Task Management app with:

- Backend: Node.js + Express + MongoDB (Mongoose)
- Frontend: React + Vite
- One model: `Task` (`title`, `description`, `status`)
- CRUD APIs + simple task UI

## Project Structure

```text
/server
/client
```

## 1) Backend Setup (`/server`)

1. Go to the server folder:
   ```bash
   cd server
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create `.env` from and set credentials:
   ```env
   PORT=5000
   MONGODB_URI=<mongodb-srv-string> can be found in your mongoDB Atlas account
   ```
4. Run backend:
   ```bash
   node index.js
   ```

Backend runs at `http://localhost:5000`.

## 2) Frontend Setup (`/client`)

1. Open a second terminal, then:
   ```bash
   cd client
   ```
2. Install dependencies:
   ```bash
   npm install
   npm run build
   ```
3. Create `.env`:
   ```env
   VITE_API_URL=http://localhost:5000/api
   ```
4. Run frontend:
   ```bash
   node index.js
   ```

Frontend runs at `http://localhost:5173`.

## API Endpoints

Base URL: `http://localhost:5000/api/tasks`

- `POST /` - Create task
- `GET /` - Get all tasks
- `PUT /:id` - Update task
- `DELETE /:id` - Delete task

## Notes

- `status` accepts only `pending` or `completed`.
- Uses `axios` for frontend API calls.
