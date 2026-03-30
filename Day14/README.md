### Lecture 14: Git Operations & Multi-Region Sync

##Task 18 :
You'll learn how to **undo mistakes** safely — one of the most important skills in Git. You'll also explore **branching strategies** used by real engineering teams to manage code at scale.

---

## Expected Output
- A markdown file: `day-25-notes.md` with your observations and answers
- Continue updating `git-commands.md` in your `devops-git-practice` repo

---

## Challenge Tasks

### Task 1: Git Reset — Hands-On
1. Make 3 commits in your practice repo (commit A, B, C)
2. Use `git reset --soft` to go back one commit — what happens to the changes?
3. Re-commit, then use `git reset --mixed` to go back one commit — what happens now?
4. Re-commit, then use `git reset --hard` to go back one commit — what happens this time?
5. Answer in your notes:
   - What is the difference between `--soft`, `--mixed`, and `--hard`?
   - Which one is destructive and why?
   - When would you use each one?
   - Should you ever use `git reset` on commits that are already pushed?

---

### Task 2: Git Revert — Hands-On
1. Make 3 commits (commit X, Y, Z)
2. Revert commit Y (the middle one) — what happens?
3. Check `git log` — is commit Y still in the history?
4. Answer in your notes:
   - How is `git revert` different from `git reset`?
   - Why is revert considered **safer** than reset for shared branches?
   - When would you use revert vs reset?

---

### Task 3: Reset vs Revert — Summary
Create a comparison in your notes:

| | `git reset` | `git revert` |
|---|---|---|
| What it does | ? | ? |
| Removes commit from history? | ? | ? |
| Safe for shared/pushed branches? | ? | ? |
| When to use | ? | ? |

---

### Task 4: Branching Strategies
Research the following branching strategies and document each in your notes with:
- How it works (short description)
- A simple diagram or flow (text-based is fine)
- When/where it's used
- Pros and cons

1. **GitFlow** — develop, feature, release, hotfix branches
2. **GitHub Flow** — simple, single main branch + feature branches
3. **Trunk-Based Development** — everyone commits to main, short-lived branches
4. Answer:
   - Which strategy would you use for a startup shipping fast?
   - Which strategy would you use for a large team with scheduled releases?
   - Which one does your favorite open-source project use? (check any repo on GitHub)

---

### Task 5: Git Commands Reference Update
Update your `git-commands.md` to cover everything from Days 22–25:
- Setup & Config
- Basic Workflow (add, commit, status, log, diff)
- Branching (branch, checkout, switch)
- Remote (push, pull, fetch, clone, fork)
- Merging & Rebasing
- Stash & Cherry Pick
- Reset & Revert

---

## Hints
- `git reflog` is your safety net — it shows everything Git has done, even after a hard reset
- For branching strategies, look at how projects like Kubernetes, React, or Linux kernel manage branches

---



This session focused on collaborating between multiple local repositories and a single central repository.

# 🛠️ Tasks Performed:-

Initialization: Used git init to set up local repositories on AWS.
Identity Setup: Configured user.name and user.email to track different authors (Mumbai vs. Singapore).

# Push/Pull Workflow:

Created and committed files in the Mumbai instance.
Uploaded (Pushed) the code to GitHub.
Downloaded (Pulled) the same code onto the Singapore instance.

* Inspection: Used git log and git show to verify code changes and commit history.

* Git Ignore: Created a .gitignore file to exclude specific file types (like .java and .css) from being tracked.

  - 📸 Lab Proof (Screenshot):-
 <img width="906" height="1005" alt="Screenshot 2026-03-01 172251" src="https://github.com/user-attachments/assets/b1226555-896c-4279-a395-e657c133c068" />
<img width="877" height="1003" alt="Screenshot 2026-03-01 180010" src="https://github.com/user-attachments/assets/5b44bf3c-1dcd-46f9-9e32-8b0acf7037ea" />

 # Day14  notes-
 ![Lecture-14-Notes-pg1 jpg](https://github.com/user-attachments/assets/96ec96b8-32d6-4bed-908c-0784d79a7eea)
![Lecture-14-Notes-pg2 jpg](https://github.com/user-attachments/assets/e9f58af4-ffc0-40cf-84c0-02a773e6f583)

