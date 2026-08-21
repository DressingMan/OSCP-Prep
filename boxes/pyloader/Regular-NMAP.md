```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 22:06:06 2024 as: nmap -p- -sV -sC -Pn --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.076s latency).
Not shown: 65518 closed tcp ports (reset), 15 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.9p1 Ubuntu 3ubuntu0.1 (Ubuntu Linux; protocol 2.0)
9666/tcp open http CherryPy wsgiserver
| http-title: Login - pyLoad
| http-robots.txt: 1 disallowed entry
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jul 15 22:07:18 2024 -- 1 IP address (1 host up) scanned in 72.34 seconds
```
