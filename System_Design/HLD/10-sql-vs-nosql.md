# 🗄️ SQL vs NoSQL

---

# 📖 Introduction

Databases are used to store and manage application data. In System Design, databases are broadly divided into two categories:

- **SQL (Relational Databases)**
- **NoSQL (Non-Relational Databases)**

Choosing the right database depends on the application’s requirements, scalability needs, and data structure.

---

# 📌 Definition

### SQL Database

A **SQL database** stores data in **tables with rows and columns** and follows a fixed schema.

Examples:

- PostgreSQL
- MySQL
- Oracle
- SQL Server

---

### NoSQL Database

A **NoSQL database** stores data in a flexible format such as documents, key-value pairs, wide columns, or graphs.

Examples:

- MongoDB
- Redis
- Cassandra
- Neo4j

---

# ❓ Why Do We Need Both?

Different applications have different needs.

- Banking → Strong consistency → **SQL**
- Social Media → Massive scale & flexible data → **NoSQL**

---

# ⚙️ Data Model

### SQL

```text
Users Table
+----+-------+-------+
| id | name  | age   |
+----+-------+-------+
| 1  | Zius  | 21    |
+----+-------+-------+
```

---

### NoSQL (Document)

```json
{
  "id": 1,
  "name": "Zius",
  "age": 21
}
```

---

# 📊 SQL vs NoSQL

| Feature | SQL | NoSQL |
|--------|-----|--------|
| Data Model | Tables | Documents / Key-Value / Graph |
| Schema | Fixed | Flexible |
| Scaling | Vertical | Horizontal |
| Transactions | Strong ACID | Often BASE |
| Joins | Supported | Limited / Avoided |
| Best For | Structured Data | Large-scale flexible data |

---

# 🌍 Real-World Example

### Banking System

- Accounts
- Transactions
- Balance updates

**Use:** SQL (PostgreSQL)

---

### Instagram / Twitter

- Posts
- Likes
- Comments
- Followers

**Use:** NoSQL (MongoDB, Cassandra, Redis)

---

# 📈 Advantages

## SQL

- Strong consistency
- ACID transactions
- Powerful queries
- Better for complex relationships

---

## NoSQL

- Easy horizontal scaling
- Flexible schema
- High availability
- Handles large volumes of data

---

# 📉 Disadvantages

## SQL

- Harder to scale horizontally
- Schema migrations required

---

## NoSQL

- Weaker consistency in some systems
- Limited joins
- Complex transactions can be difficult

---

# 🎯 Interview Keywords

- Relational Database
- Non-Relational Database
- ACID
- BASE
- Schema
- Horizontal Scaling
- Consistency

---

# ⚠️ Common Mistakes

❌ Thinking NoSQL is always faster.

❌ Using NoSQL for highly transactional systems.

❌ Ignoring consistency requirements.

---

# 🔥 Interview Questions

### ❓ What is SQL?

A relational database with structured tables and a fixed schema.

---

### ❓ What is NoSQL?

A non-relational database with flexible data models.

---

### ❓ When would you choose SQL?

For applications requiring strong consistency and transactions.

---

### ❓ When would you choose NoSQL?

For applications requiring massive scale and flexible schemas.

---

# 💡 Best Practices

- Start with SQL if data is highly relational.
- Use NoSQL for rapidly changing or large-scale data.
- Choose based on **requirements**, not trends.

---

# 🧠 Quick Revision

✅ SQL → Structured, ACID, Tables

✅ NoSQL → Flexible, Scalable, Distributed

---

# 🎉 Key Takeaways

⭐ SQL is best for structured and transactional systems.

⭐ NoSQL is best for scalable and flexible systems.

⭐ The choice depends on consistency, relationships, and scale requirements.