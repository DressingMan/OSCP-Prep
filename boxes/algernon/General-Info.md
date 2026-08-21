## Host Info
```
TARGET

OS: Windows

ASP.NET

```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -718370 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -718370 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -701385 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -701385 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -707915 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -707915 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -714878 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -714878 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-24 23:02:58 EDT for 82s
Not shown: 994 closed tcp ports (reset)
PORT     STATE SERVICE       REASON          VERSION
21/tcp   open  ftp           syn-ack ttl 125 Microsoft ftpd
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| 04-29-20  10:31PM       <DIR>          ImapRetrieval
| 06-24-24  07:58PM       <DIR>          Logs
| 04-29-20  10:31PM       <DIR>          PopRetrieval
|_04-29-20  10:32PM       <DIR>          Spool
| ftp-syst: 
|_  SYST: Windows_NT
80/tcp   open  http          syn-ack ttl 125 Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds? syn-ack ttl 125
9998/tcp open  http          syn-ack ttl 125 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-favicon: Unknown favicon MD5: 9D7294CAAB5C2DF4CD916F53653714D5
| uptime-agent-info: HTTP/1.1 400 Bad Request\x0D
| Content-Type: text/html; charset=us-ascii\x0D
| Server: Microsoft-HTTPAPI/2.0\x0D
| Date: Tue, 25 Jun 2024 03:04:12 GMT\x0D
| Connection: close\x0D
| Content-Length: 326\x0D
| \x0D
| <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">\x0D
| <HTML><HEAD><TITLE>Bad Request</TITLE>\x0D
| <META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>\x0D
| <BODY><h2>Bad Request - Invalid Verb</h2>\x0D
| <hr><p>HTTP Error 400. The request verb is invalid.</p>\x0D
|_</BODY></HTML>\x0D
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-title: Site doesn't have a title (text/html; charset=utf-8).
|_Requested resource was /interface/root
|_http-server-header: Microsoft-IIS/10.0
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows XP (90%)
OS CPE: cpe:/o:microsoft:windows_xp::sp3
Aggressive OS guesses: Microsoft Windows XP SP3 (90%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/24%OT=21%CT=1%CU=30217%PV=Y%DS=11%DC=T%G=Y%TM=667
OS:A33B4%P=x86_64-pc-linux-gnu)SEQ(SP=103%GCD=1%ISR=10C%TS=U)SEQ(SP=104%GCD
OS:=1%ISR=10C%TS=U)SEQ(SP=104%GCD=1%ISR=10C%TI=RD%TS=U)OPS(O1=M551NW8NNS%O2
OS:=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)WIN(W1=FFF
OS:F%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)ECN(R=Y%DF=Y%T=80%W=FFFF%O=M55
OS:1NW8NNS%CC=N%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(
OS:R=N)T5(R=N)T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U
OS:1(R=N)U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=9205%RUD=G
OS:)IE(R=N)

Network Distance: 11 hops
TCP Sequence Prediction: Difficulty=260 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 62479/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 46804/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 37607/udp): CLEAN (Failed to receive data)
|   Check 4 (port 18432/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time: 
|   date: 2024-06-25T03:04:15
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
|_clock-skew: 0s

TRACEROUTE (using port 3306/tcp)
HOP RTT      ADDRESS
1   63.40 ms ATTACKER
2   63.38 ms ATTACKER
3   63.41 ms TARGET
4   ... 10
11  61.21 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 24 23:04:20 2024 -- 1 IP address (1 host up) scanned in 82.90 seconds

```

#### Full Scan
```

# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -452044 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -452044 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -450996 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -450996 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -439732 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -439732 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -453345 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -453345 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -709642 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -709642 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -452348 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -452348 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -864402 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -864402 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-24 23:02:58 EDT for 645s
Not shown: 65521 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
21/tcp    open  ftp           syn-ack ttl 125 Microsoft ftpd
| ftp-syst: 
|_  SYST: Windows_NT
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| 04-29-20  10:31PM       <DIR>          ImapRetrieval
| 06-24-24  07:58PM       <DIR>          Logs
| 04-29-20  10:31PM       <DIR>          PopRetrieval
|_04-29-20  10:32PM       <DIR>          Spool
80/tcp    open  http          syn-ack ttl 125 Microsoft IIS httpd 10.0
|_http-title: IIS Windows
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds? syn-ack ttl 125
5040/tcp  open  unknown       syn-ack ttl 125
9998/tcp  open  http          syn-ack ttl 125 Microsoft IIS httpd 10.0
| uptime-agent-info: HTTP/1.1 400 Bad Request\x0D
| Content-Type: text/html; charset=us-ascii\x0D
| Server: Microsoft-HTTPAPI/2.0\x0D
| Date: Tue, 25 Jun 2024 03:13:27 GMT\x0D
| Connection: close\x0D
| Content-Length: 326\x0D
| \x0D
| <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN""http://www.w3.org/TR/html4/strict.dtd">\x0D
| <HTML><HEAD><TITLE>Bad Request</TITLE>\x0D
| <META HTTP-EQUIV="Content-Type" Content="text/html; charset=us-ascii"></HEAD>\x0D
| <BODY><h2>Bad Request - Invalid Verb</h2>\x0D
| <hr><p>HTTP Error 400. The request verb is invalid.</p>\x0D
|_</BODY></HTML>\x0D
| http-title: Site doesn't have a title (text/html; charset=utf-8).
|_Requested resource was /interface/root
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-favicon: Unknown favicon MD5: 9D7294CAAB5C2DF4CD916F53653714D5
|_http-server-header: Microsoft-IIS/10.0
17001/tcp open  remoting      syn-ack ttl 125 MS .NET Remoting services
49664/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows XP|2008 (86%)
OS CPE: cpe:/o:microsoft:windows_xp::sp3 cpe:/o:microsoft:windows_server_2008
Aggressive OS guesses: Microsoft Windows XP SP3 (86%), Microsoft Windows Server 2008 (85%)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=6/24%OT=21%CT=1%CU=41001%PV=Y%DS=4%DC=T%G=Y%TM=667A
OS:35E7%P=x86_64-pc-linux-gnu)SEQ(SP=FD%GCD=1%ISR=10B%TS=U)SEQ(SP=FD%GCD=1%
OS:ISR=10B%TI=I%TS=U)OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8N
OS:NS%O5=M551NW8NNS%O6=M551NNS)WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%
OS:W6=FF70)ECN(R=Y%DF=Y%T=80%W=FFFF%O=M551NW8NNS%CC=N%Q=)T1(R=Y%DF=Y%T=80%S
OS:=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=N)T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%
OS:F=AR%O=%RD=0%Q=)T6(R=N)T7(R=N)U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G
OS:%RIPCK=G%RUCK=779E%RUD=G)IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=253 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 62479/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 46804/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 37607/udp): CLEAN (Timeout)
|   Check 4 (port 18432/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time: 
|   date: 2024-06-25T03:13:30
|_  start_date: N/A
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
|_clock-skew: 0s

TRACEROUTE (using port 1723/tcp)
HOP RTT      ADDRESS
1   65.85 ms ATTACKER
2   57.56 ms ATTACKER
3   58.58 ms TARGET
4   58.62 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 24 23:13:43 2024 -- 1 IP address (1 host up) scanned in 645.77 seconds

```

#### UDP scan
```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:02:58 2024 as: nmap -vv --reason -Pn -T4 -sU -A --top-ports 100 -oN /home/kali/... -oX /home/kali/... TARGET
Warning: TARGET giving up on port because retransmission cap hit (6).
Increasing send delay for TARGET from 100 to 200 due to 11 out of 12 dropped probes since last increase.
Increasing send delay for TARGET from 200 to 400 due to 11 out of 14 dropped probes since last increase.
Increasing send delay for TARGET from 400 to 800 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for TARGET from 800 to 1000 due to 11 out of 20 dropped probes since last increase.
adjust_timeouts2: packet supposedly had rtt of -71394 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -71394 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.060s latency).
Scanned at 2024-06-24 23:02:58 EDT for 392s
Not shown: 83 closed udp ports (port-unreach)
PORT      STATE         SERVICE     REASON      VERSION
80/udp    open|filtered http        no-response
137/udp   open|filtered netbios-ns  no-response
138/udp   open|filtered netbios-dgm no-response
162/udp   open|filtered snmptrap    no-response
500/udp   open|filtered isakmp      no-response
518/udp   open|filtered ntalk       no-response
998/udp   open|filtered puparp      no-response
1023/udp  open|filtered unknown     no-response
1027/udp  open|filtered unknown     no-response
1028/udp  open|filtered ms-lsa      no-response
1030/udp  open|filtered iad1        no-response
1434/udp  open|filtered ms-sql-m    no-response
1900/udp  open|filtered upnp        no-response
4500/udp  open|filtered nat-t-ike   no-response
5353/udp  open|filtered zeroconf    no-response
49190/udp open|filtered unknown     no-response
49200/udp open|filtered unknown     no-response
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing an open TCP port so results incomplete
Aggressive OS guesses: Linux 2.6.18 (92%), Linux 2.6.30 (92%), Microsoft Windows Server 2008 R2 (91%), Microsoft Windows Server 2008 R2 SP1 (91%), Microsoft Windows Server 2008 SP2 Datacenter Version (91%), Microsoft Windows Server 2012 Data Center (91%), Microsoft Windows Server 2012 R2 (91%), Microsoft Windows Server 2016 (91%), Microsoft Windows 7 (91%), Microsoft Windows 7 SP1 (91%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/24%OT=%CT=%CU=7%PV=Y%DS=4%DC=T%G=N%TM=667A34EA%P=x86_64-pc-linux-gnu)
SEQ()
T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=63D4%RUD=G)
IE(R=N)

Network Distance: 4 hops

TRACEROUTE (using port 1022/udp)
HOP RTT      ADDRESS
1   61.18 ms ATTACKER
2   61.26 ms ATTACKER
3   61.28 ms TARGET
4   61.31 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 24 23:09:30 2024 -- 1 IP address (1 host up) scanned in 392.14 seconds


```

