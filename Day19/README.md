### Day 19: Arrays, String Manipulation & Path Utilities 

## Task 23 :
Write cleaner, reusable scripts — learn functions, strict mode, and real-world patterns.

You will:
- Write and call **functions**
- Use **`set -euo pipefail`** for safer scripts
- Work with **return values** and **local variables**
- Build an intermediate script

---

## Expected Output
- A markdown file: `day-18-scripting.md`
- All scripts you write during the tasks

---

## Challenge Tasks

### Task 1: Basic Functions
1. Create `functions.sh` with:
   - A function `greet` that takes a name as argument and prints `Hello, <name>!`
   - A function `add` that takes two numbers and prints their sum
   - Call both functions from the script

---

### Task 2: Functions with Return Values
1. Create `disk_check.sh` with:
   - A function `check_disk` that checks disk usage of `/` using `df -h`
   - A function `check_memory` that checks free memory using `free -h`
   - A main section that calls both and prints the results

---

### Task 3: Strict Mode — `set -euo pipefail`
1. Create `strict_demo.sh` with `set -euo pipefail` at the top
2. Try using an **undefined variable** — what happens with `set -u`?
3. Try a command that **fails** — what happens with `set -e`?
4. Try a **piped command** where one part fails — what happens with `set -o pipefail`?

**Document:** What does each flag do?
- `set -e` →
- `set -u` →
- `set -o pipefail` →

---

### Task 4: Local Variables
1. Create `local_demo.sh` with:
   - A function that uses `local` keyword for variables
   - Show that `local` variables don't leak outside the function
   - Compare with a function that uses regular variables

---

### Task 5: Build a Script — System Info Reporter
Create `system_info.sh` that uses functions for everything:
1. A function to print **hostname and OS info**
2. A function to print **uptime**
3. A function to print **disk usage** (top 5 by size)
4. A function to print **memory usage**
5. A function to print **top 5 CPU-consuming processes**
6. A `main` function that calls all of the above with section headers
7. Use `set -euo pipefail` at the top

Output should look clean and readable.

---

## Hints
- Function syntax: `function_name() { ... }`
- Local vars: `local MY_VAR="value"`
- Strict mode: `set -euo pipefail` as first line after shebang
- Pass args to functions: `greet "Shubham"` → access as `$1` inside
- `$?` gives the exit code of last command

---

## Documentation

Create `day-18-scripting.md` with:
- Each script's code and output
- Explanation of `set -euo pipefail`
- What you learned (3 key points)

---


I have completed the segment from 2:29:50 to 3:19:57 of M Prashant's Shell Scripting Masterclass. This session focused on advanced data structures and essential system utilities.

### 1. Arrays & Associative Arrays (Maps)
- **Standard Array:** `myArray=( val1 val2 val3 )`
- **Accessing Elements:** `${myArray[0]}` | **Total Length:** `${#myArray[*]}`
- **Appending Data:** `myArray+=( newVal )`
- **Associative Arrays:** `declare -A myMap=( [key]=value )` — Great for storing descriptive data like `[name]=Khushi`.

### 2. String Manipulation ✂️
- **String Length:** `${#myVar}`
- **Case Transformation:** `${myVar^^}` (Upper Case), `${myVar,,}` (Lower Case)
- **Substring Replacement:** `${myVar/old/new}` (First occurrence) or `${myVar//old/new}` (All occurrences).
- **Slicing (Substrings):** `${myVar:start:length}` (e.g., extracting specific parts of a string).

### 3. Utility Commands & Path Handling 🛠️
- **basename:** Extracts just the filename from a full path.
- **dirname:** Extracts only the directory path, stripping the filename.
- **realpath:** Resolves the absolute path of any file or directory.
- **Existence Checks:** Using `[[ -f $file ]]` for files and `[[ -d $dir ]]` for directories to make scripts more robust.

### 4. Special Bash Variables
- **$RANDOM:** Generates a random integer (useful for simulation or unique naming).
- **$UID:** Stores the User ID of the current user (Root is always `0`).

   📸 Lab Proof (Screenshot):
<img width="959" height="530" alt="Screenshot 2026-03-13 215327" src="https://github.com/user-attachments/assets/b1d50c54-cc38-4c6c-a2d1-3627a513e50f" />
