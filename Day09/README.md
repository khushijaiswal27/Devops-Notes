### Day 9: Linux User Management & File Linking
## Task 9
Today's goal is to **practice user and group management** by completing hands-on challenges.

Figure out how to:
- Create users and set passwords
- Create groups and assign users
- Set up shared directories with group permissions

Use what you learned from Days 1-7 to find the right commands!

---

## Expected Output
- A markdown file: `day-09-user-management.md`
- Screenshots of command outputs
- List of commands used

---

## Challenge Tasks

### Task 1: Create Users (20 minutes)

Create three users with home directories and passwords:
- `tokyo`
- `berlin`
- `professor`

**Verify:** Check `/etc/passwd` and `/home/` directory

---

### Task 2: Create Groups (10 minutes)

Create two groups:
- `developers`
- `admins`

**Verify:** Check `/etc/group`

---

### Task 3: Assign to Groups (15 minutes)

Assign users:
- `tokyo` → `developers`
- `berlin` → `developers` + `admins` (both groups)
- `professor` → `admins`

**Verify:** Use appropriate command to check group membership

---

### Task 4: Shared Directory (20 minutes)

1. Create directory: `/opt/dev-project`
2. Set group owner to `developers`
3. Set permissions to `775` (rwxrwxr-x)
4. Test by creating files as `tokyo` and `berlin`

**Verify:** Check permissions and test file creation

---

### Task 5: Team Workspace (20 minutes)

1. Create user `nairobi` with home directory
2. Create group `project-team`
3. Add `nairobi` and `tokyo` to `project-team`
4. Create `/opt/team-workspace` directory
5. Set group to `project-team`, permissions to `775`
6. Test by creating file as `nairobi`

---

## Hints

**Stuck? Try these commands:**
- User: `useradd`, `passwd`, `usermod`
- Group: `groupadd`, `groups`
- Permissions: `chgrp`, `chmod`
- Test: `sudo -u username command`

**Tip:** Use `-m` flag with useradd for home directory, `-aG` for adding to groups

---

## Documentation

Create `day-09-user-management.md`:

```markdown
# Day 09 Challenge

## Users & Groups Created
- Users: tokyo, berlin, professor, nairobi
- Groups: developers, admins, project-team

## Group Assignments
[List who is in which groups]

## Directories Created
[List directories with permissions]

## Commands Used
[Your commands here]

## What I Learned
[3 key points]
```

---

###  Task 10
Master file permissions and basic file operations in Linux.

- Create and read files using `touch`, `cat`, `vim`
- Understand and modify permissions using `chmod`

---

## Expected Output
- A markdown file: `day-10-file-permissions.md`
- Screenshots showing permission changes

---

## Challenge Tasks

### Task 1: Create Files (10 minutes)

1. Create empty file `devops.txt` using `touch`
2. Create `notes.txt` with some content using `cat` or `echo`
3. Create `script.sh` using `vim` with content: `echo "Hello DevOps"`

**Verify:** `ls -l` to see permissions

---

### Task 2: Read Files (10 minutes)

1. Read `notes.txt` using `cat`
2. View `script.sh` in vim read-only mode
3. Display first 5 lines of `/etc/passwd` using `head`
4. Display last 5 lines of `/etc/passwd` using `tail`

---

### Task 3: Understand Permissions (10 minutes)

Format: `rwxrwxrwx` (owner-group-others)
- `r` = read (4), `w` = write (2), `x` = execute (1)

Check your files: `ls -l devops.txt notes.txt script.sh`

Answer: What are current permissions? Who can read/write/execute?

---

### Task 4: Modify Permissions (20 minutes)

1. Make `script.sh` executable → run it with `./script.sh`
2. Set `devops.txt` to read-only (remove write for all)
3. Set `notes.txt` to `640` (owner: rw, group: r, others: none)
4. Create directory `project/` with permissions `755`

**Verify:** `ls -l` after each change

---

### Task 5: Test Permissions (10 minutes)

1. Try writing to a read-only file - what happens?
2. Try executing a file without execute permission
3. Document the error messages

---

## Hints

- Create: `touch`, `cat > file`, `vim file`
- Read: `cat`, `head -n`, `tail -n`
- Permissions: `chmod +x`, `chmod -w`, `chmod 755`

---

## Documentation

Create `day-10-file-permissions.md`:

```markdown
# Day 10 Challenge

## Files Created
[list files]

## Permission Changes
[before/after for each file]

## Commands Used
[your commands]

## What I Learned
[3 key points]
```

---


## Troubleshooting

**Permission denied?** Use `sudo`

**User can't access directory?**
- Check group: `groups username`
- Check permissions: `ls -ld /path`

---

## Task 11
Master file and directory ownership in Linux.

- Understand file ownership (user and group)
- Change file owner using `chown`
- Change file group using `chgrp`
- Apply ownership changes recursively

---

## Expected Output
- A markdown file: `day-11-file-ownership.md`
- Screenshots showing ownership changes

---

## Challenge Tasks

### Task 1: Understanding Ownership (10 minutes)

1. Run `ls -l` in your home directory
2. Identify the **owner** and **group** columns
3. Check who owns your files

**Format:** `-rw-r--r-- 1 owner group size date filename`

Document: What's the difference between owner and group?

---

### Task 2: Basic chown Operations (20 minutes)

1. Create file `devops-file.txt`
2. Check current owner: `ls -l devops-file.txt`
3. Change owner to `tokyo` (create user if needed)
4. Change owner to `berlin`
5. Verify the changes

**Try:**
```bash
sudo chown tokyo devops-file.txt
```

---

### Task 3: Basic chgrp Operations (15 minutes)

1. Create file `team-notes.txt`
2. Check current group: `ls -l team-notes.txt`
3. Create group: `sudo groupadd heist-team`
4. Change file group to `heist-team`
5. Verify the change

---

### Task 4: Combined Owner & Group Change (15 minutes)

Using `chown` you can change both owner and group together:

1. Create file `project-config.yaml`
2. Change owner to `professor` AND group to `heist-team` (one command)
3. Create directory `app-logs/`
4. Change its owner to `berlin` and group to `heist-team`

**Syntax:** `sudo chown owner:group filename`

---

### Task 5: Recursive Ownership (20 minutes)

1. Create directory structure:
   ```
   mkdir -p heist-project/vault
   mkdir -p heist-project/plans
   touch heist-project/vault/gold.txt
   touch heist-project/plans/strategy.conf
   ```

2. Create group `planners`: `sudo groupadd planners`

3. Change ownership of entire `heist-project/` directory:
   - Owner: `professor`
   - Group: `planners`
   - Use recursive flag (`-R`)

4. Verify all files and subdirectories changed: `ls -lR heist-project/`

---

### Task 6: Practice Challenge (20 minutes)

1. Create users: `tokyo`, `berlin`, `nairobi` (if not already created)
2. Create groups: `vault-team`, `tech-team`
3. Create directory: `bank-heist/`
4. Create 3 files inside:
   ```
   touch bank-heist/access-codes.txt
   touch bank-heist/blueprints.pdf
   touch bank-heist/escape-plan.txt
   ```

5. Set different ownership:
   - `access-codes.txt` → owner: `tokyo`, group: `vault-team`
   - `blueprints.pdf` → owner: `berlin`, group: `tech-team`
   - `escape-plan.txt` → owner: `nairobi`, group: `vault-team`

**Verify:** `ls -l bank-heist/`

---

## Key Commands Reference

```bash
# View ownership
ls -l filename

# Change owner only
sudo chown newowner filename

# Change group only
sudo chgrp newgroup filename

# Change both owner and group
sudo chown owner:group filename

# Recursive change (directories)
sudo chown -R owner:group directory/

# Change only group with chown
sudo chown :groupname filename
```

---

## Hints

- Most `chown`/`chgrp` operations need `sudo`
- Use `-R` flag for recursive directory changes
- Always verify with `ls -l` after changes
- User must exist before using in `chown`
- Group must exist before using in `chgrp`/`chown`

---

## Documentation

Create `day-11-file-ownership.md`:

```markdown
# Day 11 Challenge

## Files & Directories Created
[list all files/directories]

## Ownership Changes
[before/after for each file]

Example:
- devops-file.txt: user:user → tokyo:heist-team

## Commands Used
[your commands here]

## What I Learned
[3 key points about file ownership]
```

---

## Troubleshooting

**Permission denied?**
- Use `sudo` for chown/chgrp operations

**Group doesn't exist?**
- Create it first: `sudo groupadd groupname`

**User doesn't exist?**
- Create it first: `sudo useradd username`

---

## Why This Matters for DevOps

In real DevOps scenarios, you need proper file ownership for:

- Application deployments
- Shared team directories
- Container file permissions
- CI/CD pipeline artifacts
- Log file management

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
