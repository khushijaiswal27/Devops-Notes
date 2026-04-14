### Day 12: Git Lifecycle & Architecture 🛠️


Today, I deep-dived into the internal architecture of Git and how it tracks changes. Understanding the "Stages" is the foundation of becoming a DevOps Engineer.

## 📌 Key Concepts Learned:

### 1. The Three Stages of Git
Git operates in three distinct areas:
* **Working Directory:** The local folder where I create or modify files. These are "untracked" by Git initially.
* **Staging Area (Index):** A buffer zone. When I run `git add`, files move here. It allows me to group specific changes before finalizing them.
* **Local Repository:** When I run `git commit`, the changes are permanently saved as a "Snapshot" in the `.git` directory.

### 2. Snapshots vs. Incremental Backups
Unlike traditional backup systems that copy entire files every time, Git takes a **Snapshot**. If a file hasn't changed, Git simply creates a link to the previous version to save memory and improve speed.

### 3. Commit IDs & Data Integrity
Every commit is assigned a unique 40-character **SHA-1 Hash ID** (e.g., `5a3f92...`). This ID is generated based on the content, author, and timestamp, ensuring that the code history can never be tampered with.

### 4. Local vs. Central Repository
* **Git (Local):** Manages versions on my own machine.
* **GitHub (Central):** A hosting service where I `push` my local repository so others can collaborate or I can have a remote backup.

---

## 💻 Commands Practiced:

| Command | Description |
| :--- | :--- |
| `git init` | Initializes a brand new Git repository in the current folder. |
| `git add <file>` | Moves changes from the Working Directory to the Staging Area. |
| `git commit -m "msg"` | Saves the staged snapshot to the Local Repository with a message. |
| `git log` | Displays the history of all commits made in the project.  

# Day 12  Notes:
![Lecture-12-Notes-pg1 jpg](https://github.com/user-attachments/assets/7514914e-53ba-42b7-af37-3ea65cb74db4)
![Lecture-12-Notes-pg2 jpg](https://github.com/user-attachments/assets/3d9ff3ee-08d1-4b43-bf26-e5d1c47044ec)
![Lecture-12-Notes-pg3 jpg](https://github.com/user-attachments/assets/82f27318-eaa5-4b23-b2e2-bcc6068408f7)
![Lecture-12-Notes-pg4 jpg](https://github.com/user-attachments/assets/cf61783b-d824-46b3-8ad3-a03cd18872e7)
![Lecture-12-Notes-pg5 jpg](https://github.com/user-attachments/assets/1f1d4597-9f18-4135-bd1b-0aaf7fbb6984)
