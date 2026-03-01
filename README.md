# My DevOps Journey - Day 1 🚀

Today, I watched the first lecture of Technical Guftgu. 

### What I learned:
* I understood the basic concept of DevOps (the "Why" and "What").
* I learned about how software moves from planning to the final stage (SDLC).
* Most importantly, I set up my environment: LinkedIn, GitHub, and Ubuntu Terminal.

*Sharing my handwritten rough notes below just to keep a record of my start!* 
# Day 1 Notes:
![WhatsApp Image 2026-02-05 at 7 37 42 PM](https://github.com/user-attachments/assets/53bac04b-4631-467b-8921-f6ad265adc8d)
![WhatsApp Image 2026-02-05 at 7 37 43 PM](https://github.com/user-attachments/assets/82a94e65-66b1-480d-9034-ac95e4f4310b)

## Day 2: DevOps Lifecycle & Agile Methodology 🔄

Today, I focused on how teams collaborate and the various stages involved in software delivery.

### What I learned:
* The importance of coordination between Development and Operations teams to eliminate "Silos".
* The difference between the Waterfall model (step-by-step approach) and Agile methodology (working in Sprints/fast cycles).
**CI/CD pipeline- *Understanding the automation flow—Continuous Integration (using Git/Jenkins) and Continuous Deployment (using Maven).
* **DevOps Lifecycle:** Studying the "Infinity Loop" process, covering everything from Planning and Coding to Monitoring.

* # Day 2 Notes:
 ![WhatsApp Image 2026-02-06 at 1 33 26 PM](https://github.com/user-attachments/assets/072803b1-dd1d-481b-93b8-3ea3e748e39f)
![WhatsApp Image 2026-02-06 at 1 33 26 PM (1)](https://github.com/user-attachments/assets/21d47a70-1629-450a-bd9b-e0273f59e0f6)
![WhatsApp Image 2026-02-06 at 1 33 26 PM (2)](https://github.com/user-attachments/assets/fdeb436c-6dbb-447a-b779-5cd3b1dc0295)

## Day 3: AWS EC2 Setup 🔄
I have successfully launched and configured my first Linux server on AWS, following the Day 3 lecture of the DevOps series by Technical Guftgu (Imran Teli Sir).

🚀 Key Highlights:
Instance Provisioning: Launched a Linux instance using t2.micro (Free Tier) in the AWS Mumbai Region (ap-south-1).

Key Pair Management: Generated an RSA Key (.pem) and converted it to .ppk format using PuTTYgen for secure SSH access.

Security Configuration: Configured Security Groups to allow SSH (Port 22) traffic for remote management.

Health Verification: Successfully monitored and verified the instance with 3/3 Status Checks Passed (System, Instance, and EBS checks).

📸 Lab Proof (Screenshots):
<img width="1919" height="904" alt="Screenshot 2026-02-08 210504" src="https://github.com/user-attachments/assets/3c1519b3-587f-4d84-974a-8ccd4a39f5a7" />
<img width="1877" height="837" alt="Screenshot 2026-02-08 195118" src="https://github.com/user-attachments/assets/155946d0-3248-40c7-a36e-928ffadf7aa4" />
<img width="859" height="758" alt="Screenshot 2026-02-08 203642" src="https://github.com/user-attachments/assets/8be6e4dc-5b2b-4fd0-ab08-a419399c7555" />

# Day 3 Notes: 
![Lecture-03-Notes-pg1 jpg](https://github.com/user-attachments/assets/8227679b-aa35-4f98-a781-ce7826c8fd24)
![Lecture-03-Notes-pg2 jpg](https://github.com/user-attachments/assets/5a3ff14d-d392-438b-b234-ec89da89f888)
![Lecture-03-Notes-pg3 jpg](https://github.com/user-attachments/assets/28017924-079f-499b-8914-e014b58fd4b3)


#  Day 4 - Everything About Linux from Scratch

This repository documents my progress on **Day 4** of the DevOps series by **Technical Guftgu (Imran Teli Sir)**. Today, I dived deep into the history, architecture, and core features of the Linux Operating System.

## 🎯 Lab Objectives
- Understand the origin of Linux and its evolution from **UNIX**.
- Learn the difference between **CLI** (Command Line Interface) and **GUI** (Graphical User Interface).
- Explore the unique features that make Linux the preferred choice for servers.

## 📚 Key Learnings:
- **History:** Evolution from **UNICS** (1969) to the creation of **Linux** by **Linus Torvalds** in 1991, inspired by the **MINIX** OS.
- **Architecture:** Learned how the **Kernel** (the heart of the OS) interacts with software and hardware.
- **Distributions (Flavors):** Explored various flavors like **Ubuntu, CentOS, RHEL, Debian,** and **Amazon Linux**.
- **Security:** Understood why Linux is more secure than Windows (Virus isolation within folders and no need for external Antivirus).
- **Efficiency:** Linux is **lightweight** with a smaller footprint, making it faster and more stable for high-performance servers.

# Day 4 Notes: 
![Lecture-04-Notes-pg1 jpg](https://github.com/user-attachments/assets/14868e80-2fe0-413b-aa6b-708d94efaad5)
![Lecture-04-Notes-pg2 jpg](https://github.com/user-attachments/assets/c640ca7b-6530-4649-848a-7fd8da3a0f0c)


# Day 5 - Linux Architecture & File System Hierarchy

Today’s session was a deep dive into how Linux operates internally compared to Windows and understanding the crucial "Root" file system structure.

## 🎯 Lab Objectives
- Compare **Windows vs. Linux Architecture**.
- Understand the roles of the **Kernel** and **Shell**.
- Master the **Linux File System Hierarchy** (Standard directories).

## 🏗️ Architecture Comparison:
| Component | Windows | Linux |
| :--- | :--- | :--- |
| **Hardware** | Physical Machine | Physical Machine |
| **Core OS** | Operating System | **Kernel** (The Heart of OS) |
| **Interface** | Shell (CMD/PowerShell) | **Shell** (Bash, Sh, etc.) |
| **User Access** | Administrator | **Root User** |

## 📁 Key Linux Directories (File System Hierarchy):
- `/` (Root): The top-level directory (starting point).
- `/root`: Home directory for the **Root User** (Admin).
- `/home`: Home directories for **regular users**.
- `/bin`: Contains **User Binaries** (standard commands like `ls`, `cp`).
- `/sbin`: Contains **System Binaries** (commands restricted to the Root user).
- `/etc`: Stores all **Configuration Files** for the system.
- `/boot`: Contains files required for the **Booting process**.
- `/dev`: Information about **Device files** (Hardware like Disk, USB).
- `/opt`: **Optional** application software packages.

---
**Learning Point:** In Linux, everything is either a **File** or a **Directory**. 🚀

# Day 5 Notes: 

![Lecture-05-Notes-pg1 jpg](https://github.com/user-attachments/assets/8aa14a36-4748-4b39-946f-42c1234b26b7)
![Lecture-05-Notes-pg2 jpg](https://github.com/user-attachments/assets/fe05d73f-7fb6-4343-af97-44c7071b0beb)


🐧 Day 6 - File Management & Editors in Linux

In this session, I explored the core of the Linux File System. Understanding how to create and manipulate files is a foundational skill for any DevOps professional working with automation and configuration management.

🎯 Learning Objectives
Mastered the 4 primary ways to create files in Linux.

Understood file metadata and Timestamps using the stat command.

Practiced hands-on with CLI-based text editors (VI and Nano).

Learned advanced listing techniques to find hidden system files.

🛠️ File Creation Methods Practiced
1. cat Command (Concatenate)
Used for creating files and redirecting input directly from the terminal.

Create & Write: cat > filename (Press Ctrl + D to save).

Append Content: cat >> filename (Adds text without overwriting).

View Content: cat filename

2. touch Command
Used to create empty files or manipulate timestamps.

Command: touch <filename>

Deep Dive (Timestamps): Using the stat command, I learned about:

Access Time: When the file was last read.

Modify Time: When the content was last changed.

Change Time: When the metadata (permissions/owner) was updated.

3. vi / vim Editor
The industry-standard text editor for Linux.

Insert Mode: Press i to enter edit mode.

Command Mode: Press Esc to give commands.

Save & Exit: :wq

Force Quit: :q!

4. nano Editor
A user-friendly alternative for quick terminal-based editing.

Save: Ctrl + O

Exit: Ctrl + X

📸 Lab Proof (Screenshot):-
<img width="936" height="1015" alt="Screenshot 2026-02-15 194154" src="https://github.com/user-attachments/assets/625667cb-d8f0-4a41-b41a-5d98ebad797b" />

# Day 6 Notes:
![Lecture-06-Notes-pg1 jpg](https://github.com/user-attachments/assets/cf32000f-b1ba-4860-90a6-9677e62794f2)
![Lecture-06-Notes-pg2 jpg](https://github.com/user-attachments/assets/d2bfbea2-a284-4d15-b72b-40fad09907b3)
![Lecture-06-Notes-pg3 jpg](https://github.com/user-attachments/assets/06b58e10-d11c-4556-bd82-863610484f1d)


# Day 7 - Advanced Directory Management & File Operations

In today's session with **Dr. Bhupendra Rajput**, I moved beyond basic file creation to mastering directory structures and essential file operations in Linux.

## 🎯 Key Learning Objectives
- Creating and navigating nested directory structures.
- Mastering file operations: Copying, Moving, and Renaming.
- Understanding Hidden Files and Directories for system security.
- Learning how to safely remove files and non-empty directories.

---

## 🛠️ Commands & Concepts Mastered

### 1. Directory Management (`mkdir`)
- **Single Directory:** `mkdir DirName`
- **Multiple Directories:** `mkdir Dir1 Dir2 Dir3`
- **Nested (Parent) Directories:** `mkdir -p A/B/C` (The `-p` flag creates the entire path automatically).

### 2. Navigation & Pathfinding
- `cd <path>`: Change directory.
- `cd ..`: Move back one level.
- `cd ../..`: Move back two levels.
- `pwd`: Print Working Directory (To know exactly where you are).

### 3. File Operations (`cp` & `mv`)
- **Copy:** `cp source_file destination` (Copies content/file).
- **Move/Cut:** `mv source_file destination` (Moves file from one place to another).
- **Rename:** `mv old_name new_name` (Linux uses the `mv` command to rename files and folders).

### 4. Hidden Files & Folders
- **Create Hidden File:** `touch .filename` (Starting with a `.`).
- **Create Hidden Directory:** `mkdir .dirname`
- **View Hidden Files:** `ls -a` or `ls -la`.

### 5. Deletion Commands (`rm`)
- `rm filename`: Deletes a file.
- `rmdir dirname`: Deletes an **empty** directory.
- `rm -rf dirname`: **Forcefully and Recursively** deletes a directory and all its contents (Use with caution!).

---

## 📋 Quick Reference Table
| Command | Action |
| :--- | :--- |
| `ls -R` | Recursive list (shows all files in sub-folders). |
| `cd ~` | Jump to the home directory. |
| `cat filename` | View file content. |
| `history` | List all commands used in the session. |

📸 Lab Proof (Screenshot):-

<img width="932" height="1017" alt="Screenshot 2026-02-19 211008" src="https://github.com/user-attachments/assets/4410f5a3-6c6c-4d09-b12c-f7c45c2ae3c4" />
<img width="460" height="1014" alt="Screenshot 2026-02-19 211029" src="https://github.com/user-attachments/assets/614def0e-54e5-4bdf-ad1e-a266d34813c7" />

# Day 7 Notes:
![Lecture-07-Notes-pg1 jpg](https://github.com/user-attachments/assets/75e56f75-c8dd-4939-aa70-501238fa0bb4)
![Lecture-07-Notes-pg2 jpg](https://github.com/user-attachments/assets/9e2ac7d7-7aa2-4813-b220-7c82cb36c7d0)

## Day 8: Package Management & System Utilities🚀

🚀 Topics Covered:

1. **Network & Host Info:**
   - `hostname`: To check the system name.
   - `ifconfig` or `hostname -i`: To find the IP address of the instance.
2. **Package Management (YUM):**
   - `sudo yum install httpd -y`: To install Apache Web Server.
   - `sudo yum update -y`: To update all packages.
   - `sudo yum remove httpd`: To uninstall a package.
3. **Service Management:**
   - `sudo systemctl start httpd`: To start the web server.
   - `sudo systemctl status httpd`: To check if the server is active (running).
   - `sudo chkconfig httpd on`: To enable the service on boot.
4. **Advanced File Operations:**
   - `grep "text" filename`: To search for a specific word in a file.
   - `sort filename`: To sort the file content alphabetically.
   - `tree`: To view the directory structure in a visual format.
  
   - 📸 Lab Proof (Screenshot):-
   - 
<img width="833" height="436" alt="Screenshot 2026-02-20 220724" src="https://github.com/user-attachments/assets/8e4b89be-8988-4b91-8b87-531a34a7acb1" />

<img width="684" height="160" alt="Screenshot 2026-02-20 221036" src="https://github.com/user-attachments/assets/f76dfcef-4020-42a2-84c5-e0440398c6d8" />

<img width="946" height="1011" alt="Screenshot 2026-02-20 221116" src="https://github.com/user-attachments/assets/db25139c-3ecd-4c79-936e-d3b9595a7034" />

<img width="768" height="921" alt="Screenshot 2026-02-20 221137" src="https://github.com/user-attachments/assets/77726ebb-9f1e-4cea-a2d7-f4d5968db2a2" />

# Day 8 Notes:
![Lecture-08-Notes-pg1 jpg](https://github.com/user-attachments/assets/f5c443c4-1631-4879-b8f8-7869fd940b00)
![Lecture-08-Notes-pg2 jpg](https://github.com/user-attachments/assets/206229d3-37fe-4d09-bfca-8b69b3811583)
![Lecture-08-Notes-pg3 jpg](https://github.com/user-attachments/assets/5d7949a1-96d6-4136-925f-7d4097b1a2ad)


# 🐧 Day 9: Linux User Management & File Linking

## 👤 User & Group Administration
* **`sudo useradd [username]`**: Used to create a new user in the system.
* **`sudo groupadd [groupname]`**: Used to create a new group.
* **`cat /etc/passwd`**: Used to view the list of all users and their configuration.
* **`cat /etc/group`**: Used to view the list of all existing groups.
* **`sudo gpasswd -a [user] [group]`**: Used to add an existing user to a specific group.

## 🔗 Linking in Linux:-

### 1. Soft Link (Symbolic Link)
Acts as a shortcut to the original file. If the original file is deleted, the link becomes broken.
* **Command:** `ln -s [source_file] [link_name]`
### 2. Hard Link
Acts as a mirror of the file data. Even if the original file is deleted, the data remains accessible.
* **Command:** `ln [source_file] [link_name]`

## 📦 Archiving & Downloading
* **`tar -cvf`**: Used to bundle multiple files into a single "tarball" archive.
* **`gzip`**: Used to compress files to reduce their storage size.
* **`wget [URL]`**: A utility to download files directly from the internet via the command line.

  
# Day 9  Notes:
![Lecture-09-Notes-pg1 jpg](https://github.com/user-attachments/assets/ff1ea050-51cf-43e1-95d9-dcfd84abe68a)
![Lecture-09-Notes-pg2 jpg](https://github.com/user-attachments/assets/8004c1d9-b38c-4985-b402-b7c85c2d5088)


# 📂 Day 10: Master Linux Permissions & Ownership 🛡️
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




🚀 # 📂 Day 11 : Introduction to GIT (The Time Machine):- Based on Technical Guftgu's tutorial, I've mastered the following concepts:

🔹 What is Version Control?
It’s a system that records changes to a file or set of files over time so that you can recall specific versions later.

🔹 Centralized vs Distributed :-

CVCS (e.g., SVN): Everything depends on a central server. If the server goes down, you lose everything.
DVCS (GIT): Every developer has a full copy of the repository locally. It's faster and reliable even without the internet.

🔹 Key Difference: Git vs GitHub:-

Git: A local tool installed on my Linux machine to manage versions.

GitHub: A cloud-based service that hosts Git repositories 

# Day 11  Notes:
![Lecture-11-Notes-pg1 jpg](https://github.com/user-attachments/assets/f9475ebb-ed81-43f2-acee-6b5545401b1a)
![Lecture-11-Notes-pg2 jpg](https://github.com/user-attachments/assets/b7cc4364-f902-4480-a9cb-cd5e2dcc8499)

# Day 12: Git Lifecycle & Architecture 🛠️

Today, I deep-dived into the internal architecture of Git and how it tracks changes. Understanding the "Stages" is the foundation of becoming a DevOps Engineer.

## 📌 Key Concepts Learned:

### 1. The Three Stages of Git
Git operates in three distinct areas:
* **Working Directory:** The local folder where I create or modify files. These are "untracked" by Git initially.
* **Staging Area (Index):** A buffer zone. When I run `git add`, files move here. It allows me to group specific changes before finalizing them.
* **Local Repository:** When I run `git commit`, the changes are permanently saved as a "Snapshot" in the `.git` directory.

### 2. Snapshots vs. Incremental Backups
Unlike traditional backup systems that copy entire files every time, Git takes a **Snapshot**. If a file hasn't changed, Git simply creates a link to the previous version to save memory and improve speed.

### 3. Commit IDs & Data Integrity
Every commit is assigned a unique 40-character **SHA-1 Hash ID** (e.g., `5a3f92...`). This ID is generated based on the content, author, and timestamp, ensuring that the code history can never be tampered with.

### 4. Local vs. Central Repository
* **Git (Local):** Manages versions on my own machine.
* **GitHub (Central):** A hosting service where I `push` my local repository so others can collaborate or I can have a remote backup.

---

## 💻 Commands Practiced:

| Command | Description |
| :--- | :--- |
| `git init` | Initializes a brand new Git repository in the current folder. |
| `git add <file>` | Moves changes from the Working Directory to the Staging Area. |
| `git commit -m "msg"` | Saves the staged snapshot to the Local Repository with a message. |
| `git log` | Displays the history of all commits made in the project.  

# Day 12  Notes:
![Lecture-12-Notes-pg1 jpg](https://github.com/user-attachments/assets/7514914e-53ba-42b7-af37-3ea65cb74db4)
![Lecture-12-Notes-pg2 jpg](https://github.com/user-attachments/assets/3d9ff3ee-08d1-4b43-bf26-e5d1c47044ec)
![Lecture-12-Notes-pg3 jpg](https://github.com/user-attachments/assets/82f27318-eaa5-4b23-b2e2-bcc6068408f7)
![Lecture-12-Notes-pg4 jpg](https://github.com/user-attachments/assets/cf61783b-d824-46b3-8ad3-a03cd18872e7)
![Lecture-12-Notes-pg5 jpg](https://github.com/user-attachments/assets/1f1d4597-9f18-4135-bd1b-0aaf7fbb6984)

# Day 13: Git Installation & GitHub Setup
In this session, I learned how to establish coordination between a Central Repository (GitHub) and Local Repositories (AWS EC2 Instances).

🛠️ Key Learnings & Tasks Performed:

1. EC2 Instance Configuration:-
   
- Launched two Linux EC2 instances in different regions (Mumbai and Singapore) to simulate a global development environment.
- Configured Security Groups to allow inbound traffic for SSH (Port 22) and HTTP (Port 80).

2. Git Installation on Amazon Linux:-
   
Updated the system packages using:
- sudo yum update -y

Installed Git on the AWS machine:
- sudo yum install git -y

Verified the installation and checked the version:
- git --version (Result: Version 2.23.3)

3. Git Global Configuration:-
   
* Configured global identity settings to track commits accurately:
- git config --global user.name "Your Name"
- git config --global user.email "your-email@example.com"

* Verified the settings using::-
- git config --list

4. GitHub Professional Setup:-
Created and verified a new GitHub account.
Explored the GitHub UI and understood the workflow of a Central Repository.

- 📸 Lab Proof (Screenshot):-
- <img width="1036" height="164" alt="Screenshot 2026-03-01 145053" src="https://github.com/user-attachments/assets/e83c569b-5605-4ecf-b328-58ab0531aa2a" />

  # Day13 notes-
![WhatsApp Image 2026-03-01 at 2 45 17 PM](https://github.com/user-attachments/assets/ef53d76b-8069-40d7-8829-4d1335f834fc)

# Lecture 14: Git Operations & Multi-Region Sync:-

This session focused on collaborating between multiple local repositories and a single central repository.

# 🛠️ Tasks Performed:-

Initialization: Used git init to set up local repositories on AWS.
Identity Setup: Configured user.name and user.email to track different authors (Mumbai vs. Singapore).

# Push/Pull Workflow:

Created and committed files in the Mumbai instance.
Uploaded (Pushed) the code to GitHub.
Downloaded (Pulled) the same code onto the Singapore instance.

* Inspection: Used git log and git show to verify code changes and commit history.

* Git Ignore: Created a .gitignore file to exclude specific file types (like .java and .css) from being tracked.

  - 📸 Lab Proof (Screenshot):-
    

