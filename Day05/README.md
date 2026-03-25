### Day 5 - Linux Architecture & File System Hierarchy

## Linux Commands Practice
## Task
Today’s goal is to **build your Linux command confidence**.

You will create a cheat sheet of commands focused on:
- Process management
- File system
- Networking troubleshooting

This is the command toolkit you will reuse for years.

---

## Expected Output
By the end of today, you should have:

- A markdown file named:  
  `linux-commands-cheatsheet.md`

or

- A hand written cheat sheet (Recommended)

Your cheat sheet should be easy to scan during real troubleshooting.

---

## Guidelines
Follow these rules while creating your cheat sheet:

- Include **at least 20 commands** with one‑line usage notes
- Add **3 networking commands** (`ping`, `ip addr`, `dig`, `curl`, etc.)
- Group commands by category
- Keep it concise and readable

---

## Why This Matters for DevOps
Real production issues are solved at the command line.

The faster you can inspect logs and network issues, the faster you can:
- Restore service
- Reduce downtime
- Gain trust as an operator

  
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
