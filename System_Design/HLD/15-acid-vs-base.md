# ⚖️ ACID vs BASE

---

# 📖 Introduction

When designing databases, one of the biggest decisions is choosing between **strong consistency** and **high scalability/availability**.

- **ACID** is commonly used in traditional SQL databases.
- **BASE** is commonly used in many distributed NoSQL databases.

---

# 📌 Definition

### ACID

A set of properties that guarantee **reliable and consistent transactions**.

- **A**tomicity
- **C**onsistency
- **I**solation
- **D**urability

---

### BASE

A model that focuses on **availability and scalability**.

- **B**asically Available
- **S**oft State
- **E**ventual Consistency

---

# ⚙️ ACID Properties

### Atomicity

Either **all operations succeed or none**.

Example:

- Debit ₹100
- Credit ₹100

If credit fails, debit is rolled back.

---

### Consistency

Database remains in a **valid state**.

---

### Isolation

Concurrent transactions do not interfere with each other.

---

### Durability

Once committed, data is permanently stored.

---

# ⚙️ BASE Properties

### Basically Available

System remains available even during failures.

---

### Soft State

Data may change over time even without new input.

---

### Eventual Consistency

All replicas become consistent **eventually**.

---

# 📊 ACID vs BASE

| Feature | ACID | BASE |
|---|---|---|
| Consistency | Strong | Eventual |
| Availability | Lower | Higher |
| Scalability | Harder | Easier |
| Transactions | Full support | Limited |
| Typical DB | PostgreSQL | Cassandra |

---

# 🌍 Real-World Example

### Banking → ACID

- Money transfer
- Account balance
- Payments

Needs **strong consistency**.

---

### Social Media → BASE

- Likes
- Comments
- Followers
- Feeds

Slight delay is acceptable.

---

# 🎯 Interview Keywords

- Atomicity
- Consistency
- Isolation
- Durability
- Eventual Consistency
- Availability

---

# ⚠️ Common Mistakes

❌ Thinking BASE means "no consistency".

❌ Using BASE for financial transactions.

❌ Assuming ACID systems cannot scale.

---

# 🔥 Interview Questions

### ❓ What is ACID?

A set of properties ensuring reliable database transactions.

---

### ❓ What is BASE?

A model prioritizing availability and scalability with eventual consistency.

---

### ❓ When would you choose ACID?

For banking, payments, inventory, and critical transactions.

---

### ❓ When would you choose BASE?

For large-scale distributed systems like social media and analytics.

---

# 💡 Best Practices

- Use **ACID** for critical transactional data.
- Use **BASE** for highly scalable distributed workloads.
- Choose based on business requirements, not popularity.

---

# 🧠 Quick Revision

✅ ACID → Strong consistency

✅ BASE → High availability

✅ Banking → ACID

✅ Social Media → BASE

---

# 🎉 Key Takeaways

⭐ ACID guarantees reliable transactions.

⭐ BASE enables scalable distributed systems.

⭐ The right choice depends on consistency vs availability requirements.