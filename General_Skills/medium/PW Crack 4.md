# Challenge: PW Crack 4
**Category:** General Skills | **Difficulty:** Medium | **Author:** LT 'syreal' Jones

## Challenge Description
*"Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag and the hash in the same directory too. There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script."*

This challenge demonstrates how to scale dictionary attacks by using programmatic automation (`for` loops) in Python to evaluate a list of 100 candidate passwords against a given MD5 hash.

---

## Analysis
This is the advanced task of **PW Crack 3**. This challenge expands the candidate list to 100 possible passwords stored inside `pos_pw_list`:

- Testing 100 candidates manually via interactive shell prompts (`input()`) is inefficient and error-prone, so we might have to create an automatic loop to test each password independently based on the given loop.

---

## Solution

### Step 1: Downloading Challenge Files
Download `level4.py`, `level4.flag.txt.enc`, and `level4.hash.bin` into my terminal by the "wget" command:

```bash
wget https://artifacts.picoctf.net/c/21/level4.py
wget https://artifacts.picoctf.net/c/21/level4.flag.txt.enc
wget https://artifacts.picoctf.net/c/21/level4.hash.bin
```
### Step 2: Edit the 'level4.py' file using the 'nano' command:
<div align='center'><img width="458" height="107" alt="image" src="https://github.com/user-attachments/assets/852a5a55-427b-4047-b80a-c0e323991699" /><p><i>Using Ctrl + O to edit the file and Ctrl + X to exit</i></p></div>
I simply create a 'pw' variable and use it to establish a loop in pos_pw_list, which contains the list of 100 passwords. If hash-password is correct, it will print the flag and finally stop the loop.

### Step 3: Execute the Python file:
<div align='center'><img width="378" height="101" alt="image" src="https://github.com/user-attachments/assets/10a61984-bcc4-4e7c-9503-f8494ba6e547" /><p><i>The correct password in this case is 9f63</i></p></div>

___
## Final Flag
picoCTF{fl45h_5pr1ng1ng_d770d48c}

___
### Key Takeaways
- Script Automation: Automating hash comparisons is necessary when the database is huge.

- Code Refactoring: Using the given code to analyse and build structure rather than rebuilding from scratch.

