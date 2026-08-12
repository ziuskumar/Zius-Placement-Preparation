# 🧠 Cache Aside Pattern

---

# 📖 Introduction

Cache Aside is the **most commonly used caching pattern** in modern applications.

The application first checks the cache. If the data is not found, it fetches the data from the database and stores it in the cache for future requests.

---

# 📌 Definition

> **Cache Aside is a caching strategy where the application is responsible for reading from the cache and updating the cache when data is missing.**

---

# ⚙️ How It Works

### Read Flow

```text
User
  │
  ▼
Application
  │
  ▼
Cache
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

# 💻 Example

### Step 1: Request User Profile

- Cache miss
- Read from DB
- Store in Redis
- Return response

### Step 2: Request Again

- Cache hit
- Return directly from Redis

---

# 🌍 Real-World Example

### E-commerce Product Page

First request:

```text
DB → Cache → User
```

Next requests:

```text
Cache → User
```

This reduces database load significantly.

---

# 📈 Advantages

- Simple to implement
- Reduces DB load
- Fast repeated reads
- Works well for read-heavy systems

---

# 📉 Disadvantages

- Stale data possible
- Extra logic in application
- Cache miss causes DB hit

---

# 🎯 Interview Keywords

- Cache Aside
- Lazy Loading
- Cache Miss
- Cache Hit
- Redis

---

# ⚠️ Common Mistakes

❌ Forgetting to update/invalidate cache after DB update.

❌ Caching very short-lived data.

---

# 🔥 Interview Questions

### ❓ Why is it called Cache Aside?

Because the cache sits "aside" the database, and the application manages it.

### ❓ Is it read-through?

No. The application handles cache misses.

### ❓ Best use case?

Read-heavy applications such as feeds, product pages, and user profiles.

---

# 💡 Best Practices

- Set TTL for cached data.
- Invalidate cache on updates.
- Use Redis for fast access.

---

# 🧠 Quick Revision

✅ Check cache first

✅ Miss → DB

✅ Store in cache

✅ Return response

---

# 🎉 Key Takeaways

⭐ Most popular caching pattern.

⭐ Excellent for read-heavy workloads.

⭐ Simple and effective when combined with proper invalidation.
