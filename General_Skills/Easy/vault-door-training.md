# Challenge: vault-door-training
**Category:** Reverse Engineering | **Difficulty:** Easy | **Author:** Mark E. Haase

## Challenge Description
*"Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open... As a warmup, we have created a replica vault in our training facility."*

This challenge introduces basic Java static analysis and source code auditing, focusing on identifying hardcoded credentials embedded directly within application logic.

___

## Analysis
The challenge provides the Java source code file `VaultDoorTraining.java`. In this task, we might have to inspect the source code to find the flag.
## Solution
### Step 1: Downloading the Source Code
Download VaultDoorTraining.java into my workspace using 'wget':

```Bash
wget https://challenge-files.picoctf.net/c_fickle_tempest/53e3c48d19b2003fcf06190abee7ae722dff19f17c3b864191c8ec56a8c35559/VaultDoorTraining.java
```
### Step 2: Static Source Code Inspection
View the source file contents directly in the terminal using cat or any text editor:

```Bash
cat VaultDoorTraining.java
```
<div align='center'><img width="640" height="214" alt="image" src="https://github.com/user-attachments/assets/3ac05341-c3c4-4583-8c68-a2e18debd87c" /><p><i>'w4rm1ng_Up_w1tH_jAv4_000uMfhzBuS' can be the flag</i></p></div>


### Step 3: Flag Reconstruction
Combine the required prefix picoCTF{, the hardcoded secret string, and the closing brace }:

picoCTF{ + w4rm1ng_Up_w1tH_jAv4_000uMfhzBuS + } = picoCTF{w4rm1ng_Up_w1tH_jAv4_000uMfhzBuS}
___
## Final Flag
picoCTF{w4rm1ng_Up_w1tH_jAv4_000uMfhzBuS}
___
## Key Takeaways
- Hardcoded Credentials: Storing secret keys, passwords, or tokens directly in source code is a major security vulnerability. Anyone with read access to the codebase or decompiled binaries can extract them.

- Deducing ability: Use hints and knowledge to guess information.
