
```
# Nmap 7.94SVN scan initiated Sat Jul 27 19:45:49 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 88 --script=banner,krb5-enum-users -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.073s latency).
Scanned at 2024-07-27 19:45:49 EDT for 0s

PORT   STATE SERVICE      REASON               VERSION
88/udp open  kerberos-sec udp-response ttl 125 Microsoft Windows Kerberos (server time: 2024-07-27 23:45:48Z)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jul 27 19:45:49 2024 -- 1 IP address (1 host up) scanned in 0.31 seconds

```

