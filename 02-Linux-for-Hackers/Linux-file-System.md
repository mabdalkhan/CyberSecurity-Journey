# Linux File System and Basic Terminal Commands

## Introduction

The Linux file system organizes files and directories in a hierarchical structure starting from the **root directory (`/`)**. Understanding the file system and mastering basic terminal commands are essential skills for system administration, cybersecurity, and ethical hacking.

---

## Why This Topic Matters

Learning the Linux file system and terminal helps you:

- Navigate Linux efficiently
- Manage files and directories
- Use cybersecurity tools effectively
- Automate tasks using the command line
- Build a strong foundation for penetration testing

---

## Learning Objectives

After studying this topic, you should be able to:

- Understand the Linux directory structure
- Navigate the file system using the terminal
- Create, copy, move, and delete files
- View file contents
- Understand file permissions at a basic level

---

## Key Concepts

### Root Directory (`/`)

The root directory is the top-level directory from which all other directories branch.

---

### Common Linux Directories

| Directory | Purpose |
|-----------|---------|
| `/` | Root directory |
| `/home` | User home directories |
| `/root` | Root user's home directory |
| `/bin` | Essential user commands |
| `/etc` | System configuration files |
| `/var` | Variable data (logs, cache) |
| `/tmp` | Temporary files |
| `/usr` | User programs and libraries |
| `/opt` | Optional software packages |
| `/dev` | Device files |
| `/proc` | Process and kernel information |

---

## Short Explanation

Unlike Windows, Linux uses a **single directory tree** that starts at `/`. Every file, directory, storage device, and mounted partition becomes part of this unified structure.

Most interactions with Linux happen through the **terminal**, where commands allow you to navigate, manage files, and administer the system quickly.

---

## Mermaid Diagram

```mermaid
flowchart TD
A[/ Root]
A --> B[/home]
A --> C[/etc]
A --> D[/usr]
A --> E[/var]
A --> F[/tmp]
A --> G[/bin]
A --> H[/dev]
A --> I[/proc]
```

---

## Practical Examples

### Check Current Directory

```bash
pwd
```

Displays your current working directory.

---

### List Files

```bash
ls
```

Lists files and folders.

Useful options:

```bash
ls -l
```

Long listing format.

```bash
ls -la
```

Shows hidden files as well.

---

### Change Directory

```bash
cd Documents
```

Move into the `Documents` directory.

```bash
cd ..
```

Move up one directory.

```bash
cd ~
```

Go to your home directory.

---

### Create a Directory

```bash
mkdir Projects
```

Creates a new folder named `Projects`.

---

### Create an Empty File

```bash
touch notes.txt
```

Creates an empty file.

---

### Copy Files

```bash
cp notes.txt backup.txt
```

Copies a file.

---

### Move or Rename Files

```bash
mv notes.txt Documents/
```

Moves a file.

```bash
mv old.txt new.txt
```

Renames a file.

---

### Delete Files

```bash
rm notes.txt
```

Deletes a file.

Delete a directory recursively:

```bash
rm -r foldername
```

---

### View File Contents

```bash
cat notes.txt
```

Displays the entire file.

```bash
less notes.txt
```

Views large files page by page.

---

### Display Command History

```bash
history
```

Shows previously executed commands.

---

### Clear the Terminal

```bash
clear
```

Clears the terminal screen.

---

### Display Manual Pages

```bash
man ls
```

Opens the manual for the `ls` command.

> **Tip**
>
> Press **q** to exit the manual page.

---

## Best Practices

- Use absolute paths when scripting.
- Verify your current directory before deleting files.
- Use `man` to learn command options.
- Organize files into meaningful directories.
- Practice commands in a test environment.

> **Warning**
>
> Commands like `rm -r` permanently delete files. Double-check the target before executing them.

---

## Common Mistakes

- Confusing `/` (root) with `/root` (administrator's home directory).
- Forgetting to use `sudo` when administrative privileges are required.
- Accidentally deleting important files with `rm`.
- Using incorrect file paths.
- Ignoring hidden files that begin with a `.`

---

## Summary

The Linux file system provides a structured way to organize data, while the terminal offers a fast and powerful interface for interacting with the operating system. Mastering basic commands is the foundation for system administration, ethical hacking, and cybersecurity.

---

## Key Takeaways

- Linux uses a hierarchical directory structure starting at `/`.
- The terminal is the primary interface for many administrative tasks.
- Commands like `ls`, `cd`, `pwd`, `mkdir`, `cp`, `mv`, and `rm` are essential.
- Always verify file paths before modifying or deleting files.
- Practice regularly to build command-line confidence.

---

## Practice Questions

1. What is the purpose of the root (`/`) directory?
2. What is the difference between `cp` and `mv`?
3. Which command displays your current directory?
4. How do you list hidden files?
5. Why should you be careful when using `rm -r`?

---

## Useful Resources

- Linux Documentation Project (TLDP)
- Debian Documentation
- Kali Linux Documentation
- TryHackMe – Linux Fundamentals
- Hack The Box Academy – Linux Fundamentals

---

## Suggested Next Topic

**Linux File Permissions and Ownership (chmod, chown, and umask)**
