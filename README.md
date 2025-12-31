# ParoCyber Final Capstone – Penetration Testing & Ethical Hacking

## Overview
This repository documents the completion of the **ParoCyber Final Capstone Activity**, a hands-on penetration testing assessment modeled as a Capture The Flag (CTF) exercise.

The objective was to conduct a full penetration test engagement, including:
- Reconnaissance
- Vulnerability discovery
- Exploitation
- Flag retrieval
- Remediation recommendations

All activities were performed in a **controlled lab environment** for educational purposes only.

---

## Scope & Objectives
- Perform SQL Injection attacks to retrieve sensitive credentials
- Exploit web server misconfigurations
- Enumerate and exploit open SMB shares
- Analyze packet captures (PCAP) for sensitive data exposure
- Propose mitigation and remediation strategies

Target networks:
- `10.5.5.0/24`
- `192.168.0.0/24`

---

## Challenges Completed

### Challenge 1: SQL Injection
- Identified vulnerable input fields
- Extracted database credentials using SQL Injection
- Cracked password hashes
- Accessed a protected system using compromised credentials
- Retrieved the flag file

**Key Skills:** SQLi, password cracking, web exploitation

---

### Challenge 2: Web Server Vulnerabilities
- Conducted directory enumeration
- Identified directory listing misconfigurations
- Navigated exposed subdirectories
- Retrieved flag file via URL manipulation

**Key Skills:** Web reconnaissance, directory enumeration

---

### Challenge 3: SMB Share Exploitation
- Scanned the network for SMB services
- Enumerated anonymous shares
- Accessed unsecured SMB directories
- Downloaded and analyzed flag files

**Key Skills:** SMB enumeration, lateral access

---

### Challenge 4: PCAP Analysis
- Analyzed captured network traffic using Wireshark
- Identified sensitive data transmitted in clear text
- Extracted URLs, IP addresses, and exposed file contents
- Retrieved final challenge flag

**Key Skills:** Network traffic analysis, data exposure detection

---

## Tools Used
- Kali Linux
- DVWA
- Nmap
- SQLMap
- Hydra / John the Ripper
- smbclient
- Wireshark
- Web Browser Developer Tools

(Full list in `tools-used.md`)

---

## Remediation Summary
Each challenge includes remediation guidance covering:
- Input validation and prepared statements
- Secure web server configuration
- SMB access control and hardening
- Encryption of data in transit (HTTPS, SMB signing)

---

## Disclaimer
This project was completed strictly for **educational purposes** in a controlled lab environment.  
Unauthorized testing against live systems is illegal and unethical.

---

## Author
Claudius Thompson
Cybersecurity | Ethical Hacking | Cybersecurity Education  
