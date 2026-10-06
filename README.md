# websocket-chat-demo

Real-time chat application built with React, Node.js, and WebSocket. Supports multiple rooms, typing indicators, and message history.

![Chat Demo](https://via.placeholder.com/800x400?text=WebSocket+Chat+Demo)

## Features

- Real-time messaging with WebSocket
- Multiple chat rooms
- Typing indicators ("User is typing...")
- Online presence — see who's connected
- Message timestamps
- Auto-scroll to latest message
- Mobile responsive

## Tech Stack

**Frontend**
- React 18 + TypeScript
- Tailwind CSS
- Native WebSocket API

**Backend**
- Node.js + Express
- `ws` WebSocket library
- In-memory message store

## Getting Started

```bash
git clone https://github.com/madhuveeraprasath-a/websocket-chat-demo.git
cd websocket-chat-demo
```

**Start the server:**
```bash
cd server
npm install
npm start
# Server running on ws://localhost:8080
```

**Start the client:**
```bash
cd client
npm install
npm run dev
# App running on http://localhost:3000
```

## WebSocket Events

| Event | Direction | Description |
|---|---|---|
| `join` | Client → Server | Join a chat room |
| `message` | Client → Server | Send a message |
| `typing` | Client → Server | Typing indicator |
| `message` | Server → Client | Broadcast message to room |
| `presence` | Server → Client | User joined/left |
| `history` | Server → Client | Last 50 messages on join |

## Project Structure

```
websocket-chat-demo/
├── client/
│   ├── src/
│   │   ├── components/
│   │   │   ├── ChatRoom.tsx
│   │   │   ├── MessageList.tsx
│   │   │   ├── MessageInput.tsx
│   │   │   └── UserList.tsx
│   │   └── hooks/
│   │       └── useWebSocket.ts
└── server/
    ├── index.js
    └── rooms.js
```

## License

MIT
