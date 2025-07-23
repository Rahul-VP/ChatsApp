# Quick Setup Guide

## Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- Cloudinary account (optional, for image uploads)

## Quick Start

1. **Install all dependencies:**
   ```bash
   npm run install:all
   ```

2. **Set up environment variables:**
   
   Create a `.env` file in the `backend` directory:
   ```env
   PORT=5001
   NODE_ENV=development
   MONGODB_URI=mongodb://localhost:27017/chat-app
   JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
   CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
   CLOUDINARY_API_KEY=your-cloudinary-api-key
   CLOUDINARY_API_SECRET=your-cloudinary-api-secret
   FRONTEND_URL=http://localhost:5173
   ```

3. **Start MongoDB** (if using local MongoDB)

4. **Seed the database with sample users:**
   ```bash
   npm run seed
   ```

5. **Start both frontend and backend:**
   ```bash
   npm run dev
   ```

6. **Open your browser and go to:** `http://localhost:5173`

## Sample Login Credentials

After running the seed script, you can login with any of these accounts:

**Female Users:**
- emma.thompson@example.com / 123456
- olivia.miller@example.com / 123456
- sophia.davis@example.com / 123456

**Male Users:**
- james.anderson@example.com / 123456
- william.clark@example.com / 123456
- benjamin.taylor@example.com / 123456

## Features Available

- ✅ User authentication (signup, login, logout)
- ✅ Real-time messaging with Socket.IO
- ✅ User profiles with avatars
- ✅ Image sharing in messages
- ✅ Dark/Light theme support
- ✅ Responsive design
- ✅ Online/offline status
- ✅ Message timestamps
- ✅ Profile management

## Troubleshooting

1. **MongoDB Connection Error:**
   - Make sure MongoDB is running
   - Check your MONGODB_URI in the .env file

2. **Port Already in Use:**
   - Change the PORT in .env file
   - Kill the process using the port

3. **Cloudinary Errors:**
   - Set up a free Cloudinary account
   - Add your credentials to .env file
   - Or remove image upload functionality temporarily

4. **Frontend Not Loading:**
   - Check if backend is running on port 5001
   - Check browser console for errors
   - Verify CORS settings in backend

## Development Commands

- `npm run dev` - Start both frontend and backend
- `npm run dev:backend` - Start only backend
- `npm run dev:frontend` - Start only frontend
- `npm run seed` - Seed database with sample users
- `npm run build` - Build frontend for production 