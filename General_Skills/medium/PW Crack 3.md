# Challenge: PW Crack 3
**Category:** General Skills | **Difficulty:** Medium | **Author:** LT 'syreal' Jones

## Challenge Description
*"Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag and the hash in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script."*

This challenge introduces password hashing concepts and demonstrates how to conduct a targeted dictionary/wordlist attack against stored password hashes.

---

## Analysis
Unlike previous levels where passwords were stored directly as plain text or simple character representations, **PW Crack 3** uses cryptographic hashing:

- **Password Hashing:** `level3.py` computes the **MD5** hash digest of user input via `hashlib.md5()` and compares the resulting binary string against the hash stored in `level3.hash.bin`.
- **One-Way Functions:** Cryptographic hash functions are non-reversible. Verification relies on hashing input candidates and comparing hash outputs.
- **Candidate Wordlist:** Inspecting `level3.py` reveals a list of 7 potential password candidates:
  ```python
  pos_pw_list = ["8678", "f541", "91a1", "e162", "4061", "1e66", "7789"]
  ```
## Solution
### Step 1: Downloading Challenge Files
Download level3.py, level3.flag.txt.enc, and level3.hash.bin into your working directory using wget:

```Bash
wget https://artifacts.picoctf.net/c/17/level3.py
wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
wget https://artifacts.picoctf.net/c/17/level3.hash.bin
```
### Step 2: Inspecting Candidate Passwords
Open level3.py to examine the target hash checking logic and candidate array:

```Bash
cat level3.py
```
<div align='center'><img width="586" height="381" alt="image" src="https://github.com/user-attachments/assets/47181616-75ad-4385-9a52-9d3edc4d7215" /></div>

### Step 3: Identifying the Correct Password
Run the python file then test each candidate manually pos_pw_list and check which item matches correct_pw_hash:
```Bash
python3 level3.py
```
<div align='center'><img width="389" height="79" alt="image" src="https://github.com/user-attachments/assets/82f2cfa9-9455-484d-85a4-b3727469227f" /></div>
___

## Final Flag
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
___
## Key Takeaways
- Cryptographic Hashing: Understanding that MD5 is a one-way hash function compared using output digests.

- Dictionary/Wordlist Attacks: How authentication systems become vulnerable to brute-force or dictionary lookup when candidate lists or password entropy are limited.
