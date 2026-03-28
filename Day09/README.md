### Day 9: Linux User Management & File Linking

## Task
Today’s goal is to **run a focused troubleshooting drill**.

You will pick a running process/service on your system and:
- Capture a quick health snapshot (CPU, memory, disk, network)
- Trace logs for that service
- Write a **mini runbook** describing what you did and what you’d do next if things were worse

This turns yesterday’s practice into a repeatable troubleshooting routine.

### What’s a runbook?
A **runbook** is a short, repeatable checklist you follow during an incident: the exact commands you run, what you observed, and the next actions if the issue persists. Keep it concise so you can reuse it under pressure.

---

## Expected Output
By the end of today, you should have:

- A markdown file named:  
  `linux-troubleshooting-runbook.md`

or

- A hand written runbook (Recommended)

Your runbook should include both the commands you ran and brief interpretations.

---

## Guidelines
Follow these rules while creating your runbook:

- Run and record output for **at least 8 commands** (save snippets in your runbook)  
  - **Environment basics (2):** `uname -a`, `lsb_release -a` (or `cat /etc/os-release`)  
  - **Filesystem sanity (2):** create a throwaway folder and file, e.g., `mkdir /tmp/runbook-demo`, `cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo`  
  - **CPU / Memory (2):** `top`/`htop`/`ps -o pid,pcpu,pmem,comm -p <pid>`, `free -h`, `vm_stat` (mac)  
  - **Disk / IO (2):** `df -h`, `du -sh /var/log`, `iostat`/`vmstat`/`dstat`  
  - **Network (2):** `ss -tulpn`/`netstat -tulpn`, `curl -I <service-endpoint>`/`ping`  
  - **Logs (2):** `journalctl -u <service> -n 50`, `tail -n 50 /var/log/<file>.log`
- Choose **one target service/process** (e.g., `ssh`, `cron`, `docker`, your web app) and stick to it for the drill.
- For each command, add a 1–2 line note on what you observed (e.g., “CPU spikes to 80% when restarting”, “No recent errors in last 50 lines”).
- End with a **“If this worsens”** section listing 3 next steps you would take (ex: restart strategy, increase log verbosity, collect `strace`).
- Keep it concise and actionable (aim for ~1 page).

Suggested structure for `linux-troubleshooting-runbook.md`:
- Target service / process
- Snapshot: CPU & Memory
- Snapshot: Disk & IO
- Snapshot: Network
- Logs reviewed
- Quick findings
- If this worsens (next steps)

---
## Why This Matters for DevOps
Incidents rarely come with perfect clues. A fast, repeatable checklist saves minutes when services misbehave.

This drill builds:
- Habit of capturing evidence before acting
- Confidence reading resource signals (CPU, memory, disk, network)
- Log-first mindset before restarts or escalations

These habits reduce downtime and prevent guesswork in production.

---


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
