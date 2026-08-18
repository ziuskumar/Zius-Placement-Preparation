# 🔑 JSON Web Token (JWT)

---

# 📖 Introduction

JWT is a compact token format commonly used to represent authenticated users between a client and a server.

It is commonly used for:

- Authentication
- API authorization
- Stateless sessions
- Service-to-service communication

---

# 📌 Definition

> **JWT is a compact, URL-safe token format used to securely transmit claims between parties.**

A JWT has three parts:

```text
Header.Payload.Signature
```

---

# 🧩 JWT Structure

```text
JWT
 │
 ├── Header
 ├── Payload
 └── Signature
```

### 1. Header

Contains information about the token type and signing algorithm.

Example:

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

### 2. Payload

Contains claims about the user or token.

Example:

```json
{
  "userId": "123",
  "role": "user"
}
```

### 3. Signature

Used to verify that the token has not been modified.

```text
Header + Payload
       ↓
    Secret Key
       ↓
   Signature
```

---

# ⚙️ JWT Authentication Flow

```text
User
 │
 │ Login
 ▼
Server
 │
 │ Verify Credentials
 ▼
Create JWT
 │
 ▼
Client
 │
 │ Send JWT
 ▼
Protected API
 │
 ▼
Verify JWT
 │
 ├── Valid → Allow ✅
 └── Invalid → Reject ❌
```

---

# 🧠 Example

Client sends:

```http
Authorization: Bearer <JWT>
```

The server verifies the token and identifies the user.

---

# 🔐 JWT vs Session

| JWT | Session |
|---|---|
| Token contains claims | Server stores session state |
| Often stateless | Stateful |
| Easy to use across services | Requires shared session storage when scaled |
| Token must be protected | Session ID must be protected |
| Revocation can be harder | Revocation is generally easier |

---

# ⚠️ Security Considerations

### Never store sensitive information in the payload

JWT payloads are encoded, not automatically encrypted.

❌ Do not put:

```text
Password
Credit Card Number
Secrets
```

inside the payload.

### Protect the token

Use:

- HTTPS
- Short expiration times
- Secure storage
- Strong signing secrets/keys

---

# ⏳ Token Expiration

JWTs can contain an expiration claim:

```json
{
  "userId": "123",
  "exp": 1234567890
}
```

After expiration, the token should no longer be accepted.

---

# 🌍 Real-World Example

A frontend calls:

```text
GET /api/profile
```

with:

```text
Authorization: Bearer JWT
```

The backend:

```text
Receive Token
     ↓
Verify Signature
     ↓
Check Expiration
     ↓
Identify User
     ↓
Return Profile
```

---

# 🎯 Interview Keywords

- JWT
- Header
- Payload
- Signature
- Claims
- Stateless Authentication
- Bearer Token
- Expiration
- Signing Key

---

# 🔥 Interview Questions

### ❓ What are the three parts of JWT?

```text
Header
Payload
Signature
```

### ❓ Is JWT encrypted?

Not by default. JWTs are commonly signed and encoded.

### ❓ Why is the signature important?

It allows the server to verify that the token has not been modified.

### ❓ Where is JWT commonly sent?

Usually through the HTTP Authorization header:

```text
Authorization: Bearer <token>
```

### ❓ What happens when a JWT expires?

The server rejects the expired token and the client needs to authenticate again or use an appropriate refresh-token flow.

---

# 🧠 Quick Revision

```text
JWT
 │
 ├── Header
 ├── Payload
 └── Signature

Client
  ↓
Bearer Token
  ↓
Server
  ↓
Verify
  ↓
Allow / Reject
```

✅ Compact  
✅ Commonly stateless  
✅ Signed  
❌ Payload is not automatically encrypted

---

# 🎉 Key Takeaway

**JWT provides a compact way to represent authentication claims that a server can verify without storing the complete authentication state inside the token.**