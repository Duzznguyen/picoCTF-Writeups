# Challenge: First Grep
**Category:** General Skills | **Difficulty:** Easy | **Author:** Alex Fulton/Danny Tunitis

## Challenge Description
*"Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way."*

This challenge introduces `grep` (Global Regular Expression Print), one of the most essential command-line tools for searching through text files for specific patterns.

---

## Analysis
This challenge is similar to the 'strings it' challenge.
When analyzing log files, source code, or large text dumps during a CTF or security assessment, manually inspecting thousands of lines of text is impractical. We can use the 'grep' command to filter text in the file; we have to find 'picoCTF' in this case.

---

## Solution

### Step 1: Downloading the Target File
Download the file to your working directory using `wget` or via browser download:

```bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/9e4f9113960f157ceb824bdb449dc2a74504b484346c1442e64854408d5a90c5/file
```
Step 2: Searching with grep
Run grep targeting the flag prefix picoCTF against the downloaded file:

```bash
grep "picoCTF" file
```
<div align="center"><img width="624" height="54" alt="image" src="https://github.com/user-attachments/assets/22bfc13f-8b5c-4b45-8de1-4b3d03b6d207" /></div>

___
## Final Flag
picoCTF{grep_is_good_to_find_things_9C6Ef2F7}

___
## Key Takeaways
- Text Processing Efficiency: Utilizing grep to quickly extract specific patterns from massive unstructured text.

- Linux Productivity: Combining terminal search utilities to streamline static file analysis.
