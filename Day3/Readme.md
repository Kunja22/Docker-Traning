# Docker Day 3 - Docker Networking

## 📌 Objective

Understand and implement Docker Networking to enable communication between containers.

---

## 📚 Topics Covered

* What is Docker Network
* Types of Docker Networks
* Creating a custom Docker network
* Connecting containers using a network
* Container communication using container names

---

## 🐳 Docker Network Types

1. **Bridge Network**

   * Default network created by Docker
   * Used for communication between containers on the same host

2. **Host Network**

   * Container shares the host’s networking stack
   * No network isolation

3. **None Network**

   * Container has no network access

4. **Overlay Network**

   * Used for communication between multiple Docker hosts

---

## ⚙️ Commands Used

### Check Docker Networks

```bash
docker network ls
```

### Create a Custom Network

```bash
docker network create my-network
```

### Run Container with Network

```bash
docker run -d --name container1 --network my-network nginx
```

```bash
docker run -d --name container2 --network my-network busybox
```

### Inspect Network

```bash
docker network inspect my-network
```

---

## 🔗 Container Communication Example

Containers inside the same network can communicate using container names.

Example:

```bash
ping container1
```

---

## 📂 Project Structure

```
Docker-Traning
 ├── Docker-day-1
 ├── Docker-day-2
 ├── Docker-day-3
 │   └── Docker Networking
 └── README.md
```

---

## ✅ Outcome

* Learned Docker networking basics
* Created custom Docker network
* Connected multiple containers
* Verified container communication

---
1. Bridge Network
   <img width="1796" height="468" alt="image" src="https://github.com/user-attachments/assets/2c2ff3fe-3c93-43da-a94d-4d07e72f0442" />
2. Deploy Bridge Network
   <img width="1771" height="987" alt="image" src="https://github.com/user-attachments/assets/d03bd743-c315-474f-8abe-115b241d7cd3" />
3. Host Network
   <img width="1892" height="634" alt="image" src="https://github.com/user-attachments/assets/7044f9d4-4c31-4602-afec-ac3588a0fc2e" />
4. Deploy Host Network
   <img width="1037" height="575" alt="image" src="https://github.com/user-attachments/assets/9af0941f-f377-470c-9205-f7b663673dc8" />
5. Create Custom Network
   <img width="1370" height="942" alt="image" src="https://github.com/user-attachments/assets/f86bf03c-7ab4-4f87-9051-ab974e9f51b8" />
6. Network can communicate with each other
    <img width="1370" height="942" alt="image" src="https://github.com/user-attachments/assets/a25c172f-8dee-4285-92b4-ef2292bd846c" />
   
## Kubernetes Microservice Flask Application

This project demonstrates how to build, containerize, and deploy a Flask-based microservice application using Docker and Kubernetes.

The application is packaged into a Docker container and deployed to a Kubernetes cluster using Kubernetes Deployment and Service resources.

Project Architecture

User Request → Kubernetes Service → Kubernetes Pod → Flask Application

The Kubernetes Service exposes the Flask microservice running inside a containerized Pod.

Technologies Used

Python (Flask)

Docker

Kubernetes

YAML Configuration

Project Structure
microservices-k8s
│
├── app.py
├── requirements.txt
├── Dockerfile
├── kubernetes.yaml
└── README.md
Step 1: Clone the Repository
git clone https://github.com/Kunja22/microservices-k8s.git
cd microservices-k8s


