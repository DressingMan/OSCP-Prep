```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:25:30 2024 as: nmap -vv --reason -Pn -T4 -sV -p 464 --script=banner,krb5-enum-users -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-15 15:25:31 EDT for 21s

PORT    STATE SERVICE   REASON          VERSION
464/tcp open  kpasswd5? syn-ack ttl 125

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 15:25:52 2024 -- 1 IP address (1 host up) scanned in 22.52 seconds

```

