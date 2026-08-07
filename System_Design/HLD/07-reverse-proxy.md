# 🔄 Reverse Proxy

---

# 📖 Introduction

A Reverse Proxy is a server that sits between clients and backend servers. Instead of users directly accessing application servers, all requests first go to the Reverse Proxy, which forwards them to the appropriate backend server.

It improves security, performance, and scalability.

---

# 📌 Definition

> **A Reverse Proxy is a server that receives client requests, forwards them to backend servers, and returns the server's response back to the client.**

---

# ❓ Why Do We Need a Reverse Proxy?

Without a Reverse Proxy:

- Clients know the backend server addresses.
- Backend servers are directly exposed.
- Harder to manage traffic.
- Lower security.

With a Reverse Proxy:

- Hides backend servers.
- Improves security.
- Can cache responses.
- Can perform load balancing.
- Simplifies traffic management.

---

# ⚙️ How It Works

```text
        Client
          │
          ▼
   Reverse Proxy
          │
     ┌────┴────┐
     ▼         ▼
 Server 1   Server 2
```

The client communicates only with the Reverse Proxy.

---

# 📊 Reverse Proxy vs Forward Proxy

| Reverse Proxy | Forward Proxy |
|---------------|---------------|
| Protects Servers | Protects Clients |
| Used by Server Side | Used by Client Side |
| Hides Backend Servers | Hides Client Identity |
| Improves Scalability | Controls Internet Access |

---

# 🌍 Real-World Example

### Nginx

Nginx is commonly used as a Reverse Proxy.

It receives user requests and forwards them to backend application servers like Node.js, Java, or Python applications.

---

# 📈 Advantages

- Improves security
- Hides backend servers
- Supports caching
- Enables load balancing
- Improves performance

---

# 📉 Disadvantages

- Additional server to manage
- Configuration complexity
- Single point of failure if not deployed redundantly

---

# 🎯 Interview Keywords

- Reverse Proxy
- Nginx
- Backend Servers
- Load Balancing
- Caching
- Security

---

# ⚠️ Common Mistakes

❌ Confusing Reverse Proxy with Load Balancer.

❌ Confusing Reverse Proxy with Forward Proxy.

❌ Exposing backend servers directly.

---

# 🔥 Interview Questions

### ❓ What is a Reverse Proxy?

A server that sits between clients and backend servers, forwarding requests and responses.

---

### ❓ Why is a Reverse Proxy used?

To improve security, performance, scalability, and hide backend servers.

---

### ❓ Name a popular Reverse Proxy.

- Nginx
- HAProxy
- Apache HTTP Server

---

### ❓ Can a Reverse Proxy perform Load Balancing?

Yes. Many Reverse Proxies like Nginx and HAProxy can distribute traffic across multiple backend servers.

---

# 💡 Best Practices

- Hide backend servers.
- Enable HTTPS at the Reverse Proxy.
- Configure caching where appropriate.
- Deploy redundant Reverse Proxies for high availability.

---

# 🧠 Quick Revision

✅ Sits between clients and servers.

✅ Hides backend servers.

✅ Improves security and performance.

✅ Can perform caching and load balancing.

---

# 🎉 Key Takeaways

⭐ A Reverse Proxy protects backend servers.

⭐ It improves security, scalability, and performance.

⭐ Nginx is one of the most widely used Reverse Proxy servers.