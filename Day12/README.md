### Day 12: Git Lifecycle & Architecture 🛠️

## Task 16

Now that you know how to create repos, stage, and commit — it's time to learn the most powerful concept in Git: **branching**. Branches let you work on features, fixes, and experiments in isolation without breaking your main code. You'll also push your work to GitHub for the first time.

---

## Expected Output
- A markdown file: `day-23-notes.md` with your answers
- Continue updating `git-commands.md` in your `devops-git-practice` repo
- Your practice repo pushed to GitHub

---

## Challenge Tasks

### Task 1: Understanding Branches
Answer these in your `day-23-notes.md`:
1. What is a branch in Git?
2. Why do we use branches instead of committing everything to `main`?
3. What is `HEAD` in Git?
4. What happens to your files when you switch branches?

---

### Task 2: Branching Commands — Hands-On
In your `devops-git-practice` repo, perform the following:
1. List all branches in your repo
2. Create a new branch called `feature-1`
3. Switch to `feature-1`
4. Create a new branch and switch to it in a single command — call it `feature-2`
5. Try using `git switch` to move between branches — how is it different from `git checkout`?
6. Make a commit on `feature-1` that does **not** exist on `main`
7. Switch back to `main` — verify that the commit from `feature-1` is not there
8. Delete a branch you no longer need
9. Add all branching commands to your `git-commands.md`

---

### Task 3: Push to GitHub
1. Create a **new repository** on GitHub (do NOT initialize it with a README)
2. Connect your local `devops-git-practice` repo to the GitHub remote
3. Push your `main` branch to GitHub
4. Push `feature-1` branch to GitHub
5. Verify both branches are visible on GitHub
6. Answer in your notes: What is the difference between `origin` and `upstream`?

---

### Task 4: Pull from GitHub
1. Make a change to a file **directly on GitHub** (use the GitHub editor)
2. Pull that change to your local repo
3. Answer in your notes: What is the difference between `git fetch` and `git pull`?

---

### Task 5: Clone vs Fork
1. **Clone** any public repository from GitHub to your local machine
2. **Fork** the same repository on GitHub, then clone your fork
3. Answer in your notes:
   - What is the difference between clone and fork?
   - When would you clone vs fork?
   - After forking, how do you keep your fork in sync with the original repo?

---

## Hints
- When you create a branch, it starts from the commit you're currently on
- `git switch` is the modern alternative to `git checkout` for switching branches
- To push a new branch: `git push -u origin <branch-name>`
- A fork is a GitHub concept, not a Git concept

---

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
