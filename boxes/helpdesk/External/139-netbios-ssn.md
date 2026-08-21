
## NMAP

```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:54:46 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.071s latency).
Scanned at 2024-06-21 09:54:48 EDT for 83s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Windows Server (R) 2008 Standard 6001 Service Pack 1 netbios-ssn
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 09:56:11 2024 -- 1 IP address (1 host up) scanned in 85.66 seconds
```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Fri Jun 21 09:54:46 2024

[34m =========================================( [0m[32mTarget Information[0m[34m )=========================================

[0mTarget ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none

[34m ===========================( [0m[32mEnumerating Workgroup/Domain on TARGET[0m[34m )===========================

[0m[33m
[+] [0m[32mGot domain/workgroup name: WORKGROUP

[0m
[34m ===============================( [0m[32mNbtstat Information for TARGET[0m[34m )===============================

[0mLooking up status of TARGET
	HELPDESK        <00> -         B <ACTIVE>  Workstation Service
	WORKGROUP       <00> - <GROUP> B <ACTIVE>  Domain/Workgroup Name
	HELPDESK        <20> -         B <ACTIVE>  File Server Service

	MAC Address = 00-50-56-BF-74-C8

[34m ==================================( [0m[32mSession Check on TARGET[0m[34m )==================================

[0m[33m
[+] [0m[32mServer TARGET allows sessions using username '', password ''

[0m
[34m ==========================( [0m[32mGetting information via LDAP for TARGET[0m[34m )==========================

[0m[33m
[+] [0m[32m192.168.200.43 appears to be a child DC

[0m
[34m ===============================( [0m[32mGetting domain SID for TARGET[0m[34m )===============================

[0mdo_cmd: Could not initialise lsarpc. Error was NT_STATUS_ACCESS_DENIED
[33m
[+] [0m[32mCan't determine if host is part of domain or part of a workgroup

[0m
[34m ==================================( [0m[32mOS information on TARGET[0m[34m )==================================

[0m[33m
[E] [0m[31mCan't get OS info with smbclient

[0m[33m
[+] [0m[32mGot OS info for TARGET from srvinfo:
[0mdo_cmd: Could not initialise srvsvc. Error was NT_STATUS_ACCESS_DENIED

[34m ======================================( [0m[32mUsers on TARGET[0m[34m )======================================

[0m[33m
[E] [0m[31mCouldn't find users using querydispinfo: NT_STATUS_ACCESS_DENIED

[0m
[33m
[E] [0m[31mCouldn't find users using enumdomusers: NT_STATUS_ACCESS_DENIED

[0m
[34m ===============================( [0m[32mMachine Enumeration on TARGET[0m[34m )===============================

[0m[33m
[E] [0m[31mNot implemented in this version of enum4linux.

[0m
[34m ================================( [0m[32mShare Enumeration on TARGET[0m[34m )================================

[0mdo_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available
[33m
[+] [0m[32mAttempting to map shares on TARGET

[0m
[34m ===========================( [0m[32mPassword Policy Information for TARGET[0m[34m )===========================

[0m[33m
[E] [0m[31mUnexpected error from polenum:

[0m

[+] Attaching to TARGET using a NULL share

[+] Trying protocol 139/SMB...

	[!] Protocol failed: Cannot request session (Called Name:TARGET)

[+] Trying protocol 445/SMB...

	[!] Protocol failed: SMB SessionError: STATUS_ACCESS_DENIED({Access Denied} A process has requested access to an object but has not been granted those access rights.)

[33m
[E] [0m[31mFailed to get password policy with rpcclient

[0m

[34m ======================================( [0m[32mGroups on TARGET[0m[34m )======================================

[0m[33m
[+] [0m[32mGetting builtin groups:

[0m[33m
[+] [0m[32m Getting builtin group memberships:

[0m[33m
[+] [0m[32m Getting local groups:

[0m[33m
[+] [0m[32m Getting local group memberships:

[0m[33m
[+] [0m[32m Getting domain groups:

[0m[33m
[+] [0m[32m Getting domain group memberships:

[0m
[34m =================( [0m[32mUsers on TARGET via RID cycling (RIDS: 500-550,1000-1050)[0m[34m )=================

[0m[33m
[E] [0m[31mCouldn't get SID: NT_STATUS_ACCESS_DENIED.  RID cycling not possible.

[0m
[34m ==============================( [0m[32mGetting printer info for TARGET[0m[34m )==============================

[0mdo_cmd: Could not initialise spoolss. Error was NT_STATUS_ACCESS_DENIED

enum4linux complete on Fri Jun 21 09:54:59 2024

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET

NetBIOS Name Table for Host TARGET:

Incomplete packet, 155 bytes long.
Name             Service          Type
----------------------------------------
HELPDESK         Workstation Service
WORKGROUP        Domain Name
HELPDESK         File Server Service

Adapter address: 00:50:56:bf:74:c8
----------------------------------------

```

## smbclient 

```
do_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)
Anonymous login successful

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available

```

