# ⚡ Latency vs Throughput

---

# 📖 Introduction

Latency and Throughput are two important performance metrics in System Design. They help measure how fast and how much work a system can perform.

Understanding these concepts is essential before learning scalability and load balancing.

---

# 📌 Definition

### Latency

Latency is the **time taken to process a single request** from start to finish.

> **Lower latency = Faster response**

---

### Throughput

Throughput is the **number of requests processed by a system in a given amount of time**.

> **Higher throughput = More requests handled**

---

# ❓ Why Are They Important?

They help measure system performance.

- Latency focuses on **speed**.
- Throughput focuses on **capacity**.

---

# 📊 Latency vs Throughput

| Latency | Throughput |
|----------|------------|
| Measures response time | Measures number of requests |
| Unit: ms, sec | Unit: Requests/sec |
| Lower is better | Higher is better |
| User Experience | System Capacity |

---

# ⚙️ Working

Imagine a restaurant.

### Latency

Time taken to prepare one order.

```
Customer

↓

Order

↓

Food Ready

= 5 Minutes
```

Latency = **5 Minutes**

---

### Throughput

Total orders served in one hour.

```
1 Hour

↓

120 Orders Served
```

Throughput = **120 Orders/Hour**

---

# 📊 Architecture Diagram

```text
        Users
          │
          ▼
      Web Server
          │
          ▼
     Process Request
          │
          ▼
       Response

Latency → Time taken

Throughput → Requests handled
```

---

# 🌍 Real-World Example

## YouTube

### Latency

How long does a video take to start playing?

Example:

```
2 Seconds
```

---

### Throughput

How many videos can YouTube stream simultaneously?

Example:

```
10 Million Streams
```

---

# 📈 Advantages

### Low Latency

- Better user experience
- Faster response
- Improved customer satisfaction

### High Throughput

- Supports more users
- Better scalability
- Efficient resource utilization

---

# 🎯 Interview Keywords

- Latency
- Throughput
- Response Time
- Requests per Second (RPS)
- Performance
- Scalability

---

# ⚠️ Common Mistakes

❌ Thinking latency and throughput are the same.

❌ Assuming high throughput always means low latency.

❌ Ignoring performance bottlenecks.

---

# 🔥 Interview Questions

### ❓ What is Latency?

The time taken to process a single request.

---

### ❓ What is Throughput?

The number of requests processed in a given time.

---

### ❓ Which is better?

- Lower Latency ✅
- Higher Throughput ✅

---

### ❓ Can a system have high throughput but high latency?

Yes.

Example: A system processes many requests but each request takes a long time.

---

# 💡 Best Practices

- Reduce unnecessary processing.
- Use caching.
- Scale horizontally.
- Optimize database queries.
- Monitor system performance.

---

# 🧠 Quick Revision

✅ Latency → Response Time

✅ Throughput → Requests per Second

✅ Lower Latency is Better

✅ Higher Throughput is Better

---

# 🎉 Key Takeaways

⭐ Latency measures speed.

⭐ Throughput measures capacity.

⭐ Both are important for designing scalable and high-performance systems.