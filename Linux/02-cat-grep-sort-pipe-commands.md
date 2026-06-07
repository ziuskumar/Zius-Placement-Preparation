# 02. cat, grep, sort & pipe Commands

## 📌 Introduction

Linux provides powerful commands for viewing, searching, filtering, and processing text files.

These commands are widely used in Linux administration, DevOps, and backend development.

---

# 1️⃣ cat Command

## Definition

`cat` stands for concatenate.

It is used to:

* Display file contents
* Create files
* Combine multiple files

---

## Display File Content

```bash
cat notes.txt
```

### Output

```bash
Linux Commands
```

---

## Create File

```bash
cat > notes.txt
```

Press:

```bash
CTRL + D
```

to save the file.

---

## Combine Multiple Files

```bash
cat file1.txt file2.txt
```

---

# 2️⃣ grep Command

## Definition

`grep` searches for patterns or words inside files.

---

## Search Word

```bash
grep Linux notes.txt
```

---

## Ignore Case

```bash
grep -i linux notes.txt
```

---

## Show Line Numbers

```bash
grep -n Linux notes.txt
```

---

## Count Matches

```bash
grep -c error logfile.txt
```

---

# 3️⃣ sort Command

## Definition

The `sort` command arranges file contents alphabetically or numerically.

---

## Alphabetical Sort

```bash
sort names.txt
```

---

## Reverse Sort

```bash
sort -r names.txt
```

---

## Numeric Sort

```bash
sort -n marks.txt
```

---

# 4️⃣ Pipe Operator ( | )

## Definition

The pipe operator transfers output from one command to another command as input.

---

## Example 1

```bash
cat notes.txt | grep Linux
```

---

## Example 2

```bash
cat names.txt | sort
```

---

# Real World Examples

## Search Error Logs

```bash
cat logfile.txt | grep ERROR
```

---

## Sort Usernames

```bash
cat users.txt | sort
```

---

# 🎯 Interview Keywords

* Text Processing
* Pattern Matching
* Stream Processing
* Standard Input
* Standard Output
* Pipe Operator

---

# 📝 Quick Revision

* cat → Display file content
* grep → Search patterns
* sort → Sort data
* pipe (`|`) → Connect commands
* grep -i → Ignore case
* grep -n → Show line numbers
* sort -r → Reverse sorting
