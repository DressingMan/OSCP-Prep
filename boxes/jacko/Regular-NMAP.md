```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:50:30 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.066s latency).
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
80/tcp open http Microsoft IIS httpd 10.0
|_http-title: H2 Database Engine (redirect)
| http-methods:
|_  Potentially risky methods: TRACE
135/tcp open msrpc Microsoft Windows RPC
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
445/tcp open microsoft-ds?
7680/tcp open pando-pub?
8082/tcp open http H2 database http console
|_http-title: H2 Console
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Sat Jun 29 17:57:07 2024 -- 1 IP address (1 host up) scanned in 396.70 seconds
```
