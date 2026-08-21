
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 21 "--script=banner,(ftp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.078s latency).
Scanned at 2024-06-26 21:19:55 EDT for 2s

PORT   STATE SERVICE REASON          VERSION
21/tcp open  ftp     syn-ack ttl 125 FileZilla ftpd 0.9.41 beta
| banner: 220-FileZilla Server version 0.9.41 beta\x0D\x0A220-written by 
| Tim Kosse (Tim.Kosse@gmx.de)\x0D\x0A220 Please visit http://sourceforge
|_.net/projects/filezilla/
| ftp-syst: 
|_  SYST: UNIX emulated by FileZilla
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:19:57 2024 -- 1 IP address (1 host up) scanned in 3.28 seconds

```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```

no default creds 
