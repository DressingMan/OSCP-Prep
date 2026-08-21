## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 19 19:05:52 2024 as: nmap -vv --reason -Pn -T4 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-06-19 19:05:53 EDT for 161s
PORT      STATE SERVICE        VERSION
53/tcp open domain?
# Nmap done at Wed Jun 19 19:08:34 2024 -- 1 IP address (1 host up) scanned in 162.13 seconds
```

## Reverse-lookup 

```

;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.21-1-Debian <<>> -p 53 -x TARGET @TARGET
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: SERVFAIL, id: 28596
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4000
;; QUESTION SECTION:
;165.151.168.192.in-addr.arpa.	IN	PTR

;; Query time: 4800 msec
;; SERVER: TARGET#53(TARGET) (UDP)
;; WHEN: Wed Jun 19 19:06:01 EDT 2024
;; MSG SIZE  rcvd: 57

```

## DNS-Zone-Transfer

```

;; communications error to TARGET#53: timed out

; <<>> DiG 9.19.21-1-Debian <<>> AXFR -p 53 @TARGET
; (1 server found)
;; global options: +cmd
;; Query time: 4800 msec
;; SERVER: TARGET#53(TARGET) (UDP)
;; WHEN: Wed Jun 19 19:06:01 EDT 2024
;; MSG SIZE  rcvd: 28

```

