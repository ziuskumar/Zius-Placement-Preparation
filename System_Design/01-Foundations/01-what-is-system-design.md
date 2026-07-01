# 01. What is System Design?

---

# 📖 Introduction

Every application you use today—such as WhatsApp, Instagram, Netflix, Amazon, or Google—serves millions or even billions of users. Designing software that remains fast, reliable, secure, and scalable under such massive demand is the goal of **System Design**.

System Design is one of the most important subjects for Software Development Engineer (SDE) interviews because it tests how well you can build software beyond writing code.

---

# 📌 Definition

> **System Design is the process of designing the architecture, components, modules, databases, APIs, and infrastructure of a software system to satisfy functional and non-functional requirements.**

It answers questions like:

- How should the application be structured?
- How should data be stored?
- How should users communicate with the server?
- How can millions of users be supported simultaneously?
- How can failures be handled gracefully?

---

# ❓ Why Does System Design Exist?

As applications grow, a single server is no longer enough.

Without proper system design:

- ❌ Server crashes
- ❌ Slow response times
- ❌ Database overload
- ❌ Downtime
- ❌ Poor user experience

System Design helps solve these challenges before they become problems.

---

# ⚙️ What Does a System Designer Do?

A system designer decides:

- Overall architecture
- Database selection
- Communication methods
- Caching strategy
- Load balancing
- Scalability approach
- Security mechanisms
- Fault tolerance

---

# 🏛️ High-Level Design (HLD)

High-Level Design focuses on the overall architecture of the system.

It defines:

- Components
- Servers
- Databases
- APIs
- Load Balancers
- Caches
- External Services

### Example

```text
User
   │
   ▼
Load Balancer
   │
   ▼
Application Servers
   │
   ▼
Database
```

---

# 🔧 Low-Level Design (LLD)

Low-Level Design focuses on implementation details.

It includes:

- Classes
- Objects
- Functions
- Design Patterns
- Relationships
- Data Structures

### Example

```java
class User {

    int id;
    String name;
    String email;

}
```

---

# 📊 High-Level Design vs Low-Level Design

| High-Level Design (HLD) | Low-Level Design (LLD) |
|--------------------------|------------------------|
| Defines overall architecture | Defines implementation details |
| Components | Classes |
| Servers | Objects |
| Databases | Methods |
| APIs | Algorithms |
| Scalability | Code Structure |

---

# 🏗️ Basic System Design Flow

```text
              User
                │
                ▼
          Internet
                │
                ▼
         Load Balancer
                │
      ┌─────────┴─────────┐
      ▼                   ▼
 App Server 1        App Server 2
      │                   │
      └─────────┬─────────┘
                ▼
             Database
```

---

# 🌍 Real-World Example

## Instagram Photo Upload

When a user uploads a photo:

1. User sends a request.
2. The request reaches the server.
3. The server authenticates the user.
4. The image is stored in storage.
5. Metadata is saved in the database.
6. Followers receive notifications.
7. The user's feed is updated.

Although it appears simple, many backend services work together behind the scenes.

---

# 💡 Why Companies Ask System Design

Companies evaluate whether you can design software that is:

- Scalable
- Highly Available
- Reliable
- Fault Tolerant
- Performant
- Easy to Maintain

Writing code is only one part of software engineering. Designing systems is equally important.

---

# 📚 Core Components of System Design

- Client
- Server
- Database
- Cache
- Load Balancer
- CDN
- API Gateway
- Message Queue
- Object Storage
- Authentication
- Monitoring

These are the building blocks of almost every modern distributed application.

---

# 🌍 Real-World Applications

| Application | Focus Area |
|-------------|------------|
| WhatsApp | Messaging |
| Instagram | Feed Generation |
| Netflix | Video Streaming |
| Uber | Real-Time Location Tracking |
| Amazon | Order Processing |
| Google Drive | Distributed File Storage |

---

# 🎯 Interview Keywords

- System Design
- High-Level Design (HLD)
- Low-Level Design (LLD)
- Scalability
- Availability
- Reliability
- Latency
- Throughput
- Load Balancer
- Cache
- Distributed Systems
- Fault Tolerance

---

# 🚨 Common Mistakes

- Thinking System Design is only about databases.
- Ignoring scalability requirements.
- Jumping directly into coding.
- Not considering failures.
- Forgetting non-functional requirements.

---

# 🔥 Interview Traps

### Q1. Is System Design only for experienced engineers?

**Answer:** No. Freshers are increasingly asked basic System Design questions during internships and campus placements.

---

### Q2. Does System Design involve coding?

**Answer:** Usually not. It focuses on architecture, design decisions, scalability, and trade-offs rather than writing code.

---

### Q3. What is the first step in designing a system?

**Answer:** Understand the functional and non-functional requirements before selecting technologies or designing the architecture.

---

# 🧠 Quick Revision

- ✅ System Design is the process of designing scalable software systems.
- ✅ It focuses on architecture rather than implementation.
- ✅ HLD defines the overall architecture.
- ✅ LLD defines implementation details.
- ✅ Good System Design improves scalability, reliability, maintainability, and performance.
- ✅ Every large-scale application relies on System Design principles.