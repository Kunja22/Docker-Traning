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


