# Challenge: Obedient Cat
**Category:** General Skills | **Difficulty:** Easy | **Author:** syreal
___

## Challenge Description
*"This file has a flag in plain sight (aka 'in-the-clear')."*

This is a fundamental "Sanity Check" challenge. Its purpose is to verify that a participant can correctly download a resource and read its contents, which are stored in "plaintext" (unencrypted and unencoded).

___

## Analysis
In Cybersecurity, **"In-the-clear"** or **"Plaintext"** refers to data that is transmitted or stored without any encryption or obfuscation.
___

## Solution

### Step 1: File Inspection
After downloading the given file, I opened it through Notepad. As the description said, there is no further decoding or decryption process.

<img width="255" height="101" alt="the plaintext flag" src="https://github.com/user-attachments/assets/b9c814e1-c6ab-45ae-9515-de4472f9824d" />
<p>Opening the file to reveal the flag in plaintext.</p>

### Step 2: Alternative CLI Method
In a Linux environment, the same result can be achieved instantly using the `cat` command, which directly outputs the file's contents to the terminal:

- cat flag
___

## Final Flag
- picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}

___
## Key Takeaways
- Terminology: Understanding "In-the-clear" as data without protection.

- Basic Tooling: Using wget to download remote files and cat (Linux) or text editors to inspect file contents.

- Sanity Checks: Even the simplest tasks are part of a structured methodology in security analysis.
