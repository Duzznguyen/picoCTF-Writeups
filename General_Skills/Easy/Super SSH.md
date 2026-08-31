# Challenge: Super SSH
**Category:** General Skills | **Difficulty:** Easy | **Author:** Jeffery John

## Challenge Description
*"Using a Secure Shell (SSH) is going to be pretty important. Can you SSH as ctf-player to titan.picoctf.net at port 58032 to get the flag?"*

This challenge introduces Secure Shell (SSH), a fundamental protocol used in administration and security for remote command-line access over an encrypted network connection.

___

## Analysis
**SSH (Secure Shell)** operates by default on TCP port 22, but services often run on custom ports for security or environment isolation. To connect via SSH, a client needs:
1. Destination username and hostname (`ctf-player@titan.picoctf.net`).
2. Specific target port (using the `-p` parameter, in this case `58032`).
3. Password authentication (`84b12bae`).

Upon initial connection, the client must accept and store the server's public host key fingerprint into `known_hosts` to establish trust.

___

## Solution

### Step 1: Connecting via SSH
Open a terminal/command prompt and execute the SSH connection command specifying the remote port:

```bash
ssh ctf-player@titan.picoctf.net -p 58032
```
###Step 2: Host Verification & Authentication
When prompted to confirm host authenticity, type yes to accept the server's ED25519 key fingerprint.

Enter the provided password: 84b12bae (Note: Password input is hidden in terminal environments).

Upon authentication, the server outputs the banner containing the flag and terminates the connection.
<img width="462" height="224" alt="image" src="https://github.com/user-attachments/assets/367fcdcb-364f-4f39-adfd-816d581a40f0" />
<p><i>the flag after completing all of these steps</i></p>
___

## Final Flag
picoCTF{s3cur3_c0nn3ct10n_07a987ac}
___

## Key Takeaways
SSH Syntax: Understanding ssh username@hostname -p port syntax for custom port connections.

Host Verification: Understanding how SSH uses public key fingerprints and known_hosts to prevent Man-In-The-Middle (MITM) attacks.

Remote Access: Exercising remote command-line authentication skills essential for penetration testing and administration.
