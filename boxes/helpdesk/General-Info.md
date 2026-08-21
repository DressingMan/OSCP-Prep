## Host Info
```
CVE-2011-0966
CVE-2017-0143
CVE-2003-0104
CVE-2001-0926

TARGET

OS: Windows
```


## SCANS

### NMAP

#### Quick Scan

```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:53:37 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.065s latency).
Scanned at 2024-06-21 09:53:37 EDT for 68s
Not shown: 995 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds  syn-ack ttl 125 Windows Server (R) 2008 Standard 6001 Service Pack 1 microsoft-ds (workgroup: WORKGROUP)
3389/tcp open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Service
8080/tcp open  http          syn-ack ttl 125 Apache Tomcat/Coyote JSP engine 1.1
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache-Coyote/1.1
|_http-title: ManageEngine ServiceDesk Plus
| http-cookie-flags: 
|   /: 
|     JSESSIONID: 
|_      httponly flag not set
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 2008 (87%)
OS CPE: cpe:/o:microsoft:windows_server_2008:r2:sp1 cpe:/o:microsoft:windows_8
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows Server 2008 R2 SP1 (87%), Microsoft Windows Server 2008 R2 or Windows 8 (85%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/21%OT=135%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66758625%P=x86_64-pc-linux-gnu)
SEQ(SP=FB%GCD=1%ISR=FD%TI=I%TS=7)
OPS(O1=M551NW8ST11%O2=M551NW8ST11%O3=M551NW8NNT11%O4=M551NW8ST11%O5=M551NW8ST11%O6=M551ST11)
WIN(W1=2000%W2=2000%W3=2000%W4=2000%W5=2000%W6=2000)
ECN(R=Y%DF=Y%TG=80%W=2000%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Uptime guess: 0.002 days (since Fri Jun 21 09:51:49 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=251 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: Host: HELPDESK; OS: Windows; CPE: cpe:/o:microsoft:windows, cpe:/o:microsoft:windows_server_2008:r2

Host script results:
| smb2-security-mode: 
|   2:0:2: 
|_    Message signing enabled but not required
|_clock-skew: mean: 2h19m59s, deviation: 4h02m29s, median: 0s
| smb2-time: 
|   date: 2024-06-21T13:54:05
|_  start_date: 2024-06-21T13:51:56
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 22576/tcp): CLEAN (Timeout)
|   Check 2 (port 44492/tcp): CLEAN (Timeout)
|   Check 3 (port 54275/udp): CLEAN (Timeout)
|   Check 4 (port 4779/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| nbstat: NetBIOS name: HELPDESK, NetBIOS user: <unknown>, NetBIOS MAC: 00:50:56:bf:74:c8 (VMware)
| Names:
|   HELPDESK<00>         Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   HELPDESK<20>         Flags: <unique><active>
| Statistics:
|   00:50:56:bf:74:c8:00:00:00:00:00:00:00:00:00:00:00
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_  00:00:00:00:00:00:00:00:00:00:00:00:00:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb-os-discovery: 
|   OS: Windows Server (R) 2008 Standard 6001 Service Pack 1 (Windows Server (R) 2008 Standard 6.0)
|   OS CPE: cpe:/o:microsoft:windows_server_2008::sp1
|   Computer name: HELPDESK
|   NetBIOS computer name: HELPDESK\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-06-21T06:54:05-07:00

TRACEROUTE (using port 445/tcp)
HOP RTT      ADDRESS
1   64.51 ms ATTACKER
2   62.48 ms ATTACKER
3   64.56 ms TARGET
4   70.39 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jun 21 09:54:45 2024 -- 1 IP address (1 host up) scanned in 68.75 seconds

```

#### Full Scan
```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:53:37 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -205508 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -205508 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -222319 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -222319 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-21 09:53:37 EDT for 148s
Not shown: 65530 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds  syn-ack ttl 125 Windows Server (R) 2008 Standard 6001 Service Pack 1 microsoft-ds (workgroup: WORKGROUP)
3389/tcp open  ms-wbt-server syn-ack ttl 125 Microsoft Terminal Service
8080/tcp open  http          syn-ack ttl 125 Apache Tomcat/Coyote JSP engine 1.1
|_http-title: ManageEngine ServiceDesk Plus
| http-cookie-flags: 
|   /: 
|     JSESSIONID: 
|_      httponly flag not set
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache-Coyote/1.1
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running (JUST GUESSING): Microsoft Windows 2008|7|8.1 (87%)
OS CPE: cpe:/o:microsoft:windows_server_2008:r2:sp1 cpe:/o:microsoft:windows_8 cpe:/o:microsoft:windows_7::sp1 cpe:/o:microsoft:windows_8.1:r1
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
Aggressive OS guesses: Microsoft Windows Server 2008 R2 SP1 (87%), Microsoft Windows Server 2008 (86%), Microsoft Windows Server 2008 R2 (86%), Microsoft Windows Server 2008 R2 or Windows 8 (86%), Microsoft Windows 7 SP1 (86%), Microsoft Windows 8.1 R1 (86%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=6/21%OT=135%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66758675%P=x86_64-pc-linux-gnu)
SEQ(SP=101%GCD=1%ISR=10F%TS=7)
OPS(O1=M551NW8ST11%O2=M551NW8ST11%O3=M551NW8NNT11%O4=M551NW8ST11%O5=M551NW8ST11%O6=M551ST11)
WIN(W1=2000%W2=2000%W3=2000%W4=2000%W5=2000%W6=2000)
ECN(R=Y%DF=Y%TG=80%W=2000%O=M551NW8NNS%CC=N%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Uptime guess: 0.003 days (since Fri Jun 21 09:51:49 2024)
Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=257 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: Host: HELPDESK; OS: Windows; CPE: cpe:/o:microsoft:windows, cpe:/o:microsoft:windows_server_2008:r2

Host script results:
| smb2-security-mode: 
|   2:0:2: 
|_    Message signing enabled but not required
|_clock-skew: mean: 2h19m59s, deviation: 4h02m29s, median: -1s
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-time: 
|   date: 2024-06-21T13:55:24
|_  start_date: 2024-06-21T13:51:56
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 22576/tcp): CLEAN (Timeout)
|   Check 2 (port 44492/tcp): CLEAN (Timeout)
|   Check 3 (port 54275/udp): CLEAN (Timeout)
|   Check 4 (port 4779/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| nbstat: NetBIOS name: HELPDESK, NetBIOS user: <unknown>, NetBIOS MAC: 00:50:56:bf:74:c8 (VMware)
| Names:
|   HELPDESK<00>         Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   HELPDESK<20>         Flags: <unique><active>
| Statistics:
|   00:50:56:bf:74:c8:00:00:00:00:00:00:00:00:00:00:00
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_  00:00:00:00:00:00:00:00:00:00:00:00:00:00
| smb-os-discovery: 
|   OS: Windows Server (R) 2008 Standard 6001 Service Pack 1 (Windows Server (R) 2008 Standard 6.0)
|   OS CPE: cpe:/o:microsoft:windows_server_2008::sp1
|   Computer name: HELPDESK
|   NetBIOS computer name: HELPDESK\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-06-21T06:55:24-07:00

TRACEROUTE (using port 3389/tcp)
HOP RTT      ADDRESS
1   61.66 ms ATTACKER
2   61.46 ms ATTACKER
3   61.77 ms TARGET
4   61.92 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Jun 21 09:56:05 2024 -- 1 IP address (1 host up) scanned in 148.46 seconds


```

#### UDP scan
```


```

