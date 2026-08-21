## Host Info
```
TARGET



```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -741239 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -741239 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.070s latency).
Scanned at 2024-06-26 21:18:41 EDT for 72s
Not shown: 993 closed tcp ports (reset)
PORT     STATE SERVICE       REASON          VERSION
21/tcp   open  ftp           syn-ack ttl 125 FileZilla ftpd 0.9.41 beta
| ftp-syst: 
|_  SYST: UNIX emulated by FileZilla
80/tcp   open  http          syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
|_http-favicon: Unknown favicon MD5: 56F7C04657931F2D0B79371B2D6E9820
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
| http-title: Welcome to XAMPP
|_Requested resource was http://TARGET/dashboard/
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
443/tcp  open  ssl/http      syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
|_http-favicon: Unknown favicon MD5: 6EB4A43CB64C97F76562AF703893C8FD
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|_ssl-date: TLS randomness does not represent time
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-title: Welcome to XAMPP
|_Requested resource was https://TARGET/dashboard/
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a4:4cc9:9e84:b26f:9e63:9f9e:d229:dee0
| SHA-1: b023:8c54:7a90:5bfa:119c:4e8b:acca:eacf:3649:1ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
|_-----END CERTIFICATE-----
| tls-alpn: 
|_  http/1.1
445/tcp  open  microsoft-ds? syn-ack ttl 125
3306/tcp open  mysql?        syn-ack ttl 125
| mysql-info: 
|_  MySQL Error: Host 'ATTACKER' is not allowed to connect to this MariaDB server
| fingerprint-strings: 
|   DistCCD, NULL, NessusTPv12, afp, giop, kumo-server, ms-sql-s: 
|_    Host 'ATTACKER' is not allowed to connect to this MariaDB server
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3306-TCP:V=7.94SVN%I=9%D=6/26%Time=667CBDF4%P=x86_64-pc-linux-gnu%r
SF:(NULL,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(DistCC
SF:D,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20all
SF:owed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(NessusTPv1
SF:2,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20all
SF:owed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(ms-sql-s,4
SF:D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowe
SF:d\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(afp,4D,"I\0\0
SF:\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20to\
SF:x20connect\x20to\x20this\x20MariaDB\x20server")%r(kumo-server,4D,"I\0\0
SF:\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20to\
SF:x20connect\x20to\x20this\x20MariaDB\x20server")%r(giop,4D,"I\0\0\x01\xf
SF:fj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20to\x20conn
SF:ect\x20to\x20this\x20MariaDB\x20server");
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows XP (90%)
OS CPE: cpe:/o:microsoft:windows_xp::sp3
OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU
Aggressive OS guesses: Microsoft Windows XP SP3 (90%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/26%OT=21%CT=1%CU=%PV=Y%DS=4%DC=T%G=N%TM=667CBE39%P=x86_64-pc-linux-gnu)
SEQ(SP=104%GCD=1%ISR=108%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
T5(R=N)
T5(R=Y%DF=Y%TG=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=N)
T7(R=N)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-06-27T01:19:46
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 31568/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 49606/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 47033/udp): CLEAN (Failed to receive data)
|   Check 4 (port 37350/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
|_clock-skew: -1s

TRACEROUTE (using port 1723/tcp)
HOP RTT      ADDRESS
1   69.19 ms ATTACKER
2   69.09 ms ATTACKER
3   70.74 ms TARGET
4   70.77 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:19:53 2024 -- 1 IP address (1 host up) scanned in 72.47 seconds

```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -696078 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -696078 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -698021 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -698021 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -705564 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -705564 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -443424 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -443424 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -431489 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -431489 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-06-26 21:18:41 EDT for 619s
Not shown: 65520 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
21/tcp    open  ftp           syn-ack ttl 125 FileZilla ftpd 0.9.41 beta
| ftp-syst: 
|_  SYST: UNIX emulated by FileZilla
80/tcp    open  http          syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|_http-favicon: Unknown favicon MD5: 56F7C04657931F2D0B79371B2D6E9820
| http-title: Welcome to XAMPP
|_Requested resource was http://TARGET/dashboard/
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
443/tcp   open  ssl/http      syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a4:4cc9:9e84:b26f:9e63:9f9e:d229:dee0
| SHA-1: b023:8c54:7a90:5bfa:119c:4e8b:acca:eacf:3649:1ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
|_-----END CERTIFICATE-----
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|_http-favicon: Unknown favicon MD5: 6EB4A43CB64C97F76562AF703893C8FD
| tls-alpn: 
|_  http/1.1
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-title: Welcome to XAMPP
|_Requested resource was https://TARGET/dashboard/
|_ssl-date: TLS randomness does not represent time
445/tcp   open  microsoft-ds? syn-ack ttl 125
3306/tcp  open  mysql?        syn-ack ttl 125
| mysql-info: 
|_  MySQL Error: Host 'ATTACKER' is not allowed to connect to this MariaDB server
| fingerprint-strings: 
|   NJE, NULL, NessusTPv10, NoMachine, SSLSessionReq, VersionRequest, erlang-node, giop, hazelcast-http, iperf3, metasploit-msgrpc, niagara-fox, tarantool, tn3270, tor-versions: 
|_    Host 'ATTACKER' is not allowed to connect to this MariaDB server
5040/tcp  open  unknown       syn-ack ttl 125
7680/tcp  open  pando-pub?    syn-ack ttl 125
49664/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3306-TCP:V=7.94SVN%I=9%D=6/26%Time=667CBE30%P=x86_64-pc-linux-gnu%r
SF:(NULL,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(SSLSes
SF:sionReq,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\
SF:x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(Ness
SF:usTPv10,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\
SF:x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(tara
SF:ntool,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(metasp
SF:loit-msgrpc,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20
SF:not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(
SF:hazelcast-http,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\
SF:x20not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")
SF:%r(erlang-node,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\
SF:x20not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")
SF:%r(tor-versions,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is
SF:\x20not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server"
SF:)%r(NJE,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\
SF:x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(tn32
SF:70,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20al
SF:lowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(giop,4D,"
SF:I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x
SF:20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(niagara-fox,4D,"
SF:I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x
SF:20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(iperf3,4D,"I\0\0
SF:\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20to\
SF:x20connect\x20to\x20this\x20MariaDB\x20server")%r(VersionRequest,4D,"I\
SF:0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20
SF:to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(NoMachine,4D,"I\0\
SF:0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20allowed\x20to
SF:\x20connect\x20to\x20this\x20MariaDB\x20server");
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows XP|2008 (87%)
OS CPE: cpe:/o:microsoft:windows_xp::sp3 cpe:/o:microsoft:windows_server_2008
Aggressive OS guesses: Microsoft Windows XP SP3 (87%), Microsoft Windows Server 2008 (85%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/26%OT=21%CT=1%CU=41778%PV=Y%DS=4%DC=T%G=Y%TM=667C
OS:C05C%P=x86_64-pc-linux-gnu)SEQ(SP=103%GCD=1%ISR=10C%TS=U)SEQ(SP=103%GCD=
OS:2%ISR=10C%TS=U)SEQ(SP=104%GCD=1%ISR=10B%TS=U)OPS(O1=M551NW8NNS%O2=M551NW
OS:8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)WIN(W1=FFFF%W2=FF
OS:FF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)ECN(R=N)ECN(R=Y%DF=Y%T=80%W=FFFF%O=M5
OS:51NW8NNS%CC=N%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4
OS:(R=N)T5(R=N)T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)
OS:U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=D190%RUD=G)IE(R=
OS:N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: -1s
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-06-27T01:28:46
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 31568/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 49606/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 47033/udp): CLEAN (Timeout)
|   Check 4 (port 37350/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked

TRACEROUTE (using port 143/tcp)
HOP RTT      ADDRESS
1   67.73 ms ATTACKER
2   67.69 ms ATTACKER
3   68.48 ms TARGET
4   68.56 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:29:00 2024 -- 1 IP address (1 host up) scanned in 619.10 seconds


```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:18:41 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 12 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 12 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 16 dropped probes since last increase.
Increasing send delay for TARGET from 800 to 1000 due to 11 out of 22 dropped probes since last increase.
adjust_timeouts2: packet supposedly had rtt of -386768 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.071s latency).
Scanned at 2024-06-26 21:18:41 EDT for 412s
Not shown: 81 closed udp ports (port-unreach)
PORT      STATE         SERVICE     REASON      VERSION
69/udp    open|filtered tftp        no-response
111/udp   open|filtered rpcbind     no-response
120/udp   open|filtered cfdptkt     no-response
123/udp   open|filtered ntp         no-response
137/udp   open|filtered netbios-ns  no-response
138/udp   open|filtered netbios-dgm no-response
139/udp   open|filtered netbios-ssn no-response
500/udp   open|filtered isakmp      no-response
514/udp   open|filtered syslog      no-response
1813/udp  open|filtered radacct     no-response
1900/udp  open|filtered upnp        no-response
2048/udp  open|filtered dls-monitor no-response
4500/udp  open|filtered nat-t-ike   no-response
5353/udp  open|filtered zeroconf    no-response
9200/udp  open|filtered wap-wsp     no-response
49154/udp open|filtered unknown     no-response
49181/udp open|filtered unknown     no-response
49190/udp open|filtered unknown     no-response
49200/udp open|filtered unknown     no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing an open TCP port so results incomplete
Aggressive OS guesses: Linux 2.6.18 (92%), Linux 2.6.30 (92%), Microsoft Windows Server 2008 R2 (91%), Microsoft Windows Server 2008 R2 SP1 (91%), Microsoft Windows Server 2008 SP2 Datacenter Version (91%), Microsoft Windows Server 2012 Data Center (91%), Microsoft Windows Server 2012 R2 (91%), Microsoft Windows Server 2016 (91%), Microsoft Windows 7 (91%), Microsoft Windows 7 SP1 (91%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/26%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=667CBF8D%P=x86_64-pc-linux-gnu)
SEQ()
T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=43CF%RUD=G)
IE(R=N)

Network Distance: 4 hops

TRACEROUTE (using port 5060/udp)
HOP RTT      ADDRESS
1   87.12 ms ATTACKER
2   87.08 ms ATTACKER
3   87.47 ms TARGET
4   70.82 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:25:33 2024 -- 1 IP address (1 host up) scanned in 412.29 seconds


```

