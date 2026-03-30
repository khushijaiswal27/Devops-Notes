### Day 18: Logic, Loops & Automation (Hour 2+)
Today’s session was a deep dive into the "Logic" of scripting. I covered everything from decision-making to repetitive task automation (up to 2:23:42 in the masterclass).

## Task 22 :
Level up your scripting — use loops, handle arguments, and deal with errors.

You will:
- Write **for** and **while** loops
- Use **command-line arguments** (`$1`, `$2`, `$#`, `$@`)
- Install packages via script
- Add basic **error handling**

---

## Expected Output
- A markdown file: `day-17-scripting.md`
- All scripts you write during the tasks

---

## Challenge Tasks

### Task 1: For Loop
1. Create `for_loop.sh` that:
   - Loops through a list of 5 fruits and prints each one
2. Create `count.sh` that:
   - Prints numbers 1 to 10 using a for loop

---

### Task 2: While Loop
1. Create `countdown.sh` that:
   - Takes a number from the user
   - Counts down to 0 using a while loop
   - Prints "Done!" at the end

---

### Task 3: Command-Line Arguments
1. Create `greet.sh` that:
   - Accepts a name as `$1`
   - Prints `Hello, <name>!`
   - If no argument is passed, prints "Usage: ./greet.sh <name>"

2. Create `args_demo.sh` that:
   - Prints total number of arguments (`$#`)
   - Prints all arguments (`$@`)
   - Prints the script name (`$0`)

---

### Task 4: Install Packages via Script
1. Create `install_packages.sh` that:
   - Defines a list of packages: `nginx`, `curl`, `wget`
   - Loops through the list
   - Checks if each package is installed (use `dpkg -s` or `rpm -q`)
   - Installs it if missing, skips if already present
   - Prints status for each package

> Run as root: `sudo -i` or `sudo su`

---

### Task 5: Error Handling
1. Create `safe_script.sh` that:
   - Uses `set -e` at the top (exit on error)
   - Tries to create a directory `/tmp/devops-test`
   - Tries to navigate into it
   - Creates a file inside
   - Uses `||` operator to print an error if any step fails

Example:
```bash
mkdir /tmp/devops-test || echo "Directory already exists"
```

2. Modify your `install_packages.sh` to check if the script is being run as root — exit with a message if not.

---

## Hints
- For loop: `for item in list; do ... done`
- While loop: `while [ condition ]; do ... done`
- Arguments: `$1` first arg, `$#` count, `$@` all args
- Check root: `if [ "$EUID" -ne 0 ]; then echo "Run as root"; exit 1; fi`
- Check package: `dpkg -s <pkg> &> /dev/null && echo "installed"`

---

## Documentation

Create `day-17-scripting.md` with:
- Each script's code and output
- What you learned (3 key points)

---



🎯 Key Learnings:

- Conditional Logic (If-Else): Learned to use if, else, and elif to make scripts smart.

- Numerical Operators: Mastered comparisons using -eq (equal), -gt (greater than), and -ne (not equal).

- Case Statements: Used case for creating clean, menu-driven scripts (a better alternative to multiple if-else).

- Logical Operators: Combined conditions using AND (&&) and OR (||) for complex checks.

- Loops (For & While): - For Loop: Perfect for iterating over fixed lists or ranges.

- While Loop: Essential for tasks that run as long as a condition is true.

- File Reading: Successfully implemented a script to read and process a text file line-by-line using a while loop.

🛠️ Scripts Created : 

08_user_int.sh -	User Interaction / Input
09_arithmetic_ops.sh -	Mathematical Operations
10_if_else.sh -	Basic Decision Making
11_elif_demo.sh -	Multi-condition Logic
12_case_demo.sh -	Menu-driven Programming
13_logical_ops.sh -	AND/OR conditions
14_ternary_ops.sh -	Short-hand If-Else
15_forloop1.sh -	Basic Iteration
16_for_with_file.sh -	Reading files using For loop
17_while_demo.sh -	Conditional Looping
18_until_loop.sh -	Reverse condition loops
19_infinite_loop.sh -	Understanding process control
21_while_with_file.sh -	Line-by-line Text processing
22_while_with_csv.sh - Automating Data/CSV parsing

- 📸 Lab Proof (Screenshot):
  <img width="822" height="222" alt="Screenshot 2026-03-12 160855" src="https://github.com/user-attachments/assets/33d87e09-7f82-4ac5-897d-f73ffa954ae1" />
