# linux-foundations
My Journey from windows user to power user through labs and automation.
# Linux Learning & Automation
Documenting my path from a Windows user to a Linux power user.

## Current Focus
* Mastering the Command Line (CLI)
* Writing Bash Scripts to automate daily tasks
* Managing system processes and Cron jobs

## 📅 Learning Log

### Day 1: Navigation & File Basics
Goal: Master the "Command Center" and learn to navigate the Linux directory tree.

#### 1. Navigation ("Moving through the house")
* pwd — Print Working Directory: "Where am I right now?"
* ls — List: "Show me what's in this room."
* ls -la — List All: Shows hidden files and detailed info.
* cd — Change Directory: "Move to a different room/folder."
* cd .. — Go Back: Move up one level in the folder hierarchy.

#### 2. File Operations
* mkdir — Make Directory: Create a new folder.
* touch — Create a new empty file.
* nano — A simple command-line text editor.
* cat — Read the contents of a file without opening an editor.
* rm — Remove/Delete a file.

> Mindset Shift: Linux isn't just a black screen; it's a structure of "rooms" (folders) and "items" (files). Moving away from the mouse and into the keyboard is the first step toward automation.

---

### Day 2: Getting Useful & Managing the "Building"
Goal: Learn to install tools, manage files, and set "keys" (permissions) for different rooms.

#### 1. System Maintenance & Installations
* sudo apt update && sudo apt upgrade -y — The "General Maintenance" command to keep the system current.
* sudo apt install [tool] — Install new utility programs (e.g., htop, tree).

#### 2. File Management (The "Furniture" Move)
* cp — Copy: Create a backup or duplicate of a file.
* mv — Move: Used to relocate a file or rename it.
* tree — A visual map of every folder and file in your current directory.

#### 3. Permissions (The "Keys")
* ls -l — Detailed list showing who owns a file and what they can do with it.
* chmod 600 — Private: Only you can read/edit.
* chmod 755 — Public/Shared: You can change it, others can only read or use it.

| Concept | Real Life Analogy | Linux Command |
| :--- | :--- | :--- |
| Moving/Renaming | Moving furniture or relabeling boxes | mv |
| Copying | Making a photocopy of important papers | cp |
| Permissions | Who has keys to which rooms | chmod, ls -l |
| Installing Apps | Ordering new furniture or appliances | apt install |

Absolutely — here’s a clean, professional GitHub-ready version you can paste directly into a repo README or a notes file.

---

# 📘 Linux Text Processing & Regex — Day 3 Notes

## 🧭 Overview

This repository documents my early-stage Linux learning journey focused on:

* Text processing tools (`grep`, `sed`, `awk`)
* Regular expressions (regex)
* Command chaining and pipelines
* Foundational system thinking in Linux environments

At this stage, the goal is to move from learning individual commands to building **problem-solving workflows using Linux tools**.

---

# 🧠 Core Skills Learned

## 🔍 grep (searching text)

`grep` is used to search for patterns in files.

### Basic usage:

```bash
grep "error" file.txt
```

### With regex:

```bash
grep "error.*failed" logfile.txt
```

### Common patterns:

* `^error` → lines starting with "error"
* `failed$` → lines ending with "failed"
* `[0-9]` → lines containing numbers
* `.*` → matches anything

---

## ✏️ sed (stream editor)

`sed` is used to modify text streams.

### Replace text:

```bash
sed 's/error/warning/' file.txt
```

### Global replace:

```bash
sed 's/error/warning/g' file.txt
```

### Delete lines:

```bash
sed '/error/d' file.txt
```

---

## 📊 awk (text processing & filtering)

`awk` is used for structured data extraction.

### Print full file:

```bash
awk '{print}' file.txt
```

### Print specific column:

```bash
awk '{print $1}' file.txt
```

### Filter rows:

```bash
awk '$3 > 50 {print $1, $3}' file.txt
```

---

# 🔗 Pipelines (Command Chaining)

Linux allows commands to be chained using pipes:

```bash
command1 | command2 | command3
```

### Example:

```bash
cat log.txt | grep "error" | awk '{print $5}'
```

### Real-world pattern:

```bash
cat auth.log | grep "Failed password" | awk '{print $11}' | sort | uniq -c
```

This helps identify:

* Failed login attempts
* IP address frequency
* System activity patterns

---

# 🧩 Regex Fundamentals

Regex (Regular Expressions) is used to define search patterns.

## Core Symbols

| Symbol  | Meaning                               |
| ------- | ------------------------------------- |
| `.`     | Any single character                  |
| `*`     | Repeat previous character (0 or more) |
| `.*`    | Anything (wildcard match)             |
| `[abc]` | Match a, b, or c                      |
| `[0-9]` | Any number                            |
| `^`     | Start of line                         |
| `$`     | End of line                           |

---

## Example Patterns

### Match lines starting with "error":

```regex
^error
```

### Match lines ending with "failed":

```regex
failed$
```

### Match "error" followed by anything then "failed":

```regex
error.*failed
```

---

# 🔥 Real Linux Use Cases

## Log analysis:

```bash
grep "Failed password" /var/log/auth.log
```

## Process filtering:

```bash
ps aux | grep nginx
```

## File searching:

```bash
find /var/log -name "*.log"
```

## Combined workflow:

```bash
find /var/log -name "*.log" | xargs grep "error"
```

---

# 🧠 Key Concept Shift

At this stage, Linux is no longer about individual commands.

It becomes:

> A system for transforming and analyzing text using composable tools.

The real power comes from combining tools using pipelines.

---

# 🚀 Next Steps

Planned learning progression:

### Phase 1 (current)

* grep
* sed
* awk
* regex basics

### Phase 2

* pipelines mastery
* find / xargs
* log analysis patterns

### Phase 3

* bash scripting
* automation
* cron jobs

### Phase 4

* system administration basics
* networking tools (`curl`, `ss`, `netstat`)
* permissions & users

---

# 📌 Summary

This stage represents the transition from learning Linux commands individually to building **real workflows for solving system problems** using text processing tools.

---

If you want next, I can also:

* turn this into a **full GitHub README with badges + structure**
* or build you a **Day 4 repo (log analysis challenge lab)** where you simulate real server incidents
* or convert this into a **portfolio-style learning journal format**


> Mindset Shift: The Terminal is like talking to the building manager with a walkie-talkie instead of using the elevator buttons. It's direct, fast, and gives you total control.
