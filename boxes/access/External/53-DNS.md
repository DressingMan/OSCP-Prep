## NMAP 

```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:38 2024 as: nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-27 21:38:38 EDT for 160s
PORT      STATE SERVICE        VERSION
53/tcp open domain?
# Nmap done at Sat Jul 27 21:41:18 2024 -- 1 IP address (1 host up) scanned in 159.69 seconds
```

## Reverse-lookup 

```bash

;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> -p 53 -x TARGET @TARGET
;; global options: +cmd
;; no servers could be reached

```

## DNS-Zone-Transfer

```bash

;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> AXFR -p 53 @TARGET
; (1 server found)
;; global options: +cmd
;; no servers could be reached

```

