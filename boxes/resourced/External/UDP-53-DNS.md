
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jul 24 19:18:10 2024 as: nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.054s latency).
Scanned at 2024-07-24 19:18:11 EDT for 159s

PORT   STATE SERVICE REASON          VERSION
53/tcp open  domain? syn-ack ttl 125
|_dns-nsec3-enum: Can't determine domain for host TARGET; use dns-nsec3-enum.domains script arg.
|_dns-nsec-enum: Can't determine domain for host TARGET; use dns-nsec-enum.domains script arg.

Host script results:
|_dns-brute: Can't guess domain of "TARGET"; use dns-brute.domain script argument.

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
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