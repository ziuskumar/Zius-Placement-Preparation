# ⚡ Essential Docker Commands

## 📌 Why Learn Docker Commands?

Docker is mostly used through the **CLI (Command Line Interface)**.

🎯 These are the commands asked most often in interviews and used in real projects.

---

# 📥 Image Commands

### 🔹 Download an Image

```bash
docker pull nginx
```

📌 Downloads an image from Docker Hub.

---

### 🔹 View Images

```bash
docker images
```

📌 Lists all downloaded images.

---

### 🔹 Remove an Image

```bash
docker rmi nginx
```

📌 Deletes an image.

---

# 📦 Container Commands

### 🔹 Create & Start a Container

```bash
docker run nginx
```

📌 Creates a new container and starts it.

---

### 🔹 List Running Containers

```bash
docker ps
```

📌 Shows active containers.

---

### 🔹 List All Containers

```bash
docker ps -a
```

📌 Shows running + stopped containers.

---

### 🔹 Stop a Container

```bash
docker stop <container-id>
```

📌 Stops a running container.

---

### 🔹 Start a Container

```bash
docker start <container-id>
```

📌 Starts a stopped container.

---

### 🔹 Restart a Container

```bash
docker restart <container-id>
```

📌 Restarts the container.

---

### 🔹 Remove a Container

```bash
docker rm <container-id>
```

📌 Deletes a stopped container.

---

# 📋 Information Commands

### 🔹 Docker Version

```bash
docker --version
```

---

### 🔹 Docker Information

```bash
docker info
```

---

### 🔹 View Logs

```bash
docker logs <container-id>
```

---

### 🔹 Execute Command Inside Container

```bash
docker exec -it <container-id> bash
```

📌 Opens a terminal inside the container.

---

# 🎯 Most Important Commands ⭐

| Command | Purpose |
|---------|---------|
| `docker pull` | Download Image |
| `docker run` | Create & Start Container |
| `docker ps` | Running Containers |
| `docker ps -a` | All Containers |
| `docker images` | List Images |
| `docker stop` | Stop Container |
| `docker start` | Start Container |
| `docker restart` | Restart Container |
| `docker rm` | Delete Container |
| `docker rmi` | Delete Image |
| `docker logs` | View Logs |
| `docker exec` | Enter Container |

---

# ❌ Common Mistakes

❌ `docker rm` removes Images.

✅ It removes **Containers**.

---

❌ `docker rmi` removes Containers.

✅ It removes **Images**.

---

# 🔥 Interview Traps

### ❓Difference between `docker run` and `docker start`?

✅ `docker run` → Creates + Starts a new container.

✅ `docker start` → Starts an existing stopped container.

---

### ❓How to see all containers?

```bash
docker ps -a
```

---

### ❓How to enter a running container?

```bash
docker exec -it <container-id> bash
```

---

### ❓How to see container logs?

```bash
docker logs <container-id>
```

---

# ⚡ Quick Revision

📥 `docker pull` → Download Image

🚀 `docker run` → Create & Start

📦 `docker ps` → Running Containers

📋 `docker ps -a` → All Containers

🖼️ `docker images` → List Images

🛑 `docker stop` → Stop

▶️ `docker start` → Start

🔄 `docker restart` → Restart

🗑️ `docker rm` → Delete Container

🗑️ `docker rmi` → Delete Image

📄 `docker logs` → View Logs

💻 `docker exec` → Enter Container