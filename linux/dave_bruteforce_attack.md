Project: Password Compromise Simulation (Dave)
Disclaimer
For Educational Purposes Only.
The information and steps provided in this repository are for educational and authorized penetration testing demonstration purposes only. Unauthorized access to computer systems is illegal. The author is not responsible for any misuse of this information.

Overview
This project demonstrates how a target user ("Dave") can have their credentials compromised via a dictionary attack using THC-Hydra. The goal is to highlight the dangers of weak passwords and the importance of implementing account lockout policies and multi-factor authentication (MFA).

Scenario
Target User: Dave - always makes simple passwords
Target Service: SSH (running on port 22)
Attack Vector: Brute-force/Dictionary Attack
Environment: Isolated lab network (e.g., Kali Linux and a vulnerable VM)

🛠️ Tools Used
THC-Hydra: A fast network login cracker.
Either you can use the rock you list or make your own list
Nmap: Used for initial service discovery to confirm the target is reachable.  

This is an extremely easy box. 
