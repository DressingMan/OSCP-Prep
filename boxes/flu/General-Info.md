## Host Info
```

TARGET


```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:17:44 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -320398 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -320398 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -423470 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -423470 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.056s latency).
Scanned at 2024-10-30 15:17:44 EDT for 28s
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE       REASON         VERSION
22/tcp   open  ssh           syn-ack ttl 61 OpenSSH 9.0p1 Ubuntu 1ubuntu8.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 02:79:64:84:da:12:97:23:77:8a:3a:60:20:96:ee:cf (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEXrRUno9oC8lTzQc4mkRYkhVE1WFraJqALzhn+4EmH4j57s4WioLYYYESpMPsdluWAXJreN+LVlUL/5UteMBbI=
|   256 dd:49:a3:89:d7:57:ca:92:f0:6c:fe:59:a6:24:cc:87 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIITU00dnwzhT+PFW6y7qRlFYCQ0UzFakp4R4NIq5TWiS
8090/tcp open  opsmessaging? syn-ack ttl 61
Device type: general purpose|firewall|WAP
Running (JUST GUESSING): OpenBSD 4.X (90%), FreeBSD 6.X (88%), Check Point embedded (86%), Linux 2.6.X (86%), Apple embedded (85%)
OS CPE: cpe:/o:openbsd:openbsd:4.0 cpe:/o:freebsd:freebsd:6.2 cpe:/h:checkpoint:zonealarm_z100g cpe:/o:linux:linux_kernel:2.6.36 cpe:/h:apple:airport_extreme
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: OpenBSD 4.0 (90%), FreeBSD 6.2-RELEASE (88%), OpenBSD 4.3 (87%), Check Point ZoneAlarm Z100G firewall (86%), Linux 2.6.36 (86%), Apple AirPort Extreme WAP (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/30%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=67228674%P=x86_64-pc-linux-gnu)
SEQ()
SEQ(SP=108%GCD=1%ISR=10A%TI=Z%II=I)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=O%F=AS%RD=0%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=O%F=AR%O=%RD=0%Q=)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 0.000 days (since Wed Oct 30 15:18:05 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=264 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 554/tcp)
HOP RTT      ADDRESS
1   55.01 ms ATTACKER
2   54.68 ms ATTACKER
3   55.30 ms TARGET
4   55.38 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct 30 15:18:12 2024 -- 1 IP address (1 host up) scanned in 28.30 seconds

```

#### Full Scan
```bash


```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:18:16 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received reset ttl 61 (0.056s latency).
Scanned at 2024-10-30 15:18:16 EDT for 139s

PORT      STATE  SERVICE         REASON
7/udp     closed echo            port-unreach ttl 61
9/udp     closed discard         port-unreach ttl 61
17/udp    closed qotd            port-unreach ttl 61
19/udp    closed chargen         port-unreach ttl 61
49/udp    closed tacacs          port-unreach ttl 61
53/udp    closed domain          port-unreach ttl 61
67/udp    closed dhcps           port-unreach ttl 61
68/udp    closed dhcpc           port-unreach ttl 61
69/udp    closed tftp            port-unreach ttl 61
80/udp    closed http            port-unreach ttl 61
88/udp    closed kerberos-sec    port-unreach ttl 61
111/udp   closed rpcbind         port-unreach ttl 61
120/udp   closed cfdptkt         port-unreach ttl 61
123/udp   closed ntp             port-unreach ttl 61
135/udp   closed msrpc           port-unreach ttl 61
136/udp   closed profile         port-unreach ttl 61
137/udp   closed netbios-ns      port-unreach ttl 61
138/udp   closed netbios-dgm     port-unreach ttl 61
139/udp   closed netbios-ssn     port-unreach ttl 61
158/udp   closed pcmail-srv      port-unreach ttl 61
161/udp   closed snmp            port-unreach ttl 61
162/udp   closed snmptrap        port-unreach ttl 61
177/udp   closed xdmcp           port-unreach ttl 61
427/udp   closed svrloc          port-unreach ttl 61
443/udp   closed https           port-unreach ttl 61
445/udp   closed microsoft-ds    port-unreach ttl 61
497/udp   closed retrospect      port-unreach ttl 61
500/udp   closed isakmp          port-unreach ttl 61
514/udp   closed syslog          port-unreach ttl 61
515/udp   closed printer         port-unreach ttl 61
518/udp   closed ntalk           port-unreach ttl 61
520/udp   closed route           port-unreach ttl 61
593/udp   closed http-rpc-epmap  port-unreach ttl 61
623/udp   closed asf-rmcp        port-unreach ttl 61
626/udp   closed serialnumberd   port-unreach ttl 61
631/udp   closed ipp             port-unreach ttl 61
996/udp   closed vsinet          port-unreach ttl 61
997/udp   closed maitrd          port-unreach ttl 61
998/udp   closed puparp          port-unreach ttl 61
999/udp   closed applix          port-unreach ttl 61
1022/udp  closed exp2            port-unreach ttl 61
1023/udp  closed unknown         port-unreach ttl 61
1025/udp  closed blackjack       port-unreach ttl 61
1026/udp  closed win-rpc         port-unreach ttl 61
1027/udp  closed unknown         port-unreach ttl 61
1028/udp  closed ms-lsa          port-unreach ttl 61
1029/udp  closed solid-mux       port-unreach ttl 61
1030/udp  closed iad1            port-unreach ttl 61
1433/udp  closed ms-sql-s        port-unreach ttl 61
1434/udp  closed ms-sql-m        port-unreach ttl 61
1645/udp  closed radius          port-unreach ttl 61
1646/udp  closed radacct         port-unreach ttl 61
1701/udp  closed L2TP            port-unreach ttl 61
1718/udp  closed h225gatedisc    port-unreach ttl 61
1719/udp  closed h323gatestat    port-unreach ttl 61
1812/udp  closed radius          port-unreach ttl 61
1813/udp  closed radacct         port-unreach ttl 61
1900/udp  closed upnp            port-unreach ttl 61
2000/udp  closed cisco-sccp      port-unreach ttl 61
2048/udp  closed dls-monitor     port-unreach ttl 61
2049/udp  closed nfs             port-unreach ttl 61
2222/udp  closed msantipiracy    port-unreach ttl 61
2223/udp  closed rockwell-csp2   port-unreach ttl 61
3283/udp  closed netassistant    port-unreach ttl 61
3456/udp  closed IISrpc-or-vat   port-unreach ttl 61
3703/udp  closed adobeserver-3   port-unreach ttl 61
4444/udp  closed krb524          port-unreach ttl 61
4500/udp  closed nat-t-ike       port-unreach ttl 61
5000/udp  closed upnp            port-unreach ttl 61
5060/udp  closed sip             port-unreach ttl 61
5353/udp  closed zeroconf        port-unreach ttl 61
5632/udp  closed pcanywherestat  port-unreach ttl 61
9200/udp  closed wap-wsp         port-unreach ttl 61
10000/udp closed ndmp            port-unreach ttl 61
17185/udp closed wdbrpc          port-unreach ttl 61
20031/udp closed bakbonenetvault port-unreach ttl 61
30718/udp closed unknown         port-unreach ttl 61
31337/udp closed BackOrifice     port-unreach ttl 61
32768/udp closed omad            port-unreach ttl 61
32769/udp closed filenet-rpc     port-unreach ttl 61
32771/udp closed sometimes-rpc6  port-unreach ttl 61
32815/udp closed unknown         port-unreach ttl 61
33281/udp closed unknown         port-unreach ttl 61
49152/udp closed unknown         port-unreach ttl 61
49153/udp closed unknown         port-unreach ttl 61
49154/udp closed unknown         port-unreach ttl 61
49156/udp closed unknown         port-unreach ttl 61
49181/udp closed unknown         port-unreach ttl 61
49182/udp closed unknown         port-unreach ttl 61
49185/udp closed unknown         port-unreach ttl 61
49186/udp closed unknown         port-unreach ttl 61
49188/udp closed unknown         port-unreach ttl 61
49190/udp closed unknown         port-unreach ttl 61
49191/udp closed unknown         port-unreach ttl 61
49192/udp closed unknown         port-unreach ttl 61
49193/udp closed unknown         port-unreach ttl 61
49194/udp closed unknown         port-unreach ttl 61
49200/udp closed unknown         port-unreach ttl 61
49201/udp closed unknown         port-unreach ttl 61
65024/udp closed unknown         port-unreach ttl 61

Read data files from: /usr/bin/../share/nmap
# Nmap done at Wed Oct 30 15:20:35 2024 -- 1 IP address (1 host up) scanned in 139.14 seconds


```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Wed Oct 30 15:18:09 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.059s latency).
Scanned at 2024-10-30 15:18:09 EDT for 133s
Not shown: 65405 closed tcp ports (reset), 127 filtered tcp ports (no-response)
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
PORT     STATE SERVICE       REASON         VERSION
22/tcp   open  ssh           syn-ack ttl 61 OpenSSH 9.0p1 Ubuntu 1ubuntu8.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 02:79:64:84:da:12:97:23:77:8a:3a:60:20:96:ee:cf (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEXrRUno9oC8lTzQc4mkRYkhVE1WFraJqALzhn+4EmH4j57s4WioLYYYESpMPsdluWAXJreN+LVlUL/5UteMBbI=
|   256 dd:49:a3:89:d7:57:ca:92:f0:6c:fe:59:a6:24:cc:87 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIITU00dnwzhT+PFW6y7qRlFYCQ0UzFakp4R4NIq5TWiS
8090/tcp open  opsmessaging? syn-ack ttl 61
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.1 302 
|     Cache-Control: no-store
|     Expires: Thu, 01 Jan 1970 00:00:00 GMT
|     X-Confluence-Request-Time: 1730315924352
|     Set-Cookie: JSESSIONID=009E9230366A751C5A99496194B6FE18; Path=/; HttpOnly
|     X-XSS-Protection: 1; mode=block
|     X-Content-Type-Options: nosniff
|     X-Frame-Options: SAMEORIGIN
|     Content-Security-Policy: frame-ancestors 'self'
|     Location: http://localhost:8090/login.action?os_destination=%2Findex.action&permissionViolation=true
|     Content-Type: text/html;charset=UTF-8
|     Content-Length: 0
|     Date: Wed, 30 Oct 2024 19:18:44 GMT
|     Connection: close
|   HTTPOptions: 
|     HTTP/1.1 200 
|     MS-Author-Via: DAV
|     Content-Type: text/html;charset=UTF-8
|     Content-Length: 0
|     Date: Wed, 30 Oct 2024 19:18:44 GMT
|     Connection: close
|   RTSPRequest: 
|     HTTP/1.1 400 
|     Content-Type: text/html;charset=utf-8
|     Content-Language: en
|     Content-Length: 1924
|     Date: Wed, 30 Oct 2024 19:18:44 GMT
|     Connection: close
|     <!doctype html><html lang="en"><head><title>HTTP Status 400 
|     Request</title><style type="text/css">body {font-family:Tahoma,Arial,sans-serif;} h1, h2, h3, b {color:white;background-color:#525D76;} h1 {font-size:22px;} h2 {font-size:16px;} h3 {font-size:14px;} p {font-size:12px;} a {color:black;} .line {height:1px;background-color:#525D76;border:none;}</style></head><body><h1>HTTP Status 400 
|_    Request</h1><hr class="line" /><p><b>Type</b> Exception Report</p><p><b>Message</b> Invalid character found in the HTTP protocol [RTSP&#47;1.00x0d0x0a0x0d0x0a...]</p><p><b>Description</b> The server cannot or will not process the request due to something that is perceived to be a client error (e.g., malformed request syntax, invalid
8091/tcp open  jamlink?      syn-ack ttl 61
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.1 204 No Content
|     Server: Aleph/0.4.6
|     Date: Wed, 30 Oct 2024 19:19:20 GMT
|     Connection: Close
|   GetRequest: 
|     HTTP/1.1 204 No Content
|     Server: Aleph/0.4.6
|     Date: Wed, 30 Oct 2024 19:18:49 GMT
|     Connection: Close
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Access-Control-Allow-Origin: *
|     Access-Control-Max-Age: 31536000
|     Access-Control-Allow-Methods: OPTIONS, GET, PUT, POST
|     Server: Aleph/0.4.6
|     Date: Wed, 30 Oct 2024 19:18:49 GMT
|     Connection: Close
|     content-length: 0
|   Help, Kerberos, LDAPSearchReq, LPDString, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 414 Request-URI Too Long
|     text is empty (possibly HTTP/0.9)
|   RTSPRequest: 
|     HTTP/1.1 200 OK
|     Access-Control-Allow-Origin: *
|     Access-Control-Max-Age: 31536000
|     Access-Control-Allow-Methods: OPTIONS, GET, PUT, POST
|     Server: Aleph/0.4.6
|     Date: Wed, 30 Oct 2024 19:18:49 GMT
|     Connection: Keep-Alive
|     content-length: 0
|   SIPOptions: 
|     HTTP/1.1 200 OK
|     Access-Control-Allow-Origin: *
|     Access-Control-Max-Age: 31536000
|     Access-Control-Allow-Methods: OPTIONS, GET, PUT, POST
|     Server: Aleph/0.4.6
|     Date: Wed, 30 Oct 2024 19:19:25 GMT
|     Connection: Keep-Alive
|_    content-length: 0
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port8090-TCP:V=7.94SVN%I=7%D=10/30%Time=67228695%P=x86_64-pc-linux-gnu%
SF:r(GetRequest,22F,"HTTP/1\.1\x20302\x20\r\nCache-Control:\x20no-store\r\
SF:nExpires:\x20Thu,\x2001\x20Jan\x201970\x2000:00:00\x20GMT\r\nX-Confluen
SF:ce-Request-Time:\x201730315924352\r\nSet-Cookie:\x20JSESSIONID=009E9230
SF:366A751C5A99496194B6FE18;\x20Path=/;\x20HttpOnly\r\nX-XSS-Protection:\x
SF:201;\x20mode=block\r\nX-Content-Type-Options:\x20nosniff\r\nX-Frame-Opt
SF:ions:\x20SAMEORIGIN\r\nContent-Security-Policy:\x20frame-ancestors\x20'
SF:self'\r\nLocation:\x20http://localhost:8090/login\.action\?os_destinati
SF:on=%2Findex\.action&permissionViolation=true\r\nContent-Type:\x20text/h
SF:tml;charset=UTF-8\r\nContent-Length:\x200\r\nDate:\x20Wed,\x2030\x20Oct
SF:\x202024\x2019:18:44\x20GMT\r\nConnection:\x20close\r\n\r\n")%r(HTTPOpt
SF:ions,97,"HTTP/1\.1\x20200\x20\r\nMS-Author-Via:\x20DAV\r\nContent-Type:
SF:\x20text/html;charset=UTF-8\r\nContent-Length:\x200\r\nDate:\x20Wed,\x2
SF:030\x20Oct\x202024\x2019:18:44\x20GMT\r\nConnection:\x20close\r\n\r\n")
SF:%r(RTSPRequest,820,"HTTP/1\.1\x20400\x20\r\nContent-Type:\x20text/html;
SF:charset=utf-8\r\nContent-Language:\x20en\r\nContent-Length:\x201924\r\n
SF:Date:\x20Wed,\x2030\x20Oct\x202024\x2019:18:44\x20GMT\r\nConnection:\x2
SF:0close\r\n\r\n<!doctype\x20html><html\x20lang=\"en\"><head><title>HTTP\
SF:x20Status\x20400\x20\xe2\x80\x93\x20Bad\x20Request</title><style\x20typ
SF:e=\"text/css\">body\x20{font-family:Tahoma,Arial,sans-serif;}\x20h1,\x2
SF:0h2,\x20h3,\x20b\x20{color:white;background-color:#525D76;}\x20h1\x20{f
SF:ont-size:22px;}\x20h2\x20{font-size:16px;}\x20h3\x20{font-size:14px;}\x
SF:20p\x20{font-size:12px;}\x20a\x20{color:black;}\x20\.line\x20{height:1p
SF:x;background-color:#525D76;border:none;}</style></head><body><h1>HTTP\x
SF:20Status\x20400\x20\xe2\x80\x93\x20Bad\x20Request</h1><hr\x20class=\"li
SF:ne\"\x20/><p><b>Type</b>\x20Exception\x20Report</p><p><b>Message</b>\x2
SF:0Invalid\x20character\x20found\x20in\x20the\x20HTTP\x20protocol\x20\[RT
SF:SP&#47;1\.00x0d0x0a0x0d0x0a\.\.\.\]</p><p><b>Description</b>\x20The\x20
SF:server\x20cannot\x20or\x20will\x20not\x20process\x20the\x20request\x20d
SF:ue\x20to\x20something\x20that\x20is\x20perceived\x20to\x20be\x20a\x20cl
SF:ient\x20error\x20\(e\.g\.,\x20malformed\x20request\x20syntax,\x20invali
SF:d\x20");
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port8091-TCP:V=7.94SVN%I=7%D=10/30%Time=6722869A%P=x86_64-pc-linux-gnu%
SF:r(GetRequest,68,"HTTP/1\.1\x20204\x20No\x20Content\r\nServer:\x20Aleph/
SF:0\.4\.6\r\nDate:\x20Wed,\x2030\x20Oct\x202024\x2019:18:49\x20GMT\r\nCon
SF:nection:\x20Close\r\n\r\n")%r(HTTPOptions,EC,"HTTP/1\.1\x20200\x20OK\r\
SF:nAccess-Control-Allow-Origin:\x20\*\r\nAccess-Control-Max-Age:\x2031536
SF:000\r\nAccess-Control-Allow-Methods:\x20OPTIONS,\x20GET,\x20PUT,\x20POS
SF:T\r\nServer:\x20Aleph/0\.4\.6\r\nDate:\x20Wed,\x2030\x20Oct\x202024\x20
SF:19:18:49\x20GMT\r\nConnection:\x20Close\r\ncontent-length:\x200\r\n\r\n
SF:")%r(RTSPRequest,F1,"HTTP/1\.1\x20200\x20OK\r\nAccess-Control-Allow-Ori
SF:gin:\x20\*\r\nAccess-Control-Max-Age:\x2031536000\r\nAccess-Control-All
SF:ow-Methods:\x20OPTIONS,\x20GET,\x20PUT,\x20POST\r\nServer:\x20Aleph/0\.
SF:4\.6\r\nDate:\x20Wed,\x2030\x20Oct\x202024\x2019:18:49\x20GMT\r\nConnec
SF:tion:\x20Keep-Alive\r\ncontent-length:\x200\r\n\r\n")%r(Help,46,"HTTP/1
SF:\.1\x20414\x20Request-URI\x20Too\x20Long\r\n\r\ntext\x20is\x20empty\x20
SF:\(possibly\x20HTTP/0\.9\)")%r(SSLSessionReq,46,"HTTP/1\.1\x20414\x20Req
SF:uest-URI\x20Too\x20Long\r\n\r\ntext\x20is\x20empty\x20\(possibly\x20HTT
SF:P/0\.9\)")%r(TerminalServerCookie,46,"HTTP/1\.1\x20414\x20Request-URI\x
SF:20Too\x20Long\r\n\r\ntext\x20is\x20empty\x20\(possibly\x20HTTP/0\.9\)")
SF:%r(TLSSessionReq,46,"HTTP/1\.1\x20414\x20Request-URI\x20Too\x20Long\r\n
SF:\r\ntext\x20is\x20empty\x20\(possibly\x20HTTP/0\.9\)")%r(Kerberos,46,"H
SF:TTP/1\.1\x20414\x20Request-URI\x20Too\x20Long\r\n\r\ntext\x20is\x20empt
SF:y\x20\(possibly\x20HTTP/0\.9\)")%r(FourOhFourRequest,68,"HTTP/1\.1\x202
SF:04\x20No\x20Content\r\nServer:\x20Aleph/0\.4\.6\r\nDate:\x20Wed,\x2030\
SF:x20Oct\x202024\x2019:19:20\x20GMT\r\nConnection:\x20Close\r\n\r\n")%r(L
SF:PDString,46,"HTTP/1\.1\x20414\x20Request-URI\x20Too\x20Long\r\n\r\ntext
SF:\x20is\x20empty\x20\(possibly\x20HTTP/0\.9\)")%r(LDAPSearchReq,46,"HTTP
SF:/1\.1\x20414\x20Request-URI\x20Too\x20Long\r\n\r\ntext\x20is\x20empty\x
SF:20\(possibly\x20HTTP/0\.9\)")%r(SIPOptions,F1,"HTTP/1\.1\x20200\x20OK\r
SF:\nAccess-Control-Allow-Origin:\x20\*\r\nAccess-Control-Max-Age:\x203153
SF:6000\r\nAccess-Control-Allow-Methods:\x20OPTIONS,\x20GET,\x20PUT,\x20PO
SF:ST\r\nServer:\x20Aleph/0\.4\.6\r\nDate:\x20Wed,\x2030\x20Oct\x202024\x2
SF:019:19:25\x20GMT\r\nConnection:\x20Keep-Alive\r\ncontent-length:\x200\r
SF:\n\r\n");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct 30 15:20:22 2024 -- 1 IP address (1 host up) scanned in 133.28 seconds

```

