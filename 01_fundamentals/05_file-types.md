# Linux File Types 📂

Linux ma files different types ko huncha.  
DevOps ma yo bujhnu **mandatory** because logs, scripts, binaries, configs sab different file types ma huncha.  

---

## 1️⃣ Regular File
- Normal text or binary file
- Examples: `hello.txt`, `app.py`, `/bin/ls`
- Commands:
```bash
file hello.txt           # Check file type
cat hello.txt            # View content
head -n 10 hello.txt     # First 10 lines
tail -f /var/log/syslog  # Monitor log file live

2️⃣ Directory

Folder that contains files or other directories

Examples: /home/nimesh, /etc

Commands:
ls -l /home/nimesh        # List files
tree /home/nimesh          # Show directory structure
mkdir /home/nimesh/project # Create directory
rmdir /home/nimesh/old     # Remove empty directory


3️⃣ Symbolic Link (Symlink)

Shortcut / pointer to another file or directory

Symlink = shortcut / pointer to another file or directory

Original file lai move, rename, or copy nagari access garna sakcha

Linux ma ln -s command le bantauncha

Think of it like Windows shortcut.


Example: /usr/bin/python -> /usr/bin/python3.10

Commands:
