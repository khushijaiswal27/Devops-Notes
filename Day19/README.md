### Day 19: Arrays, String Manipulation & Path Utilities 

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
