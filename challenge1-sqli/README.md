# Challenge 1: SQL Injection

In this part, you must discover user account information on a server and crack the password of Bob Smith's account. You will then locate the file with Challenge 1 code and use Bob Smith's account credentials to open the file at 192.168.0.10 to view its contents.

## Step 1:Preliminary setup
**Open a browser and go to the website at 10.5.5.12.**

<img width="832" height="428" alt="image" src="https://github.com/user-attachments/assets/6e9f3b48-a3a9-45bc-99c3-62984643008f" />

**Login with the credentials admin / password**

<img width="834" height="425" alt="image" src="https://github.com/user-attachments/assets/d3b899a8-68d3-42ab-abca-d3677e47a915" />

**Set the DVWA security level to low and click Submit.**

<img width="383" height="305" alt="image" src="https://github.com/user-attachments/assets/fc0638ec-c06a-4c7d-a972-0ac2a9bd7f43" />

## Step 2: Retrieve the user credentials for the Bob Smith’s account

Identify the table that contains usernames and passwords

Using the payload: `1' OR 1=1 UNION SELECT 1,column_name FROM information_schema.columns WHERE table_name='users'#`

<img width="1657" height="826" alt="image" src="https://github.com/user-attachments/assets/01e1cb39-c571-4cba-8073-85a07baffdd0" />

Retrieve the username and the password hash for Bob Smith's account.

To retrieve the password for the user Bob, we use the payload: `1' OR 1=1 UNION SELECT user, password FROM users #`

<img width="1605" height="765" alt="image" src="https://github.com/user-attachments/assets/ed6b811b-6bdb-4565-bde8-e030ba838bda" />

## Step 3: Crack Bob Smith’s account password

We will use [crackstation](https://crackstation.net/) to crack the hash

<img width="907" height="321" alt="image" src="https://github.com/user-attachments/assets/e9f38fa8-8d3a-44d2-8001-a5d59c7599f7" />

The password of Bob Smith’s account:

<img width="1603" height="160" alt="image" src="https://github.com/user-attachments/assets/cc3a6e1b-16c3-4d3f-b161-cd27689f40ee" />

## Step 4: Locate and open the file with Challenge 1 code

Log into 192.168.0.10 as Bob Smith through SSH

<img width="606" height="310" alt="image" src="https://github.com/user-attachments/assets/e0968a65-b7b5-4415-a233-a29d8c37c8d0" />

Locate and open the flag file in the user's home directory. What is the name of the file with the code?

<img width="718" height="135" alt="image" src="https://github.com/user-attachments/assets/1764a45e-b3c8-4d42-8ae6-75adc3e568cb" />

What is the message contained in the file?

<img width="733" height="217" alt="image" src="https://github.com/user-attachments/assets/414b8208-aa6c-4087-9bc4-80424c7a41b6" />

## Step 5: Research and propose SQL attack remediation

What are five remediation methods for preventing SQL injection exploits?

Five effective remediation methods for preventing SQL injection exploits are:
 - prepared statements
 - implementing the principle of least privilege
 - employing input validation
 - utilizing stored procedures
 - managing error messages securely










