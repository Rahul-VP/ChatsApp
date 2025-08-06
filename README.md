# Fullstack ChatsApp

A real-time chat application built with React, Node.js, Express, MongoDB, and Socket.IO.

## Features

- 🔐 User authentication (signup, login, logout)
- 💬 Real-time messaging with Socket.IO
- 👥 User profiles with avatars
- 🖼️ Image sharing in messages
- 🌙 Dark/Light theme support
- 📱 Responsive design
- 🔒 JWT-based authentication
- ☁️ Cloudinary integration for image uploads

## Tech Stack

### Frontend
- React 18
- Vite
- Tailwind CSS
- DaisyUI
- Zustand (State Management)
- Socket.IO Client
- Axios
- React Router DOM
- React Hot Toast

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- Socket.IO
- JWT Authentication
- bcryptjs for password hashing
- Cloudinary for image uploads
- CORS enabled

## Prerequisites

- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- Cloudinary account (for image uploads)

## Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd fullstack-chat-app
```

### 2. Backend Setup

```bash
cd backend
npm install
```
### 3. Frontend Setup

```bash
cd frontend
npm install
```

### 4. Database Setup

Start MongoDB and run the seed script to populate with sample users:
```bash
cd backend
npm run seed
```

### Development Mode

1. Start the backend server:
```bash
cd backend
npm run dev
```

2. Start the frontend development server:
```bash
cd frontend
npm run dev
```

3. Open your browser and navigate to `http://localhost:5173`

### Production Mode

1. Build the frontend:
```bash
cd frontend
npm run build
```

2. Start the backend server:
```bash
cd backend
npm start
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/check` - Check authentication status
- `PUT /api/auth/update-profile` - Update user profile

### Messages
- `GET /api/messages/users` - Get all users for sidebar
- `GET /api/messages/:id` - Get messages with a specific user
- `POST /api/messages/send/:id` - Send a message to a user

## Socket.IO Events

- `connection` - User connects to socket
- `disconnect` - User disconnects from socket
- `getOnlineUsers` - Broadcast online users
- `newMessage` - Send new message to receiver

## Project Structure

```
fullstack-chat-app/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── auth.controller.js
│   │   │   └── message.controller.js
│   │   ├── lib/
│   │   │   ├── cloudinary.js
│   │   │   ├── db.js
│   │   │   ├── socket.js
│   │   │   └── utils.js
│   │   ├── middleware/
│   │   │   └── auth.middleware.js
│   │   ├── models/
│   │   │   ├── message.model.js
│   │   │   └── user.model.js
│   │   ├── routes/
│   │   │   ├── auth.route.js
│   │   │   └── message.route.js
│   │   ├── seeds/
│   │   │   └── user.seed.js
│   │   └── index.js
│   ├── package.json
│   └── start.js
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── AuthImagePattern.jsx
│   │   │   ├── ChatContainer.jsx
│   │   │   ├── ChatHeader.jsx
│   │   │   ├── MessageInput.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── NoChatSelected.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   └── skeletons/
│   │   ├── constants/
│   │   │   └── index.js
│   │   ├── lib/
│   │   │   ├── axios.js
│   │   │   └── utils.js
│   │   ├── pages/
│   │   │   ├── HomePage.jsx
│   │   │   ├── LoginPage.jsx
│   │   │   ├── ProfilePage.jsx
│   │   │   ├── SettingsPage.jsx
│   │   │   └── SignUpPage.jsx
│   │   ├── store/
│   │   │   ├── useAuthStore.js
│   │   │   ├── useChatStore.js
│   │   │   └── useThemeStore.js
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
└── README.md
```
