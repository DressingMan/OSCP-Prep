## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 3306 "--script=banner,(mysql* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.068s latency).
Scanned at 2024-06-26 21:19:55 EDT for 9s

PORT     STATE SERVICE REASON          VERSION
3306/tcp open  mysql?  syn-ack ttl 125
| banner: I\x00\x00\x01\xFFj\x04Host 'ATTACKER' is not allowed to c
|_onnect to this MariaDB server
| mysql-info: 
|_  MySQL Error: Host 'ATTACKER' is not allowed to connect to this MariaDB server
|_mysql-empty-password: Host 'ATTACKER' is not allowed to connect to this MariaDB server
| fingerprint-strings: 
|   DNSStatusRequestTCP, GetRequest, HTTPOptions, Help, JavaRMI, NULL, NotesRPC, RPCCheck, RTSPRequest, SIPOptions, SMBProgNeg, TerminalServer, TerminalServerCookie, oracle-tns: 
|_    Host 'ATTACKER' is not allowed to connect to this MariaDB server
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3306-TCP:V=7.94SVN%I=7%D=6/26%Time=667CBE3C%P=x86_64-pc-linux-gnu%r
SF:(NULL,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(GetReq
SF:uest,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20
SF:allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(HTTPOpt
SF:ions,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20
SF:allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(RTSPReq
SF:uest,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20
SF:allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(RPCChec
SF:k,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20all
SF:owed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(DNSStatusR
SF:equestTCP,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20no
SF:t\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(He
SF:lp,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20al
SF:lowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(TerminalS
SF:erverCookie,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20
SF:not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(
SF:SMBProgNeg,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20n
SF:ot\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(S
SF:IPOptions,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20no
SF:t\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(Te
SF:rminalServer,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x2
SF:0not\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r
SF:(NotesRPC,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20no
SF:t\x20allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(Ja
SF:vaRMI,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x2
SF:0allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server")%r(oracle
SF:-tns,4D,"I\0\0\x01\xffj\x04Host\x20'192\.168\.45\.155'\x20is\x20not\x20
SF:allowed\x20to\x20connect\x20to\x20this\x20MariaDB\x20server");

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:20:04 2024 -- 1 IP address (1 host up) scanned in 10.51 seconds

```

