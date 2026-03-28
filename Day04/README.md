### Day 4 - Everything About Linux from Scratch

## Task 1
Today’s goal is to **understand how Linux works under the hood**.

You will create a short note that explains:
- The core components of Linux (kernel, user space, init/systemd)
- How processes are created and managed
- What systemd does and why it matters

This is the foundation for all troubleshooting you will do as a DevOps engineer.

---

## Expected Output
By the end of today, you should have:

- A markdown file named:  
  `linux-architecture-notes.md`

or

- A hand written set of notes (Recommended)

Your notes should be clear enough that someone new to Linux can follow them.

---

## Why This Matters for DevOps
Linux is the base OS for almost every production system.

If you know how processes and systemd work, you can:
- Debug crashed services faster
- Fix CPU/memory issues
- Understand logs and service restarts confidently

This knowledge saves hours during incidents.

---

## Task 2
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
