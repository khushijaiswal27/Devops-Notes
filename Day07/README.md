
### Day 7 - Advanced Directory Management & File Operations

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
