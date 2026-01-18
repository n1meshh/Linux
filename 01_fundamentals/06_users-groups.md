# Linux Users & Groups 👥

Linux is a **multi-user system**.  
Understanding **users and groups** is **mandatory for DevOps**, because permissions, access control, and server management depend on them.

---

## 1️⃣ Users

### Types of Users
1. **Root User (Superuser)**
   - UID = 0  
   - Full privileges (can read/write/execute anything)  
   - Example: system administrator

2. **Normal User**
   - Limited privileges  
   - Cannot modify system files  
   - Example: developer, tester

3. **System / Service User**
   - Created by Linux for system services  
   - Usually no login  
   - Example: `www-data`, `mysql` 

---

### Commands for Users

```bash
whoami                     # Show current user
id                         # Show UID, GID, groups of current user
useradd nimesh             # Create new user
passwd nimesh              # Set password for user
usermod -aG docker nimesh  # Add user to group
deluser nimesh             # Delete user




2️⃣ Groups

Group = collection of users

Helps manage permissions efficiently

Each user belongs to at least one group

Important Files
File	Purpose
/etc/passwd	Stores user info (username, UID, home directory)
/etc/group	Stores group info
/etc/shadow	Stores encrypted passwords
/etc/sudoers	Users with sudo privileges
Commands for Groups
groups                     # Show groups for current user
groupadd devops            # Create new group
gpasswd -a nimesh devops   # Add user to group
delgroup devops            # Delete group

# 👥 Linux Users & Groups — Clean & Practical Guide

Linux is a **multi-user operating system**.  
Understanding **users & groups** is essential for DevOps, SysAdmin, and server security because permissions, access control, and resource isolation depend on them.

---

## 1️⃣ Users

Linux has different user types based on privilege levels:

### 🔹 **Root User (Superuser)**
- UID = `0`
- Full privileges (read/write/execute anywhere)
- Can install packages, manage system files, configure servers

### 🔹 **Normal User**
- Limited privileges
- Cannot modify system files
- Example: developer, tester, analyst

### 🔹 **System / Service Users**
- Created by Linux/services internally
- Often used by daemons
- Login not required
- Examples: `www-data`, `mysql`, `docker`

---

## 📌 Commands for User Management

```bash
whoami                     # Display current user
id                         # Show UID, GID, group info
useradd nimesh             # Create a new user
passwd nimesh              # Set user password
usermod -aG docker nimesh  # Add user to group
deluser nimesh             # Delete a user
```

---

## 2️⃣ Groups

A **group** = collection of users.  
Groups are used for shared permissions and access control.

Each user belongs to at least **one primary group**, and optionally multiple **supplementary groups**.

---

## 📁 Important System Files

| File | Purpose |
|---|---|
| `/etc/passwd` | User info (username, UID, shell, home) |
| `/etc/group` | Group names & GIDs |
| `/etc/shadow` | Encrypted passwords |
| `/etc/sudoers` | Defines sudo privileges |

---

## 📌 Commands for Group Management

```bash
groups                     # Show groups for current user
groupadd devops            # Create new group
gpasswd -a nimesh devops   # Add user to group
delgroup devops            # Delete group
```

---

## 🔐 Why This Matters in DevOps?

✔ Controls access to servers  
✔ Manages deployment permissions  
✔ Restricts unauthorized changes  
✔ Used heavily in Docker, Kubernetes, CI/CD, SSH, and automation



