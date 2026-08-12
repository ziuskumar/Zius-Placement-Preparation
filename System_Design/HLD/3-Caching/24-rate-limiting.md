# 🚦 Rate Limiting

---

# 📖 Introduction

Rate Limiting controls how many requests a client can make to a system within a specific time period.

It protects services from:

- Too much traffic
- Abuse
- DDoS attacks
- API misuse
- Server overload

---

# 📌 Definition

> **Rate Limiting is the process of restricting the number of requests a client can make during a given time window.**

Example:

```text
100 requests / minute / user
```

If the user exceeds the limit, additional requests are rejected or delayed.

---

# ⚙️ How It Works

```text
        Client
          │
          ▼
    Rate Limiter
          │
     ┌────┴────┐
     ▼         ▼
 Within      Limit
 Limit       Exceeded
     │          │
     ▼          ▼
   Server     Reject
```

---

# 🧠 Example

Suppose an API allows:

```text
100 requests / minute
```

A client sends:

```text
Request 1  → ✅
Request 2  → ✅
...
Request 100 → ✅
Request 101 → ❌
```

The 101st request may receive:

```text
HTTP 429 Too Many Requests
```

---

# 📊 Common Rate Limiting Algorithms

### 1. Fixed Window

Requests are counted within fixed time intervals.

```text
12:00 ───────── 12:01
       100 requests
```

Simple, but traffic can spike around window boundaries.

---

### 2. Sliding Window

Tracks requests over a continuously moving time window.

```text
Current Time
     │
     ▼
[---- Last 60 Seconds ----]
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
   │  Bucket   │
   └───────────┘
        │
        ▼
     Request
```

Allows controlled bursts when tokens are available.

---

# 🌍 Real-World Example

An authentication API might limit login attempts:

```text
5 login attempts / minute / IP
```

This helps reduce brute-force attacks and protects the authentication service.

---

# 📍 Where Can Rate Limiting Be Applied?

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

Rate limiting is commonly implemented at an API Gateway or dedicated service.

---

# ✅ Advantages

- Protects servers
- Prevents abuse
- Controls traffic
- Improves availability
- Protects APIs
- Reduces resource exhaustion

---

# ❌ Disadvantages

- Legitimate requests can be rejected
- Requires configuration
- Distributed systems need shared rate-limit state
- Poor limits can affect user experience

---

# 🎯 Interview Keywords

- Rate Limiting
- API Protection
- HTTP 429
- Token Bucket
- Sliding Window
- Fixed Window
- API Gateway
- DDoS Protection

---

# ⚠️ Common Mistakes

❌ Setting extremely low limits.

❌ Applying the same limit to every type of API.

❌ Forgetting distributed rate limiting when multiple servers are used.

---

# 🔥 Interview Questions

### ❓ What is Rate Limiting?

It restricts the number of requests a client can make within a specific period.

### ❓ Why is it needed?

To prevent abuse, overload, and excessive resource consumption.

### ❓ What status code is commonly returned?

```text
HTTP 429 — Too Many Requests
```

### ❓ Name common algorithms.

- Fixed Window
- Sliding Window
- Token Bucket

---

# 🧠 Quick Revision

```text
Client
  ↓
Rate Limiter
  ↓
Within Limit? ── Yes → Server
       │
       No
       ↓
HTTP 429
```

✅ Controls request rate  
✅ Protects APIs  
✅ Prevents server overload  
✅ Common algorithms: Fixed Window, Sliding Window, Token Bucket

---

# 🎉 Key Takeaway

**Rate Limiting protects a system by controlling how many requests a client can make within a specific time period.**