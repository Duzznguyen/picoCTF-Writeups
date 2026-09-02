# Challenge: PW Crack 2
**Category:** General Skills | **Difficulty:** Easy | **Author:** LT 'syreal' Jones

## Challenge Description
*"Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag in the same directory too."*

This challenge demonstrates how to reverse obfuscated password strings represented in hexadecimal ASCII values within Python scripts.

___

## Analysis
Unlike **PW Crack 1** where the password was hardcoded in plain text, this challenge obscures the required key using dynamic function calls:

- **Source Inspection:** Analyzing `level2.py` reveals the conditional authentication check:
  ```python
  if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
  ```
We can see that the password we need to fill in is "0x33 0x39 0x63 0x65", which can be resolved using CyberChef this password.

## Solution:
### Step 1: Downloading the given files by the "wget" command
```
wget https://artifacts.picoctf.net/c/15/level2.py
wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
```
### Step 2: Extracting the Obfuscated Key
We can extract "0x33 0x39 0x63 0x65" through CyberChief by "From Hex" recipe:
<div align='center'><img width="1449" height="658" alt="image" src="https://github.com/user-attachments/assets/d46c92e6-1e81-4dd4-b931-f844eb946dc8" /><p><i>The password revealed!</i></p>
</div>

### Step 3: Executing the Password Checker
Run 'level2.py' in the terminal and fill the password to find the flag:
<div align='center'><img width="401" height="75" alt="image" src="https://github.com/user-attachments/assets/1012e4d7-4c0d-435b-b430-1c01fdfd7077" /></div>

___
## Final Flag
picoCTF{tr45h_51ng1ng_502ec42e}

___
## Key Takeaways
- ASCII & Hex Representation: Understanding how integer hex representations translate into ASCII character sequences (chr()).

- Tools combination: Learn how to combine tools like CyberChief in cybersecurity.
