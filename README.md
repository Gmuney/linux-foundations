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

> Mindset Shift: The Terminal is like talking to the building manager with a walkie-talkie instead of using the elevator buttons. It's direct, fast, and gives you total control.
