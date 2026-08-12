# ⏳ TTL & Cache Eviction

---

# 📖 Introduction

A cache has limited memory, so it cannot store data forever.

Two important mechanisms help manage cached data:

- **TTL (Time To Live)** → Determines how long data remains in the cache.
- **Cache Eviction** → Determines which data should be removed when the cache is full.

---

# 📌 TTL — Time To Live

TTL defines the amount of time a cached item remains valid.

Example:

```text
User Data
   │
   ▼
Cache
   │
   ▼
TTL = 60 seconds
   │
   ▼
Expires after 60 seconds
```

After the TTL expires, the cached entry is removed or treated as expired.

---

# ⚙️ Example

```text
Product Price
₹999

TTL = 300 seconds

↓

After 5 minutes

↓

Cache Entry Expires
```

The next request can fetch the latest value from the database and cache it again.

---

# 📌 Cache Eviction

Eviction happens when the cache reaches its memory limit and needs to remove existing data.

Common eviction policies include:

### LRU — Least Recently Used

Removes the item that has not been accessed for the longest time.

```text
A → B → C → D

If cache is full

↓

Remove A
```

---

### LFU — Least Frequently Used

Removes the item that has been accessed the fewest times.

```text
A → 10 accesses
B → 2 accesses
C → 7 accesses

↓

Remove B
```

---

### FIFO — First In, First Out

Removes the item that entered the cache first.

```text
A → B → C → D

↓

Remove A
```

---

# 📊 TTL vs Eviction

| TTL | Eviction |
|---|---|
| Time-based | Capacity/policy-based |
| Expires data after a duration | Removes data based on policy |
| Controls freshness | Controls memory usage |
| Example: 60 seconds | Example: LRU |

---

# 🌍 Real-World Example

A food delivery application may cache restaurant information:

```text
Restaurant Data
       │
       ▼
     Redis
       │
       ├── TTL → 10 minutes
       │
       └── LRU → Remove least recently used data
```

This keeps frequently accessed data available while controlling memory usage.

---

# 🎯 Interview Keywords

- TTL
- Time To Live
- Cache Expiration
- Cache Eviction
- LRU
- LFU
- FIFO
- Cache Memory

---

# ⚠️ Common Mistakes

❌ Thinking TTL and eviction are the same.

❌ Using extremely long TTLs for frequently changing data.

❌ Ignoring cache memory limits.

---

# 🔥 Interview Questions

### ❓ What is TTL?

TTL defines how long a cached item remains valid.

### ❓ What is cache eviction?

Removing cached data according to an eviction policy, often when the cache reaches its capacity.

### ❓ What is LRU?

**Least Recently Used** removes the item that has not been accessed for the longest time.

### ❓ What is LFU?

**Least Frequently Used** removes the item with the fewest accesses.

---

# 🧠 Quick Revision

```text
TTL
↓
Controls how long data lives

Eviction
↓
Controls what gets removed

LRU
↓
Remove least recently used

LFU
↓
Remove least frequently used
```

---

# 🎉 Key Takeaway

**TTL manages cache freshness, while eviction policies manage cache memory by deciding which entries should be removed.**
