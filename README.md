# DevSync

This project is a **Real-time Collaborative Code Editor** built using **React** and **Socket.IO**. It allows multiple users to join a room, collaborate on code in real-time, and sync their code changes across all connected clients.

## Features

- Real-time collaborative code editing with multiple users.
- Syntax highlighting and intelligent editor behavior using **Codemirror**.
- Automatic syncing of code changes across all connected clients.
- Ability to copy Room ID and invite others to collaborate.
- Join and leave rooms with notifications for all users.
- Built-in error handling for socket connections.

## Tech Stack

- **Frontend**: React, Codemirror for the editor, React Hot Toast for notifications, React Router DOM for navigation.
- **Backend**: Node.js, Express.js, Socket.IO for real-time communication.
- **Dev Tools**: Concurrently for running both frontend and backend servers, Nodemon for automatic server restart during development.

## Installation and Setup Instructions

1. **Clone the repository**

    ```bash
    git clone https://github.com/your-username/realtime-code-editor.git
    cd realtime-code-editor
    ```

2. **Install dependencies**

    Install both frontend and backend dependencies:

    ```bash
    npm install
    ```

3. **Start the development servers**

    You can run both the frontend and backend concurrently with the following command:

    ```bash
    npm run dev
    ```

    This will start the frontend React app at [http://localhost:3000](http://localhost:3000) and the backend server at [http://localhost:5000](http://localhost:5000).

4. **Create a room**

    Once the app is running, go to the homepage and either paste an existing Room ID or click "Create new room". Share the Room ID with others to collaborate.

5. **Join a room**

    You can enter a Room ID and your username to join an existing room.

## Project Structure

- `server.js`: The backend server using Express and Socket.IO.
- `src/pages/EditorPage.js`: The main page where the code editor and client list is rendered.
- `src/pages/Home.js`: The home page where users can create or join a room.
- `src/components/Client.js`: Displays a connected user with their avatar.
- `src/components/Editor.js`: The Codemirror-based code editor.
- `src/socket.js`: Initializes and manages Socket.IO connections.
- `src/Actions.js`: Contains constants for socket events (JOIN, CODE_CHANGE, etc.).

## Scripts

- **Start the app**: `npm run dev`
- **Start only frontend**: `npm run start:front`
- **Start only backend**: `npm run start:back`
- **Build the frontend**: `npm run build`

## Dependencies

### Core Dependencies

- **React**: Frontend framework.
- **Socket.IO**: Real-time communication.
- **Codemirror**: Code editor library with syntax highlighting.
- **React Hot Toast**: For notification toasts.
- **UUID**: For generating unique Room IDs.

### Dev Dependencies

- **Nodemon**: Automatically restarts the Node.js server when files change.
- **Concurrently**: Runs both the frontend and backend servers simultaneously in development mode.

## License

This project is licensed under the MIT License.

