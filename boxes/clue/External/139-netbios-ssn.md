
## NMAP

```
# Nmap 7.94SVN scan initiated Fri Jun 21 13:31:09 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.093s latency).
Scanned at 2024-06-21 13:31:10 EDT for 396s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
Service Info: Host: CLUE
Host script results:
| smb2-security-mode:
|_    Message signing enabled but not required
# Nmap done at Fri Jun 21 13:37:46 2024 -- 1 IP address (1 host up) scanned in 397.50 seconds
```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Fri Jun 21 13:31:09 2024

[34m =========================================( [0m[32mTarget Information[0m[34m )=========================================

[0mTarget ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none

[34m ==========================( [0m[32mEnumerating Workgroup/Domain on TARGET[0m[34m )==========================

[0m[33m
[E] [0m[31mCan't find workgroup/domain

[0m

[34m ==============================( [0m[32mNbtstat Information for TARGET[0m[34m )==============================

[0mLooking up status of TARGET
No reply from TARGET

[34m ==================================( [0m[32mSession Check on TARGET[0m[34m )==================================

[0m[33m
[+] [0m[32mServer TARGET allows sessions using username '', password ''

[0m
[34m ==========================( [0m[32mGetting information via LDAP for TARGET[0m[34m )==========================

[0m[33m
[+] [0m[32m192.168.200.240 appears to be a child DC

[0m
[34m ===============================( [0m[32mGetting domain SID for TARGET[0m[34m )===============================

[0mDomain Name: WORKGROUP
Domain Sid: (NULL SID)
[33m
[+] [0m[32mCan't determine if host is part of domain or part of a workgroup

[0m
[34m =================================( [0m[32mOS information on TARGET[0m[34m )=================================

[0m[33m
[E] [0m[31mCan't get OS info with smbclient

[0m[33m
[+] [0m[32mGot OS info for TARGET from srvinfo:
[0m	CLUE           Wk Sv PrQ Unx NT SNT Samba 4.9.5-Debian
	platform_id     :	500
	os version      :	6.1
	server type     :	0x809a03

[34m ======================================( [0m[32mUsers on TARGET[0m[34m )======================================

[0mUse of uninitialized value $users in print at ./enum4linux.pl line 972.
Use of uninitialized value $users in pattern match (m//) at ./enum4linux.pl line 975.

Use of uninitialized value $users in print at ./enum4linux.pl line 986.
Use of uninitialized value $users in pattern match (m//) at ./enum4linux.pl line 988.

[34m ===============================( [0m[32mMachine Enumeration on TARGET[0m[34m )===============================

[0m[33m
[E] [0m[31mNot implemented in this version of enum4linux.

[0m
[34m ================================( [0m[32mShare Enumeration on TARGET[0m[34m )================================

[0m
	Sharename       Type      Comment
	---------       ----      -------
	print$          Disk      Printer Drivers
	backup          Disk      Backup web directory shares
	IPC$            IPC       IPC Service (Samba 4.9.5-Debian)
Reconnecting with SMB1 for workgroup listing.

	Server               Comment
	---------            -------

	Workgroup            Master
	---------            -------
	WORKGROUP
[33m
[+] [0m[32mAttempting to map shares on TARGET

[0m//TARGET/print$	[35mMapping: [0mDENIED[35m Listing: [0mN/A[35m Writing: [0mN/A
//TARGET/backup	[35mMapping: [0mOK[35m Listing: [0mOK[35m Writing: [0mN/A
[33m
[E] [0m[31mCan't understand response:

[0mNT_STATUS_OBJECT_NAME_NOT_FOUND listing \*
//TARGET/IPC$	[35mMapping: [0mN/A[35m Listing: [0mN/A[35m Writing: [0mN/A

[34m ==========================( [0m[32mPassword Policy Information for TARGET[0m[34m )==========================

[0m

[+] Attaching to TARGET using a NULL share

[+] Trying protocol 139/SMB...

[+] Found domain(s):

	[+] CLUE
	[+] Builtin

[+] Password Info for Domain: CLUE

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

[33m
[+] [0m[32mRetieved partial password policy with rpcclient:

[0mPassword Complexity: Disabled
Minimum Password Length: 5

[34m =====================================( [0m[32mGroups on TARGET[0m[34m )=====================================

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
[I] [0m[36mFound new SID:
[0mS-1-22-1
[33m
[I] [0m[36mFound new SID:
[0mS-1-5-32
[33m
[I] [0m[36mFound new SID:
[0mS-1-5-32
[33m
[I] [0m[36mFound new SID:
[0mS-1-5-32
[33m
[I] [0m[36mFound new SID:
[0mS-1-5-32
[33m
[+] [0m[32mEnumerating users using SID S-1-5-21-371521109-471433649-4134737347 and logon username '', password ''

[0mS-1-5-21-371521109-471433649-4134737347-501 CLUE\nobody (Local User)
	User Name   :	nobody
	Full Name   :	nobody
	Home Drive  :
	Dir Drive   :	(null)
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Wed, 31 Dec 1969 19:00:00 EST
	Logoff Time              :	Wed, 13 Sep 30828 22:48:05 EDT
	Kickoff Time             :	Wed, 13 Sep 30828 22:48:05 EDT
	Password last set Time   :	Wed, 31 Dec 1969 19:00:00 EST
	Password can change Time :	Wed, 31 Dec 1969 19:00:00 EST
	Password must change Time:	Wed, 31 Dec 1969 19:00:00 EST
	unknown_2[0..31]...
	user_rid :	0x1f5
	group_rid:	0x201
	acb_info :	0x00000010
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : False
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

S-1-5-21-371521109-471433649-4134737347-513 CLUE\None (Domain Group)
	Group Name:	None
	Description:	Ordinary Users
	Group Attribute:7
	Num Members:0

[33m
[+] [0m[32mEnumerating users using SID S-1-5-32 and logon username '', password ''

[0mS-1-5-32-544 BUILTIN\Administrators (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-545 BUILTIN\Users (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-546 BUILTIN\Guests (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-547 BUILTIN\Power Users (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-548 BUILTIN\Account Operators (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-549 BUILTIN\Server Operators (Local Group)
[33m
[E] [0m[31mNo info found

[0mS-1-5-32-550 BUILTIN\Print Operators (Local Group)
[33m
[E] [0m[31mNo info found

[0m[33m
[+] [0m[32mEnumerating users using SID S-1-22-1 and logon username '', password ''

[0mS-1-22-1-1000 Unix User\cassie (Local User)
Use of uninitialized value $user_info in pattern match (m//) at ./enum4linux.pl line 1030.

S-1-22-1-1001 Unix User\anthony (Local User)
Use of uninitialized value $user_info in pattern match (m//) at ./enum4linux.pl line 1030.

[34m ==============================( [0m[32mGetting printer info for TARGET[0m[34m )==============================

[0mNo printers returned.

enum4linux complete on Fri Jun 21 13:36:40 2024

```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET

```

## smbclient 

```

	Sharename       Type      Comment
	---------       ----      -------
	print$          Disk      Printer Drivers
	backup          Disk      Backup web directory shares
	IPC$            IPC       IPC Service (Samba 4.9.5-Debian)
Reconnecting with SMB1 for workgroup listing.

	Server               Comment
	---------            -------

	Workgroup            Master
	---------            -------
	WORKGROUP

```

```
smbclient -L \\\\TARGET\\
```

![Pasted image 20240621135422.png](Evidence/Pasted%20image%2020240621135422.png)

![Pasted image 20240621135440.png](Evidence/Pasted%20image%2020240621135440.png)

![Pasted image 20240621135329.png](Evidence/Pasted%20image%2020240621135329.png)

![Pasted image 20240621135508.png](Evidence/Pasted%20image%2020240621135508.png)

![Pasted image 20240621140757.png](Evidence/Pasted%20image%2020240621140757.png)

```
<param name="a1-hash" value="c6440e5de50b403206989679159de89a"/>

```
