## Host Info
```

TARGET



```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:31 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -167839 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -167839 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -176340 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -176340 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-10-14 10:32:32 EDT for 19s
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE REASON         VERSION
22/tcp   open  ssh     syn-ack ttl 61 OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 37:80:01:4a:43:86:30:c9:79:e7:fb:7f:3b:a4:1e:dd (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDBCcfKYKMXuTWeyLKlFNHgmebcXbFAjSpbr39R8GFHYRmc/mZXKNgEoa5gkFAVr8kVVul4X6//DcnRuHtrCpHcnTIZLT9g1DPB09VsLzsjT0TpmqkcDYtZazo1mjnBZdaM+AxoDMghZd8AXiNrCl7jCN+vRjUQc8T1wD4PoC02XjeCAI8Yha++Mv9ZrSPZ+/gBvgZPL3pdQhVGUSUHOmXod4xcdm5ReNiZRNZklOhhscbGfSCqQIdJogegZfMrlueeG3EY7Kkf5CxAUDH/9ir2dEDDifIpqKV8W7ncKEpsZiqgDh36OdMX4LPJ0NmZiT/g8CvINx7k4HWj3ksT+5C7
|   256 b6:18:a1:e1:98:fb:6c:c6:87:55:45:10:c6:d4:45:b9 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEK0B9iLJQztyEpGiNffHgQuGcxZRO/BOi+r0j/P8Hkz02pIWW2hFrArbzehUNQ46ZmFwMhxxmrIOLBpUt9ZGBw=
|   256 ab:8f:2d:e8:a2:04:e7:b7:65:d3:fe:5e:93:1e:03:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIOAlO2qlRhyMwzzf3xAK4wOGz1UD5t9+QQO5J3QjTkaZ
80/tcp   open  http    syn-ack ttl 61 Apache httpd 2.4.38 ((Debian))
|_http-server-header: Apache/2.4.38 (Debian)
|_http-favicon: Unknown favicon MD5: ED9A8C7810E8C9FB7035B6C3147C9A3A
| http-robots.txt: 1 disallowed entry 
|_/
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-title: SuiteCRM
|_Requested resource was index.php?action=Login&module=Users
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
3306/tcp open  mysql   syn-ack ttl 61 MySQL (unauthorized)
Device type: general purpose|storage-misc|firewall
Running (JUST GUESSING): Linux 2.6.X|3.X|4.X (85%), Synology DiskStation Manager 5.X (85%), WatchGuard Fireware 11.X (85%)
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:3.5 cpe:/o:linux:linux_kernel:4.2 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Linux 2.6.32 (85%), Linux 3.5 (85%), Linux 4.2 (85%), Linux 4.4 (85%), Synology DiskStation Manager 5.1 (85%), WatchGuard Fireware 11.8 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=10/14%OT=22%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=670D2B93%P=x86_64-pc-linux-gnu)
SEQ(SP=106%GCD=1%ISR=107%TI=Z%TS=A)
OPS(O1=M551ST11NW7%O2=M551ST11NW7%O3=M551NNT11NW7%O4=M551ST11NW7%O5=M551ST11NW7%O6=M551ST11)
WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)
ECN(R=Y%DF=Y%TG=40%W=FAF0%O=M551NNSNW7%CC=Y%Q=)
T1(R=Y%DF=Y%TG=40%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=Y%DF=Y%TG=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=Y%DFI=N%TG=40%CD=S)

Uptime guess: 46.870 days (since Wed Aug 28 13:40:33 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 8888/tcp)
HOP RTT      ADDRESS
1   58.35 ms ATTACKER
2   58.33 ms ATTACKER
3   59.39 ms TARGET
4   59.27 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 14 10:32:51 2024 -- 1 IP address (1 host up) scanned in 19.93 seconds

```

#### Full Scan
```bash


```

#### UDP scan
```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:35:15 2024 as: nmap -vvv --top-ports 100 -sU -oN nmap_udp TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.056s latency).
Scanned at 2024-10-14 10:35:15 EDT for 2s

PORT      STATE         SERVICE         REASON
7/udp     open|filtered echo            no-response
9/udp     open|filtered discard         no-response
17/udp    open|filtered qotd            no-response
19/udp    open|filtered chargen         no-response
49/udp    open|filtered tacacs          no-response
53/udp    open|filtered domain          no-response
67/udp    open|filtered dhcps           no-response
68/udp    open|filtered dhcpc           no-response
69/udp    open|filtered tftp            no-response
80/udp    open|filtered http            no-response
88/udp    open|filtered kerberos-sec    no-response
111/udp   open|filtered rpcbind         no-response
120/udp   open|filtered cfdptkt         no-response
123/udp   open|filtered ntp             no-response
135/udp   open|filtered msrpc           no-response
136/udp   open|filtered profile         no-response
137/udp   open|filtered netbios-ns      no-response
138/udp   open|filtered netbios-dgm     no-response
139/udp   open|filtered netbios-ssn     no-response
158/udp   open|filtered pcmail-srv      no-response
161/udp   open|filtered snmp            no-response
162/udp   open|filtered snmptrap        no-response
177/udp   open|filtered xdmcp           no-response
427/udp   open|filtered svrloc          no-response
443/udp   closed        https           port-unreach ttl 61
445/udp   open|filtered microsoft-ds    no-response
497/udp   open|filtered retrospect      no-response
500/udp   open|filtered isakmp          no-response
514/udp   open|filtered syslog          no-response
515/udp   open|filtered printer         no-response
518/udp   open|filtered ntalk           no-response
520/udp   open|filtered route           no-response
593/udp   open|filtered http-rpc-epmap  no-response
623/udp   open|filtered asf-rmcp        no-response
626/udp   open|filtered serialnumberd   no-response
631/udp   open|filtered ipp             no-response
996/udp   open|filtered vsinet          no-response
997/udp   open|filtered maitrd          no-response
998/udp   open|filtered puparp          no-response
999/udp   open|filtered applix          no-response
1022/udp  open|filtered exp2            no-response
1023/udp  open|filtered unknown         no-response
1025/udp  open|filtered blackjack       no-response
1026/udp  open|filtered win-rpc         no-response
1027/udp  open|filtered unknown         no-response
1028/udp  open|filtered ms-lsa          no-response
1029/udp  open|filtered solid-mux       no-response
1030/udp  open|filtered iad1            no-response
1433/udp  open|filtered ms-sql-s        no-response
1434/udp  open|filtered ms-sql-m        no-response
1645/udp  open|filtered radius          no-response
1646/udp  open|filtered radacct         no-response
1701/udp  open|filtered L2TP            no-response
1718/udp  open|filtered h225gatedisc    no-response
1719/udp  open|filtered h323gatestat    no-response
1812/udp  open|filtered radius          no-response
1813/udp  open|filtered radacct         no-response
1900/udp  open|filtered upnp            no-response
2000/udp  open|filtered cisco-sccp      no-response
2048/udp  open|filtered dls-monitor     no-response
2049/udp  open|filtered nfs             no-response
2222/udp  open|filtered msantipiracy    no-response
2223/udp  open|filtered rockwell-csp2   no-response
3283/udp  open|filtered netassistant    no-response
3456/udp  open|filtered IISrpc-or-vat   no-response
3703/udp  open|filtered adobeserver-3   no-response
4444/udp  open|filtered krb524          no-response
4500/udp  closed        nat-t-ike       port-unreach ttl 61
5000/udp  open|filtered upnp            no-response
5060/udp  open|filtered sip             no-response
5353/udp  open|filtered zeroconf        no-response
5632/udp  open|filtered pcanywherestat  no-response
9200/udp  open|filtered wap-wsp         no-response
10000/udp open|filtered ndmp            no-response
17185/udp open|filtered wdbrpc          no-response
20031/udp open|filtered bakbonenetvault no-response
30718/udp open|filtered unknown         no-response
31337/udp open|filtered BackOrifice     no-response
32768/udp open|filtered omad            no-response
32769/udp open|filtered filenet-rpc     no-response
32771/udp open|filtered sometimes-rpc6  no-response
32815/udp open|filtered unknown         no-response
33281/udp open|filtered unknown         no-response
49152/udp open|filtered unknown         no-response
49153/udp open|filtered unknown         no-response
49154/udp open|filtered unknown         no-response
49156/udp open|filtered unknown         no-response
49181/udp open|filtered unknown         no-response
49182/udp open|filtered unknown         no-response
49185/udp open|filtered unknown         no-response
49186/udp open|filtered unknown         no-response
49188/udp open|filtered unknown         no-response
49190/udp open|filtered unknown         no-response
49191/udp open|filtered unknown         no-response
49192/udp open|filtered unknown         no-response
49193/udp closed        unknown         port-unreach ttl 61
49194/udp open|filtered unknown         no-response
49200/udp open|filtered unknown         no-response
49201/udp open|filtered unknown         no-response
65024/udp open|filtered unknown         no-response

Read data files from: /usr/bin/../share/nmap
# Nmap done at Mon Oct 14 10:35:17 2024 -- 1 IP address (1 host up) scanned in 2.42 seconds


```

#### Regular NMAP
```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:34:09 2024 as: nmap -p- -sV -sC -vvv --open -oN nmap TARGET
Nmap scan report for TARGET
Host is up, received echo-reply ttl 61 (0.065s latency).
Scanned at 2024-10-14 10:34:09 EDT for 40s
Not shown: 65486 closed tcp ports (reset), 45 filtered tcp ports (no-response)
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
PORT      STATE SERVICE REASON         VERSION
22/tcp    open  ssh     syn-ack ttl 61 OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 37:80:01:4a:43:86:30:c9:79:e7:fb:7f:3b:a4:1e:dd (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDBCcfKYKMXuTWeyLKlFNHgmebcXbFAjSpbr39R8GFHYRmc/mZXKNgEoa5gkFAVr8kVVul4X6//DcnRuHtrCpHcnTIZLT9g1DPB09VsLzsjT0TpmqkcDYtZazo1mjnBZdaM+AxoDMghZd8AXiNrCl7jCN+vRjUQc8T1wD4PoC02XjeCAI8Yha++Mv9ZrSPZ+/gBvgZPL3pdQhVGUSUHOmXod4xcdm5ReNiZRNZklOhhscbGfSCqQIdJogegZfMrlueeG3EY7Kkf5CxAUDH/9ir2dEDDifIpqKV8W7ncKEpsZiqgDh36OdMX4LPJ0NmZiT/g8CvINx7k4HWj3ksT+5C7
|   256 b6:18:a1:e1:98:fb:6c:c6:87:55:45:10:c6:d4:45:b9 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEK0B9iLJQztyEpGiNffHgQuGcxZRO/BOi+r0j/P8Hkz02pIWW2hFrArbzehUNQ46ZmFwMhxxmrIOLBpUt9ZGBw=
|   256 ab:8f:2d:e8:a2:04:e7:b7:65:d3:fe:5e:93:1e:03:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIOAlO2qlRhyMwzzf3xAK4wOGz1UD5t9+QQO5J3QjTkaZ
80/tcp    open  http    syn-ack ttl 61 Apache httpd 2.4.38 ((Debian))
| http-robots.txt: 1 disallowed entry 
|_/
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
| http-title: SuiteCRM
|_Requested resource was index.php?action=Login&module=Users
|_http-favicon: Unknown favicon MD5: ED9A8C7810E8C9FB7035B6C3147C9A3A
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
3306/tcp  open  mysql   syn-ack ttl 61 MySQL (unauthorized)
33060/tcp open  mysqlx? syn-ack ttl 61
| fingerprint-strings: 
|   DNSStatusRequestTCP, LDAPSearchReq, NotesRPC, SSLSessionReq, TLSSessionReq, X11Probe, afp: 
|     Invalid message"
|     HY000
|   LDAPBindReq: 
|     *Parse error unserializing protobuf message"
|     HY000
|   oracle-tns: 
|     Invalid message-frame."
|_    HY000
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port33060-TCP:V=7.94SVN%I=7%D=10/14%Time=670D2BFD%P=x86_64-pc-linux-gnu
SF:%r(NULL,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(GenericLines,9,"\x05\0\0\0\
SF:x0b\x08\x05\x1a\0")%r(GetRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(HT
SF:TPOptions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(RTSPRequest,9,"\x05\0\0\0
SF:\x0b\x08\x05\x1a\0")%r(RPCCheck,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNS
SF:VersionBindReqTCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNSStatusRequestT
SF:CP,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\
SF:x0fInvalid\x20message\"\x05HY000")%r(Help,9,"\x05\0\0\0\x0b\x08\x05\x1a
SF:\0")%r(SSLSessionReq,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08
SF:\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000")%r(TerminalServerCo
SF:okie,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TLSSessionReq,2B,"\x05\0\0\0\x
SF:0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20messa
SF:ge\"\x05HY000")%r(Kerberos,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(SMBProgN
SF:eg,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(X11Probe,2B,"\x05\0\0\0\x0b\x08\
SF:x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x0
SF:5HY000")%r(FourOhFourRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LPDStr
SF:ing,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LDAPSearchReq,2B,"\x05\0\0\0\x0
SF:b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20messag
SF:e\"\x05HY000")%r(LDAPBindReq,46,"\x05\0\0\0\x0b\x08\x05\x1a\x009\0\0\0\
SF:x01\x08\x01\x10\x88'\x1a\*Parse\x20error\x20unserializing\x20protobuf\x
SF:20message\"\x05HY000")%r(SIPOptions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r
SF:(LANDesk-RC,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TerminalServer,9,"\x05\
SF:0\0\0\x0b\x08\x05\x1a\0")%r(NCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(Not
SF:esRPC,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x
SF:1a\x0fInvalid\x20message\"\x05HY000")%r(JavaRMI,9,"\x05\0\0\0\x0b\x08\x
SF:05\x1a\0")%r(WMSRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(oracle-tns,
SF:32,"\x05\0\0\0\x0b\x08\x05\x1a\0%\0\0\0\x01\x08\x01\x10\x88'\x1a\x16Inv
SF:alid\x20message-frame\.\"\x05HY000")%r(ms-sql-s,9,"\x05\0\0\0\x0b\x08\x
SF:05\x1a\0")%r(afp,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01
SF:\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Oct 14 10:34:49 2024 -- 1 IP address (1 host up) scanned in 39.81 seconds

```

