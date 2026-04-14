### Day 10: Master Linux Permissions & Ownership 

*(Inspired by TechGuftgu DevOps Series)*

Today's learning was focused on the security layer of Linux. In DevOps, managing access is crucial for protecting servers and automation scripts.

---

## 🔍 Understanding the Permission String
When you run `ls -l`, you see something like:  
`drwxr-xr--`

| Position | Meaning | Examples |
| :--- | :--- | :--- |
| **1st Char** | File Type | `-` (File), `d` (Directory), `l` (Link) |
| **2-4 Char** | **Owner** Permissions | `rwx` (Read, Write, Execute) |
| **5-7 Char** | **Group** Permissions | `r-x` (Read, Execute only) |
| **8-10 Char** | **Others** Permissions | `r--` (Read only) |

---

## 🔢 The Numeric Method (The 4-2-1 Rule)
Linux assigns a number to each permission type. To set permissions, we just sum them up!

- **4** = Read (r)
- **2** = Write (w)
- **1** = Execute (x)
- **0** = No Permission

### **Common Permission Combinations:**
- **777** : `rwxrwxrwx` (Full access for everyone - *Risky!*)
- **755** : `rwxr-xr-x` (Owner can do everything, others can only Read/Execute)
- **644** : `rw-r--r--` (Standard file: Owner can Edit, others can only Read)
- **400** : `r--------` (Read-only for Owner - *Used for .pem keys*)

---

## 🛠️ Essential Commands

### 1. Changing Permissions (`chmod`)
- **Numeric:** `chmod 700 secret.txt`
- **Symbolic:** `chmod u+x script.sh` (Give execute power to User)

### 2. Changing Ownership (`chown`)
To change who "owns" the file:
- `sudo chown khushi:devops group_file.txt`  
*(Changes Owner to 'khushi' and Group to 'devops')*

### 3. Changing Group (`chgrp`)
To change only the group:
- `sudo chgrp developers project_folder`

---

## 💡 Key Takeaway from TechGuftgu
> "Permissions are the first line of defense in DevOps. Never give '777' permissions unless absolutely necessary for debugging, as it opens your system to everyone!"

- 📸 Lab Proof (Screenshot):
<img width="686" height="785" alt="Screenshot 2026-02-25 140510" src="https://github.com/user-attachments/assets/d6f7f410-7268-4f29-9231-7ce7e3fb40ed" />
<img width="701" height="813" alt="Screenshot 2026-02-25 140547" src="https://github.com/user-attachments/assets/c5d0ada6-b37f-4d82-8eb2-d41cb747db58" />

# Day 10  Notes:

![Lecture-10-Notes-pg1 jpg](https://github.com/user-attachments/assets/602c84d6-ddbc-41f2-b2bf-d77d8aad8be1)
![Lecture-10-Notes-pg2 jpg](https://github.com/user-attachments/assets/d2111cfd-49af-4839-82ab-9a420edb20bb)
