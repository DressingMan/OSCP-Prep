
## NMAP

```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:51:47 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.066s latency).
Scanned at 2024-06-29 17:51:48 EDT for 42s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb2-time: ERROR: Script execution failed (use -d to debug)
# Nmap done at Sat Jun 29 17:52:30 2024 -- 1 IP address (1 host up) scanned in 42.96 seconds
```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Sat Jun 29 17:51:47 2024

[34m =========================================( [0m[32mTarget Information[0m[34m )=========================================

[0mTarget ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none

[34m ===========================( [0m[32mEnumerating Workgroup/Domain on TARGET[0m[34m )===========================

[0m[33m
[E] [0m[31mCan't find workgroup/domain

[0m

[34m ===============================( [0m[32mNbtstat Information for TARGET[0m[34m )===============================

[0mLooking up status of TARGET
No reply from TARGET

[34m ==================================( [0m[32mSession Check on TARGET[0m[34m )==================================

[0m[33m
[E] [0m[31mServer doesn't allow session using username '', password ''.  Aborting remainder of tests.

[0m

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET

```

## smbclient 

```
session setup failed: NT_STATUS_ACCESS_DENIED

```

![Pasted image 20240629182114.png](Evidence/Pasted%20image%2020240629182114.png)

