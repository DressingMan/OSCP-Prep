## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:51 2024 as: nmap -vv --reason -Pn -T4 -sV -p 3306 "--script=banner,(mysql* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-14 10:32:52 EDT for 2s

PORT     STATE SERVICE REASON         VERSION
3306/tcp open  mysql   syn-ack ttl 61 MySQL (unauthorized)
| banner: G\x00\x00\x00\xFFj\x04Host 'ATTACKER' is not allowed to c
|_onnect to this MySQL server
|_mysql-empty-password: Host 'ATTACKER' is not allowed to connect to this MySQL server

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 14 10:32:54 2024 -- 1 IP address (1 host up) scanned in 3.04 seconds

```