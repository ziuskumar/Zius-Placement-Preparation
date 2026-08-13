# 🔧 Reliability

---

# 📖 Introduction

Reliability describes how consistently a system performs its intended functions correctly over a period of time.

A reliable system should continue working correctly and recover from failures without producing incorrect results.

---

# 📌 Definition

> **Reliability is the ability of a system to perform its intended function correctly and consistently for a specified period under defined conditions.**

---

# ⚙️ How to Improve Reliability

```text
              System
                 │
        ┌────────┼────────┐
        ▼        ▼        ▼
   Redundancy  Backup   Monitoring
        │        │        │
        └────────┼────────┘
                 ▼
          Reliable System
```

Common techniques:

- Redundancy
- Replication
- Backups
- Health checks
- Monitoring
- Retries
- Fault isolation
- Disaster recovery

---

# 🧠 Reliability vs Availability

| Reliability | Availability |
|---|---|
| System performs correctly | System remains accessible |
| Focuses on correct operation | Focuses on uptime |
| Measures failure-free operation | Measures operational time |
| Can fail functionally | Can be available but produce incorrect results |

### Example

A payment service may be:

```text
Available ✅
     ↓
Accepts requests
     ↓
Charges wrong amount ❌
```

The service is available but not reliable.

---

# 🌍 Real-World Example

### Payment System

A reliable payment system should:

```text
Payment Request
      ↓
Process Payment
      ↓
Store Transaction
      ↓
Return Correct Result
```

Even if a temporary failure occurs, the system should avoid:

- Duplicate payments
- Lost transactions
- Incorrect balances

---

# 📈 Reliability Techniques

### 1. Redundancy

Use multiple instances so one failure does not stop the system.

### 2. Replication

Maintain copies of important data or services.

### 3. Monitoring

Detect failures and abnormal behavior.

### 4. Retry

Retry temporary failures carefully.

### 5. Backup

Maintain recoverable copies of important data.

---

# ⚠️ Common Mistakes

❌ Assuming high availability automatically means high reliability.

❌ Ignoring data corruption or incorrect results.

❌ Retrying requests without considering duplicate operations.

❌ Relying on a single component.

---

# 🎯 Interview Keywords

- Reliability
- Failure Rate
- Redundancy
- Replication
- Backup
- Monitoring
- Recovery
- Fault Isolation
- Disaster Recovery

---

# 🔥 Interview Questions

### ❓ What is Reliability?

The ability of a system to perform its intended functions correctly and consistently over time.

### ❓ What is the difference between Reliability and Availability?

Availability focuses on whether the system is accessible, while reliability focuses on whether it performs correctly and consistently.

### ❓ How can reliability be improved?

Using redundancy, replication, backups, monitoring, retries, and fault isolation.

### ❓ Can a system be available but unreliable?

Yes. A system can be running and accepting requests while producing incorrect results.

---

# 🧠 Quick Revision

```text
Reliability
     ↓
Correct Operation
     ↓
Consistent Results
     ↓
Over Time
```

✅ Correctness  
✅ Consistency  
✅ Failure handling  
✅ Recovery

---

# 🎉 Key Takeaway

**Reliability means the system continues to perform its intended functions correctly and consistently over time.**