# Challenge: PW Crack 5
**Category:** General Skills | **Difficulty:** Medium | **Author:** LT 'syreal' Jones

## Challenge Description
*"Can you crack the password to get the flag? Download the password checker here, and you'll need the encrypted flag and the hash in the same directory too. Here's a dictionary with all possible passwords based on the password conventions we've seen so far."*

This challenge completes the **PW Crack** series by introducing real-world dictionary attack workflows, requiring Python file I/O operations to read candidate passwords from an external wordlist file (`dictionary.txt`).

___

## Analysis
- In this task, we have been provided with 4 files, and the new one is 'dictionary.txt'. So in this task, I might have to input this file into the Python code and use the 'strip()' function to trim the whitespace from the password.

___

## Solution

### Step 1: Downloading Challenge Files
Download `level5.py`, `level5.flag.txt.enc`, `level5.hash.bin`, and `dictionary.txt` into my terminal:

```bash
wget https://artifacts.picoctf.net/c/32/level5.py
wget https://artifacts.picoctf.net/c/32/level5.flag.txt.enc
wget https://artifacts.picoctf.net/c/32/level5.hash.bin
wget https://artifacts.picoctf.net/c/32/dictionary.txt
```
### Step 2: Using the 'nano' command to analyse and edit the code:
<div align='center'><img width="522" height="206" alt="image" src="https://github.com/user-attachments/assets/b4487ba1-0dce-4d2b-a505-d3cfdb3df409" /><p><i>We can see that this code structure is similar to the 'PW Crack 4' challenge</i></p></div>

### Step 3: Create a password-tested loop based on the code structure:
<div align='center'><img width="517" height="144" alt="image" src="https://github.com/user-attachments/assets/ef52c82e-7243-43c5-b71c-bded3d2897ed" /></div>

- 'with open("dictionary.txt", "r") as post_pw:' opens the file with only 'read' permission.

- 'pw = line.strip()' trims the whitespace of each word.

- The conditional statement 'if' is used to find the correct password and the flag.


### Step 4: Execute the Python file:
<div align='center'><img width="349" height="79" alt="image" src="https://github.com/user-attachments/assets/6320a648-6fc2-4ef1-b622-f2b0ac365d0b" /><p><i>Type any word to run the loop</i></p></div>

___
## Final Flag
picoCTF{h45h_sl1ng1ng_40f26f81}

___
## Key Takeaways
- Python File Handling: Utilizing open() and with context managers to read external data files safely.

- String Sanitization: Using .strip() to clean raw input strings and hidden whitespace before hashing.

- Dictionary Attack Foundation: Understanding how password cracking tools (like John the Ripper or Hashcat) operate.
