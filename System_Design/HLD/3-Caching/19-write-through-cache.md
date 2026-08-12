# ✍️ Write Through Cache

---

# 📖 Introduction

Write Through Cache is a caching strategy where data is written to the **cache and database at the same time**.

This keeps the cache consistent with the database.

---

# 📌 Definition

> **Write Through Cache writes data to the cache first and synchronously updates the database before confirming the write.**

---

# ⚙️ How It Works

```text
        Client
          │
          ▼
        Server
          │
          ▼
        Cache
          │
          ▼
       Database
          │
          ▼
       Response
```

The application writes to the cache and database as part of the same write operation.

---

# 🧠 Example

Suppose a user's name changes:

```text
Old Name: Rahul

New Name: Rohan
```

Write Through:

```text
Application
     │
     ├──→ Cache → Rohan
     │
     └──→ Database → Rohan
```

The updated value exists in both places.

---

# 📊 Write Through vs Cache Aside

| Write Through | Cache Aside |
|---|---|
| Cache updated during write | Cache updated during read |
| Database updated synchronously | Application writes DB directly |
| Better cache consistency | Simpler implementation |
| Write latency can increase | Cache may become stale |

---

# ✅ Advantages

- Better cache consistency
- Reduced cache misses after writes
- Simple read path
- Useful for frequently read data

---

# ❌ Disadvantages

- Higher write latency
- Every write requires cache + database update
- Cache may contain data that is rarely read
- More write operations

---

# 🌍 Real-World Example

Consider an e-commerce product:

```text
Product Price = ₹999
```

When the price changes:

```text
Application
     │
     ├──→ Cache = ₹899
     │
     └──→ Database = ₹899
```

Future users immediately receive the updated price from the cache.

---

# 🎯 Interview Keywords

- Write Through
- Cache Consistency
- Synchronous Write
- Cache
- Database
- Write Latency

---

# 🔥 Interview Questions

### ❓ What is Write Through Cache?

A strategy where data is synchronously written to both cache and database.

### ❓ What is the main advantage?

The cache remains consistent with the database.

### ❓ What is the main disadvantage?

Higher write latency because both cache and database must be updated.

---

# 🧠 Quick Revision

```text
Write Through

Write
  ↓
Cache
  ↓
Database
  ↓
Response
```

✅ Better consistency  
✅ Simple reads  
❌ Higher write latency

---

# 🎉 Key Takeaway

**Write Through Cache prioritizes cache consistency by updating the cache and database during every write operation.**