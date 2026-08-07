# 🖼️ Images vs 📦 Containers

## 📌 What is a Docker Image?

A **Docker Image** is a **read-only blueprint** used to create containers.

Think of it as 📸 a **Class** or **Template**.

Examples:

- nginx
- ubuntu
- node
- mysql

---

## 📌 What is a Docker Container?

A **Container** is a **running instance** of an Image.

Think of it as 🏠 an **Object** created from a Class.

---

## ⚙️ Workflow

```
Dockerfile
     │
     ▼
🖼️ Image
     │
docker run
     │
     ▼
📦 Container
```

---

## 📊 Image vs Container

| 🖼️ Image | 📦 Container |
|-----------|-------------|
| Blueprint | Running Instance |
| Read-only | Read & Write |
| Static | Dynamic |
| Cannot Execute | Executes Application |
| Creates Containers | Created from Image |

---

## 🌍 Real-Life Example

🎂 **Image = Cake Recipe**

🍰 **Container = Prepared Cake**

👉 One recipe can make many cakes.

👉 One Image can create multiple Containers.

---

## 💻 Commands

### 📥 Download an Image

```bash
docker pull nginx
```

---

### 🖼️ View Images

```bash
docker images
```

---

### 🚀 Run a Container

```bash
docker run nginx
```

---

### 📦 View Running Containers

```bash
docker ps
```

---

## 🎯 Interview Keywords

- 🖼️ Image
- 📦 Container
- Blueprint
- Instance
- Read-only
- Running Process

---

## ❌ Common Mistakes

❌ Image is Running

✅ Container is Running.

---

❌ Container creates Image.

✅ Image creates Container.

---

## 🔥 Interview Traps

### ❓Can one Image create multiple Containers?

✅ Yes

---

### ❓Can a Container exist without an Image?

❌ No

---

### ❓Is an Image executable?

❌ No

---

### ❓What is actually running?

✅ Container

---

## ⚡ Quick Revision

📌 Image = Blueprint 🖼️

📌 Container = Running Image 📦

📌 Image → Read-only

📌 Container → Read & Write

📌 One Image ➜ Multiple Containers

📌 `docker pull` → Download Image

📌 `docker run` → Create & Start Container

📌 `docker images` → List Images

📌 `docker ps` → List Running Containers