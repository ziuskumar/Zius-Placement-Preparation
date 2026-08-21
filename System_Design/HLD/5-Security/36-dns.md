# 🌐 DNS — Domain Name System

---

# 📖 Introduction

DNS translates human-readable domain names into IP addresses that computers can use to communicate.

Example:

```text
google.com
    ↓
142.250.x.x
```

---

# 📌 Definition

> **DNS is a distributed naming system that maps domain names to IP addresses.***

---

# ⚙️ How DNS Works

```text
User
  │
  ▼
Browser
  │
  ▼
DNS Resolver
  │
  ▼
DNS Server
  │
  ▼
IP Address
  │
  ▼
Web Server
```

The browser can then connect to the returned IP address.

---

# 🧠 Main DNS Components

### DNS Resolver

Receives the DNS query from the client and finds the required IP address.

### Root DNS Server

Provides information about the appropriate Top-Level Domain server.

### TLD Server

Handles domains such as:

```text
.com
.org
.in
```

### Authoritative DNS Server

Contains the actual DNS records for a domain.

---

# 📊 Common DNS Records

| Record | Purpose |
|---|---|
| A | Maps domain to IPv4 |
| AAAA | Maps domain to IPv6 |
| CNAME | Alias for another domain |
| MX | Mail server |
| NS | Authoritative name server |
| TXT | Text/verification information |

---

# ⚡ DNS Caching

DNS responses can be cached to avoid repeatedly querying DNS servers.

```text
Browser Cache
     ↓
OS Cache
     ↓
DNS Resolver Cache
     ↓
DNS Server
```

Caching reduces lookup time and DNS traffic.

---

# ⏳ TTL

DNS records have a **TTL (Time To Live)**.

Example:

```text
example.com
TTL = 300 seconds
```

The record can be cached for 300 seconds before needing a fresh lookup.

---

# 🌍 Real-World Example

When you visit:

```text
https://example.com
```

The browser needs the server's IP address.

```text
example.com
     ↓
DNS Lookup
     ↓
IP Address
     ↓
Connect to Server
```

---

# 🎯 Interview Keywords

- DNS
- Domain Name
- IP Address
- DNS Resolver
- Root Server
- TLD Server
- Authoritative Server
- DNS Record
- TTL
- DNS Cache

---

# ⚠️ Common Mistakes

❌ Thinking DNS stores website content.

❌ Thinking DNS only uses A records.

❌ Forgetting DNS caching.

❌ Confusing DNS with a Load Balancer.

---

# 🔥 Interview Questions

### ❓ What is DNS?

DNS maps human-readable domain names to IP addresses.

### ❓ Why is DNS needed?

Humans use domain names, while computers communicate using IP addresses.

### ❓ What is DNS caching?

Temporarily storing DNS responses to reduce lookup time and DNS traffic.

### ❓ What is an A record?

An A record maps a domain name to an IPv4 address.

### ❓ What is a CNAME?

A CNAME creates an alias that points one domain name to another domain name.

---

# 🧠 Quick Revision

```text
Domain Name
     ↓
DNS Resolver
     ↓
DNS Servers
     ↓
IP Address
     ↓
Web Server
```

✅ Converts domain → IP  
✅ Distributed system  
✅ Uses caching  
✅ Uses DNS records

---

# 🎉 Key Takeaway

**DNS acts like the internet's directory by translating domain names into IP addresses so clients can locate servers.**