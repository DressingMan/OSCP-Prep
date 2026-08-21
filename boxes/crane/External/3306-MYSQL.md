## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:51 2024 as: nmap -vv --reason -Pn -T4 -sV -p 3306 "--script=banner,(mysql* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-14 10:32:52 EDT for 2s
PORT      STATE SERVICE        VERSION
3306/tcp open mysql MySQL (unauthorized)
# Nmap done at Mon Oct 14 10:32:54 2024 -- 1 IP address (1 host up) scanned in 3.04 seconds
```
