# Challenge: Python Wrangling
**Category:** General Skills | **Difficulty:** Medium | **Author:** syreal

## Challenge Description
*"Python scripts are invoked kind of like programs in the Terminal... Can you run ende.py using password.txt to get flag.txt.en?"*

---

## Analysis
Python scripts require an interpreter (`python` or `python3`) to run in a terminal environment. In this challenge, there are three provided files:
- **`ende.py`**: A Python script designed to handle file encryption (`-e`) and decryption (`-d`).
- **`password.txt`**: A text file containing the decryption key required by `ende.py`.
- **`flag.txt.en`**: The encrypted flag.

---

## Solution

### Step 1: Downloading Challenge Files
Retrieve `ende.py`, `password.txt`, and `flag.txt.en` into active shell session using `wget`:

```bash
wget https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/ende.py
wget https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/password.txt
wget https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/flag.txt.en
```
### Step 2: Inspecting the Password
View the key content stored inside password.txt by the 'cat' command and then copy it:

```Bash
cat password.txt
```

<div align='center'><img align="center" width="432" height="44" alt="image" src="https://github.com/user-attachments/assets/8840ca46-bbf7-415a-9a31-e570093fc170" /></div>

### Step 3: Executing the Decryption Script
Run the script using python3, and -d as the decryption flag along with the encrypted target file:

```Bash
python3 ende.py -d flag.txt.en
```
### Step 4: Flag Retrieval
When the script requires a password, paste the password from the 'password.txt' file. The script will output the decrypted flag directly to the terminal.

<div align='center'><img width="598" height="79" alt="image" src="https://github.com/user-attachments/assets/c8479f15-ea70-4b2c-bb2d-3917d1836f83" /></div>

## Final Flag
picoCTF{45_c4ll1ng_c0d3_3b02a281}

## Key Takeaways
- CLI Python Execution: Invoking scripts via the python3 script.py command structure.

- Command Line Flags: Understanding how scripts parse flags (such as -d for decryption) via --help/-h flag.
