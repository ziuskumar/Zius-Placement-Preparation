# ⚡ Why Cache?

---

# 📖 Introduction

Databases are much slower than memory. If every request goes to the database, the application becomes slow and expensive.

**Caching** stores frequently accessed data in fast memory (RAM) so that future requests can be served quickly.

---

# 📌 Definition

> **Cache is a temporary high-speed storage layer used to store frequently accessed data to reduce latency and improve performance.**

---

# ❓ Why Do We Need Cache?

Without cache:

- Slow responses
- High database load
- More CPU usage
- Poor user experience

With cache:

- Faster responses
- Reduced database traffic
- Better scalability
- Lower infrastructure cost

---

# ⚙️ How It Works

```text
User
  │
  ▼
Application
  │
  ▼
Cache (Redis)
  │
Hit? ── Yes ──► Return Data
  │
  No
  ▼
Database
  │
  ▼
Store in Cache
  │
  ▼
Return Data
```

---

# 🌍 Real-World Example

### Instagram

When a user opens the home feed:

- First request → Database
- Feed stored in Redis
- Next requests → Cache

Result: Much faster loading.

---

# 📈 Advantages

- Low latency
- Reduced DB load
- Better scalability
- Improved user experience

---

# 📉 Disadvantages

- Extra memory cost
- Cache invalidation is hard
- Possible stale data

---

# 🎯 What Should Be Cached?

✅ User profiles

✅ Product details

✅ Home feeds

✅ Session data

❌ Frequently changing financial data

---

# 🎯 Interview Keywords

- Cache Hit
- Cache Miss
- Redis
- Memcached
- Latency
- Scalability

---

# ⚠️ Common Mistakes

❌ Caching everything.

❌ Not setting expiration time.

❌ Ignoring stale data.

---

# 🔥 Interview Questions

### ❓ What is a cache?

A fast temporary storage for frequently accessed data.

### ❓ Why use cache?

To reduce latency and database load.

### ❓ What is a cache hit?

Data found in cache.

### ❓ What is a cache miss?

Data not found in cache.

---

# 💡 Best Practices

- Cache frequently read data.
- Set appropriate TTL.
- Monitor hit ratio.
- Keep cache smaller than total dataset.

---

# 🧠 Quick Revision

✅ Cache = Fast memory

✅ Hit = Found

✅ Miss = Not found

✅ Improves performance

---

# 🎉 Key Takeaways

⭐ Cache reduces response time.

⭐ Cache reduces database load.

⭐ Redis is the most common caching solution in modern systems.