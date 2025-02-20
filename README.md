# Flashcard Leitner System

A full-stack application for managing flashcards using the Leitner system, built with React (Vite) frontend and Express.js backend.

## Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- Git

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/flashcard-leitner-system.git
   cd flashcard-leitner-system
   ```

2. Install dependencies for both client and server:
   ```bash
   cd client && npm install
   cd ../server && npm install
   ```

## Environment Variables

Create a `.env` file in the server directory with the following variables:
```
MONGO_URI=mongodb://localhost:27017/flashcards
JWT_SECRET=your_jwt_secret_key
PORT=5000
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

## Project Structure

```
.
├── client/              # React frontend
│   ├── public/           # Static assets
│   ├── src/              # Application source code
│   │   ├── components/   # React components
│   │   ├── pages/        # Page components
│   │   ├── services/     # API services
│   │   └── ...          # Other source files
├── server/               # Express backend
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/           # Mongoose models
│   ├── routes/           # API routes
│   └── server.js         # Main server file
```

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

