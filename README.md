# Website Cloning & SMB Vulnerability Scanning Labs

## Overview
This repository documents two cybersecurity labs conducted during weekend practical sessions:

1. Website Cloning using SEToolkit
2. SMB Vulnerability Scanning using Enum4Linux

All activities were performed in a controlled lab environment for educational and testing purposes only.

## Ethical Disclaimer
All demonstrations were conducted on authorized lab machines.
Unauthorized cloning, scanning, or exploitation of real-world systems is illegal and unethical.

# LAB 1 — Website Cloning (SEToolkit)
## Objective
To demonstrate how attackers clone websites to harvest credentials and how this technique is studied for defensive awareness and penetration testing training.
## Tools Used
1. Kali Linux
2. SEToolkit
3. BeEF (Browser Exploitation Framework)
## Commands Used
sudo su
setoolkit
## SEToolkit Menu Navigation
1) Social-Engineering Attacks
2) Website Attack Vectors
3) Credential Harvester Attack Method
2) Site Cloner
## Target IP used:
10.6.6.1 - An HTML file was created containing the intended URL to be cloned.
## How the Website Cloning Works
SEToolkit copies the structure of a legitimate website and hosts it locally. When users interact with the cloned site, entered credentials are captured by the credential harvester. This lab demonstrates how phishing attacks are created so defenders can recognize and prevent them.
## Social Exploitation (BeEF)
sudo beef-xss
BeEF was used to demonstrate browser-based exploitation techniques after the victim interacts with the cloned site.
## Screenshots 
SEToolkit menu selection
- Cloned website loaded in browser
- Credential harvester output
- BeEF control panel

<br/>
# LAB 2 — SMB Vulnerability Scanning (Enum4Linux)



 
# website-cloning-and-smb-enumeration-labs
Cybersecurity lab documentation covering website cloning with SEToolkit and SMB vulnerability scanning using Enum4Linux in a controlled environment.

# Ethical Disclaimer
All activities documented in this repository were performed strictly in a controlled lab environment using intentionally vulnerable machines for educational purposes only.

No real world systems were targeted. Unauthorized scanning or cloning of live systems is illegal and unethical.
