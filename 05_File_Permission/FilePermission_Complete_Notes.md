# File Permissions Management in Linux

## Introduction to File Permissions
Linux file permissions determine who can read, write, or execute files and directories. Each file and directory has three levels of permission: 
- **Owner (User)**: The creator of the file.
- **Group**: Users belonging to the assigned group.
- **Others**: All other users on the system.
  
  Permissions are represented as:
- **Read (`r` or `4`)** – View file contents.
- **Write (`w` or `2`)** – Modify file contents.
- **Execute (`x` or `1`)** – Run scripts or programs.

To check file permissions, use:
```bash
ls -l filename
```
Output example:
```bash
-rwxr--r-- 1 user group 1234 Mar 28 10:00 myfile.sh
```
## Changing Permissions with `chmod`
### Using Symbolic Mode
Modify permissions using symbols:
- Add (`+`), remove (`-`), or set (`=`) permissions.
