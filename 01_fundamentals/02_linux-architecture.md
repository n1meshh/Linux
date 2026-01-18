# Linux Architecture 🐧

## What is Linux Architecture?
Linux architecture bhaneko Linux operating system ko internal structure ho  
jasle hardware ra user bich interaction manage garcha.

---

## Main Components of Linux Architecture

Linux system mainly **4 layers** ma divided huncha:

1. Hardware
2. Kernel
3. Shell
4. Applications

---

## 1️⃣ Hardware Layer
- CPU
- Memory (RAM)
- Disk
- Network devices

👉 Hardware directly user le use garna paudaina.

---

## 2️⃣ Kernel (Core of Linux)
Kernel Linux ko heart ho.

### Kernel ko kaam:
- Process management
- Memory management
- Device management
- File system management
- Network management

👉 Kernel bina Linux chalnai sakdaina.

---

## 3️⃣ Shell
Shell user ra kernel bich ko bridge ho.

### Shell ko kaam:
- User bata command lincha
- Kernel lai execute garna dincha
- Output user lai return garcha

Common shells:
- bash
- sh
- zsh

---

## 4️⃣ Applications / User Space
- System commands (ls, cd, grep)
- User installed software
- DevOps tools (Docker, Git, Jenkins)

---

## System Calls
System calls le user-space programs lai kernel sanga communicate garna help garcha.

Example:
- open()
- read()
- write()

---

## Linux Architecture Diagram (Text View)

+---------------------+
| Applications        |
+---------------------+
| Shell               |
+---------------------+
| Kernel              |
+---------------------+
| Hardware            |
+---------------------+



---

## Why Linux Architecture is Important for DevOps?
- Performance issues diagnose garna
- Resource usage bujhna
- Container & cloud understanding
- Debugging production problems

---

## DevOps Real Example
If an application is slow:
- Hardware? (CPU/RAM)
- Kernel? (process/memory)
- Application issue?

Architecture bujhe pachi root cause easily vetincha.

---

## Summary
- Kernel is the core of Linux
- Shell connects user to kernel
- Applications run in user space
- Architecture knowledge helps in debugging




