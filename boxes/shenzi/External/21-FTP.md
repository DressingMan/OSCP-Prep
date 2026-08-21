
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 21 "--script=banner,(ftp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.078s latency).
Scanned at 2024-06-26 21:19:55 EDT for 2s
PORT      STATE SERVICE        VERSION
21/tcp open ftp FileZilla ftpd 0.9.41 beta
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Wed Jun 26 21:19:57 2024 -- 1 IP address (1 host up) scanned in 3.28 seconds
```

```
hydra -C /usr/share/seclists/Passwords/Default-Credentials/ftp-betterdefaultpasslist.txt TARGET ftp
```

no default creds 
