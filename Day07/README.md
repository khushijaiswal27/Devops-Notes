
### Day 7 - Advanced Directory Management & File Operations

## Task 7
Today's goal is to **understand where things live in Linux** and **practice troubleshooting like a DevOps engineer**.

You will create notes covering:
- Linux File System Hierarchy (the most important directories)
- Practice solving real-world scenarios step by step

This consolidates your Linux fundamentals and prepares you for real-world troubleshooting.

---

## Expected Output
By the end of today, you should have:

- A markdown file named:
  `day-07-linux-fs-and-scenarios.md`

or

- A hand written set of notes (Recommended)

Your notes should have two sections: File System Hierarchy and Scenario Practice.

---

## Guidelines

### Part 1: Linux File System Hierarchy (30 minutes)

Document the purpose of these **essential** directories:

**Core Directories (Must Know):**
- `/` (root) - The starting point of everything
- `/home` - User home directories
- `/root` - Root user's home directory
- `/etc` - Configuration files
- `/var/log` - Log files (very important for DevOps!)
- `/tmp` - Temporary files

**Additional Directories (Good to Know):**
- `/bin` - Essential command binaries
- `/usr/bin` - User command binaries
- `/opt` - Optional/third-party applications

For each directory:
- Write 1-2 lines explaining what it contains
- Run `ls -l <directory>` and note 1-2 files/folders you see
- Write one sentence: "I would use this when..."

**Hands-on task:**
```bash
# Find the largest log file in /var/log
du -sh /var/log/* 2>/dev/null | sort -h | tail -5

# Look at a config file in /etc
cat /etc/hostname

# Check your home directory
ls -la ~
```

---

### Part 2: Scenario-Based Practice (40 minutes)

**Important:** Focus on understanding the **troubleshooting flow**, not memorizing commands. Use the hints!

---

#### SOLVED EXAMPLE: Understanding How to Approach Scenarios

**Example Scenario: Check if a service is running**
```
Question: How do you check if the 'nginx' service is running?
```

**My Solution (Step by step):**

**Step 1:** Check service status
```bash
systemctl status nginx
```
**Why this command?** It shows if the service is active, failed, or stopped

**Step 2:** If service is not found, list all services
```bash
systemctl list-units --type=service
```
**Why this command?** To see what services exist on the system

**Step 3:** Check if service is enabled on boot
```bash
systemctl is-enabled nginx
```
**Why this command?** To know if it will start automatically after reboot

**What I learned:** Always check status first, then investigate based on what you see.

---

Now try these scenarios yourself:

---

**Scenario 1: Service Not Starting** 
```
A web application service called 'myapp' failed to start after a server reboot.
What commands would you run to diagnose the issue?
Write at least 4 commands in order.
```

**Hint:**
- First check: Is the service running or failed?
- Then check: What do the logs say?
- Finally check: Is it enabled to start on boot?

**Commands to explore:** `systemctl status myapp`, `systemctl is-enabled myapp`, `journalctl -u myapp -n 50`

**Resource:** Review Day 04 (Process and Services practice)

**Template for your answer:**
```
Step 1: [command]
Why: [one line explanation]

Step 2: [command]
Why: [one line explanation]

...
```

---

**Scenario 2: High CPU Usage** 
```
Your manager reports that the application server is slow.
You SSH into the server. What commands would you run to identify
which process is using high CPU?
```

**Hint:**
- Use a command that shows **live** CPU usage
- Look for processes sorted by CPU percentage
- Note the PID (Process ID) of the top process

**Commands to explore:** `top` (press 'q' to quit), `htop`, `ps aux --sort=-%cpu | head -10`

**Resource:** Review Day 05 (Troubleshooting Drill - CPU & Memory section)

---

**Scenario 3: Finding Service Logs** 
```
A developer asks: "Where are the logs for the 'docker' service?"
The service is managed by systemd.
What commands would you use?
```

**Hint:**
- systemd services → logs are in journald
- Command pattern: `journalctl -u <service-name>`
- Use -n flag to limit number of lines
- Use -f flag to follow logs in real-time (like tail -f)

**Commands to explore:**
```bash
# Check service status first
systemctl status ssh

# View last 50 lines of logs
journalctl -u ssh -n 50

# Follow logs in real-time
journalctl -u ssh -f
```

**Resource:** Review Day 04 (Process and Services - Log checks section)

---

**Scenario 4: File Permissions Issue** 
```
A script at /home/user/backup.sh is not executing.
When you run it: ./backup.sh
You get: "Permission denied"

What commands would you use to fix this?
```

**Hint:**
- First: Check what permissions the file has
- Understand: Files need 'x' (execute) permission to run
- Fix: Add execute permission with chmod

**Step-by-step solution structure:**
```
Step 1: Check current permissions
Command: ls -l /home/user/backup.sh
Look for: -rw-r--r-- (notice no 'x' = not executable)

Step 2: Add execute permission
Command: chmod +x /home/user/backup.sh

Step 3: Verify it worked
Command: ls -l /home/user/backup.sh
Look for: -rwxr-xr-x (notice 'x' = executable)

Step 4: Try running it
Command: ./backup.sh
```

**Resource:** Review Day 02 (File Permissions and Users Management)

---

## Why This Matters for DevOps
Understanding the file system is critical for:
- Knowing where to find logs, configs, and binaries
- Troubleshooting deployment issues
- Writing automation scripts that work across systems

Scenario-based practice prepares you for:
- Real production incidents
- DevOps interviews
- On-call troubleshooting under pressure

These are questions you **will** face in interviews and during real incidents.

---


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
