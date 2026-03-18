 🚀 Docker Multi-Service Application (Day5)

This project demonstrates how to run a multi-container application using Docker Compose with:

🟢 Frontend (Nginx)

🔵 Backend (Node.js)

🟡 Database (MongoDB)

📁 Project Structure
Day5/
│── docker-compose.yml
│
├── backend/
│   ├── Dockerfile
│   ├── server.js
│   └── data/
│
├── frontend/
│   ├── Dockerfile
│   └── index.html

⚙️ Services Used
1️⃣ MongoDB

Image: mongo:latest

Port: 27017

2️⃣ Backend (Node.js)

Runs on port 5000

Simple HTTP server

3️⃣ Frontend (Nginx)

Serves static HTML

Runs on port 5173
