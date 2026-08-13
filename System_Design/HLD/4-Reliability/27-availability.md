# 🟢 Availability

---

# 📖 Introduction

Availability describes how often a system is **operational and accessible when users need it**.

A highly available system continues serving users even when some components fail.

---

# 📌 Definition

> **Availability is the percentage of time a system remains operational and accessible to users.**

It is commonly measured using:

```text
Availability =
(Uptime / Total Time) × 100
```

---

# 📊 Availability Levels

Availability is often expressed using "nines":

| Availability | Approx. Downtime / Year |
|---|---:|
| 99% | 3.65 days |
| 99.9% | 8.76 hours |
| 99.99% | 52.6 minutes |
| 99.999% | 5.26 minutes |

Higher availability means less acceptable downtime.

---

# ⚙️ How to Improve Availability

```text
             Users
                │
                ▼
         Load Balancer
          ┌─────┴─────┐
          ▼           ▼
       Server 1    Server 2
          │           │
          └─────┬─────┘
                ▼
          Replicated DB
```

Common techniques:

- Horizontal scaling
- Load balancing
- Replication
- Redundancy
- Health checks
- Failover
- Multiple availability zones

---

# 🌍 Real-World Example

Consider an online banking system.

If one application server fails:

```text
Server 1 ❌
    │
    ▼
Load Balancer
    │
    ▼
Server 2 ✅
    │
    ▼
User
```

The user can continue using the service.

---

# 📊 Availability vs Reliability

| Availability | Reliability |
|---|---|
| Is the system available now? | Does the system operate correctly over time? |
| Focuses on uptime | Focuses on failure-free operation |
| Measured using uptime percentage | Often measured using failure metrics |

A system can be highly available but still have bugs that produce incorrect results.

---

# ✅ Advantages of High Availability

- Reduced downtime
- Better user experience
- Higher business continuity
- Improved fault tolerance
- Reduced impact of server failures

---

# ⚠️ Common Mistakes

❌ Thinking 100% availability is always realistic.

❌ Using a single server for a highly available system.

❌ Forgetting database availability.

❌ Ignoring failure and recovery scenarios.

---

# 🎯 Interview Keywords

- Availability
- Uptime
- Downtime
- Redundancy
- Failover
- Replication
- Load Balancer
- Fault Tolerance
- SLA

---

# 🔥 Interview Questions

### ❓ What is Availability?

The percentage of time a system remains operational and accessible.

### ❓ How can availability be improved?

Using redundancy, replication, load balancing, health checks, and failover mechanisms.

### ❓ What does 99.99% availability mean?

Approximately 99.99% of the expected service time is available, allowing roughly 52.6 minutes of downtime per year.

### ❓ What is a single point of failure?

A component whose failure can cause the entire system or critical functionality to become unavailable.

---

# 🧠 Quick Revision

```text
Availability
     ↓
System stays accessible
     ↓
Redundancy + Replication
     ↓
Failover
     ↓
Less Downtime
```

✅ Measures uptime  
✅ Higher availability = less downtime  
✅ Redundancy improves availability

---

# 🎉 Key Takeaway

**Availability measures how consistently a system remains accessible and operational, even when individual components fail.**