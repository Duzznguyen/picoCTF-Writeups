# Challenge: PW Crack 1
**Category:** General Skills | **Difficulty:** Easy | **Author:** LT 'syreal' Jones

## Challenge Description
*"Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag in the same directory too."*

This challenge introduces static code analysis of Python scripts, demonstrating how hardcoded credentials embedded directly in source code lead to trivial authentication bypasses.

---

## Analysis
When an application performs authentication checks locally without using secure hashing or remote verification services:
- **Static Analysis:** Inspecting the underlying script (`level1.py`) directly exposes the exact execution logic and conditional checks.
- **Hardcoded Credentials:** Storing plain text passwords directly in code allows anyone with read access to discover the key without executing brute-force attacks or complex reverse-engineering.

---

## Solution

### Step 1: Downloading Challenge Files
Download both the password checking script (`level1.py`) and the encrypted payload (`level1.flag.txt.enc`) into my terminal using `wget`:

```bash
wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
wget https://artifacts.picoctf.net/c/11/level1.py
```
Step 2: Inspecting the Script Source Code
View the content of level1.py using cat or nano command to locate the password verification logic; And you can see the correct password to reveal the flag is '1e1a':
<div align='center'><img width="632" height="266" alt="image" src="https://github.com/user-attachments/assets/63f2ab07-99aa-4b2b-982b-b500862fe415" /></div>

Step 3: Executing the Script & Decrypting the Flag
Run the Python script and supply the extracted password '1e1a' at the prompt:

```Bash
python3 level1.py
```
 <div align='center'><img width="469" height="97" alt="image" src="https://github.com/user-attachments/assets/d900a4a8-5455-464d-892e-3a3bf3305494" /></div>

___
## Final Flag
picoCTF{545h_r1ng1ng_fa343060}

___
## Key Takeaways
- Hardcoded Credentials: Storing secrets, passwords, or API keys directly in source code creates severe security flaws.

- Static Analysis First: Reviewing script or binary contents often reveals authentication mechanisms faster than active fuzzing or brute-forcing.
