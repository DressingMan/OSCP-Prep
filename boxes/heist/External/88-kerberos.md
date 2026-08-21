

## NMAP
```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:05:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 88 --script=banner,krb5-enum-users TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-19 19:05:53 EDT for 17s
PORT      STATE SERVICE        VERSION
88/tcp open kerberos-sec Microsoft Windows Kerberos (server time: 2024-06-19 23:06:00Z)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Wed Jun 19 19:06:10 2024 -- 1 IP address (1 host up) scanned in 18.54 seconds
```
