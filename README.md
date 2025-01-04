**Linux File Permissions Management Portfolio Document**

**Project Description:** As a security professional, I ensured secure and proper access control in the file system of an organizational environment. This document demonstrates my practical experience using Linux commands to check, interpret, and modify file and directory permissions to maintain system security.

---

### **Section 1: Checking File and Directory Details**

**Command I Used:** `ls -la`

**What I Did:** I used the `ls -la` command to list all files and directories, including hidden ones, along with their associated details such as permissions, ownership, size, and modification date.

**Example Output:**

```bash
-rw-r--r--  1 user group 1024 Jan 4 15:30 research_data.txt
-rw-------  1 user group 2048 Jan 4 15:45 .project_x.txt
drwx------  2 user group 4096 Jan 4 16:00 drafts
```

---

### **Section 2: Explaining the Permissions String**

**What I Did:** I analyzed the 10-character permissions string from the `ls -la` output to understand access control.

**Explanation:**
- The first character indicates the file type (`-` for a regular file, `d` for a directory).
- The next nine characters are grouped into three sets for the owner, group, and others:
  - `r`: Read permission
  - `w`: Write permission
  - `x`: Execute permission
  - `-`: No permission

**Example:** For `-rw-r--r--`:
- Owner: Read and write
- Group: Read-only
- Others: Read-only

---

### **Section 3: Modifying File Permissions**

**Command I Used:** `chmod`

**What I Did:** I used `chmod` to modify file permissions to match organizational security policies.

**Examples:**
1. To grant write permission to the group:
   ```bash
   chmod g+w research_data.txt
   ```
2. To remove read permission for others:
   ```bash
   chmod o-r research_data.txt
   ```

---

### **Section 4: Adjusting Permissions for a Hidden File**

**Command I Used:** `chmod`

**What I Did:** I modified permissions for `.project_x.txt`, ensuring it remained secure while accessible only to authorized users.

**Example:**

```bash
chmod 640 .project_x.txt
```

This command allowed the user to read and write, the group to read, and others to have no access.

---

### **Section 5: Modifying Directory Permissions**

**Command I Used:** `chmod`

**What I Did:** I restricted directory access to authorized users.

**Examples:**
1. To allow only the owner to access the directory:
   ```bash
   chmod 700 drafts
   ```
2. To allow group members to enter and modify the directory:
   ```bash
   chmod 770 research_folder
   ```

---

### **Section 6: Including Linux Commands**

To present my work, I followed best practices for including Linux commands:

#### **Screenshots:**
- I captured screenshots of commands as entered in the Bash shell.
- I excluded any lab instructions visible on the screen.

#### **Typed Commands:**
- I highlighted typed commands in gray.
- I used a monospaced font for readability, as shown below:
  ```bash







## Section 7: Summary

**Accomplishments:**  
In this project, I demonstrated my ability to manage file and directory permissions in Linux. I checked permissions, interpreted their meanings, and applied modifications using commands like `chmod` and `ls -la`. By ensuring permissions aligned with organizational requirements, I restricted access to sensitive files and directories, showcasing my capability to enforce secure access controls effectively.

