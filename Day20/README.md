### Day 20: Script Automation & Job Scheduling 📂

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
