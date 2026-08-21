```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:51:25 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 123 "--script=banner,(ntp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-07-15 15:51:25 EDT for 10s
PORT      STATE SERVICE        VERSION
123/udp open ntp udp-response ttl 125 NTP v3
# Nmap done at Mon Jul 15 15:51:35 2024 -- 1 IP address (1 host up) scanned in 10.88 seconds
```
