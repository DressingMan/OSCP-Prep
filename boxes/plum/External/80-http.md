## NMAP 

```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:42 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-21 08:57:43 EDT for 34s
PORT      STATE SERVICE        VERSION
80/tcp open http Apache httpd 2.4.56 ((Debian))
```
