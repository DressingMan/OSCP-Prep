
## NMAP

```
# Nmap 7.94SVN scan initiated Fri Jun 21 09:54:46 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.071s latency).
Scanned at 2024-06-21 09:54:48 EDT for 83s

PORT    STATE SERVICE     REASON          VERSION
139/tcp open  netbios-ssn syn-ack ttl 125 Windows Server (R) 2008 Standard 6001 Service Pack 1 netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb-protocols: 
|   dialects: 
|     NT LM 0.12 (SMBv1) [dangerous, but default]
|_    2:0:2
| nbstat: NetBIOS name: HELPDESK, NetBIOS user: <unknown>, NetBIOS MAC: 00:50:56:bf:74:c8 (VMware)
| Names:
|   HELPDESK<00>         Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   HELPDESK<20>         Flags: <unique><active>
| Statistics:
|   00:50:56:bf:74:c8:00:00:00:00:00:00:00:00:00:00:00
|   00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00:00
|_  00:00:00:00:00:00:00:00:00:00:00:00:00:00
| smb-mbenum: 
|_  ERROR: Call to Browser Service failed with status = 2184
| smb2-time: 
|   date: 2024-06-21T13:54:55
|_  start_date: 2024-06-21T13:51:56
|_smb-print-text: false
| smb-enum-shares: 
|   note: ERROR: Enumerating shares failed, guessing at common ones (NT_STATUS_ACCESS_DENIED)
|   account_used: <blank>
|   \\TARGET\ADMIN$: 
|     warning: Couldn't get details for share: NT_STATUS_ACCESS_DENIED
|     Anonymous access: <none>
|   \\TARGET\C$: 
|     warning: Couldn't get details for share: NT_STATUS_ACCESS_DENIED
|     Anonymous access: <none>
|   \\TARGET\IPC$: 
|     warning: Couldn't get details for share: NT_STATUS_ACCESS_DENIED
|     Anonymous access: READ
|   \\TARGET\PUBLIC: 
|     warning: Couldn't get details for share: NT_STATUS_ACCESS_DENIED
|_    Anonymous access: <none>
|_smb-vuln-ms10-061: NT_STATUS_ACCESS_DENIED
| smb2-security-mode: 
|   2:0:2: 
|_    Message signing enabled but not required
| smb-vuln-ms17-010: 
|   VULNERABLE:
|   Remote Code Execution vulnerability in Microsoft SMBv1 servers (ms17-010)
|     State: VULNERABLE
|     IDs:  CVE:CVE-2017-0143
|     Risk factor: HIGH
|       A critical remote code execution vulnerability exists in Microsoft SMBv1
|        servers (ms17-010).
|           
|     Disclosure date: 2017-03-14
|     References:
|       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-0143
|       https://blogs.technet.microsoft.com/msrc/2017/05/12/customer-guidance-for-wannacrypt-attacks/
|_      https://technet.microsoft.com/en-us/library/security/ms17-010.aspx
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb-os-discovery: 
|   OS: Windows Server (R) 2008 Standard 6001 Service Pack 1 (Windows Server (R) 2008 Standard 6.0)
|   OS CPE: cpe:/o:microsoft:windows_server_2008::sp1
|   Computer name: HELPDESK
|   NetBIOS computer name: HELPDESK\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-06-21T06:54:55-07:00
| smb2-capabilities: 
|   2:0:2: 
|_    Distributed File System

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
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

