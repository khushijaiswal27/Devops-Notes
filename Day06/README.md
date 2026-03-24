### Day 6 - File Management & Editors in Linux

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
