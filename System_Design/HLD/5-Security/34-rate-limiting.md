# 🚦 Rate Limiting

---

# 📖 Introduction

Rate Limiting controls how many requests a client can make to a system within a specific time period.

It protects APIs and services from:

- Excessive traffic
- Abuse
- Brute-force attacks
- Server overload
- Resource exhaustion

---

# 📌 Definition

> **Rate Limiting is the process of restricting the number of requests a client can make within a given time period.**

Example:

```text
100 requests / minute / user
```

---

# ⚙️ How It Works

```text
Client
  │
  ▼
Rate Limiter
  │
  ├── Within Limit → ✅ Allow
  │
  └── Limit Exceeded → ❌ Reject
```

When the limit is exceeded, the server commonly returns:

```text
HTTP 429 Too Many Requests
```

---

# 🧠 Common Rate Limiting Algorithms

### 1. Fixed Window

Counts requests within a fixed time period.

```text
12:00 ───────── 12:01
       100 Requests
```

---

### 2. Sliding Window

Tracks requests over a continuously moving time period.

```text
<------ 60 seconds ------>
             ↑
        Current Time
```

Provides smoother limiting than a fixed window.

---

### 3. Token Bucket

Tokens are added to a bucket at a fixed rate.

Each request consumes one token.

```text
       Tokens
      ↓ ↓ ↓ ↓
   ┌───────────┐
   │   Bucket  │
   └───────────┘
        │
        ▼
     Request
```

It can allow short bursts when tokens are available.

---

# 🌍 Real-World Example

A login API may allow:

```text
5 attempts / minute / IP
```

After exceeding the limit:

```text
Login Request
      ↓
Rate Limiter
      ↓
Limit Exceeded
      ↓
429 Too Many Requests
```

This helps protect against brute-force attacks.

---

# 📍 Where Is Rate Limiting Applied?

```text
Client
  ↓
API Gateway
  ↓
Rate Limiter
  ↓
Application Server
  ↓
Database
```

Rate limiting can be implemented at an API Gateway, reverse proxy, application layer, or dedicated service.

---

# 📊 Rate Limiting Strategies

| Strategy | Example |
|---|---|
| Per IP | 100 requests/minute/IP |
| Per User | 1000 requests/hour/user |
| Per API Key | 10,000 requests/day/key |
| Per Endpoint | Login: 5 requests/minute |

---

# ✅ Advantages

- Protects APIs
- Prevents abuse
- Controls traffic
- Reduces server overload
- Improves system stability
- Protects expensive resources

---

# ❌ Disadvantages

- Legitimate requests may be rejected
- Requires configuration
- Distributed systems need shared state
- Poor limits can hurt user experience

---

# 🎯 Interview Keywords

- Rate Limiting
- HTTP 429
- Token Bucket
- Fixed Window
- Sliding Window
- API Gateway
- API Protection
- Brute Force

---

# 🔥 Interview Questions

### ❓ What is Rate Limiting?

Restricting the number of requests a client can make during a specific time period.

### ❓ Why is it needed?

To prevent abuse, excessive traffic, and resource exhaustion.

### ❓ What status code is commonly returned?

```text
429 Too Many Requests
```

### ❓ Name common algorithms.

- Fixed Window
- Sliding Window
- Token Bucket

### ❓ Where can Rate Limiting be implemented?

At the API Gateway, reverse proxy, application server, or dedicated rate-limiting service.

---

# 🧠 Quick Revision

```text
Client
  ↓
Rate Limiter
  ↓
Within Limit?
 ├── Yes → Server
 └── No  → 429
```

✅ Controls request rate  
✅ Protects APIs  
✅ Prevents overload  
✅ Supports abuse protection

---

# 🎉 Key Takeaway

**Rate Limiting protects a system by controlling how many requests a client can make within a specific period.**