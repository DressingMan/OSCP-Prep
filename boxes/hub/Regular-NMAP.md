```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:23 2024 as: nmap -p- -sV -sC --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up (0.091s latency).
Not shown: 65126 closed tcp ports (reset), 405 filtered tcp ports (no-response)
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
80/tcp open http nginx 1.18.0
|_http-title: 403 Forbidden
8082/tcp open http Barracuda Embedded Web Server
| http-methods:
|_  Potentially risky methods: PROPFIND PATCH PUT COPY DELETE MOVE MKCOL PROPPATCH LOCK UNLOCK
|_http-title: Home
9999/tcp open ssl/http Barracuda Embedded Web Server
| ssl-cert: Subject: commonName=FuguHub/stateOrProvinceName=California/countryName=US
|_http-title: Home
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
# Nmap done at Mon Jul  1 17:34:21 2024 -- 1 IP address (1 host up) scanned in 57.81 seconds
```
