
```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:43:06 2024 as: nmap -vv --reason -Pn -T4 -sV -p 631 "--script=banner,(cups* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-10-17 16:43:06 EDT for 27s
PORT      STATE SERVICE        VERSION
631/tcp open ipp CUPS 2.2
# Nmap done at Thu Oct 17 16:43:33 2024 -- 1 IP address (1 host up) scanned in 27.06 seconds
```

