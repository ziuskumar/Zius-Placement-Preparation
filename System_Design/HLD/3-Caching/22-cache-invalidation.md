# 🔄 Cache Invalidation

---

# 📖 Introduction

Cache Invalidation is the process of **removing or updating stale data from the cache** when the original data changes.

It is important because cached data can become outdated.

---

# 📌 Definition

> **Cache Invalidation is the process of ensuring that outdated cached data is removed or updated when the underlying data changes.**

---

# ❓ Why Is It Important?

Suppose the database contains:

```text
Product Price = ₹999
```

The cache also stores:

```text
₹999
```

The price changes in the database:

```text
Database = ₹899
Cache    = ₹999 ❌
```

The cache now contains **stale data**.

Invalidation fixes this.

---

# ⚙️ How It Works

```text
       Application
            │
            ▼
         Database
            │
            │ Update
            ▼
        Invalidate
          Cache
            │
            ▼
       Fresh Data
```

When data changes, the corresponding cache entry is deleted or updated.

---

# 🧠 Common Invalidation Strategies

### 1. Delete on Write

Update the database and remove the cached value.

```text
Write
  │
  ├──→ Database Update
  │
  └──→ Delete Cache
```

The next read fetches fresh data from the database.

---

### 2. Update on Write

Update both the database and cache.

```text
Write
  │
  ├──→ Database
  │
  └──→ Cache Update
```

---

### 3. TTL-Based Expiration

Let cached data expire automatically after a fixed time.

```text
Cache Entry
    │
    ▼
TTL = 60 sec
    │
    ▼
Expired
```

This is simple but data may remain stale until the TTL expires.

---

# 📊 Cache Invalidation vs TTL

| Cache Invalidation | TTL |
|---|---|
| Explicitly removes/updates data | Automatically expires data |
| Can provide fresher data | May temporarily serve stale data |
| Triggered by data changes | Triggered by time |
| More complex | Simpler |

---

# 🌍 Real-World Example

### E-Commerce Product

```text
Product Price
₹999
```

User changes the price:

```text
Database → ₹899
Cache → Delete old ₹999
```

Next request:

```text
Cache Miss
    ↓
Database
    ↓
₹899
    ↓
Cache
```

The cache now contains the latest value.

---

# ⚠️ Common Challenges

- Stale data
- Cache consistency
- Race conditions
- Distributed cache synchronization
- Incorrect invalidation logic

> **Cache invalidation is often considered one of the harder parts of caching because the system must know when cached data is no longer valid.**

---

# 🎯 Interview Keywords

- Cache Invalidation
- Stale Data
- Cache Consistency
- TTL
- Cache Miss
- Delete on Write
- Update on Write

---

# 🔥 Interview Questions

### ❓ What is Cache Invalidation?

Removing or updating stale data from the cache when the underlying data changes.

### ❓ Why is it needed?

To prevent users from receiving outdated information.

### ❓ What are common strategies?

- Delete on Write
- Update on Write
- TTL Expiration

### ❓ Is TTL the same as invalidation?

No. TTL expires data based on time, while invalidation can happen immediately when the underlying data changes.

---

# 🧠 Quick Revision

```text
Database Changes
       ↓
Cache Becomes Stale
       ↓
Invalidate / Update Cache
       ↓
Fresh Data
```

✅ Prevents stale data  
✅ Improves cache consistency  
✅ Can use TTL, delete, or update strategies

---

# 🎉 Key Takeaway

**Cache Invalidation keeps cached data fresh by removing or updating entries when the underlying data changes.**