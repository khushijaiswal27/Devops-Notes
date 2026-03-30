### Day 20: Script Automation & Job Scheduling 📂

## Task 24 :

Apply everything from Days 16–18 in real-world mini projects.

You will:
- Write a **log rotation** script
- Write a **server backup** script
- Schedule them with **crontab**

---

## Expected Output
- A markdown file: `day-19-project.md`
- All scripts you write during the tasks

---

## Challenge Tasks

### Task 1: Log Rotation Script
Create `log_rotate.sh` that:
1. Takes a log directory as an argument (e.g., `/var/log/myapp`)
2. Compresses `.log` files older than 7 days using `gzip`
3. Deletes `.gz` files older than 30 days
4. Prints how many files were compressed and deleted
5. Exits with an error if the directory doesn't exist

---

### Task 2: Server Backup Script
Create `backup.sh` that:
1. Takes a source directory and backup destination as arguments
2. Creates a timestamped `.tar.gz` archive (e.g., `backup-2026-02-08.tar.gz`)
3. Verifies the archive was created successfully
4. Prints archive name and size
5. Deletes backups older than 14 days from the destination
6. Handles errors — exit if source doesn't exist

---

### Task 3: Crontab
1. Read: `crontab -l` — what's currently scheduled?
2. Understand cron syntax:
   ```
   * * * * *  command
   │ │ │ │ │
   │ │ │ │ └── Day of week (0-7)
   │ │ │ └──── Month (1-12)
   │ │ └────── Day of month (1-31)
   │ └──────── Hour (0-23)
   └────────── Minute (0-59)
   ```
3. Write cron entries (in your markdown, don't apply if unsure) for:
   - Run `log_rotate.sh` every day at 2 AM
   - Run `backup.sh` every Sunday at 3 AM
   - Run a health check script every 5 minutes

---

### Task 4: Combine — Scheduled Maintenance Script
Create `maintenance.sh` that:
1. Calls your log rotation function
2. Calls your backup function
3. Logs all output to `/var/log/maintenance.log` with timestamps
4. Write the cron entry to run it daily at 1 AM

---

## Hints
- Compress old files: `find /path -name "*.log" -mtime +7 -exec gzip {} \;`
- Timestamp: `date +%Y-%m-%d`
- Tar: `tar -czf backup.tar.gz /source/dir`
- Cron edit: `crontab -e`
- Log with timestamp: `echo "$(date): message" >> logfile`

---

## Documentation

Create `day-19-project.md` with:
- Each script's code
- Sample outputs
- Cron entries you wrote
- What you learned (3 key points)

---



Today’s session focused on making scripts autonomous and handling system outputs professionally.

### 1. Output Redirection (`>` and `>>`)
I mastered how to capture script output into files:
- `>` : **Overwrite** - Replaces existing file content with new output.
- `>>` : **Append** - Adds new output to the end of the file (Preserves history).

### 2. Running Scripts in Background
To prevent scripts from terminating when the terminal session ends:
- `nohup ./script.sh &` 
- **nohup**: (No Hang Up) ensures the process ignores the SIGHUP signal.
- **&**: Forces the script to run in the background.

### 3. Linux Job Scheduling: `at` Command 🕒
Used for **one-time** execution of tasks.
- **Workflow:** `at <time>` -> Write Command -> `Ctrl + D` to save.
- **Management:** - `atq`: View pending jobs.
  - `atrm <ID>`: Remove a scheduled job.

### 4. Linux Job Scheduling: `Cron` Command 🔄
Used for **recurring** tasks (Daily/Weekly/Monthly).
- `crontab -l`: List all active cron jobs.
- `crontab -e`: Edit the cron schedule.
- **Syntax:** `* * * * *` (Minute, Hour, Day of Month, Month, Day of Week).

### 5. Essential Setup on EC2
If the cron service is missing on an Amazon Linux/EC2 instance:
sudo yum install cronie -y
sudo systemctl start crond
sudo systemctl enable crond

📸 Lab Proof (Screenshot):
<img width="927" height="1007" alt="Screenshot 2026-03-17 181859" src="https://github.com/user-attachments/assets/ac95bf37-f3bd-44b0-b88a-1af378e1dd34" />
<img width="927" height="1007" alt="Screenshot 2026-03-17 181859" src="https://github.com/user-attachments/assets/fa84a421-6744-43f3-9822-7b769c6ffe93" />
