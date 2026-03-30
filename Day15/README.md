### Day 15: Git Branching, Stashing, and Undo Operations 🛠️

##Task 19 :
Every time you switch to the browser to create a PR, check an issue, or manage a repo — you lose context. The **GitHub CLI (`gh`)** lets you do all of that without leaving your terminal. For DevOps engineers, this is essential — especially when you start automating workflows, scripting PR reviews, and managing repos at scale.

---

## Expected Output
- A markdown file: `day-26-notes.md` with your observations and answers
- Add `gh` commands to your `git-commands.md`

---

## Challenge Tasks

### Task 1: Install and Authenticate
1. Install the GitHub CLI on your machine
2. Authenticate with your GitHub account
3. Verify you're logged in and check which account is active
4. Answer in your notes: What authentication methods does `gh` support?

---

### Task 2: Working with Repositories
1. Create a **new GitHub repo** directly from the terminal — make it public with a README
2. Clone a repo using `gh` instead of `git clone`
3. View details of one of your repos from the terminal
4. List all your repositories
5. Open a repo in your browser directly from the terminal
6. Delete the test repo you created (be careful!)

---

### Task 3: Issues
1. Create an issue on one of your repos from the terminal — give it a title, body, and a label
2. List all open issues on that repo
3. View a specific issue by its number
4. Close an issue from the terminal
5. Answer in your notes: How could you use `gh issue` in a script or automation?

---

### Task 4: Pull Requests
1. Create a branch, make a change, push it, and create a **pull request** entirely from the terminal
2. List all open PRs on a repo
3. View the details of your PR — check its status, reviewers, and checks
4. Merge your PR from the terminal
5. Answer in your notes:
   - What merge methods does `gh pr merge` support?
   - How would you review someone else's PR using `gh`?

---

### Task 5: GitHub Actions & Workflows (Preview)
1. List the workflow runs on any public repo that uses GitHub Actions
2. View the status of a specific workflow run
3. Answer in your notes: How could `gh run` and `gh workflow` be useful in a CI/CD pipeline?

(Don't worry if you haven't learned GitHub Actions yet — this is a preview for upcoming days)

---

### Task 6: Useful `gh` Tricks
Explore and try these — add the ones you find useful to your `git-commands.md`:
1. `gh api` — make raw GitHub API calls from the terminal
2. `gh gist` — create and manage GitHub Gists
3. `gh release` — create and manage releases
4. `gh alias` — create shortcuts for commands you use often
5. `gh search repos` — search GitHub repos from the terminal

---

## Hints
- `gh help` and `gh <command> --help` are your best friends
- Most `gh` commands work with `--repo owner/repo` to target a specific repo
- Use `--json` flag with most commands to get machine-readable output (useful for scripting)
- `gh pr create --fill` auto-fills the PR title and body from your commits

---




Today’s session focused on advanced Git workflows, specifically how to manage parallel development and revert mistakes.

### Key Learnings:
- **Branching & Checkout**: Created branches to isolate new features from the master branch, enabling parallel development.
- **Git Merge & Conflicts**: Learned how to combine code from different branches and manually resolve conflicts when changes overlap in the same file.
- **Git Stash**: Mastered the use of `git stash` to temporarily save uncommitted work-in-progress, allowing me to switch tasks without losing progress.
- **Git Reset (Soft/Mixed)**: Learned to move files out of the staging area back to the working directory using `git reset`.
- **Git Reset --hard**: Practiced completely reverting the working directory and staging area to the last stable commit to discard unwanted changes.

"Mastering these commands ensures a clean and stable project history even when mistakes happen." 🚀

- 📸 Lab Proof (Screenshot):
<img width="951" height="1017" alt="Screenshot 2026-03-04 124759" src="https://github.com/user-attachments/assets/5c27aab6-3791-43a4-a1a8-c93dd0bc2232" />
<img width="920" height="1014" alt="Screenshot 2026-03-04 125240" src="https://github.com/user-attachments/assets/d049465a-56af-4c51-ab05-a9913490d6d5" />
<img width="927" height="1012" alt="Screenshot 2026-03-04 133358" src="https://github.com/user-attachments/assets/3823a1ef-e0c6-4044-82d8-4449d5f1ce6f" />
<img width="785" height="1019" alt="Screenshot 2026-03-04 135535" src="https://github.com/user-attachments/assets/ccfa72af-3ebc-45e5-8b4e-cba8e6686b66" />
<img width="884" height="694" alt="Screenshot 2026-03-04 140513" src="https://github.com/user-attachments/assets/74a14104-1cb1-4014-8e9f-e77424d0c703" />

 # Day15  notes-
 ![Lecture-15-Notes-pg1 jpg](https://github.com/user-attachments/assets/4ce85292-1eb9-49b0-b95b-2b71e32731a5)
![Lecture-15-Notes-pg2 jpg](https://github.com/user-attachments/assets/421d5f63-50b4-498a-923a-0738fd692548)
![Lecture-15-Notes-pg3 jpg](https://github.com/user-attachments/assets/d63941c0-b3c3-4f8d-8e83-d47b41c17b91)
![Lecture-15-Notes-pg4 jpg](https://github.com/user-attachments/assets/fccd2241-0238-41b1-a57b-57f629567b45)

