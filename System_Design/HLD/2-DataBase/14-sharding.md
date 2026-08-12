# 🧩 Sharding

---

# 📖 Introduction

As a database grows, storing all data on a single server becomes difficult. Queries become slower, storage becomes limited, and the server may get overloaded.

**Sharding** is used to split data across multiple database servers.

---

# 📌 Definition

> **Sharding is the process of dividing a large database into smaller independent pieces called shards, where each shard stores a subset of the data.**

Each shard has:

- Its own storage
- Its own CPU/RAM
- Its own indexes

---

# ❓ Why Do We Need Sharding?

Without sharding:

- Database becomes very large
- Queries slow down
- Storage limits reached
- Single server becomes a bottleneck

With sharding:

- Better scalability
- Faster queries
- More storage capacity
- Load distributed across servers

---

# ⚙️ How It Works

### Before Sharding

```text
Users
  │
  ▼
Single Database
```

---

### After Sharding

```text
Users
  │
  ▼
Router / Application
  ├── Shard 1 (A-F)
  ├── Shard 2 (G-M)
  ├── Shard 3 (N-S)
  └── Shard 4 (T-Z)
```

Data is distributed based on a **shard key**.

---

# 🔑 Shard Key

A **shard key** determines where a record is stored.

Examples:

- user_id
- customer_id
- region
- email hash

---

# 📊 Sharding Strategies

| Strategy | Example |
|----------|---------|
| Range-based | 1-1000, 1001-2000 |
| Hash-based | hash(user_id) |
| Geographic | India, US, Europe |

---

# 🌍 Real-World Example

### Instagram

- User 1 → Shard 1
- User 2 → Shard 3
- User 3 → Shard 2

Millions of users are distributed across many database servers.

---

# 📈 Advantages

- Horizontal scalability
- Faster queries on smaller datasets
- Higher storage capacity
- Better load distribution

---

# 📉 Disadvantages

- More complex architecture
- Cross-shard joins are difficult
- Rebalancing can be expensive
- Choosing a bad shard key causes hotspots

---

# 🎯 Interview Keywords

- Sharding
- Shard Key
- Horizontal Partitioning
- Hotspot
- Rebalancing
- Distributed Database

---

# ⚠️ Common Mistakes

❌ Choosing a non-uniform shard key.

❌ Using auto-increment IDs without planning.

❌ Ignoring cross-shard queries.

---

# 🔥 Interview Questions

### ❓ What is sharding?

Splitting a large database into smaller independent databases called shards.

---

### ❓ Why is sharding used?

To achieve horizontal scalability and distribute load.

---

### ❓ What is a shard key?

A field used to decide which shard stores a record.

---

### ❓ Difference between replication and sharding?

- **Replication** → copies the same data.
- **Sharding** → splits different data across servers.

---

# 💡 Best Practices

- Choose a high-cardinality shard key.
- Ensure even data distribution.
- Monitor shard sizes.
- Plan for future rebalancing.

---

# 🧠 Quick Revision

✅ Sharding = Split data

✅ Replication = Copy data

✅ Horizontal scalability

⚠️ Shard key is critical

---

# 🎉 Key Takeaways

⭐ Sharding distributes data across multiple servers.

⭐ It enables horizontal scaling for very large databases.

⭐ The shard key is the most important design decision.