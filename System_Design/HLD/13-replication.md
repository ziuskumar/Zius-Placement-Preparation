# 🔁 Replication

---

# 📖 Introduction

As applications grow, a single database server may become a bottleneck or a single point of failure.

**Replication** is used to create copies of a database on multiple servers to improve **availability, reliability, and read performance**.

---

# 📌 Definition

> **Replication is the process of copying data from one database server to one or more other database servers.**

- **Primary (Master)** → receives writes.
- **Replica (Secondary)** → receives copied data.

---

# ❓ Why Do We Need Replication?

Without replication:

- Database failure can cause downtime.
- Read queries overload one server.
- Backups become risky.

With replication:

- High availability
- Better read scalability
- Disaster recovery
- Reduced load on primary DB

---

# ⚙️ How It Works

```text
        Application
             │
      Write Queries
             ▼
        Primary DB
         /      \
        /        \
       ▼          ▼
   Replica 1   Replica 2
    (Read)      (Read)
```

- Writes go to **Primary**.
- Data is copied to **Replicas**.
- Reads can be distributed across replicas.

---

# 📊 Types of Replication

| Type | Description |
|------|-------------|
| Synchronous | Waits for replica confirmation |
| Asynchronous | Primary does not wait |
| Semi-Synchronous | Waits for at least one replica |

---

# 🌍 Real-World Example

### E-commerce Website

- User places order → **Primary DB**
- Product search → **Replica**
- Order history → **Replica**

This reduces load on the primary database.

---

# 📈 Advantages

- High availability
- Better read performance
- Fault tolerance
- Easier backups

---

# 📉 Disadvantages

- Replication lag
- More infrastructure
- Complex failover
- Data inconsistency (temporary)

---

# 🎯 Interview Keywords

- Primary
- Replica
- Read Replica
- Replication Lag
- High Availability
- Failover

---

# ⚠️ Common Mistakes

❌ Sending writes to replicas.

❌ Ignoring replication lag.

❌ Assuming replicas are always perfectly up-to-date.

---

# 🔥 Interview Questions

### ❓ What is replication?

Copying data from one database to other database servers.

---

### ❓ Why use replication?

To improve availability and read scalability.

---

### ❓ What is a read replica?

A replica used mainly for read queries.

---

### ❓ What is replication lag?

Delay between primary update and replica update.

---

# 💡 Best Practices

- Send writes only to primary.
- Use replicas for heavy reads.
- Monitor replication lag.
- Configure automatic failover.

---

# 🧠 Quick Revision

✅ Primary handles writes

✅ Replicas handle reads

✅ Improves availability

⚠️ Replication lag may occur

---

# 🎉 Key Takeaways

⭐ Replication creates copies of a database.

⭐ It improves read performance and availability.

⭐ Replication is a core concept in scalable database systems.