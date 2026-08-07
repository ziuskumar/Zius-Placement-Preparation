# 🏗️ Docker Architecture

## 📌 What is Docker Architecture?

Docker Architecture defines **how Docker works internally** to build, manage, and run containers.

👉 It follows a **Client-Server Architecture**.

---

## 🧩 Components

### 👨‍💻 1. Docker Client

- Used by developers.
- Accepts Docker commands.
- Sends requests to Docker Daemon.

Examples:

```bash
docker build
docker run
docker pull
docker ps
```

---

### ⚙️ 2. Docker Daemon (dockerd)

- Core of Docker 🚀
- Builds Images
- Creates Containers
- Manages Networks
- Manages Volumes

👉 It listens for requests from the Docker Client.

---

### 📦 3. Docker Images

- Read-only template.
- Used to create containers.
- Stored locally or on Docker Hub.

Think of it as 📸 **Blueprint**.

---

### 📂 4. Docker Containers

- Running instance of an Image.
- Lightweight and isolated.

Think of it as 🏠 **Actual House built from the Blueprint.**

---

### ☁️ 5. Docker Registry

Stores Docker Images.

Example:

- Docker Hub
- AWS ECR
- Azure Container Registry

---

## ⚙️ Workflow

```text
👨‍💻 Docker Client
        │
 docker run
        │
        ▼
⚙️ Docker Daemon
        │
Pull/Build Image
        │
        ▼
🖼️ Docker Image
        │
Create
        ▼
📦 Docker Container
```

---

## 🌍 Real-Life Example

You run:

```bash
docker run nginx
```

✅ Docker Client sends request

⬇️

✅ Docker Daemon checks Image

⬇️

❌ Not Found?

⬇️

☁️ Downloads from Docker Hub

⬇️

📦 Creates & Starts Container

---

## 🎯 Interview Keywords

- 👨‍💻 Docker Client
- ⚙️ Docker Daemon
- 📦 Container
- 🖼️ Image
- ☁️ Docker Hub
- 📂 Registry
- Client-Server Architecture

---

## ❌ Common Mistakes

❌ Client creates Containers

✅ Daemon creates Containers.

---

❌ Image is Running

✅ Container is Running.

---

## 🔥 Interview Traps

### ❓Who creates Containers?

👉 Docker Daemon

---

### ❓Who accepts Docker commands?

👉 Docker Client

---

### ❓Where are Images stored?

👉 Docker Registry (Docker Hub)

---

### ❓Can Docker work without Daemon?

❌ No

---

## ⚡ Quick Revision

📌 Docker follows Client-Server Architecture

👨‍💻 Client → Sends Commands

⚙️ Daemon → Executes Commands

🖼️ Image → Blueprint

📦 Container → Running Image

☁️ Docker Hub → Stores Images