# Chat Application

## Overview
This is a real-time chat application built using HTML, CSS (Tailwind CSS), JavaScript, Node.js, Express.js, and Socket.io. Users can join the chat, send messages, view active users, and leave the chat anytime.

## Features
- User can join the chat by entering their name.
- Messages are displayed in real-time using WebSockets (Socket.io).
- Active users list is dynamically updated.
- Users can send emoji messages using `emojionearea`.
- Messages have timestamps.
- Users can leave the chat, and their departure is announced.

## Technologies Used
- **Frontend**: HTML, Tailwind CSS, JavaScript, EmojioneArea, Socket.io Client
- **Backend**: Node.js, Express.js, Socket.io Server

## Installation and Setup
### Prerequisites
- Node.js and npm installed on your system.

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/chat-app.git
   cd chat-app
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node server.js
   ```
4. Open the application in a browser:
   ```sh
   http://localhost:9000
   ```

## File Structure
```
chat-app/
│-- public/
│   ├── index.html  # Frontend UI
│   ├── styles.css  # (If any custom styles)
│   ├── script.js   # Client-side JavaScript
│-- server.js       # Node.js Server
│-- package.json    # Project dependencies
│-- README.md       # Documentation
```

## How It Works
### Frontend (index.html & script.js)
- The chat interface allows users to enter their names and join the chat.
- Messages are sent and received using `socket.emit()` and `socket.on()`.
- Active users list is updated dynamically when a user joins or leaves.
- Emojis can be added using the `emojionearea` plugin.

### Backend (server.js)
- Express.js serves the frontend files.
- Socket.io handles real-time communication between clients.
- When a user joins, their name is broadcasted to all users.
- Messages are transmitted in real-time.
- Active users are managed using a `Set` to avoid duplicates.
- Users leaving the chat are removed from the active users list.

## Socket.io Events
| Event Name     | Description |
|---------------|-------------|
| `join`        | A user joins the chat. |
| `user-message` | A user sends a message. |
| `leave`       | A user leaves the chat. |
| `disconnect`  | A user disconnects (e.g., closes the tab). |
| `update-users`| Updates and displays the active users list. |
| `message`     | Receives and displays messages. |

## Future Improvements
- Private messaging feature.
- User authentication (login/logout).
- Message history storage using a database.
- UI enhancements for better UX.

## License
This project is open-source. Feel free to modify and improve it!

---
### Author: Gulam Kadir

