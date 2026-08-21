## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jun 29 16:34:23 2024 as: nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-29 16:34:24 EDT for 22s
PORT      STATE SERVICE        VERSION
53/tcp open domain NLnet Labs NSD
# Nmap done at Sat Jun 29 16:34:46 2024 -- 1 IP address (1 host up) scanned in 23.20 seconds
```

## Reverse-lookup 

```

;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.21-1-Debian <<>> -p 53 -x TARGET @TARGET
;; global options: +cmd
;; no servers could be reached

```

## DNS-Zone-Transfer

```

;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.21-1-Debian <<>> AXFR -p 53 @TARGET
; (1 server found)
;; global options: +cmd
;; no servers could be reached

```

