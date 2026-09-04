# Challenge: Enhance!
**Category:** Forensics | **Difficulty:** Medium | **Author:** LT 'syreal' Jones

## Challenge Description
*"Download this image file and find the flag."*

This challenge plays on the classic "CSI enhance" trope by providing a Scalable Vector Graphics (SVG) image where the flag characters are hidden within the underlying XML code structure.

___

## Analysis
Unlike raster images (such as PNG or JPEG), which store pixel color data, **SVG** files are text-based XML documents, so I might have to inspect the source code to find the flag.

___

## Solution

### Step 1: Downloading the Challenge File
Download the SVG image file into your working directory:
```bash
wget [https://artifacts.picoctf.net/c/.../drawing.flag.svg](https://artifacts.picoctf.net/c/.../drawing.flag.svg)
```

### Step 2: Inspecting and Analysing the file code:
Inspect the contents of the file using cat or strings:
```Bash
cat drawing.flag.svg
```
<div align='center'><img width="704" height="698" alt="image" src="https://github.com/user-attachments/assets/ade9b6f4-4c67-41aa-9c3a-8f6e92e22118" /><p><i>We can realise that the '<tspan>' tags undermine the flag</i></p></div>

### Step 3: Grepping the targeted tags and reconstructing the Flag
<div align='center'><img width="528" height="194" alt="image" src="https://github.com/user-attachments/assets/5271b3a4-cb11-4410-8f8c-6e9f31317a38" /><p><i>Concatenating the extracted character sequences and removing the spaces between them produces the complete flag.</i></p></div>

___
## Final Flag
picoCTF{3nh4nc3d_24374675}

___
## Key Takeaways
- SVG File: SVG files are XML text documents rather than binary pixel images, making them susceptible to direct text inspection.

- Source Code Forensics: Always check the underlying markup/source code of vector images or web assets before attempting complex image processing.

- Command-Line Text Processing: Using tools like grep to parse structured markup files speeds up forensic extraction.
