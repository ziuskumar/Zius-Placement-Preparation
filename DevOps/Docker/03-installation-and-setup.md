# 💻 Docker Installation & Setup

## 📌 Why Install Docker?

Docker lets you **build, run, and manage containers** on your system.

---

## 🖥️ System Requirements

✅ Windows 10/11 (64-bit)

✅ macOS

✅ Linux (Ubuntu, Fedora, etc.)

---

## 📥 Installation Steps

### 🪟 Windows

1. Download **Docker Desktop**
2. Install it
3. Enable **WSL 2**
4. Restart PC
5. Launch Docker Desktop

---

### 🐧 Linux (Ubuntu)

```bash
sudo apt update
sudo apt install docker.io
```

Start Docker:

```bash
sudo systemctl start docker
```

Enable on Boot:

```bash
sudo systemctl enable docker
```

---

## ✅ Verify Installation

Check Docker Version

```bash
docker --version
```

Example Output

```text
Docker version 28.x.x
```

---

Check Docker Info

```bash
docker info
```

Shows:

- Docker Engine
- Containers
- Images
- Storage Driver

---

## 🚀 First Docker Command

Run:

```bash
docker run hello-world
```

Output:

```text
Hello from Docker!
This message shows that your installation appears to be working correctly.
```

🎉 Congratulations! Docker is installed successfully.

---

## 📂 Check Running Containers

```bash
docker ps
```

---

## 📂 Check All Containers

```bash
docker ps -a
```

---

## 🖼️ Check Images

```bash
docker images
```

---

## 🎯 Interview Keywords

- 🐳 Docker Desktop
- ⚙️ Docker Engine
- 🐧 WSL 2
- 📦 hello-world
- 🖥️ docker --version
- 📋 docker info

---

## ❌ Common Mistakes

❌ Docker Desktop not running.

✅ Start Docker Desktop before executing commands.

---

❌ Forgetting to enable WSL 2 (Windows).

✅ Enable WSL 2 before installation.

---

## 🔥 Interview Traps

### ❓How do you verify Docker is installed?

```bash
docker --version
```

---

### ❓Which command tests Docker installation?

```bash
docker run hello-world
```

---

### ❓How to list Docker Images?

```bash
docker images
```

---

### ❓How to list Running Containers?

```bash
docker ps
```

---

## ⚡ Quick Revision

📌 Install Docker Desktop / docker.io

📌 Verify → `docker --version`

📌 Test → `docker run hello-world`

📌 Images → `docker images`

📌 Running Containers → `docker ps`

📌 All Containers → `docker ps -a`