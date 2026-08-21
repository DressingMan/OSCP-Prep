
```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:51:25 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 88 --script=banner,krb5-enum-users -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-15 15:51:25 EDT for 0s

PORT   STATE SERVICE      REASON               VERSION
88/udp open  kerberos-sec udp-response ttl 125 Microsoft Windows Kerberos (server time: 2024-07-15 19:51:25Z)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 15:51:25 2024 -- 1 IP address (1 host up) scanned in 0.51 seconds

```

