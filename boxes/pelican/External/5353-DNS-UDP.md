
## NMAP

```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:46:34 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 5353 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-10-17 16:46:35 EDT for 0s
PORT      STATE SERVICE        VERSION
5353/udp open mdns udp-response ttl 252 DNS-based service discovery
# Nmap done at Thu Oct 17 16:46:35 2024 -- 1 IP address (1 host up) scanned in 0.65 seconds
```

