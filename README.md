# Recipe Book — MERN Stack

A responsive Recipe Book app built with React + Vite, Node.js, Express, MongoDB Atlas, and Mongoose.

## Features
- Add, list, view, edit, and delete recipes
- Search recipes by name or ingredients
- Category and cooking-time details
- Form validation and success/error messages
- Responsive layout
- Recipes are stored in MongoDB through a REST API

## Requirements
- Node.js 18+
- A MongoDB Atlas database (or local MongoDB)

## 1. Configure the backend
Open a terminal in this folder:

```bash
cd backend
```

Copy `.env.example` to `.env`, then add your MongoDB connection string:

```env
PORT=5000
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster-url>/recipebook?retryWrites=true&w=majority
CLIENT_URL=http://localhost:5173
```

In MongoDB Atlas, create a database user and allow your current IP address in Network Access. Keep your `.env` file private.

Install dependencies and start the API:

```bash
npm install
npm run dev
```

The API runs at `http://localhost:5000`.

## 2. Start the frontend
Open a second terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL Vite prints (usually `http://localhost:5173`).

## API endpoints
- `GET /api/recipes` — list recipes; optional `?search=` and `?category=`
- `GET /api/recipes/:id` — get one recipe
- `POST /api/recipes` — create a recipe
- `PUT /api/recipes/:id` — update a recipe
- `DELETE /api/recipes/:id` — delete a recipe
- `GET /api/health` — health check

## Notes
- The app requires a working MongoDB connection for recipe data.
- Do not commit `.env` or share your database credentials.
