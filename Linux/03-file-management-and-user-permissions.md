# 03. File Management & User Permissions

## 📌 Introduction

Linux provides commands for creating, copying, moving, deleting files, and managing user permissions.

Permissions help secure files and directories from unauthorized access.

---

# 1️⃣ cp Command

## Definition

`cp` copies files and directories.

---

## Copy File

```bash
cp source.txt destination.txt
```

---

## Copy Directory

```bash
cp -r Folder1 Folder2
```

---

# 2️⃣ mv Command

## Definition

`mv` moves or renames files and directories.

---

## Rename File

```bash
mv old.txt new.txt
```

---

## Move File

```bash
mv notes.txt Documents/
```

---

# 3️⃣ mkdir Command

## Definition

Creates a new directory.

---

## Create Directory

```bash
mkdir Linux
```

---

# 4️⃣ rm Command

## Definition

Deletes files and directories.

---

## Delete File

```bash
rm notes.txt
```

---

## Delete Directory

```bash
rm -r Linux
```

---

# 5️⃣ rmdir Command

## Definition

Deletes empty directories.

---

## Example

```bash
rmdir Test
```

---

# 6️⃣ User Permissions

## Permission Types

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

# View Permissions

```bash
ls -l
```

Example Output:

```bash
-rwxr-xr--
```

---

# Permission Breakdown

```text
Owner   Group   Others
rwx     r-x     r--
```

---

# 7️⃣ chmod Command

## Definition

Changes file permissions.

---

## Example

```bash
chmod 755 script.sh
```

---

# Numeric Permission Table

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |

---

# 8️⃣ chown Command

## Definition

Changes file ownership.

---

## Example

```bash
chown user file.txt
```

---

# 🎯 Interview Keywords

* File Permissions
* chmod
* chown
* Owner
* Group
* Execute Permission

---

# 📝 Quick Revision

* cp → Copy files
* mv → Move/Rename files
* mkdir → Create directory
* rm → Delete files/directories
* chmod → Change permissions
* chown → Change ownership
* rwx → Read, Write, Execute
