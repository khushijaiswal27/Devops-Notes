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

# Day 6 Notes:
![Lecture-07-Notes-pg1 jpg](https://github.com/user-attachments/assets/75e56f75-c8dd-4939-aa70-501238fa0bb4)
![Lecture-07-Notes-pg2 jpg](https://github.com/user-attachments/assets/9e2ac7d7-7aa2-4813-b220-7c82cb36c7d0)
