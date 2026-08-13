# 🛡️ Fault Tolerance

---

# 📖 Introduction

Fault Tolerance is the ability of a system to **continue operating even when one or more components fail**.

A fault-tolerant system detects failures and uses backup or alternative components to continue serving users.

---

# 📌 Definition

> **Fault Tolerance is the ability of a system to continue functioning correctly despite failures in one or more components.**

---

# ⚙️ How It Works

```text
             Users
               │
               ▼
        Load Balancer
          ┌────┴────┐
          ▼         ▼
       Server 1   Server 2
          │         │
          ❌         ✅
          │         │
          └────┬────┘
               ▼
        Healthy Server
```

If Server 1 fails, traffic can be redirected to Server 2.

---

# 🧠 Common Fault Tolerance Techniques

### 1. Redundancy

Use multiple instances of the same component.

```text
Server 1
Server 2
Server 3
```

If one fails, others continue working.

---

### 2. Replication

Maintain multiple copies of data or services.

```text
Primary
   │
   ├── Replica 1
   └── Replica 2
```

---

### 3. Failover

Automatically switch to a healthy backup when the primary component fails.

```text
Primary ❌
   ↓
Backup ✅
```

---

### 4. Health Checks

Continuously check whether servers and services are healthy.

```text
Health Check
     │
     ├── Server 1 ❌
     └── Server 2 ✅
```

Traffic is sent only to healthy instances.

---

### 5. Circuit Breaker

Stops sending requests to a failing service temporarily.

```text
Service A
   │
   ▼
Circuit Breaker
   │
   X
Service B ❌
```

This prevents cascading failures.

---

# 🌍 Real-World Example

### Payment System

Suppose a payment server fails during a transaction.

A fault-tolerant system can:

```text
Payment Request
      │
      ▼
Payment Server 1 ❌
      │
      ▼
Failover
      │
      ▼
Payment Server 2 ✅
```

The system continues processing requests.

---

# 📊 Fault Tolerance vs Reliability

| Fault Tolerance | Reliability |
|---|---|
| Handles component failures | Performs correctly over time |
| Focuses on surviving failures | Focuses on consistent operation |
| Uses redundancy and failover | Uses monitoring, testing, backups, etc. |

---

# 📈 Advantages

- Higher availability
- Reduced downtime
- Better resilience
- Prevents single points of failure
- Improves user experience

---

# 📉 Challenges

- Higher infrastructure cost
- More complex architecture
- Requires monitoring
- Requires failure detection
- Data consistency can become difficult

---

# 🎯 Interview Keywords

- Fault Tolerance
- Failover
- Redundancy
- Replication
- Health Checks
- Circuit Breaker
- High Availability
- Failure Recovery

---

# ⚠️ Common Mistakes

❌ Assuming redundancy alone guarantees fault tolerance.

❌ Forgetting database failures.

❌ Ignoring network failures.

❌ Not testing failure scenarios.

---

# 🔥 Interview Questions

### ❓ What is Fault Tolerance?

The ability of a system to continue functioning despite component failures.

### ❓ How can fault tolerance be achieved?

Using redundancy, replication, failover, health checks, and circuit breakers.

### ❓ What is Failover?

Automatically switching from a failed component to a healthy backup.

### ❓ Why is redundancy important?

Because it provides alternative components when the primary component fails.

---

# 🧠 Quick Revision

```text
Component Failure
       ↓
Failure Detection
       ↓
Failover / Backup
       ↓
System Continues
```

✅ Redundancy  
✅ Replication  
✅ Failover  
✅ Health Checks  
✅ Circuit Breaker

---

# 🎉 Key Takeaway

**Fault tolerance allows a system to continue operating even when individual components fail.**