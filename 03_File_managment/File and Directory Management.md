# File management in Linux

### File and Directory Management
1. **`ls`** – Lists files and directories in the current location.
2. **`ls -a wa ls -la`** – Lists files and directories in the current location as well as hidden files and in long format.
3. **`ls -l`** - List files in long detail form 
4. **`cd /path/to/directory`** – Changes the working directory.
5. **`pwd`** – Prints the current working directory.
6. **`mkdir new_folder`** – Creates a new directory.
7. **`touch new_file`** – Creates a new file.
8. **`rmdir empty_folder`** – Removes an empty directory.
9.  **`rm file.txt`** – Deletes a file.
10. **`rm -r folder`** – Deletes a folder and its contents.
11. **`cp file1.txt file2.txt`** – Copies a file.
12. **`cp source_path/*.txt destination_path/`** – Copies a file of one dir to another dir 
13. **`cp -r dir1 dir2`** – Copies a directory recursively.
14. **`mv old_name new_name`** – Moves or renames a file or directory.
    
### File Viewing and Editing
11. **`cat file.txt`** – Displays file content.
12. **`tac file.txt`** – Displays file content in reverse order.
13. **`less file.txt`** – Opens a file for viewing with scrolling support.
14. **`more file.txt`** – Similar to `less`, but only moves forward.
15. **`head -n 10 file.txt`** – Displays the first 10 lines of a file.
16. **`tail -n 10 file.txt`** – Displays the last 10 lines of a file.
17. **`nano file.txt`** – Opens a simple text editor.
18. **`vi file.txt`** – Opens a powerful text editor.
19. **`echo 'Hello' > file.txt`** – Writes text to a file, overwriting existing content.
20. **`echo 'Hello' >> file.txt`** – Appends text to a file without overwriting.