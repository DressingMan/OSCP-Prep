
## NMAP

```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:25:30 2024 as: nmap -vv --reason -Pn -T4 -sV -p 389 "--script=banner,(ldap* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-07-15 15:25:32 EDT for 17s
PORT      STATE SERVICE        VERSION
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: hutch.offsec, Site: Default-Fi...
```
