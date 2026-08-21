
```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:25:29 2024 as: nmap -vv --reason -Pn -T4 -sV -p 88 --script=banner,krb5-enum-users -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-07-15 15:25:31 EDT for 18s

PORT   STATE SERVICE      REASON          VERSION
88/tcp open  kerberos-sec syn-ack ttl 125 Microsoft Windows Kerberos (server time: 2024-07-15 19:25:38Z)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 15:25:49 2024 -- 1 IP address (1 host up) scanned in 19.51 seconds

```

