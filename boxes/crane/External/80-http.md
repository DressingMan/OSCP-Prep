## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:51 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-10-14 10:32:52 EDT for 94s
PORT      STATE SERVICE        VERSION
80/tcp open http Apache httpd 2.4.38 ((Debian))
| http-title: SuiteCRM
| http-robots.txt: 1 disallowed entry
```
