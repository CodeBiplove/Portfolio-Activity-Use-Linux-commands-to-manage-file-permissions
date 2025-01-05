**Linux File Permissions Management Portfolio Document**

**Project Description:** The research team at my organization needed to update the file permissions for certain files and directories within the projects directory. The permissions did not currently reflect the level of authorization that should be given. Checking and updating these permissions helped keep their system secure. To complete this task, I performed the following steps:

---

### **Section 1: Checking File and Directory Details**

**Command Used:** `ls -la`

**What I Did:** I used the `ls -la` command to determine the existing permissions set for a specific directory in the file system. This command lists all contents of the directory, including hidden files, and provides detailed information.

**Example Output:**

```bash
-rw-r--r--  1 user group 1024 Jan 4 15:30 research_data.txt
-rw-------  1 user group 2048 Jan 4 15:45 .project_x.txt
drwx------  2 user group 4096 Jan 4 16:00 drafts
```

The output of my command indicates there is one directory named `drafts`, one hidden file named `.project_x.txt`, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.

---

### **Section 2: Explaining the Permissions String**

**What I Did:** I analyzed the 10-character permissions string from the `ls -la` output to understand access control.

#### **Explanation:**
- **1st Character:** Indicates the file type (`-` for a regular file, `d` for a directory).
- **2nd-4th Characters:** Represent the read (r), write (w), and execute (x) permissions for the user.
- **5th-7th Characters:** Represent the read (r), write (w), and execute (x) permissions for the group.
- **8th-10th Characters:** Represent the read (r), write (w), and execute (x) permissions for others.

When one of these characters is a hyphen (`-`), it indicates that the permission is not granted.

**Example:** For `-rw-r--r--`:
- **Owner:** Read and write
- **Group:** Read-only
- **Others:** Read-only

---

### **Section 3: Changing File Permissions**

**Command Used:** `chmod`

**What I Did:** I modified file permissions to match organizational security policies.

#### **Example 1:**
To remove write access for others:
```bash
chmod o-w project_k.txt
```

#### **Example 2:**
To grant write access to the group:
```bash
chmod g+w research_data.txt
```

After making changes, I used `ls -la` to verify the updated permissions.

---

### **Section 4: Changing Permissions on a Hidden File**

**Command Used:** `chmod`

**What I Did:** The team archived `project_x.txt`, ensuring no one has write access while allowing the user and group to retain read access.

**Example:**
```bash
chmod 640 .project_x.txt
```
This command:
- Removed write permissions for the user (`u-w`).
- Removed write permissions for the group (`g-w`).
- Added read permissions for the group (`g+r`).

---

### **Section 5: Changing Directory Permissions**

**Command Used:** `chmod`

**What I Did:** Restricted directory access to authorized users.

#### **Example 1:**
To allow only the owner to access the directory:
```bash
chmod 700 drafts
```

#### **Example 2:**
To ensure only the `researcher2` user has execute permissions:
```bash
chmod 700 drafts
```
The output confirmed the directory permissions aligned with the organization’s requirements.

---

### **Section 6: Including Linux Commands**

To present my work, I followed best practices for including Linux commands:

#### **Screenshots:**
- Captured commands entered in the Bash shell.
- Excluded visible lab instructions.

#### **Typed Commands:**
Highlighted commands in gray and used a monospaced font for readability.

Example:
```bash
grep OS updates.txt
```

---

### **Section 7: Summary**

**What I Accomplished:** I changed multiple permissions to match the level of authorization my organization wanted for files and directories in the `projects` directory. The steps included:
- Checking permissions using `ls -la`.
- Modifying file and directory permissions with `chmod`.

These actions ensured secure and appropriate access control, safeguarding the system effectively.

---

