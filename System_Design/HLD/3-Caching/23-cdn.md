# 🌐 CDN — Content Delivery Network

---

# 📖 Introduction

A **CDN (Content Delivery Network)** is a distributed network of servers placed in different geographical locations.

It delivers static content such as:

- Images
- Videos
- CSS
- JavaScript
- Documents

from a server closer to the user.

---

# 📌 Definition

> **A CDN is a distributed network of edge servers that delivers cached content to users from a location geographically closer to them.**

---

# ⚙️ How It Works

```text
              User
                │
                ▼
               DNS
                │
                ▼
           Nearest Edge
           CDN Server
                │
        ┌───────┴───────┐
        │               │
     Cache Hit       Cache Miss
        │               │
        ▼               ▼
     Content        Origin Server
                        │
                        ▼
                    CDN Cache
                        │
                        ▼
                      User
```

---

# 🧠 Cache Hit vs Cache Miss

### Cache Hit

Content is already available at the CDN edge.

```text
User → CDN → Content ✅
```

Fast response and no request to the origin server.

---

### Cache Miss

Content is not available at the edge.

```text
User → CDN → Origin Server
                 │
                 ▼
             CDN Cache
                 │
                 ▼
               User
```

The CDN fetches the content from the origin and may cache it for future requests.

---

# 📊 CDN vs Origin Server

| CDN | Origin Server |
|---|---|
| Stores cached content | Stores original content |
| Located near users | Central source |
| Reduces latency | Handles original requests |
| Reduces origin load | Higher load without CDN |

---

# 🌍 Real-World Example

Suppose a user in India requests a video from a service whose origin server is in the US.

Without CDN:

```text
India → USA → Video
```

With CDN:

```text
India → Nearby CDN Edge → Video
```

The content can be delivered with lower network latency.

---

# ✅ Advantages

- Lower latency
- Faster content delivery
- Reduces origin server load
- Handles traffic spikes
- Improves availability
- Better user experience

---

# ❌ Disadvantages

- Additional cost
- Cache invalidation can be challenging
- Cached content may become stale
- Dynamic content is harder to cache effectively

---

# 🎯 Interview Keywords

- CDN
- Edge Server
- Origin Server
- Cache Hit
- Cache Miss
- Edge Location
- Latency
- Static Content

---

# ⚠️ Common Mistakes

❌ Thinking CDN replaces the database.

❌ Assuming all dynamic requests should be cached.

❌ Confusing CDN with a Load Balancer.

---

# 🔥 Interview Questions

### ❓ What is a CDN?

A distributed network of edge servers that delivers cached content closer to users.

### ❓ Why does CDN reduce latency?

Because content can be served from an edge location geographically closer to the user.

### ❓ What is an Origin Server?

The original server where the requested content is stored.

### ❓ What happens during a Cache Miss?

The CDN requests the content from the origin server and can cache it for future requests.

---

# 🧠 Quick Revision

```text
User
 ↓
CDN Edge
 ↓
Cache Hit → Return Content

Cache Miss
 ↓
Origin Server
 ↓
CDN Cache
 ↓
User
```

✅ Lower latency  
✅ Less origin load  
✅ Faster static content delivery

---

# 🎉 Key Takeaway

**A CDN improves content delivery by caching data at geographically distributed edge servers closer to users.**