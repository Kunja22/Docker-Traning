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

# Step 1 
install docker compose 
<img width="1905" height="941" alt="image" src="https://github.com/user-attachments/assets/fc84bff4-6089-414c-ad0f-2c5096b88326" />
<img width="1910" height="922" alt="image" src="https://github.com/user-attachments/assets/04cd1fa4-53a9-49a0-8ad0-b40670791292" />
# Step 2
docker compose file 
<img width="755" height="738" alt="image" src="https://github.com/user-attachments/assets/0283f4f4-211a-48d1-94a7-70469aa1ba5b" />
## Step 3 
Container is running
<img width="1813" height="913" alt="image" src="https://github.com/user-attachments/assets/c3edb8b2-7280-4393-96af-cd968357c534" />

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
<img width="1391" height="680" alt="image" src="https://github.com/user-attachments/assets/4c539d0c-4d24-44b9-b897-d86eb962b9bb" />



