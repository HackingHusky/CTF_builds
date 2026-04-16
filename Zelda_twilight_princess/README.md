# Twilight Corruption of Hyrule — CTF Lab
A multi-machine penetration testing lab inspired by The Legend of Zelda: Twilight Princess, designed to simulate real-world OSCP / PNPT attack paths.
Story
Hyrule has fallen into darkness.
You take the role of Link, guided by Midna, to uncover the corruption spreading across the kingdom.
From the cursed forests to the shadowed castle, and finally into the Twilight Realm, you must reclaim the Triforce by exploiting systems, pivoting networks, and defeating the forces of Zant and Ganondorf.

 
## Objectives
Perform network-based reconnaissance
Exploit Linux services for initial access
Pivot using credential discovery
Gain access to a Windows system via RDP
Dump credentials and perform Pass-the-Hash attacks
Compromise an Active Directory domain


## Lab Architecture


Kali (Attacker)
   
   |
   |--- [Faron Woods - Linux]        
   |
   |--- [Hyrule Castle - Windows]    
   |
   |--- [Twilight Realm - AD/DC]     
​

## Machines Overview:


Faron Woods (Linux)
Focus: Network Enumeration & Initial Access
FTP (Anonymous access)
SMB (Credential leak)
SSH (User login)
Custom service (port 9001)
Privilege escalation via sudo misconfiguration

​
Hyrule Castle (Windows)
Focus: Lateral Movement & Credential Discovery
RDP access via discovered credentials
Stored credentials (pivot to AD)
Weak service permissions (optional privesc)

​
Twilight Realm (Active Directory)
Focus: Domain Compromise
Credential dumping (Mimikatz / secretsdump)
Pass-the-Hash authentication
Lateral movement to Domain Controller
Domain Admin takeover

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
Assign static IPs:
Linux: 10.10.10.10
Windows: 10.10.10.20
DC: 10.10.10.30

### 3. Access
Kali Linux as attacker machine
Ensure required ports are open:
21, 22, 139, 445, 3389, 5985, 88
🔐 Credentials (For Lab Setup Only)
Linux:
link : hyrule123

Windows / AD:
midna : Twilight#Realm1
zelda : Princess123!
ganon : TriforceGod!
​


## Skills Practiced
Network enumeration
Credential harvesting
Linux privilege escalation
Windows privilege escalation
Lateral movement
Active Directory attacks
Pass-the-Hash

## Disclaimer
This lab is intended for educational purposes only.
Do not use these techniques on systems you do not own or have explicit permission to test.

 
## Final Words
"The light returns not because darkness fades…
but because someone fights it."
Good luck, hero.
