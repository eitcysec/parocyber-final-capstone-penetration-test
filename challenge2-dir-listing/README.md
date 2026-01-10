# Challenge 2: Web Server Vulnerabilities 

In this part, you must find vulnerabilities on an HTTP server. Misconfiguration of a web server can allow for the listing of files contained in directories on the server. You can use any of the tools you learned in earlier labs to perform reconnaissance to find the vulnerable directories.
In this challenge, you will locate the flag file in a vulnerable directory on a web server.

## Step 1: Preliminary setup

Log into the server at 10.5.5.12 with the admin / password credentials

<img width="716" height="397" alt="image" src="https://github.com/user-attachments/assets/6e377b3e-5cde-47c7-a73a-80609c18e685" />

Set the application security level to low

<img width="993" height="643" alt="image" src="https://github.com/user-attachments/assets/352d5f06-519d-4df4-a45a-9a7dfae39068" />

## Step 2: From the results of your reconnaissance, determine which directories are viewable using a web browser and URL manipulation

Perform reconnaissance on the server to find directories where indexing was found using Nikto
Command: `nikto -h 10.5.5.12`

<img width="464" height="237" alt="image" src="https://github.com/user-attachments/assets/19dd2317-9079-4161-afa7-81ad508339ae" />

Which directories can be accessed through a web browser to list the files and subdirectories that they contain?

<img width="1257" height="784" alt="image" src="https://github.com/user-attachments/assets/9b63f242-0b9b-402d-a75c-f8bd17fcec96" />

## Step 3: View the files contained in each directory to find the db_form.html file.

Create a URL in the web browser to access the viewable subdirectories. Find the file with the code for Challenge 2 located in one of the subdirectories

<img width="1234" height="721" alt="image" src="https://github.com/user-attachments/assets/07d813ff-7eaf-4569-b47e-08f8404082fd" />

In which two subdirectories can you look for the file?

<img width="739" height="223" alt="image" src="https://github.com/user-attachments/assets/fa2475d7-4c38-4d22-89d6-196638de176d" />

What is the filename with the Challenge 2 code?

<img width="85" height="18" alt="image" src="https://github.com/user-attachments/assets/54933dab-01b7-461d-baee-a0a4ff9b206d" />

What is the message contained in the flag file?

<img width="250" height="63" alt="image" src="https://github.com/user-attachments/assets/2720ff54-5ffc-405f-91c6-4dc62dc2c9e2" />

## Step 4: Research and propose directory listing exploit remediation

What are two remediation methods for preventing directory listing exploits?

Two effective methods to prevent directory listing exploits are:
 - Disabling directory listing in your web server's configuration (e.g., using Options -Indexes in Apache or autoindex off in Nginx)
 - Placing a default index file (like index.html)

