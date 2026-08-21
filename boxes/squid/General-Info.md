## Host Info
```bash
TARGET

64-bit

Windows 


```


## SCANS

### NMAP

#### Quick Scan

```bash
# Nmap 7.94SVN scan initiated Wed Jul 24 17:59:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-07-24 17:59:58 EDT for 108s
Not shown: 996 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
135/tcp  open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds? syn-ack ttl 125
3128/tcp open  http-proxy    syn-ack ttl 125 Squid http proxy 4.14
|_http-title: ERROR: The requested URL could not be retrieved
|_http-server-header: squid/4.14
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/24%OT=135%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A179CA%P=x86_64-pc-linux-gnu)
SEQ(SP=107%GCD=1%ISR=10B%TI=I%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T3(R=N)
T4(R=N)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=263 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-time: 
|   date: 2024-07-24T22:01:07
|_  start_date: N/A
|_clock-skew: -1s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 22962/tcp): CLEAN (Timeout)
|   Check 2 (port 19982/tcp): CLEAN (Timeout)
|   Check 3 (port 16942/udp): CLEAN (Timeout)
|   Check 4 (port 39856/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required

TRACEROUTE (using port 135/tcp)
HOP RTT      ADDRESS
1   63.59 ms ATTACKER
2   63.62 ms ATTACKER
3   63.68 ms TARGET
4   63.74 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 18:01:46 2024 -- 1 IP address (1 host up) scanned in 108.04 seconds

```

#### Full Scan
```bash

# Nmap 7.94SVN scan initiated Wed Jul 24 17:59:58 2024 as: nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN /home/kali/... -oX /home/kali/... TARGET
adjust_timeouts2: packet supposedly had rtt of -458292 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -458292 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -888406 microseconds.  Ignoring time.
adjust_timeouts2: packet supposedly had rtt of -888406 microseconds.  Ignoring time.
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-07-24 17:59:58 EDT for 199s
Not shown: 65529 filtered tcp ports (no-response)
PORT      STATE SERVICE       REASON          VERSION
135/tcp   open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 125 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds? syn-ack ttl 125
3128/tcp  open  http-proxy    syn-ack ttl 125 Squid http proxy 4.14
|_http-title: ERROR: The requested URL could not be retrieved
|_http-server-header: squid/4.14
49666/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 125 Microsoft Windows RPC
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
OS fingerprint not ideal because: Missing a closed TCP port so results incomplete
No OS matches for host
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=7/24%OT=135%CT=%CU=%PV=Y%DS=4%DC=T%G=N%TM=66A17A25%P=x86_64-pc-linux-gnu)
SEQ(SP=102%GCD=1%ISR=10C%TS=U)
OPS(O1=M551NW8NNS%O2=M551NW8NNS%O3=M551NW8%O4=M551NW8NNS%O5=M551NW8NNS%O6=M551NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%TG=80%W=FFFF%O=M551NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%TG=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=N)
T2(R=Y%DF=Y%TG=80%W=401%S=O%A=O%F=A%O=%RD=0%Q=)
T3(R=N)
T4(R=N)
T4(R=Y%DF=Y%TG=80%W=FFFF%S=O%A=O%F=AS%O=M551NW8NNS%RD=0%Q=)
U1(R=N)
IE(R=N)

Network Distance: 4 hops
TCP Sequence Prediction: Difficulty=258 (Good luck!)
IP ID Sequence Generation: Busy server or unknown class
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 22962/tcp): CLEAN (Timeout)
|   Check 2 (port 19982/tcp): CLEAN (Timeout)
|   Check 3 (port 16942/udp): CLEAN (Timeout)
|   Check 4 (port 39856/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2024-07-24T22:02:37
|_  start_date: N/A
|_clock-skew: 0s

TRACEROUTE (using port 445/tcp)
HOP RTT      ADDRESS
1   53.48 ms ATTACKER
2   53.47 ms ATTACKER
3   55.94 ms TARGET
4   55.93 ms TARGET

Read data files from: /usr/bin/../share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 18:03:17 2024 -- 1 IP address (1 host up) scanned in 199.02 seconds

```

#### UDP scan
```bash


```

