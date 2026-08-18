# 🛡️ Authorization

---

# 📖 Introduction

Authorization determines **what an authenticated user is allowed to do**.

It answers:

> **"What are you allowed to access?"**

Authentication verifies identity, while authorization verifies permissions.

---

# 📌 Definition

> **Authorization is the process of determining whether an authenticated user has permission to access a resource or perform an action.**

---

# ⚙️ How It Works

```text
User
 │
 ▼
Authentication
 │
 ▼
Identity Verified
 │
 ▼
Authorization
 │
 ├── Allowed ✅
 │
 └── Denied ❌
```

---

# 🧠 Example

Suppose an application has two users:

```text
Admin
User
```

Admin:

```text
Create User      ✅
Delete User      ✅
View Dashboard   ✅
```

Normal User:

```text
Create User      ❌
Delete User      ❌
View Dashboard   ✅
```

Authorization decides these permissions.

---

# 🔐 Authentication vs Authorization

| Authentication | Authorization |
|---|---|
| Verifies identity | Verifies permissions |
| "Who are you?" | "What can you do?" |
| Happens during login | Happens when accessing resources |
| Uses credentials | Uses roles/permissions |

```text
Authentication → Identity
Authorization  → Permission
```

---

# 🏗️ Common Authorization Models

### 1. RBAC — Role-Based Access Control

Permissions are assigned based on roles.

```text
Admin
 ├── Create
 ├── Read
 ├── Update
 └── Delete

User
 └── Read
```

---

### 2. Permission-Based Access

Users are directly assigned specific permissions.

```text
User
 ├── read_posts
 └── create_posts
```

---

# 🌍 Real-World Example

### E-Commerce Admin Panel

```text
User Login
    ↓
Authentication ✅
    ↓
Check Role
    ↓
Admin?
 ┌──┴──┐
Yes   No
 ↓     ↓
Allow  Deny
```

Only authorized administrators can access sensitive management operations.

---

# 🚨 HTTP Status Code

When a user is authenticated but does not have permission:

```text
403 Forbidden
```

Example:

```text
Authenticated User
        ↓
Permission Check
        ↓
No Permission
        ↓
403 Forbidden
```

---

# ✅ Advantages

- Protects sensitive resources
- Controls user permissions
- Supports role-based access
- Prevents unauthorized actions
- Helps implement least privilege

---

# ⚠️ Common Mistakes

❌ Confusing authentication with authorization.

❌ Checking only authentication and ignoring permissions.

❌ Giving every user admin privileges.

❌ Performing authorization checks only on the frontend.

> Authorization must be enforced on the server/backend.

---

# 🎯 Interview Keywords

- Authorization
- RBAC
- Permissions
- Roles
- Access Control
- Least Privilege
- 403 Forbidden

---

# 🔥 Interview Questions

### ❓ What is Authorization?

Authorization determines whether an authenticated user has permission to perform an action or access a resource.

### ❓ Authentication vs Authorization?

```text
Authentication → Who are you?
Authorization   → What can you do?
```

### ❓ What status code represents insufficient permission?

```text
403 Forbidden
```

### ❓ What is RBAC?

**Role-Based Access Control** assigns permissions based on a user's role.

---

# 🧠 Quick Revision

```text
Authentication
      ↓
Who are you?
      ↓
Authorization
      ↓
What can you do?
      ↓
Allow / Deny
```

✅ Identity → Authentication  
✅ Permission → Authorization  
✅ Roles → RBAC  
✅ No permission → 403

---

# 🎉 Key Takeaway

**Authorization controls what an authenticated user is allowed to access or perform.**