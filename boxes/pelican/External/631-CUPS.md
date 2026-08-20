
```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:43:06 2024 as: nmap -vv --reason -Pn -T4 -sV -p 631 "--script=banner,(cups* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-10-17 16:43:06 EDT for 27s

PORT    STATE SERVICE REASON         VERSION
631/tcp open  ipp     syn-ack ttl 61 CUPS 2.2
|_http-server-header: CUPS/2.2 IPP/2.1
|_cups-queue-info: ERROR: Script execution failed (use -d to debug)
|_cups-info: ERROR: Script execution failed (use -d to debug)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 17 16:43:33 2024 -- 1 IP address (1 host up) scanned in 27.06 seconds

```

