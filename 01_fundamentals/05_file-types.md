
# 📂 Linux File Types — Explained Simply

Linux supports multiple file types. In DevOps, SysAdmin, Programming, and Server environments, understanding these file types is important because logs, configs, scripts, and binaries all behave differently.

---

## 1️⃣ **Regular File**
Stores normal data (text / binary).

💡 **Examples**
- `hello.txt`
- `app.py`
- `/bin/ls`

🛠 **Useful Commands**
```bash
file hello.txt            # Check file type
cat hello.txt             # View content
head -n 10 hello.txt      # First 10 lines
tail -f /var/log/syslog   # Monitor log live (logs)
```

---

## 2️⃣ **Directory**
Contains files and other directories.

💡 **Examples**
- `/home/nimesh`
- `/etc`

🛠 **Useful Commands**
```bash
ls -l /home/nimesh        # List with details
tree /home/nimesh         # Show directory structure
mkdir project             # Create directory
rmdir old                 # Remove empty directory
```

---

## 3️⃣ **Symbolic Link (Symlink)**
Shortcut / pointer to another file or directory. Works even if the original file moves.

📝 **Think:** Windows Shortcut

📍 **Example**
```
/usr/bin/python → /usr/bin/python3.10
```

🛠 **Create Symlink**
```bash
ln -s /usr/bin/python3.10 /usr/bin/python
```

🎯 **Demo**
```bash
cd /home/nimesh
ln -s script.sh myscript
ls -l
# lrwxrwxrwx ... myscript -> script.sh
```

> Deleting the symlink (`rm myscript`) does NOT delete the original file.

---

## 4️⃣ **Hard Link**
Shares the same inode. Even if the original file is deleted, data stays accessible through the hard link.

🛠 **Example**
```bash
ln original.txt copy.txt
```

---

## 5️⃣ **Character Device File**
Used by character-based I/O devices (e.g., terminals, serial ports).

📍 **Example Location:** `/dev/tty`

---

## 6️⃣ **Block Device File**
Used by block-based storage devices (disk, SSD, USB).

📍 **Examples:** `/dev/sda`, `/dev/nvme0n1`

---

## 7️⃣ **FIFO (Named Pipe)**
Used for inter-process communication (IPC).

🛠 **Example**
```bash
mkfifo pipe1
```

---

## 8️⃣ **Socket**
Used for network communication between processes (e.g., web servers, DB servers).

📍 **Example:**
```
/var/run/docker.sock
```

---

## ✅ **Summary Table**

| Type | Purpose |
|---|---|
| Regular File | Text / Binary storage |
| Directory | Folder / Container |
| Symlink | Shortcut / Pointer |
| Hard Link | Shares inode (duplicate reference) |
| Character Device | Hardware character I/O |
| Block Device | Disk / Storage devices |
| FIFO | IPC Pipe |
| Socket | Network communication |

---
