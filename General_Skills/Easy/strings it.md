# Challenge: strings it
**Category:** General Skills | **Difficulty:** Easy | **Author:** Sanjay C/Danny Tunitis

## Challenge Description
*"Can you find the flag in file without running it?"*

This challenge introduces fundamental static analysis, focusing on using the `strings` command to extract human-readable text embedded inside binary files without executing them.

___

## Analysis
When binaries or compiled executables are generated, hardcoded text—such as status messages, variable values, or keys—is stored directly within the file's data sections in plain text.

- **Static Analysis:** Inspecting file contents without running the program, allowing safe analysis of unknown or untrusted binaries.
- **`strings` Utility:** Scans binary files for sequences of printable characters and prints them.
- **Pattern Matching (`grep`):** Pipelining `strings` output into `grep` allows filtering specifically for target patterns such as `picoCTF{`.

___

## Solution

### Step 1: Downloading the given file with "wget"
Download the target file to my terminal.

### Step 2: Extracting Strings with Piping
Run the `strings` utility against the downloaded file and pipe (`|`) the result to `grep` to filter the targeted text:

```bash
strings file | grep picoCTF
```

<div align="center"><img width="535" height="46" alt="image" src="https://github.com/user-attachments/assets/412cb7b0-9c3b-46c1-bc66-cc1177a8ea0a" /></div>

___
## Final Flag
picoCTF{5tRINg5_1T_d6306c19}
___
## Key Takeaways
- Static Binary Inspection: Utilizing strings as an efficient initial step during reverse engineering or binary triage to uncover hardcoded credentials or parameters.

- Pipeline Efficiency: Combining strings with grep to quickly parse massive streams of text output down to specific search strings.

- Non-Execution Security: Extracting sensitive artifacts from compiled files without running potentially dangerous code.
