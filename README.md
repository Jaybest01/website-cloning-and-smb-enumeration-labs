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
- sudo su
- setoolkit
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
- sudo beef-xss
BeEF was used to demonstrate browser-based exploitation techniques after the victim interacts with the cloned site.
## Screenshots 
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
- SEToolkit menu selection
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
- Cloned website loaded in browser
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
- Credential harvester output
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
- BeEF control panel
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">

<div class="multi-image"></div>
.multi-image {
  width: 300px;      /* width of the container */
  height: 200px;     /* height of the container */
  background-image: 
    url('https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/sudo%20su.png'),
    url('image2.png'),
    url('image3.jpg');  /* multiple images separated by commas */
  background-position: 
    top left, 
    center, 
    bottom right;       /* position for each image */
  background-repeat: no-repeat;
  background-size: 
    100px 100px,        /* size for image1 */
    80px 80px,          /* size for image2 */
    120px 120px;        /* size for image3 */
}

<br/>

# LAB 2 — SMB Vulnerability Scanning (Enum4Linux)
- smb-enum4linux-lab/
## Objective
To identify SMB misconfigurations such as:
 * User enumeration
 * Anonymous access
 * Exposed shares
## Tools Used
* Enum4Linux
* Nmap
* smbclient
* Kali Linux
## Commands Used: - Help & Discovery
- enum4linux -help
- nmap -sN 172.17.0.0/24
## SMB Enumeration Commands
- enum4linux -U 172.17.0.2   -----------  # Enumerate users
- enum4linux -S 172.17.0.2   -----------  # Enumerate shares
- enum4linux -Sv 172.17.0.2  -----------  # Verbose share enumeration
- enum4linux -P 172.17.0.2   -----------  # Password policy
- enum4linux -a 172.17.0.2   -----------  # Aggressive scan (all checks)

## Findings
The target system exposed SMB services that allowed:
- Enumeration of users
- Discovery of shared directories
- Identification of weak SMB configurations
These findings demonstrate how attackers gather intelligence before launching further attacks.

## SMB Client Interaction
- smbclient --help
- smbclient -L //172.17.0.2/
- smbclient //172.17.0.2/print$
- smbclient //172.17.0.2/tmp
## SMB Client Commands Used
- help
- dir
- put avirus.exe .conf-admin
This demonstrates file interaction within SMB shares, highlighting the risk of writable shares in insecure environments.

## Screenshots to Include
* Enum4Linux output
* Nmap scan results
* SMB share listing
* smbclient directory access

# Key Takeaways
- Website cloning is commonly used in phishing attacks
- SMB misconfigurations allow attackers to enumerate sensitive information
- Proper security controls can prevent these attack vectors

<br/>

# Conclusion
These labs provided hands-on experience with common penetration testing techniques used to identify and mitigate real-world security risks.
