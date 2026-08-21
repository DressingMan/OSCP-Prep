
## NMAP

```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:04:21 2024 as: nmap -vv --reason -Pn -T4 -sV -p 21 "--script=banner,(ftp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.068s latency).
Scanned at 2024-06-24 23:04:23 EDT for 2s

PORT   STATE SERVICE REASON          VERSION
21/tcp open  ftp     syn-ack ttl 125 Microsoft ftpd
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| 04-29-20  10:31PM       <DIR>          ImapRetrieval
| 06-24-24  07:58PM       <DIR>          Logs
| 04-29-20  10:31PM       <DIR>          PopRetrieval
|_04-29-20  10:32PM       <DIR>          Spool
|_banner: 220 Microsoft FTP Service
| ftp-syst: 
|_  SYST: Windows_NT
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 24 23:04:25 2024 -- 1 IP address (1 host up) scanned in 4.43 seconds

```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```

Brute forced login credentials for FTP 

![Pasted image 20240624231930.png](Evidence/Pasted%20image%2020240624231930.png)

Found three logins and all output the same directories

![Pasted image 20240624232032.png](Evidence/Pasted%20image%2020240624232032.png)

![Pasted image 20240624232250.png](Evidence/Pasted%20image%2020240624232250.png)

bunch of logs...

Administrative log looks interesting...

![Pasted image 20240624232348.png](Evidence/Pasted%20image%2020240624232348.png)

all of the directories are empty except for the logs directory full of logs.


![Pasted image 20240624232556.png](Evidence/Pasted%20image%2020240624232556.png)

we have a valid user -> admin

