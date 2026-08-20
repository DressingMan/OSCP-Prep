
## NMAP

```bash
# Nmap 7.94SVN scan initiated Thu Oct 17 16:42:24 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-10-17 16:42:24 EDT for 351s

PORT    STATE SERVICE     REASON         VERSION
139/tcp open  netbios-ssn syn-ack ttl 61 Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
Service Info: Host: PELICAN

Host script results:
| smb-mbenum: 
|   DFS Root
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Potential Browser
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Print server
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Server
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Server service
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Unix server
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Windows NT/2000/XP/2003 server
|     PELICAN  0.0  Samba 4.9.5-Debian
|   Workstation
|_    PELICAN  0.0  Samba 4.9.5-Debian
| smb-enum-sessions: 
|_  <nobody>
| smb2-capabilities: 
|   2:0:2: 
|     Distributed File System
|   2:1:0: 
|     Distributed File System
|     Leasing
|   3:0:0: 
|     Distributed File System
|     Leasing
|   3:0:2: 
|     Distributed File System
|     Leasing
|   3:1:1: 
|     Distributed File System
|_    Leasing
|_smb-vuln-ms10-061: false
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
|_smb-print-text: false
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.9.5-Debian)
|   Computer name: pelican
|   NetBIOS computer name: PELICAN\x00
|   Domain name: \x00
|   FQDN: pelican
|_  System time: 2024-10-17T16:42:51-04:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_smb-system-info: ERROR: Script execution failed (use -d to debug)
| smb-enum-shares: 
|   account_used: guest
|   \\TARGET\IPC$: 
|     Type: STYPE_IPC_HIDDEN
|     Comment: IPC Service (Samba 4.9.5-Debian)
|     Users: 3
|     Max Users: <unlimited>
|     Path: C:\tmp
|     Anonymous access: READ/WRITE
|     Current user access: READ/WRITE
|   \\TARGET\print$: 
|     Type: STYPE_DISKTREE
|     Comment: Printer Drivers
|     Users: 0
|     Max Users: <unlimited>
|     Path: C:\var\lib\samba\printers
|     Anonymous access: <none>
|_    Current user access: <none>
| smb2-time: 
|   date: 2024-10-17T20:42:54
|_  start_date: N/A
| smb-enum-domains: 
|   Builtin
|     Groups: n/a
|     Users: n/a
|     Creation time: unknown
|     Passwords: min length: 5; min age: n/a days; max age: n/a days; history: n/a passwords
|     Account lockout disabled
|   PELICAN
|     Groups: n/a
|     Users: n/a
|     Creation time: unknown
|     Passwords: min length: 5; min age: n/a days; max age: n/a days; history: n/a passwords
|_    Account lockout disabled
| smb-protocols: 
|   dialects: 
|     NT LM 0.12 (SMBv1) [dangerous, but default]
|     2:0:2
|     2:1:0
|     3:0:0
|     3:0:2
|_    3:1:1

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Oct 17 16:48:15 2024 -- 1 IP address (1 host up) scanned in 350.54 seconds

```
## Enum4linux 

```bash
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Thu Oct 17 17:01:28 2024

 =========================================( Target Information )=========================================

Target ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none


 ===========================( Enumerating Workgroup/Domain on TARGET )===========================


[E] Can't find workgroup/domain



 ===============================( Nbtstat Information for TARGET )===============================

Looking up status of TARGET
No reply from TARGET

 ==================================( Session Check on TARGET )==================================


[+] Server TARGET allows sessions using username '', password ''


 ===============================( Getting domain SID for TARGET )===============================

Domain Name: WORKGROUP
Domain Sid: (NULL SID)

[+] Can't determine if host is part of domain or part of a workgroup


 ==================================( OS information on TARGET )==================================


[E] Can't get OS info with smbclient


[+] Got OS info for TARGET from srvinfo: 
	PELICAN        Wk Sv PrQ Unx NT SNT Samba 4.9.5-Debian
	platform_id     :	500
	os version      :	6.1
	server type     :	0x809a03


 ======================================( Users on TARGET )======================================



 ================================( Share Enumeration on TARGET )================================


	Sharename       Type      Comment
	---------       ----      -------
	print$          Disk      Printer Drivers
	IPC$            IPC       IPC Service (Samba 4.9.5-Debian)
Reconnecting with SMB1 for workgroup listing.

	Server               Comment
	---------            -------

	Workgroup            Master
	---------            -------
	WORKGROUP            

[+] Attempting to map shares on TARGET

//TARGET/print$	Mapping: DENIED Listing: N/A Writing: N/A

[E] Can't understand response:

NT_STATUS_OBJECT_NAME_NOT_FOUND listing \*
//TARGET/IPC$	Mapping: N/A Listing: N/A Writing: N/A

 ===========================( Password Policy Information for TARGET )===========================



[+] Attaching to TARGET using a NULL share

[+] Trying protocol 139/SMB...

[+] Found domain(s):

	[+] PELICAN
	[+] Builtin

[+] Password Info for Domain: PELICAN

	[+] Minimum password length: 5
	[+] Password history length: None
	[+] Maximum password age: 37 days 6 hours 21 minutes 
	[+] Password Complexity Flags: 000000

		[+] Domain Refuse Password Change: 0
		[+] Domain Password Store Cleartext: 0
		[+] Domain Password Lockout Admins: 0
		[+] Domain Password No Clear Change: 0
		[+] Domain Password No Anon Change: 0
		[+] Domain Password Complex: 0

	[+] Minimum password age: None
	[+] Reset Account Lockout Counter: 30 minutes 
	[+] Locked Account Duration: 30 minutes 
	[+] Account Lockout Threshold: None
	[+] Forced Log off Time: 37 days 6 hours 21 minutes 



[+] Retieved partial password policy with rpcclient:


Password Complexity: Disabled
Minimum Password Length: 5


 ======================================( Groups on TARGET )======================================


[+] Getting builtin groups:


[+]  Getting builtin group memberships:


[+]  Getting local groups:


[+]  Getting local group memberships:


[+]  Getting domain groups:


[+]  Getting domain group memberships:


 =================( Users on TARGET via RID cycling (RIDS: 500-550,1000-1050) )=================


[I] Found new SID: 
S-1-22-1

[I] Found new SID: 
S-1-5-32

[I] Found new SID: 
S-1-5-32

[I] Found new SID: 
S-1-5-32

[I] Found new SID: 
S-1-5-32

[+] Enumerating users using SID S-1-22-1 and logon username '', password ''

S-1-22-1-1000 Unix User\charles (Local User)

[+] Enumerating users using SID S-1-5-21-3775993406-1587906097-1752599619 and logon username '', password ''

S-1-5-21-3775993406-1587906097-1752599619-501 PELICAN\nobody (Local User)
S-1-5-21-3775993406-1587906097-1752599619-513 PELICAN\None (Domain Group)

[+] Enumerating users using SID S-1-5-32 and logon username '', password ''

S-1-5-32-544 BUILTIN\Administrators (Local Group)
S-1-5-32-545 BUILTIN\Users (Local Group)
S-1-5-32-546 BUILTIN\Guests (Local Group)
S-1-5-32-547 BUILTIN\Power Users (Local Group)
S-1-5-32-548 BUILTIN\Account Operators (Local Group)
S-1-5-32-549 BUILTIN\Server Operators (Local Group)
S-1-5-32-550 BUILTIN\Print Operators (Local Group)

 ==============================( Getting printer info for TARGET )==============================

No printers returned.


enum4linux complete on Thu Oct 17 17:06:21 2024


```
## Enum4linux-ng

```bash
ENUM4LINUX - next generation (v1.3.3)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... TARGET
[*] Username ......... ''
[*] Random Username .. 'jubhxgfe'
[*] Password ......... ''
[*] Timeout .......... 5 second(s)

 =======================================
|    Listener Scan on TARGET    |
 =======================================
[*] Checking LDAP
[-] Could not connect to LDAP on 389/tcp: connection refused
[*] Checking LDAPS
[-] Could not connect to LDAPS on 636/tcp: connection refused
[*] Checking SMB
[+] SMB is accessible on 445/tcp
[*] Checking SMB over NetBIOS
[+] SMB over NetBIOS is accessible on 139/tcp

 =============================================================
|    NetBIOS Names and Workgroup/Domain for TARGET    |
 =============================================================
[V] Trying to get NetBIOS names information, running command: nmblookup -s /tmp/tmpdfqmpnet -A TARGET
[-] Could not get NetBIOS names information via 'nmblookup': timed out

 ===========================================
|    SMB Dialect Check on TARGET    |
 ===========================================
[*] Trying on 445/tcp
[+] Supported dialects and settings:
Supported dialects:
  SMB 1.0: true
  SMB 2.02: true
  SMB 2.1: true
  SMB 3.0: true
  SMB 3.1.1: true
Preferred dialect: SMB 3.0
SMB1 only: false
SMB signing required: false

 =============================================================
|    Domain Information via SMB session for TARGET    |
 =============================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found domain information via SMB
NetBIOS computer name: PELICAN
NetBIOS domain name: ''
DNS domain: ''
FQDN: pelican
Derived membership: workgroup member
Derived domain: unknown

 ===========================================
|    RPC Session Check on TARGET    |
 ===========================================
[*] Check for null session
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -t 5 -c help '//TARGET/ipc$'
[+] Server allows session using username '', password ''
[*] Check for random user
[V] Attempting to make session, running command: smbclient -W WORKGROUP -U jubhxgfe% -s /tmp/tmpdfqmpnet -t 5 -c help '//TARGET/ipc$'
[+] Server allows session using username 'jubhxgfe', password ''
[H] Rerunning enumeration with user 'jubhxgfe' might give more results

 =====================================================
|    Domain Information via RPC for TARGET    |
 =====================================================
[V] Attempting to get domain SID, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c lsaquery TARGET
[+] Domain: WORKGROUP
[+] Domain SID: NULL SID
[+] Membership: workgroup member

 =================================================
|    OS Information via RPC for TARGET    |
 =================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found OS information via SMB
[*] Enumerating via 'srvinfo'
[V] Attempting to get OS info with command, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c srvinfo TARGET
[+] Found OS information via 'srvinfo'
[+] After merging OS information we have the following result:
OS: Linux/Unix (Samba 4.9.5-Debian)
OS version: '6.1'
OS release: ''
OS build: '0'
Native OS: Windows 6.1
Native LAN manager: Samba 4.9.5-Debian
Platform id: '500'
Server type: '0x809a03'
Server type string: Wk Sv PrQ Unx NT SNT Samba 4.9.5-Debian

 =======================================
|    Users via RPC on TARGET    |
 =======================================
[*] Enumerating users via 'querydispinfo'
[V] Attempting to get userlist, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c querydispinfo TARGET
[+] Found 0 user(s) via 'querydispinfo'
[*] Enumerating users via 'enumdomusers'
[V] Attempting to get userlist, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c enumdomusers TARGET
[+] Found 0 user(s) via 'enumdomusers'

 ========================================
|    Groups via RPC on TARGET    |
 ========================================
[*] Enumerating local groups
[V] Attempting to get local groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c 'enumalsgroups domain' TARGET
[+] Found 0 group(s) via 'enumalsgroups domain'
[*] Enumerating builtin groups
[V] Attempting to get builtin groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c 'enumalsgroups builtin' TARGET
[+] Found 0 group(s) via 'enumalsgroups builtin'
[*] Enumerating domain groups
[V] Attempting to get domain groups, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c enumdomgroups TARGET
[+] Found 0 group(s) via 'enumdomgroups'

 ========================================
|    Shares via RPC on TARGET    |
 ========================================
[V] Attempting to get share list using authentication, running command: smbclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -t 5 -L //TARGET -g
[*] Enumerating shares
[+] Found 2 share(s):
IPC$:
  comment: IPC Service (Samba 4.9.5-Debian)
  type: IPC
print$:
  comment: Printer Drivers
  type: Disk
[*] Testing share IPC$
[V] Attempting to map share //TARGET/IPC$, running command: smbclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -t 5 -c dir '//TARGET/IPC$'
[-] Could not check share: STATUS_OBJECT_NAME_NOT_FOUND
[*] Testing share print$
[V] Attempting to map share //TARGET/print$, running command: smbclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -t 5 -c dir '//TARGET/print$'
[+] Mapping: DENIED, Listing: N/A

 ===========================================
|    Policies via RPC for TARGET    |
 ===========================================
[*] Trying port 445/tcp
[+] Found policy:
Domain password information:
  Password history length: None
  Minimum password length: 5
  Maximum password age: 49710 days 6 hours 21 minutes
  Password properties:
  - DOMAIN_PASSWORD_COMPLEX: false
  - DOMAIN_PASSWORD_NO_ANON_CHANGE: false
  - DOMAIN_PASSWORD_NO_CLEAR_CHANGE: false
  - DOMAIN_PASSWORD_LOCKOUT_ADMINS: false
  - DOMAIN_PASSWORD_PASSWORD_STORE_CLEARTEXT: false
  - DOMAIN_PASSWORD_REFUSE_PASSWORD_CHANGE: false
Domain lockout information:
  Lockout observation window: 30 minutes
  Lockout duration: 30 minutes
  Lockout threshold: None
Domain logoff information:
  Force logoff time: 49710 days 6 hours 21 minutes

 ===========================================
|    Printers via RPC for TARGET    |
 ===========================================
[V] Attempting to get printer info, running command: rpcclient -W WORKGROUP -U % -s /tmp/tmpdfqmpnet -c enumprinters TARGET
[+] No printers returned (this is not an error)

Completed after 18.60 seconds


```
## nbtscan 

```bash
Doing NBT name scan for addresses from TARGET



```

## smbclient 

```bash

	Sharename       Type      Comment
	---------       ----      -------
	print$          Disk      Printer Drivers
	IPC$            IPC       IPC Service (Samba 4.9.5-Debian)
Reconnecting with SMB1 for workgroup listing.

	Server               Comment
	---------            -------

	Workgroup            Master
	---------            -------
	WORKGROUP


```

