# Flashcard Leitner System

A full-stack application for managing flashcards using the Leitner system, built with React (Vite) frontend and Express.js backend.
---

## 🔑 Demo Credentials
To try the app, use the following credentials:  
- **Username:** `mukul`  
- **Password:** `mukul`  

---
## Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- Git

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/mukulgupta11/Flashcard-learning-using-Leitner-system
   ```

2. Install dependencies for both client and server:
   ```bash
   cd client && npm install
   cd ../server && npm install
   ```

## Environment Variables

Create a `.env` file in the server directory with the following variables:
```
MONGO_URI=mongodb+srv://sruti26psty:XlcWyCq7kz55dsWR@cluster0.iqqez.mongodb.net/
PORT=5001
JWT_SECRET=secret123
```

## Running the Application

### Client (Frontend)
1. Navigate to the client directory:
   ```bash
   cd client
   ```
2. Start the development server:
   ```bash
   npm run dev
   ```
3. The application will be available at `http://localhost:5173`

### Server (Backend)
1. Navigate to the server directory:
   ```bash
   cd server
   ```
2. Start the development server:
   ```bash
   npm run dev
   ```
3. The API will be available at `http://localhost:5000`

---

## 🎯 Leitner System Logic
- **Flashcards start at Level 0**.
- **If answered correctly**, they move to the next level (up to Level 4).
- **If answered incorrectly**, they go back to Level 0.
- **Higher levels have longer review intervals**:
  - **Level 0 → 1 day**
  - **Level 1 → 2 days**
  - **Level 2 → 4 days**
  - **Level 3 → 7 days**
  - **Level 4 → 14 days**
- Flashcards are fetched **based on their next review date**.

---

## 📌 API Endpoints (Backend)
| Method | Endpoint             | Description |
|--------|----------------------|-------------|
| **POST**   | `/api/flashcards`        | Add a new flashcard |
| **GET**    | `/api/flashcards`        | Get all due flashcards |
| **PUT**    | `/api/flashcards/:id`    | Update a flashcard level |
| **DELETE** | `/api/flashcards/:id`    | Delete a flashcard |

---

## 🎨 UI Features (Frontend)
- **Show Answer Button** – Reveals the answer.
- **"Got it Right" / "Got it Wrong" Buttons** – Updates flashcard progress.
- **Due Flashcards Count** – Displays how many flashcards are due for review.
- **Minimalist UI** – Simple, clean, and distraction-free.



## Technologies Used

### Frontend
- React
- Vite
- TailwindCSS
- Material UI
- Axios

### Backend
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- Bcrypt for password hashing

