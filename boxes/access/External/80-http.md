## NMAP 

```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:38 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-07-27 21:38:39 EDT for 35s
PORT      STATE SERVICE        VERSION
80/tcp open http Apache httpd 2.4.48 ((Win64) OpenSSL/1.1.1k PHP/8.0.7)
|_http-title: Access The Event
| http-methods:
|_  Potentially risky methods: TRACE
```
