### Day 17: Shell Scripting Fundamentals (Hour 1)

Today, I officially started my Shell Scripting journey with M Prashant’s Masterclass. This phase is all about automating the manual Linux tasks I've learned so far.

🎯 Key Learnings:

- Shell & Kernel: Built a clear understanding of how the Shell acts as an interface between the user and the Linux Kernel.

- The Shebang: Learned why #!/bin/bash is mandatory at the start of every script to tell the system which interpreter to use.

- Execution: Mastered running scripts using bash script.sh and the importance of executable permissions.

- Variables: Practiced User-Defined Variables and used the readonly keyword to create constants that cannot be changed.

- Arrays & Strings: Learned to store multiple values in Arrays and performed advanced string operations like Slicing ${var:offset:len} and Case Conversion ${var^^}.

### Task 21 
Start your shell scripting journey — learn the fundamentals every script needs.

You will:
- Understand **shebang** (`#!/bin/bash`) and why it matters
- Work with **variables**, **echo**, and **read**
- Write basic **if-else** conditions

---

## Expected Output
- A markdown file: `day-16-shell-scripting.md`
- All scripts you write during the tasks

---

## Challenge Tasks

### Task 1: Your First Script
1. Create a file `hello.sh`
2. Add the shebang line `#!/bin/bash` at the top
3. Print `Hello, DevOps!` using `echo`
4. Make it executable and run it

```bash
chmod +x hello.sh
./hello.sh
```

**Document:** What happens if you remove the shebang line?

---

### Task 2: Variables
1. Create `variables.sh` with:
   - A variable for your `NAME`
   - A variable for your `ROLE` (e.g., "DevOps Engineer")
   - Print: `Hello, I am <NAME> and I am a <ROLE>`
2. Try using single quotes vs double quotes — what's the difference?

---

### Task 3: User Input with read
1. Create `greet.sh` that:
   - Asks the user for their name using `read`
   - Asks for their favourite tool
   - Prints: `Hello <name>, your favourite tool is <tool>`

---

### Task 4: If-Else Conditions
1. Create `check_number.sh` that:
   - Takes a number using `read`
   - Prints whether it is **positive**, **negative**, or **zero**

2. Create `file_check.sh` that:
   - Asks for a filename
   - Checks if the file **exists** using `-f`
   - Prints appropriate message

---

### Task 5: Combine It All
Create `server_check.sh` that:
1. Stores a service name in a variable (e.g., `nginx`, `sshd`)
2. Asks the user: "Do you want to check the status? (y/n)"
3. If `y` — runs `systemctl status <service>` and prints whether it's **active** or **not**
4. If `n` — prints "Skipped."

---

## Hints
- Shebang: `#!/bin/bash` tells the system which interpreter to use
- Variables: `NAME="Shubham"` (no spaces around `=`)
- Read: `read -p "Enter name: " NAME`
- If syntax: `if [ condition ]; then ... elif ... else ... fi`
- File check: `if [ -f filename ]; then`

---

## Documentation

Create `day-16-shell-scripting.md` with:
- Each script's code and output
- What you learned (3 key points)

---



- 📸 Lab Proof (Screenshot):
<img width="753" height="90" alt="Screenshot 2026-03-09 200519" src="https://github.com/user-attachments/assets/22d747d0-5000-46c6-8217-4556c755ce65" />
<img width="882" height="1000" alt="Screenshot 2026-03-09 200601" src="https://github.com/user-attachments/assets/d2293a7c-afa8-45f7-8dec-1c967f81497b" />

