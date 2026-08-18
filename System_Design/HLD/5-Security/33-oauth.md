# 🔐 OAuth

---

# 📖 Introduction

OAuth is an authorization framework that allows an application to access a user's resources **without requiring the application to know the user's password**.

It is commonly used for:

- Google Login
- GitHub Login
- Facebook Login
- Third-party API access

---

# 📌 Definition

> **OAuth allows a user to grant limited access to their resources to an application without sharing their credentials with that application.**

---

# ⚙️ Basic OAuth Flow

```text
User
 │
 ▼
Application
 │
 ▼
OAuth Provider
 │
 │ User Login + Consent
 ▼
Authorization Code
 │
 ▼
Application
 │
 ▼
Access Token
 │
 ▼
Protected Resource
```

---

# 🧠 Key Components

### Resource Owner

The user who owns the data.

### Client

The application requesting access.

### Authorization Server

Authenticates the user and issues tokens.

### Resource Server

Stores the protected resources and validates access tokens.

---

# 🌍 Real-World Example

Suppose an application provides:

```text
Continue with Google
```

Instead of giving the application your Google password:

```text
Application
     ↓
Google
     ↓
User Login + Consent
     ↓
Access Token
     ↓
Application
```

The application can access only the resources allowed by the granted permissions.

---

# 🔑 Access Token

An access token represents permission to access protected resources.

Example:

```text
Application
    ↓
Access Token
    ↓
Google API
    ↓
Allowed Resource
```

The application does not need the user's Google password.

---

# 📊 OAuth vs JWT

| OAuth | JWT |
|---|---|
| Authorization framework | Token format |
| Defines authorization flows | Represents claims |
| Used for delegated access | Can be used for authentication/authorization |
| Often uses access tokens | JWT can be an access token format |

> OAuth and JWT are not the same thing. OAuth can use JWTs, but OAuth itself is an authorization framework.

---

# 🔐 OAuth 2.0 Authorization Code Flow

A common flow for web applications is:

```text
User
 │
 ▼
Client Application
 │
 ▼
Authorization Server
 │
 ▼
User Consent
 │
 ▼
Authorization Code
 │
 ▼
Client
 │
 ▼
Token Endpoint
 │
 ▼
Access Token
```

The client then uses the access token to access permitted resources.

---

# 🎯 Scopes

Scopes limit what an application can access.

Example:

```text
read:profile
read:email
write:posts
```

The user can grant only the permissions required by the application.

---

# ✅ Advantages

- Password is not shared with the application
- Supports delegated access
- Fine-grained permissions through scopes
- Works well with third-party services
- Standardized authorization flows

---

# ❌ Challenges

- More complex than basic authentication
- Token management is required
- Incorrect configuration can create security vulnerabilities
- Requires careful scope management

---

# 🎯 Interview Keywords

- OAuth
- OAuth 2.0
- Authorization Server
- Resource Server
- Client
- Resource Owner
- Access Token
- Authorization Code
- Scope
- Delegated Access

---

# 🔥 Interview Questions

### ❓ What is OAuth?

An authorization framework that allows applications to access protected resources without receiving the user's password.

### ❓ Is OAuth authentication?

OAuth primarily addresses **authorization**. Authentication is commonly handled using related identity protocols such as OpenID Connect.

### ❓ What is an Access Token?

A credential that represents the permissions granted to a client for accessing protected resources.

### ❓ What are scopes?

Scopes define the specific permissions granted to an application.

### ❓ OAuth vs JWT?

OAuth is an authorization framework, while JWT is a token format.

---

# 🧠 Quick Revision

```text
User
 ↓
Application
 ↓
OAuth Provider
 ↓
Consent
 ↓
Authorization Code
 ↓
Access Token
 ↓
Protected Resource
```

✅ Delegated access  
✅ Password not shared  
✅ Scope-based permissions  
✅ Common for third-party login/access

---

# 🎉 Key Takeaway

**OAuth allows applications to obtain limited access to protected resources without requiring the user's password.**