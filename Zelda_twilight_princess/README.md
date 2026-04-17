# Twilight Princess CTF (Ubuntu Lab)

<img width="1024" height="1024" alt="Husky hacker Twilight Princess CTF" src="https://github.com/user-attachments/assets/96544f60-b4b2-462e-961f-4f3157648ec3" />
_"Light and shadow are two sides of the same coin..." — Midna_


A Zelda-themed Capture The Flag (CTF) challenge I made myself. It's a fun, easy box for starters, and when I got into cybersecurity, I combined my favorite video game with CTF.

 
## Objectives
You awaken in the Twilight Realm, stripped of power and memory.
To escape, you must uncover secrets, exploit weaknesses, and reclaim control.




​
## Attack Path
1. Nmap scan → enumerate services
2. FTP/SMB → discover credentials
3. SSH → access Linux system
4. Enumerate → find Midna credentials
5. RDP → access Windows machine
6. Dump hashes → obtain NTLM hashes
7. Pass-the-Hash → authenticate to Domain Controller
8. Gain Domain Admin → capture final flag
​

## Setup Instructions


### 1. Virtualization
Use VMware
Configure all machines on the same internal network

### 2. Networking
You can keep the default IP address once configured. 

### 3. Access
Kali Linux as an attacker machine
Ensure required ports are open:
22 and 80

​

## Disclaimer
This lab is intended for educational purposes only.
Do not use these techniques on systems you do not own or have explicit permission to test.

 
## Final Words
"The light returns not because darkness fades…
but because someone fights it."
Good luck, hero.
