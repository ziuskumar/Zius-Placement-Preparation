# 01. Linux Filesystem & Navigation

## 📌 What is Linux?

Linux is an open-source operating system widely used in servers, cloud computing, DevOps, and software development.

Most production servers run Linux.

---

# Important Directories

## Root Directory

```bash
/
```

The top-most directory in Linux.

Everything starts from here.

---

## Home Directory

```bash
/home
```

Stores user files.

Example:

```bash
/home/lucky
```

---

## Configuration Files

```bash
/etc
```

Contains system configuration files.

---

## Log Files

```bash
/var/log
```

Stores application and system logs.

---

## Temporary Files

```bash
/tmp
```

Stores temporary files.

---

# Linux Navigation Commands

## pwd

Print Working Directory.

Shows your current location.

```bash
pwd
```

Example Output:

```bash
/home/lucky
```

---

## ls

Lists files and directories.

```bash
ls
```

---

### Detailed List

```bash
ls -l
```

---

### Hidden Files

```bash
ls -a
```

---

## cd

Change Directory.

```bash
cd Documents
```

Move into Documents folder.

---

### Go Back One Directory

```bash
cd ..
```

---

### Go Home

```bash
cd ~
```

---

# Directory Operations

## mkdir

Create Directory.

```bash
mkdir Linux
```

---

## rm

Delete File.

```bash
rm file.txt
```

---

## Remove Directory

```bash
rm -r Linux
```

---

# File Operations

## cp

Copy Files.

```bash
cp source.txt destination.txt
```

---

## mv

Move or Rename Files.

Rename:

```bash
mv file1.txt file2.txt
```

Move:

```bash
mv file.txt Documents/
```

---

## cat

Display File Content.

```bash
cat notes.txt
```

---

## less

View Large Files Page by Page.

```bash
less logfile.txt
```

Exit:

```bash
q
```

---

## man

Display Manual Pages.

```bash
man ls
```

Shows detailed documentation for commands.

---

# Interview Keywords

* Root Directory
* Home Directory
* Absolute Path
* Relative Path
* File Permissions
* Linux Shell
* Command Line Interface (CLI)

---

# Common Interview Questions

### Difference between Absolute and Relative Path?

Absolute:

```bash
/home/lucky/Documents
```

Relative:

```bash
Documents
```

---

### Difference between cp and mv?

cp → Copies file

mv → Moves or renames file

---

# Practice Commands

```bash
pwd

mkdir Linux_Practice

cd Linux_Practice

touch notes.txt

ls

cat notes.txt

cd ..

rm -r Linux_Practice
```

---

# Quick Revision

* pwd → Current directory
* ls → List files
* cd → Change directory
* mkdir → Create directory
* rm → Delete file/directory
* cp → Copy files
* mv → Move/Rename files
* cat → Display file content
* less → View large files
* man → Help documentation
