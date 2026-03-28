### Day 5 - Linux Architecture & File System Hierarchy

## Task 4
Today’s goal is to **practice Linux fundamentals with real commands**.

You will create a short practice note by actually running basic commands and capturing what you see:
- Check running processes
- Inspect one systemd service
- Capture a small troubleshooting flow

This is hands-on. Keep it simple and focused on fundamentals.

---

## Expected Output
By the end of today, you should have:

- A markdown file named:  
  `linux-practice.md`

or

- A hand written practice log (Recommended)

Your note should show what you actually ran on your system.

---

## Guidelines
Follow these rules while creating your practice note:

- Run and record output for **at least 6 commands**
- Include **2 process commands** (`ps`, `top`, `pgrep`, etc.)
- Include **2 service commands** (`systemctl status`, `systemctl list-units`, etc.)
- Include **2 log commands** (`journalctl -u <service>`, `tail -n 50`, etc.)
- Pick **one service on your system** (example: `ssh`, `cron`, `docker`) and inspect it
- Keep it **simple and actionable**

Suggested structure for `linux-practice.md`:
- Process checks
- Service checks
- Log checks
- Mini troubleshooting steps

---
## Why This Matters for DevOps
Hands‑on practice builds speed and confidence.

When issues happen in production, you won’t have time to search for basic commands.  
This day helps you build muscle memory with Linux fundamentals.

---

## Task 5
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
