# Cloud-academy-05
Week 4 - Linux and Bash - 🚀 Exercise - File Permissions

This exercise will guide you through modifying file permissions on an AWS EC2 Linux instance. Ensure you have access to your EC2 instance and a file named `class_notes.txt`.

---

### Task 1: Making `class_notes.txt` Readable by Everyone

**Objective:** Ensure that everyone can read `class_notes.txt`, but no one can write to or execute it.

1. **Check current permissions:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
2. **Change permissions to read-only for all users (numeric mode):**
    
    ```bash
    chmod 444 class_notes.txt
    
    ```
    
3. **Verify the changes:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
    **Expected Output:**
    
    ```
    -r--r--r-- 1 [owner] [group] [size] [date] class_notes.txt
    
    ```
    

---

### Task 2: Allowing the Owner to Write

**Objective:** Permit the file owner to edit `class_notes.txt`, while keeping it readable by everyone.

1. **Check current permissions:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
2. **Change permissions to allow the owner to write (numeric mode):**
    
    ```bash
    chmod 644 class_notes.txt
    
    ```
    
3. **Verify the changes:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
    **Expected Output:**
    
    ```
    -rw-r--r-- 1 [owner] [group] [size] [date] class_notes.txt
    
    ```
    

---

### Task 3: Making `class_notes.txt` Executable by the Owner

**Objective:** Allow the owner to run `class_notes.txt` as a script.

1. **Check current permissions:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
2. **Change permissions to allow execution by the owner (numeric mode):**
    
    ```bash
    chmod 744 class_notes.txt
    
    ```
    
3. **Verify the changes:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
    **Expected Output:**
    
    ```
    -rwxr--r-- 1 [owner] [group] [size] [date] class_notes.txt
    
    ```
    

---

### Task 4: Adding Execute Permissions for the Group

**Objective:** Add execute permissions for the group to `class_notes.txt`.

1. **Check current permissions:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
2. **Change permissions to add execute for the group (symbolic mode):**
    
    ```bash
    chmod g+x class_notes.txt
    
    ```
    
3. **Verify the changes:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
    **Expected Output:**
    
    ```
    -rwxr-xr-- 1 [owner] [group] [size] [date] class_notes.txt
    
    ```
    

---

### Task 5: Revoking Write Access from the Group

**Objective:** Ensure the group cannot modify `class_notes.txt`.

1. **Check current permissions:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
2. **Change permissions to remove write for the group (symbolic mode):**
    
    ```bash
    chmod g-w class_notes.txt
    
    ```
    
3. **Verify the changes:**
    
    ```bash
    ls -l class_notes.txt
    
    ```
    
    **Expected Output:**
    
    ```
    -rwxr-xr-- 1 [owner] [group] [size] [date] class_notes.txt
    
    ```
    

---

By following these steps, you will have practiced setting and verifying file permissions on a Linux system, which is essential for managing security and access control in any Unix-like operating system.
