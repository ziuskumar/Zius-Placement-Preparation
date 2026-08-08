# 🐘 PostgreSQL Basics

---

# 📖 Introduction

PostgreSQL is one of the most popular **open-source relational databases** used in modern applications. It is known for reliability, ACID compliance, powerful SQL support, and scalability.

Companies like Instagram, Reddit, Spotify, and many startups use PostgreSQL.

---

# 📌 Definition

> **PostgreSQL is an open-source relational database management system (RDBMS) that stores data in tables and supports SQL for querying and managing data.**

---

# ❓ Why Use PostgreSQL?

- Open source
- ACID compliant
- Supports complex queries
- Reliable and stable
- Extensible
- Good performance

---

# ⚙️ Basic Architecture

```text
Client
   │
   ▼
PostgreSQL Server
   │
   ├── Database
   │     ├── Tables
   │     ├── Indexes
   │     └── Views
   │
   └── Storage
```

---

# 🗄️ Core Concepts

## Database

A collection of related data.

Example:

```sql
CREATE DATABASE appdb;
```

---

## Table

Stores data in rows and columns.

```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);
```

---

## Row

Represents a single record.

---

## Column

Represents an attribute of the record.

---

# ⚡ Basic SQL Operations

### Insert

```sql
INSERT INTO users(name, email)
VALUES('Zius', 'zius@example.com');
```

---

### Select

```sql
SELECT * FROM users;
```

---

### Update

```sql
UPDATE users
SET name = 'Lucky'
WHERE id = 1;
```

---

### Delete

```sql
DELETE FROM users
WHERE id = 1;
```

---

# 🔑 Primary Key

A column that uniquely identifies each row.

```sql
id SERIAL PRIMARY KEY
```

- Unique
- Not NULL

---

# 🔗 Foreign Key

Creates a relationship between tables.

```sql
CREATE TABLE orders (
    id SERIAL PRIMARY KEY,
    user_id INT REFERENCES users(id)
);
```

---

# 🌍 Real-World Example

### E-commerce

**users**

| id | name |
|----|------|
| 1 | Zius |

**orders**

| id | user_id |
|----|---------|
| 101 | 1 |

This shows **Zius placed order 101**.

---

# 📈 Advantages

- Strong consistency
- ACID transactions
- Rich SQL features
- Excellent for relational data

---

# 📉 Disadvantages

- More complex than some NoSQL databases
- Horizontal scaling is harder

---

# 🎯 Interview Keywords

- PostgreSQL
- RDBMS
- ACID
- Primary Key
- Foreign Key
- SQL
- Transactions

---

# ⚠️ Common Mistakes

❌ No primary key.

❌ Storing unrelated data in one table.

❌ Ignoring indexes.

---

# 🔥 Interview Questions

### ❓ What is PostgreSQL?

An open-source relational database.

---

### ❓ What is a primary key?

A unique identifier for each row.

---

### ❓ What is a foreign key?

A column that references another table's primary key.

---

### ❓ Is PostgreSQL ACID compliant?

Yes.

---

# 💡 Best Practices

- Use primary keys.
- Normalize data.
- Add indexes for frequent queries.
- Use transactions for critical operations.

---

# 🧠 Quick Revision

✅ PostgreSQL = Relational Database

✅ Tables store data

✅ Primary Key = Unique ID

✅ Foreign Key = Relationship

✅ Supports ACID transactions

---

# 🎉 Key Takeaways

⭐ PostgreSQL is a powerful and reliable relational database.

⭐ It is widely used in production systems.

⭐ Understanding tables, keys, and basic SQL is essential for System Design interviews.