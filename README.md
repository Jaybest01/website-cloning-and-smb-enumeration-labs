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
- SEToolkit Exploitation
<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/sudo%20su.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/setoolkit..png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/setoolkit.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/commit/9b3f765c03b0d4f16325d4f23a425f79bb13d6f3" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/3)%20credential%20Attack.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/3)%20credential%20Attack.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/2)%20site%20cloner.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/2)%20Website%20Attack.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/cloning%26listening.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/cloned.png" alt="Girl in a jacket" width="1000" height="1200">

- BeEF control panel
<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/beef-xss-%20credintial%20hervester.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/beef-xss-%20credintial%20hervester...png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/wed%20credintial%20attack.png" alt="Girl in a jacket" width="1000" height="1200">,<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Web-Exploit-Capture/website%20stolen%20credintial.png" alt="Girl in a jacket" width="1000" height="1200">

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
  <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-help.png" alt="Girl in a jacket" width="1000" height="1200">  <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/nmap%20-openportcheck.png" alt="Girl in a jacket" width="1000" height="1200">  <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-U.png" alt="Girl in a jacket" width="1000" height="1200">  <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-S.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-S%20result.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-Sv.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-Sv%20result.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-Sv%20result..png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-P.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-a.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/enum4linux%20-a%20result.png" alt="Girl in a jacket" width="1000" height="1200">

* SMB share listing smbclient directory access
<img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20-L.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20print%24_tmp.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20accessed.png" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20accessed%20(dir).png" alt="Girl in a jacket" width="1000" height="1200"> <img src="" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20accessed%20(exploiting).png
" alt="Girl in a jacket" width="1000" height="1200"> <img src="https://github.com/Jaybest01/website-cloning-and-smb-enumeration-labs/blob/main/Enum4Linux_SMB-Exploit-Capture/smbclient%20accessed%20(installing%20malicious%20file).png" alt="Girl in a jacket" width="1000" height="1200">



# Key Takeaways
- Website cloning is commonly used in phishing attacks
- SMB misconfigurations allow attackers to enumerate sensitive information
- Proper security controls can prevent these attack vectors

<br/>

# Conclusion
These labs provided hands-on experience with common penetration testing techniques used to identify and mitigate real-world security risks.
