# Challenge: Big Zip
**Category:** General Skills | **Difficulty:** Easy | **Author:** LT 'syreal' Jones

## Challenge Description
*"Unzip this archive and find the flag."*

This challenge focuses on navigating deeply nested directory structures containing thousands of files, demonstrating the necessity of recursive command-line searches over manual file inspection.

___

## Analysis
After unzipping `big-zip-files.zip`, a complex directory tree with numerous subfolders and individual `.txt` files is created:

- **Need for Automation:** Manually opening or searching through each file individually across dozens of subdirectories is practically impossible.
- **Recursive Pattern Matching (`grep -r` / `grep -R`):** The `grep` tool features recursive flags (`-r` or `-R`) that allow it to traverse all subdirectories under a specified target path, inspecting every file for a matching pattern (e.g., `picoCTF`).

___

## Solution

### Step 1: Downloading & Extracting the Archive
Download the zip archive with 'wget' and extract its contents in my terminal using `unzip`:

```bash
wget https://artifacts.picoctf.net/c/503/big-zip-files.zip
unzip big-zip-files.zip
```
### Step 2: Using the 'grep' function to find the flag:
<div align='center'><img width="635" height="79" alt="image" src="https://github.com/user-attachments/assets/b6123fe3-5b68-4049-ad59-0f3c51145765" /><p><i>Using the '-R' flag to filter all files and subdirectories in that unzipped file.</p></div>
<p align='center'><i>(You can use 'man grep' to find available flags of grep)</i></p>

___
## Final Flag
picoCTF{gr3p_15_m4g1c_ef8790dc}

___
## Key Takeaways
- Recursive Search (grep -R): Using -R or -r instructs grep to scan all files within subdirectories automatically.

- Efficient File Navigation: Combining archive extraction (unzip) with terminal text utilities provides an instant solution for needle-in-a-haystack search scenarios.
