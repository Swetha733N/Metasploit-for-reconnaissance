## Reg.no:212222110050
## NAME:SWETHA N
# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find out the ip address of the attackers system

## OUTPUT:

![image](https://github.com/user-attachments/assets/46b77fae-d904-4c81-9f48-fa9852b49931)

Invoke msfconsole: 
![image](https://github.com/user-attachments/assets/ca0f43b5-a59e-4440-a598-6f0e4af1fa23)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
![image](https://github.com/user-attachments/assets/e199dcfc-e9e0-41e7-8528-51d030e6a61c)


## Portscannig:

Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![image](https://github.com/user-attachments/assets/c78c4d2d-6166-41c9-ad16-1e080b3c663d)

step4: use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

## OUTPUT:

![image](https://github.com/user-attachments/assets/7996fd0b-5819-496d-8d8f-d545354dcbbe)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
## OUTPUT:
![374878610-b7fae978-cd19-4bf9-909a-4b1bb675325c](https://github.com/user-attachments/assets/53fe0441-5891-44fc-848e-6e46240c5be7)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
The info command provides information regarding a module or platform.

## OUTPUT:
![374878760-fad6d941-f0b2-4858-9df5-3ea49880600a](https://github.com/user-attachments/assets/cd4503ff-c9bf-4118-b1a3-dacb088d9c74)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init

### MYSQL ENUMERATION:
Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address> 
![374878832-00f5d101-b106-4260-90fe-9c48af3bf1f2](https://github.com/user-attachments/assets/511f4b6e-206e-4779-9253-d62bb7302253)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql 
![374878895-7b606c3d-c7c2-4cc0-8da0-dc3493b32dd8](https://github.com/user-attachments/assets/7b703529-db6b-41d9-9482-9d82d1849107)

use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version 
![374879000-c272702f-85fa-4797-9259-1b04298e48ec](https://github.com/user-attachments/assets/56d7e0f1-2d15-49f3-9ce3-7cc6e986b007)

Use the set rhosts command to set the parameter and run the module, as follows:
![374879011-7cb2df0e-aebd-454e-a992-5b6b8de362a9](https://github.com/user-attachments/assets/600548f8-0e1a-4c3a-9549-cc3f9567a54f)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module. 
![374879075-6d98cae1-206d-40e2-a5d9-e33b68e1f48a](https://github.com/user-attachments/assets/d664b922-b40b-4862-b881-ba9375ce186b)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true 

![374879122-4618a435-9885-45ed-8a5e-362bedc1f987](https://github.com/user-attachments/assets/ab4ca71c-b963-4f44-9893-1128f424e7bf)


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
