## Day 21: Shell Scripting DevOps Projects Portfolio


This repository contains real-world Shell Scripts developed during Day 21 of the Shell Scripting Masterclass. These projects focus on automating System Administration and monitoring tasks.

🛠 Projects Documentation
1. 👤 User Management Automation (Project 1)
File: create_user.sh

Purpose: To automate the process of adding a new local user with a secure, auto-generated password.

Logic: 1. Root Check: Verifies if the script is run by a user with Root privileges (UID 0).
2. Input Handling: Takes the username as a command-line argument ($1) and treating the rest as comments.
3. Password Generation: Automatically creates a unique password using date +%s%N.
4. Security: Forces the user to change their password on the very first login (passwd -e).

2. 📂 Automated File Archiving & Backup (Project 2)
File: archive_project.sh

Purpose: To identify large files (20MB+) and compress them into a backup folder to save disk space.

Logic:

Search: Uses the find command to locate files based on size (-size +20M) and type (-f).

Compression: Applies gzip to shrink file sizes.

Migration: Moves compressed .gz files to a dedicated /archive folder.

Automation: Can be scheduled via Crontab to run every night at 2:00 AM.

3. 📊 RAM Monitoring Script (Project 3)
File: ram_monitor.sh

Purpose: To track system memory health and alert the admin when the server is running low on RAM.

Logic: Uses free -m to extract memory stats and awk to target the free memory column. If free memory is below a certain threshold (e.g., 500MB), it triggers a warning on the terminal.

📧 4. Disk Usage Alert with Email (Project 4)
File: disk_alert.sh

Purpose: To monitor disk partition usage and send an automated email alert if usage exceeds a set limit.

Logic: Parses the df -h command to check usage percentage. Integrates with Postfix (Mail Server) to send a notification to the SysAdmin for immediate action.

🔑 Key Learnings (Day 21 Focus)
Real-World Automation: Moving from simple commands to building end-to-end solutions.

Error Handling: Using exit statuses ($?) to ensure scripts stop if a command fails.

Advanced Find & Grep: Filtering system data precisely for monitoring.

Crontab Scheduling: Implementing background automation for maintenance tasks.

⚙️ How to Setup
Clone the Repository:
git clone https://github.com/khushijaiswal27/shellscript_Tasks.git

Give Execution Permission:
chmod +x *.sh

Execute the Script:
sudo ./script_name.sh
