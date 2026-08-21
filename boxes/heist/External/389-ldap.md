
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:05:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 389 "--script=banner,(ldap* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-06-19 19:05:53 EDT for 18s
PORT      STATE SERVICE        VERSION
389/tcp open ldap Microsoft Windows Active Directory LDAP (Domain: heist.offsec, Site: Default-Fi...
Service Info: Host: DC01; OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Wed Jun 19 19:06:11 2024 -- 1 IP address (1 host up) scanned in 19.94 seconds
```

![Pasted image 20240715203631.png](Evidence/Pasted%20image%2020240715203631.png)

