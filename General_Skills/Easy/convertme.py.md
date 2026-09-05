# Challenge: convertme.py
**Category:** General Skills | **Difficulty:** Easy | **Author:** LT 'syreal' Jones

## Challenge Description
*"Run the Python script and convert the given number from decimal to binary to get the flag."*

This challenge tests basic numeral system conversion (Decimal to Binary) and running interactive Python scripts via CLI.
___

## Analysis
The challenge provides a Python script that generates a random decimal number between 10 and 100 on each execution. To retrieve the flag, the script requires user input containing the exact binary representation of that decimal number.

In the execution shown:
- **Target Decimal:** $97_{10}$
- **Binary Conversion:**
  - $97 = 64 + 32 + 1 = 2^6 + 2^5 + 2^0$
  - Converting to binary bits: $1100001_2$ (or 8-bit padded: `01100001`)

___

## Solution

### Step 1: Download and Execute the Python script
Using `wget` to download the file and run it with `python3`:

```bash
wget https://artifacts.picoctf.net/c/22/convertme.py
python3 convertme.py
```
### Step 2: Decimal to Binary Calculation
The Python script shows a question: 'If 97 is in decimal base, what is it in binary base?'
You can solve this in two ways: calculate it manually (show at analyse section) or use CyberChief; I would prefer the latter because it saves me time.
<div align='center'><img width="431" height="279" alt="image" src="https://github.com/user-attachments/assets/bb721e24-c40d-4d59-9c55-46393821a00e" /><p><i>The answer is 01100001!</i></p></div>

### Step 3: Input the answer at the prompt to unlock the flag
<div align='center'><img width="555" height="78" alt="image" src="https://github.com/user-attachments/assets/468d6cd7-d57e-466c-aa4e-833a515adbda" /><p><i>The flag revealed!</i></p></div>

___
## Final Flag
picoCTF{4ll_y0ur_b4535_762f748e}

___
## Key Takeaways
- Base Conversions in Security: Understanding conversions between Decimal, Binary, Hexadecimal, and Base64 is essential for decoding network packets, memory dumps, and cryptosystems.

- Tool integrity: smoothly use external tools to speed up any task/work.
