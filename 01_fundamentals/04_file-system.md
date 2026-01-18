# Linux File System Structure 🗂️

## What is File System?
Linux file system bhaneko hierarchical structure ho, jasle sab files ra directories organize garcha.

Linux ma **root (`/`)** bata sab start huncha. Sab files, folders root ko under huncha.

---

## Main Directories

| Directory | Purpose | DevOps Tip |
|-----------|---------|------------|
| `/` | Root directory | Starting point of all files |
| `/bin` | Essential binaries/commands | Commands like ls, cp, mv |
| `/sbin` | System binaries | System admin commands like ifconfig, fdisk |
| `/etc` | Configuration files | Server configs stored here |
| `/home` | User home directories | Each user ka personal files |
| `/var` | Variable data | Logs, cache, spool files |
| `/usr` | User-installed software | Software, libraries, docs |
| `/tmp` | Temporary files | Auto-cleaned after reboot |
| `/dev` | Devices | Hardware devices, e.g., /dev/sda |
| `/lib` | Libraries | Required for binaries |
| `/boot` | Boot files | Kernel, initrd |

---

## Linux File Types
- Regular file (text, binary)
- Directory
- Symbolic link (shortcut)
- Device file (hardware)
- Socket / pipe (inter-process communication)

---

## Important Commands

```bash
ls -l /home      # List details of home directory
tree /           # Show tree structure from root
df -h            # Disk space usage
du -sh /var/log  # Size of folder
file /bin/ls     # Check file type
