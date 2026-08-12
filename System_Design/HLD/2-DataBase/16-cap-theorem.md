# 🌐 CAP Theorem

---

# 📖 Introduction

In distributed systems, data is stored across multiple servers. During network failures, a system cannot guarantee all desirable properties at the same time.

The **CAP Theorem** explains this trade-off.

It is one of the most important concepts in System Design interviews.

---

# 📌 Definition

> **CAP Theorem states that a distributed system can guarantee at most two out of the following three properties simultaneously:**

- **C**onsistency
- **A**vailability
- **P**artition Tolerance

---

# ⚙️ The Three Properties

### Consistency (C)

Every read receives the **latest written value**.

---

### Availability (A)

Every request receives a **response**, even if some servers are down.

---

### Partition Tolerance (P)

The system continues to work despite **network failures between servers**.

---

# 📊 CAP Triangle

```text
        Consistency
           /\
          /  \
         /    \
        /      \
       /        \
      /          \
Availability ---- Partition Tolerance
```

In a network partition, you must choose between:

- **CP** (Consistency + Partition Tolerance)
- **AP** (Availability + Partition Tolerance)

---

# ❓ Why Can't We Have All Three?

Imagine two database servers.

```text
Client A ── Server 1

      X  (network failure)

Client B ── Server 2
```

Now:

- If Server 1 accepts a write,
- Server 2 cannot immediately know about it.

You must choose:

- Return old data → **Availability**
- Reject requests until synchronized → **Consistency**

---

# 🌍 Real-World Examples

## CP Systems

- PostgreSQL (with strict replication)
- HBase
- MongoDB (strong consistency settings)

During a partition, some requests may fail to keep data consistent.

---

## AP Systems

- Cassandra
- DynamoDB
- Riak

System remains available, but replicas may temporarily differ.

---

# 📈 Advantages

## CP

- Strong consistency
- Correct data
- Good for financial systems

## AP

- High availability
- Better user experience
- Good for large-scale distributed systems

---

# 📉 Disadvantages

## CP

- Lower availability during failures

## AP

- Eventual consistency
- Temporary stale reads

---

# 🎯 Interview Keywords

- CAP Theorem
- Consistency
- Availability
- Partition Tolerance
- Eventual Consistency
- Distributed Systems

---

# ⚠️ Common Mistakes

❌ Thinking CA is possible in real distributed systems.

❌ Assuming AP means no consistency.

❌ Confusing CAP with ACID.

---

# 🔥 Interview Questions

### ❓ What is CAP Theorem?

A distributed system can guarantee at most two of Consistency, Availability, and Partition Tolerance during a partition.

---

### ❓ What is a network partition?

A communication failure between nodes in a distributed system.

---

### ❓ Which is usually unavoidable?

**Partition Tolerance**.

---

### ❓ What do most modern distributed databases choose?

Usually **AP** or **CP** depending on requirements.

---

# 💡 Best Practices

- Financial systems → Prefer **CP**
- Social media / feeds → Prefer **AP**
- Understand business requirements first.

---

# 🧠 Quick Revision

✅ C = Latest data

✅ A = Always responds

✅ P = Survives network failure

✅ In partitions: choose **CP** or **AP**

---

# 🎉 Key Takeaways

⭐ CAP is about trade-offs in distributed systems.

⭐ Partition tolerance is usually mandatory.

⭐ Choose between consistency and availability based on business needs.