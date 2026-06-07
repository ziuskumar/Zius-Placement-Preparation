# 05. Processes, Users & SSH

## 📌 Processes

A process is a running program in Linux.

---

# 1️⃣ ps Command

## Definition

Displays running processes.

---

## Example

```bash
ps
```

---

## Detailed Processes

```bash
ps -aux
```

---

# 2️⃣ top Command

## Definition

Displays real-time system processes.

---

## Example

```bash
top
```

---

# 3️⃣ kill Command

## Definition

Terminates a process using PID.

---

## Example

```bash
kill PID
```

---

# 4️⃣ User Management

## Add User

```bash
sudo adduser lucky
```

---

## Switch User

```bash
su lucky
```

---

## Current User

```bash
whoami
```

---

# 5️⃣ SSH

## Definition

SSH (Secure Shell) enables secure remote login between systems.

---

## Connect Remote Server

```bash
ssh user@ip-address
```

Example:

```bash
ssh ubuntu@192.168.1.10
```

---

# SSH Features

* Secure communication
* Remote access
* Remote command execution

---

# 🎯 Interview Keywords

* Process
* PID
* SSH
* Remote Access
* User Management
* Process Management

---

# 📝 Quick Revision

* ps → Show processes
* top → Real-time monitoring
* kill → Stop process
* adduser → Create user
* whoami → Current user
* ssh → Remote login
