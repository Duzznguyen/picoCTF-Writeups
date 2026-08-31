# Challenge: Warmed Up
**Category:** General Skills | **Difficulty:** Easy | **Author:** Sanjay C / Danny Tunitis
___
## Challenge Description
*"What is 0x3D (base 16) in decimal (base 10)?"*

This is a foundational challenge designed to test basic understanding of number systems, specifically converting numbers from Hexadecimal (base 16) to Decimal (base 10).

___

## Analysis
In computer science:
- **Hexadecimal (Base 16)** uses digits `0-9` and letters `A-F` (where A=10, B=11, C=12, D=13, E=14, F=15).
- **Decimal (Base 10)** is the standard positional numeral system using digits `0-9`. The `0x` prefix denotes hexadecimal notation.

To convert `0x3D` manually:
- Position 1 (rightmost): $\text{D} = 13 \times 16^0 = 13$
- Position 2 (leftmost): $3 = 3 \times 16^1 = 48$
- Sum: $48 + 13 = 61$

___

## Solution

### Step 1: Conversion via CyberChef
1. Open [CyberChef](https://gchq.github.io/CyberChef/).
2. Input `0x3D` into the **Input** panel.
3. Add the **From Hex** recipe followed by **To Decimal** (or use **To Base** recipe).

<div align="center">
  <img width="1528" height="783" alt="image" src="https://github.com/user-attachments/assets/26592aea-b594-4d9d-8592-e42220e9bb3d" />
  <p><i>Converting 0x3D from Hexadecimal to Decimal using CyberChef.</i></p>
</div>

## Final Flag
picoCTF{61}
___
## Key Takeaways
- Number Systems: Understanding Hexadecimal positional notation (0x prefix) and character values (A–F).
- Flag Formatting: Wrapping calculated outputs into the required picoCTF{...} flag wrapper.
