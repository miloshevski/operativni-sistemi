# Linux Commands Cheat Sheet

## `ls` - Listing Files and Directories

- `ls` - Lists all files and directories in the current working directory.
- `ls -a` - Lists all files, including hidden files (those starting with a dot `.`).
- `ls -s` - Displays the contents of the directory along with file sizes in KB.
- `ls | more` - Lists files page by page if there are too many to display at once.
- `ls -l` - Lists files in the current directory in long format.

### `ls -l` Explained

#### Explanation of Columns:

| Column | Description                 |
| ------ | --------------------------- |
| (1)    | File type and permissions   |
| (2)    | Number of hard links        |
| (3)    | Owner of the file           |
| (4)    | File size in bytes          |
| (5)    | Last modification date/time |
| (6)    | Filename                    |

---

### (1) File Type & Permissions

The first column shows the file type and access permissions:

- **File Type:**

  - `-` : Regular file
  - `d` : Directory
  - `l` : Symbolic link

- **Permissions:**
  - `r` : Read permission
  - `w` : Write permission
  - `x` : Execute permission
  - `-` : No permission

**Example:**  
`drwxr-xr-x`

- `d` → Directory
- `rwx` → Owner has **read, write, execute** permissions
- `r-x` → Group has **read, execute** permissions
- `r-x` → Others have **read, execute** permissions

---

### (2) Number of Hard Links

Indicates how many hard links point to the file.

---

### (3) Owner

Displays the user who owns the file.

---

### (4) File Size

Shows the file size in **bytes**.

---

### (5) Last Modification Date

- If modified **this year** → shows **date and time**
- If modified **previous years** → shows **date and year**

---

### (6) Filename

The name of the file or directory.

---

## Example Usage of `ls`

```bash
ls -l
ls -lh  # Human-readable sizes
ls -la  # Show hidden files

chmod [options] mode file

chmod ug+rw sample
chmod +r file
chmod -x file
chmod u=rw,go= file
chmod +rw file
chmod -R u+w,go-w docs/
chmod 666 file
chmod 755 file
chmod -R u+rwX,g-rwX,g-rwx,o-rwx <directory>

mv source destination

mv moj.txt /users/student  # Moves moj.txt to /users/student
mv moj.txt /users/student/mojnov.txt  # Renames and moves moj.txt
mv student /users/admin  # Moves the directory student to /users/admin
mv proba.txt moj.txt  # Renames proba.txt to moj.txt

rm [options] file

rm moj.txt  # Deletes moj.txt
rm -r student  # Recursively deletes the directory student and its contents
rm res.01 res.02  # Deletes both res.01 and res.02

cat file

cat >> results.csv
Add line 1 to the end.

cat results.csv > res.csv  # Overwrites res.csv with contents of results.csv

Task 1: Complete the report.
Task 2: Send the email.

cat >> notes.txt
Task 3: Prepare the presentation.
Task 1: Complete the report.
Task 2: Send the email.
Task 3: Prepare the presentation.

cat notes.txt
```
