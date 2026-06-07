# 04. Linux Repository, Tar, Environment Variables & Regex

## 📌 Linux Repository

A repository stores software packages for installation and updates.

---

# Update Repository

```bash
sudo apt update
```

---

# Install Package

```bash
sudo apt install nginx
```

---

# 1️⃣ tar Command

## Definition

`tar` is used to archive and compress files.

---

## Create Tar File

```bash
tar -cvf archive.tar folder/
```

---

## Extract Tar File

```bash
tar -xvf archive.tar
```

---

# 2️⃣ Environment Variables

## Definition

Environment variables store system-wide configuration values.

---

## View Variables

```bash
printenv
```

---

## Display PATH Variable

```bash
echo $PATH
```

---

## Create Variable

```bash
export NAME=Lucky
```

---

# 3️⃣ Regex (Regular Expressions)

## Definition

Regex is used for pattern matching.

---

## Search Digits

```bash
grep "[0-9]" data.txt
```

---

## Search Alphabets

```bash
grep "[a-z]" data.txt
```

---

## Search Starting Pattern

```bash
grep "^Linux" notes.txt
```

---

# 🎯 Interview Keywords

* Repository
* Package Manager
* tar
* Environment Variable
* PATH Variable
* Regular Expression
* Pattern Matching

---

# 📝 Quick Revision

* apt update → Update repositories
* apt install → Install packages
* tar → Archive/compress files
* printenv → Show variables
* export → Create variable
* regex → Pattern matching
