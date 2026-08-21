```
# Nmap 7.94SVN scan initiated Sat Jun 29 20:51:19 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.057s latency).
Not shown: 65531 filtered tcp ports (no-response), 1 closed tcp port (reset)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
80/tcp open http
| http-title: Boolean
33017/tcp open http Apache httpd 2.4.38 ((Debian))
|_http-title: Development
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Sat Jun 29 20:55:58 2024 -- 1 IP address (1 host up) scanned in 278.88 seconds
```
