## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:51:47 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-29 17:51:48 EDT for 297s
PORT      STATE SERVICE        VERSION
80/tcp open http Microsoft IIS httpd 10.0
```
