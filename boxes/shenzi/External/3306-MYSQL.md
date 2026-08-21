## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 3306 "--script=banner,(mysql* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.068s latency).
Scanned at 2024-06-26 21:19:55 EDT for 9s
PORT      STATE SERVICE        VERSION
3306/tcp open mysql?
# Nmap done at Wed Jun 26 21:20:04 2024 -- 1 IP address (1 host up) scanned in 10.51 seconds
```

