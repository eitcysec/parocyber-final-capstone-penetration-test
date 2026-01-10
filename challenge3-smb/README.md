# Challenge 3: Exploit open SMB Server Shares

In this part, you want to discover if there are any unsecured shared directories located on an SMB server in the 10.5.5.0/24 network. You can use any of the tools you learned in earlier labs to find the drive shares available on the servers.

# Step 1: Step 1:Scan for potential targets running SMB.

Use scanning tools to scan the 10.5.5.0/24 LAN for potential targets for SMB enumeration.<br>
Command: `nmap -p139,445 10.5.5.0/24`

<img width="547" height="89" alt="image" src="https://github.com/user-attachments/assets/6452951d-648e-481b-8b2e-1af64c82a22b" />

Which host on the 10.5.5.0/24 network has open ports indicating it is likely running SMB services?

<img width="362" height="110" alt="image" src="https://github.com/user-attachments/assets/8072efc3-9829-49e7-98f6-fef1321de8af" />

# Step 2: Step 2:Determine which SMB directories are shared and can be accessed by anonymous users.

Step 2:Determine which SMB directories are shared and can be accessed by anonymous users.<br>
Command: `enum4linux -S 10.5.5.14`<br>
`-S`: This option get sharelist

<img width="422" height="380" alt="image" src="https://github.com/user-attachments/assets/b1056c85-e101-4cbd-af11-5fe3f58d692d" />

# Step 3: Investigate each shared directory to find the file

Use the SMB-native client to access the drive shares on the SMB server. Use the dir, ls, cd, and other commands to find subdirectories and files.<br>
Command: `smbclient -L //10.5.5.14 -N`<br>
`-L`:                           Get a list of shares available on a host<br>
`-N`:                                Don't ask for a password

<img width="433" height="221" alt="image" src="https://github.com/user-attachments/assets/a84b3f4a-82e2-4065-9a3c-fb5730767023" />


Locate the file with the Challenge 3 code. Download the file and open it locally.
<img width="969" height="550" alt="image" src="https://github.com/user-attachments/assets/c1d4c798-2935-4b97-8507-cbb6def77f30" />

<img width="1309" height="739" alt="image" src="https://github.com/user-attachments/assets/28ec86b8-7fd9-44e2-9778-209f834388fe" />

<img width="1050" height="91" alt="image" src="https://github.com/user-attachments/assets/30b4de8e-4006-47c6-8566-c4b629f6f3e1" />

Enter the code for Challenge 3

<img width="478" height="157" alt="image" src="https://github.com/user-attachments/assets/bbb65e3f-45ce-4893-b2e8-bca889a7424f" />

# Step 4: Research and propose SMB attack remediation.

What are two remediation methods for preventing SMB servers from being accessed? 

Two key remediation methods for preventing unauthorized SMB server access are:
 - Network segmentation and firewall rules to restrict access to trusted IPs/VLANs 
 - Disabling legacy SMB versions (SMBv1) and enforcing strong authentication (like Kerberos/NTLMv2 with MFA) to prevent exploits and interception. 


