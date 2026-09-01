# Challenge: where are the robots
**Category:** Web Exploitation | **Difficulty:** Easy | **Author:** zaratec/Danny

## Challenge Description
*"Can you find the robots?"*

This challenge introduces web reconnaissance focusing on `robots.txt`, a standard configuration file used by web servers to communicate with web crawlers and web spiders.

---

## Analysis
The **Robots Exclusion Protocol** relies on a plain text file named `robots.txt` hosted at the root directory of a web server (e.g., `http://example.com/robots.txt`).

- **Purpose:** Instructs web crawlers which pages or paths should or should not be indexed.
- **Security Implications:** While designed for search engine indexing, `robots.txt` is publicly accessible to any user. Security assessors and attackers frequently inspect this file during reconnaissance to discover hidden, unlinked, or sensitive administrative endpoints listed under `Disallow:` directives.

---

## Solution

### Step 1: Inspecting `robots.txt`
Append `/robots.txt` to the target URL in your browser address bar or query it directly using `curl`:

```bash
curl -s [http://fickle-tempest.picoctf.net:60592/robots.txt](http://fickle-tempest.picoctf.net:60592/robots.txt)
```
<div align='center'><img width="341" height="71" alt="image" src="https://github.com/user-attachments/assets/f0e37c08-7e90-425b-981c-9a15e81e8320" /><p><i>a website's text appears</i></p></div>

### Step 2: Accessing the Disallowed Endpoint
Navigate to the restricted HTML page discovered in the Disallow entry (/cc6b1.html) and then the flag will reveal:
<div align="center"><img width="638" height="103" alt="image" src="https://github.com/user-attachments/assets/21f9be7f-d767-4a7b-aded-0a929cdb337d" /></div>

___

## Final Flag
picoCTF{1f_u_f0110w_th3_r0b0t5_1d82b74f}

___
## Key Takeaways
- Security Through Obscurity: Disallowing sensitive paths via robots.txt does not restrict access because the file is publicly viewable; it often acts as an unintended map of sensitive locations.

- Web Reconnaissance: Always audit common metadata paths (/robots.txt, /sitemap.xml, /.well-known/) during initial web security assessments.
