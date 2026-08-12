# 📑 Indexing

---

# 📖 Introduction

When a database table contains millions of rows, searching data by scanning every row becomes slow.

**Indexing** is used to make data retrieval much faster.

It is one of the most frequently asked database topics in System Design and interviews.

---

# 📌 Definition

> **An index is a data structure that improves the speed of data retrieval operations on a database table.**

Think of it like the **index page of a book**.

- Without index → read every page.
- With index → jump directly to the required page.

---

# ❓ Why Do We Need Indexing?

Without indexing:

- Slow searches
- Slow filtering
- Slow sorting
- High database load

With indexing:

- Faster queries
- Better performance
- Reduced response time

---

# ⚙️ How It Works

Suppose we have a table:

| id | name |
|----|------|
| 1 | A |
| 2 | B |
| 3 | C |

Query:

```sql
SELECT * FROM users WHERE id = 3;
```

### Without Index

```text
Row 1 → Row 2 → Row 3
```

### With Index

```text
Index → Directly to Row 3
```

---

# 🏗️ Index Structure

Most databases use a **B-Tree**.

```text
        [20]
       /    \
    [10]   [30]
```

This allows fast searching in **O(log n)** time.

---

# 💻 Create Index

### Single Column

```sql
CREATE INDEX idx_user_email
ON users(email);
```

### Multiple Columns

```sql
CREATE INDEX idx_user_name_age
ON users(name, age);
```

---

# 📊 Types of Indexes

| Type | Use |
|------|-----|
| Primary Index | Primary key |
| Unique Index | Prevent duplicates |
| Composite Index | Multiple columns |
| Full-Text Index | Text search |

---

# 🌍 Real-World Example

### Instagram Login

Query:

```sql
SELECT * FROM users
WHERE email = 'a@b.com';
```

An index on **email** makes login very fast.

---

# 📈 Advantages

- Faster search
- Faster filtering
- Faster sorting
- Better query performance

---

# 📉 Disadvantages

- Extra storage
- Slower INSERT
- Slower UPDATE
- Slower DELETE

Because indexes also need to be updated.

---

# 🎯 Interview Keywords

- Index
- B-Tree
- Composite Index
- Unique Index
- Query Optimization
- O(log n)

---

# ⚠️ Common Mistakes

❌ Adding indexes on every column.

❌ Indexing columns with very few unique values.

❌ Ignoring write overhead.

---

# 🔥 Interview Questions

### ❓ What is an index?

A data structure that speeds up data retrieval.

---

### ❓ Why is indexing faster?

Because the database does not scan every row.

---

### ❓ What is a composite index?

An index created on multiple columns.

---

### ❓ Does indexing improve INSERT performance?

No. It usually makes writes slightly slower.

---

# 💡 Best Practices

- Index columns used in **WHERE**.
- Index columns used in **JOIN**.
- Index columns used in **ORDER BY**.
- Avoid unnecessary indexes.

---

# 🧠 Quick Revision

✅ Index = Faster reads

✅ Uses B-Tree

✅ O(log n) search

❌ Extra storage

❌ Slower writes

---

# 🎉 Key Takeaways

⭐ Indexing is essential for large databases.

⭐ It dramatically improves read performance.

⭐ Use indexes carefully based on query patterns.