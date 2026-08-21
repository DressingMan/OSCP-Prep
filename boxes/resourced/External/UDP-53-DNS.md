
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jul 24 19:18:10 2024 as: nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.054s latency).
Scanned at 2024-07-24 19:18:11 EDT for 159s
PORT      STATE SERVICE        VERSION
53/tcp open domain?
# Nmap done at Wed Jul 24 19:20:50 2024 -- 1 IP address (1 host up) scanned in 160.43 seconds
```

## reverse-lookup

```
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> -p 53 -x TARGET @TARGET
;; global options: +cmd
;; no servers could be reached

```

## DNS-Zone-Transfer

```
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> AXFR -p 53 @TARGET
; (1 server found)
;; global options: +cmd
;; no servers could be reached

```
