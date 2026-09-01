# Challenge: Wave a flag
**Category:** General Skills | **Difficulty:** Easy | **Author:** syreal

## Challenge Description
*"Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information..."*

This challenge focuses on Linux file permissions (specifically the executable bit) and interacting with compiled binaries using standard command-line flags/arguments (such as `-h` for help).

___

## Analysis
In Linux environments:
- Files downloaded from external sources often lack execution permissions by default for security reasons. Attempting to execute them triggers a `Permission denied` error.
- Standard Command-Line Interface (CLI) utilities and custom binaries frequently accept parameters or options (often called "flags" in software engineering, e.g., `-h` or `--help`) to output documentation or trigger specific functions.

___

## Solution
### Step 1: Using 'wget' to download the given file named 'warm'
<div align="center"><img width="1415" height="255" alt="image" src="https://github.com/user-attachments/assets/7d77189c-cbc6-4f8d-bdf8-cf374899362b" />
<p><i>using 'wget' command to download file</i></p></div>

### Step 2: Using 'chmod +x' command to resolve 'permission denied'
Attempting to run the downloaded binary `warm` initially fails due to missing execution privileges:
```bash
chmod +x warm
```

### Step 3: Running the file with the -h/--help flag
<div align="center"><img width="936" height="44" alt="image" src="https://github.com/user-attachments/assets/624e0dc1-13eb-4d16-8ded-b3ce52b5511e" />
<p><i>The flag revealed!</p></div>

___
## Final Flag
picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}

___
## Key Takeaways
- Linux File Permissions: Understanding read/write/execute permission flags and modifying them using chmod +x.

- CLI Interactivity: Passing runtime arguments/flags (-h, --help) to binaries to inspect utility capabilities.

- Error Diagnosis: Recognizing Permission denied errors as file permission restrictions.

