# Challenge: MOD 26
**Category:** Cryptography | **Difficulty:** Easy | **Author:** Pandu

## Challenge Description
*"Cryptography can be easy, do you know what ROT13 is?"*

This challenge introduces ROT13 (Rotate by 13 places), a simple substitution cipher that replaces a letter with the 13th letter after it in the alphabet.

---

## Analysis
**ROT13** is a special case of the classic **Caesar Cipher**. Since the English alphabet contains 26 letters:
- Shifting a character forward by 13 positions twice ($13 \times 2 = 26$) returns the original character.
- Therefore, ROT13 is **symmetric**—the exact same operation is used for both encryption and decryption.
- Only alphabetic characters (A-Z, a-z) are rotated; numbers, underscores, and special characters remain unchanged.

___

## Solution

### Step 1: File Inspection
Downloading a given file named `values.txt`. Opening the file reveals the encrypted string (ciphertext):
```text
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_45559noq}
```
### Step 2: Decryption via CyberChef
Open CyberChef.

Input the ciphertext string into the Input panel.

Add the ROT13 recipe to the pipeline (ensuring both uppercase and lowercase rotations are enabled).
<img width="760" height="396" alt="image" src="https://github.com/user-attachments/assets/a45c1b18-2e41-4301-9082-abe7b988ccd4" />
<p><i>the plaintext flag revealed!</i></p>

### Alternative CLI Method
In a Linux terminal, the same decryption can be achieved using the tr (translate) command:

```bash
cat values.txt | tr 'A-Za-Za-z' 'N-ZA-Mn-za-m'
```
___
## Final Flag
picoCTF{next_time_I'll_try_2_rounds_of_rot13_45559abd}
___
## Key Takeaways
Caesar Cipher / ROT13: Understanding basic monoalphabetic substitution ciphers.

Symmetric Decryption: Recognizing that ROT13 is its own inverse cipher.

Tooling Efficiency: Utilizing CyberChef or Linux tr for rapid cryptographic decoding during reconnaissance.
