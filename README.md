# 💬 Real-Time Chat Application

<div align="center">

![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-4.7.5-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-8.20.1-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

A full-stack real-time chat application with instant messaging, multiple rooms, reactions, and typing indicators.

### 🌐 Live Demo

**Frontend (Client):** [https://your-app-name.netlify.app](https://your-app-name.netlify.app)  
**Backend (Server):** [https://your-server-name.onrender.com](https://your-server-name.onrender.com)

---

[Features](#-features) • [Installation](#-installation) • [API](#-api-documentation)

</div>


---

## 📸 Screenshots

<div align="center">

### Login Screen
<img src="./client/public/screenshots/login.png" alt="Login Screen" width="600"/>

### Chat with Typing Indicator
<img src="./client/public/screenshots/chat-typing.png" alt="Chat with Typing" width="600"/>

### Active Chat Room
<img src="./client/public/screenshots/chat-room.png" alt="Chat Room" width="600"/>

</div>

---

## ✨ Features

- ✅ Real-time messaging with WebSocket
- ✅ Multiple chat rooms (create, join, switch)
- ✅ User authentication with avatars
- ✅ Typing indicators
- ✅ Message reactions (👍 ❤️ 😂 😮 😢 🔥)
- ✅ Message editing and deletion
- ✅ Private messaging
- ✅ Online user list
- ✅ Message search
- ✅ Dark/Light theme
- ✅ MongoDB persistence
- ✅ Responsive design

---

## 🛠 Tech Stack

**Frontend:** React 18, Vite, Socket.io Client  
**Backend:** Node.js, Express, Socket.io, MongoDB, Mongoose  
**Hosting:** Render (backend), Netlify (frontend)

---

## 📦 Installation

### Prerequisites

- Node.js 18+ ([Download](https://nodejs.org/))
- MongoDB (local or [Atlas](https://www.mongodb.com/cloud/atlas))
- Git

### Setup

**1. Clone Repository**
```bash
git clone https://github.com/PLP-MERN-Stack-Development/real-time-communication-with-socket-io-ErikWambua.git
cd real-time-communication-with-socket-io-ErikWambua
```

**2. Server Setup**
```bash
cd server
npm install
```

Create `server/.env`:
```env
PORT=5000
CLIENT_URL=http://localhost:5173
MONGODB_URI=mongodb://localhost:27017/chat-app
```

**3. Client Setup**
```bash
cd client
npm install
```

Create `client/.env`:
```env
VITE_SOCKET_URL=http://localhost:5000
```

**4. Run Application**

Terminal 1 (Server):
```bash
cd server
npm run dev
```

Terminal 2 (Client):
```bash
cd client
npm run dev
```

Access: http://localhost:5173

---

## 🔧 API Documentation

### REST Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/health` | Server health check |
| GET | `/api/messages/:roomId` | Get message history |
| GET | `/api/users` | Get online users |
| GET | `/api/rooms` | Get all rooms |

### Socket Events

**Client → Server:**
- `user_join` - Join chat
- `send_message` - Send message
- `typing` - Typing status
- `create_room` - Create room
- `join_room` - Join room
- `message_reaction` - Add reaction

**Server → Client:**
- `receive_message` - New message
- `user_list` - Online users
- `typing_users` - Who's typing
- `room_list` - Available rooms
- `message_history` - Room history

---

## 🏗 Project Structure

```
├── client/
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── socket/        # Socket.io config
│   │   └── context/       # Theme context
│   └── package.json
├── server/
│   ├── models/            # MongoDB models
│   ├── server.js          # Main server
│   └── package.json
└── screenshots/           # App screenshots
```

---

## 🚨 Troubleshooting

**Connection Issues:**
- Check server is running on correct port
- Verify environment variables
- Check CORS settings

**Messages Not Sending:**
- Ensure WebSocket connection is active
- Check browser console for errors
- Verify you're in the same room

**MongoDB Connection Failed:**
- Check MongoDB is running
- Verify connection string
- Whitelist IP in Atlas

---

## 📞 Contact

**Developer:** Erik Wambua  
**GitHub:** [@ErikWambua](https://github.com/ErikWambua)  
**Repository:** [View on GitHub](https://github.com/PLP-MERN-Stack-Development/real-time-communication-with-socket-io-ErikWambua)

---

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

---

<div align="center">

**Built with ❤️ using React, Socket.io, and MongoDB**

</div> 