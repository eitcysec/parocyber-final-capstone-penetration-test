# Challenge 4: Analyze a .pcap file to find information.

As part of your reconnaissance effort, your team captured traffic using Wireshark. The capture file, SA.pcap, is located in the Downloads subdirectory within the kali user home directory

##  Step 1: Find and analyze the SA.pcap file

Analyze the content of the PCAP file to determine the IP address of the target computer and the URL location of the file with the Challenge 4 code

<img width="1615" height="790" alt="image" src="https://github.com/user-attachments/assets/1079696b-eb59-4efe-945f-3b1943793d80" />

Follow TCP streams to see paths revealed in the captured traffic.

<img width="1033" height="654" alt="image" src="https://github.com/user-attachments/assets/76e7ea1a-00bc-445b-a532-fb3fc7111898" />

## Step 2: Use a web browser to display the contents of the directories on the target computer.

Use a web browser to investigate the URLs listed in the Wireshark output. Find the file with the code for Challenge 4.

<img width="1395" height="717" alt="image" src="https://github.com/user-attachments/assets/f1fccb4f-2553-4f38-9c8d-2795d3e7080d" />

What is the content of the file?

<img width="1164" height="823" alt="image" src="https://github.com/user-attachments/assets/cb213d7f-01db-4407-85bd-b5d2f698b6e7" />

## Step 3: Step 3:Research and propose remediation that would prevent file content from being transmitted in clear text.

Two key remediation methods to prevent unauthorized viewing of file content are: 
 - Data Encryption (rendering data unreadable without a key)
 - Implementing robust Access Controls (like strong passwords, multi-factor authentication, and permissions
