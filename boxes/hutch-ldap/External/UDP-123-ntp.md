```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:51:25 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 123 "--script=banner,(ntp* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-07-15 15:51:25 EDT for 10s

PORT    STATE SERVICE REASON               VERSION
123/udp open  ntp     udp-response ttl 125 NTP v3
| ntp-info: 
|_  receive time stamp: 2024-07-15T19:51:33

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 15:51:35 2024 -- 1 IP address (1 host up) scanned in 10.88 seconds

```