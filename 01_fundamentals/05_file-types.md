# Linux File Types 📂

Linux ma files multiple types ko huncha.  
DevOps ma yo concept important cha because logs, scripts, binaries, configs sab different file types ma aaucha.

---

## 1️⃣ Regular File
Normal text or binary data store garne file.

**Examples:**
- `hello.txt`
- `app.py`
- `/bin/ls`

**Useful Commands:**
```bash
file hello.txt            # Check file type
cat hello.txt             # View content
head -n 10 hello.txt      # First 10 lines
tail -f /var/log/syslog   # Monitor log live
```

---

## 2️⃣ Directory
Folders that contain files or other directories.

**Examples:**
- `/home/nimesh`
- `/etc`

**Useful Commands:**
```bash
ls -l /home/nimesh         # List files with details
tree /home/nimesh          # Show directory structure
mkdir project              # Create directory
rmdir old                  # Remove empty directory
```

---

## 3️⃣ Symbolic Link (Symlink)
Shortcut / pointer to another file or directory.  
Original file lai move, rename, copy nagarda pani access garna milcha.

**Think of it like:** Windows shortcut.

**Example:**
```
/usr/bin/python -> /usr/bin/python3.10
```

**Command to create symlink:**
```bash
ln -s /usr/bin/python3.10 /usr/bin/python
```

# Suppose we have a file called script.sh in /home/nimesh
cd /home/nimesh
ls
# Output:
# script.sh

# Create a symbolic link to script.sh called myscript
ln -s script.sh myscript

ls -l
# Output:
# lrwxrwxrwx 1 nimesh nimesh 9 Jan 18 12:00 myscript -> script.sh

rm myscript
# Only deletes symlink, original file is untouched


---

## 4️⃣ Hard Link
Same inode lai share garne duplicate reference.  
File delete bhaye pani aru hardlink le data hold garirakhcha.

**Example:**
```bash
ln original.txt copy.txt
```

---

## 5️⃣ Character Device Files
Character-based I/O handle garne device files (e.g., keyboard, serial ports).

**Location Example:** `/dev/tty`

---

## 6️⃣ Block Device Files
Block-based devices jastai disk, USB, SSD.

**Location Example:** `/dev/sda`

---

## 7️⃣ FIFO (Named Pipe)
Inter-process communication ko lagi use huncha.

**Example:**
```bash
mkfifo mypipe
```

---

## 8️⃣ Socket
Network communication ko lagi use huncha (e.g., web server, DB server).

**Example:**
```
/var/run/docker.sock
```

---

## Summary Table
| Type | Purpose |
|---|---|
| Regular File | Text / Binary |
| Directory | Folder |
| Symlink | Shortcut / Pointer |
| Hard Link | Duplicate inode reference |
| Character Device | Char-based hardware |
| Block Device | Disk-based hardware |
| FIFO | IPC pipe |
| Socket | Network communication |

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
