# ⚖️ Load Balancer

---

# 📖 Introduction

As the number of users increases, a single server cannot handle all requests efficiently. A **Load Balancer** distributes incoming traffic across multiple servers to improve performance, availability, and reliability.

It is one of the most important components in modern System Design.

---

# 📌 Definition

> **A Load Balancer is a device or software that distributes incoming client requests across multiple servers to ensure no single server becomes overloaded.**

---

# ❓ Why Do We Need a Load Balancer?

Without a Load Balancer:

- Server overload
- Slow response time
- Single Point of Failure (SPOF)
- Poor user experience

With a Load Balancer:

- Even traffic distribution
- Better performance
- High availability
- Fault tolerance

---

# ⚙️ How It Works

```text
        Users
          │
          ▼
    Load Balancer
     ┌────┼────┐
     ▼    ▼    ▼
 Server1 Server2 Server3
```

The Load Balancer receives all requests and forwards them to the most suitable server.

---

# 📊 Load Balancing Algorithms

### 1. Round Robin

Requests are distributed one after another.

```text
Request 1 → Server 1
Request 2 → Server 2
Request 3 → Server 3
Request 4 → Server 1
```

---

### 2. Least Connections

The server with the fewest active connections receives the next request.

---

### 3. IP Hash

The client's IP determines which server handles the request.

---

# 🌍 Real-World Example

### Netflix

Millions of users watch videos simultaneously.

A Load Balancer distributes requests across multiple streaming servers, ensuring smooth playback even during peak hours.

---

# 📈 Advantages

- Better performance
- High availability
- Fault tolerance
- Scalability
- No server overload

---

# 📉 Disadvantages

- Additional infrastructure cost
- Configuration complexity
- Can become a bottleneck if not redundant

---

# 🎯 Interview Keywords

- Load Balancer
- Round Robin
- Least Connections
- High Availability
- Scalability
- Fault Tolerance

---

# ⚠️ Common Mistakes

❌ Assuming one server is enough.

❌ Forgetting health checks.

❌ Using only one Load Balancer without backup.

---

# 🔥 Interview Questions

### ❓ What is a Load Balancer?

A component that distributes incoming traffic across multiple servers.

---

### ❓ Why is it used?

To improve availability, scalability, and performance.

---

### ❓ Name some Load Balancing algorithms.

- Round Robin
- Least Connections
- IP Hash

---

### ❓ Does a Load Balancer increase system availability?

Yes. If one server fails, traffic is redirected to healthy servers.

---

# 💡 Best Practices

- Use health checks.
- Deploy redundant Load Balancers.
- Monitor server performance.
- Scale servers horizontally.

---

# 🧠 Quick Revision

✅ Distributes requests across servers.

✅ Prevents server overload.

✅ Improves availability and scalability.

✅ Common Algorithms:
- Round Robin
- Least Connections
- IP Hash

---

# 🎉 Key Takeaways

⭐ A Load Balancer is the entry point for client requests.

⭐ It improves performance, scalability, and reliability.

⭐ It is a core component of modern distributed systems.