# Challenge: Tab, Tab, Attack
**Category:** General Skills | **Difficulty:** Easy | **Author:** syreal

## Challenge Description
*"Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames."*

This challenge demonstrates the efficiency of Command-Line Interface (CLI) autocompletion using the `Tab` key, particularly when navigating deeply nested directory structures and executing files with complex names.

___

## Analysis
In terminal environments:
- **Tab Completion:** Pressing `Tab` automatically completes unique directory and file paths. When directories are sequentially nested with single path options, hitting `Tab` rapidly allows instant traversal through complex directory trees without manual typing.
- **Deep Directory Trees:** Archives like `.zip` files can obscure binary payloads inside deeply nested subdirectories.
- **Binary Execution / Inspection:** Executing compiled ELF binaries (or inspecting them via `cat`/`strings`) reveals dynamic outputs or embedded hardcoded string buffers containing secrets like flags.

___

## Solution

### Step 1: Extracting the Archive
After downloading the file, extract the contents of `Addadshashanammu.zip` using the `unzip` utility:
```bash
unzip Addadshashanammu.zip
```
### Step 2: Path Traversal via Tab Completion
Instead of manually typing each folder name, leverage terminal autocompletion by typing './Addad' or 'cat Addad' and pressing Tab repeatedly to auto-fill the nested path, then press enter to reveal the flag:

```Bash
./Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
```
<div align="center"><img width="1157" height="64" alt="image" src="https://github.com/user-attachments/assets/f35262a6-6752-4ca1-b824-91b74b3cccc6" />
<p><i>The flag appears!</i></p></div>

___
## Final Flag
picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

___
## Key Takeaways
- CLI Efficiency: Utilizing Tab autocompletion to accelerate directory traversal and reduce syntax errors.

- Archive Handling: Using unzip to inspect and extract compressed directory trees.

- Executable Inspection: Recognizing that flags can be retrieved either by direct binary execution or static string extraction (strings/cat).

