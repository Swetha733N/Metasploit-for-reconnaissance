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


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
