
## NMAP

```
# Nmap 7.94SVN scan initiated Mon Jul 15 15:51:25 2024 as: nmap -vv --reason -Pn -T4 -sU -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-07-15 15:51:25 EDT for 18s
PORT      STATE SERVICE        VERSION
53/udp open domain udp-response ttl 125 Simple DNS Plus
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
# Nmap done at Mon Jul 15 15:51:43 2024 -- 1 IP address (1 host up) scanned in 18.13 seconds
```

## reverse-lookup

```
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> -p 53 -x TARGET @TARGET
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: SERVFAIL, id: 61016
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4000
;; QUESTION SECTION:
;122.230.168.192.in-addr.arpa.	IN	PTR

;; Query time: 4132 msec
;; SERVER: TARGET#53(TARGET) (UDP)
;; WHEN: Mon Jul 15 15:51:34 EDT 2024
;; MSG SIZE  rcvd: 57

```

## DNS-Zone-Transfer

```
;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.25-185-g392e7199df2-1-Debian <<>> AXFR -p 53 @TARGET
; (1 server found)
;; global options: +cmd
;; Query time: 4136 msec
;; SERVER: TARGET#53(TARGET) (UDP)
;; WHEN: Mon Jul 15 15:51:34 EDT 2024
;; MSG SIZE  rcvd: 28

```
