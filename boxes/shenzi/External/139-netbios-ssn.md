
## NMAP

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 139 "--script=banner,(nbstat or smb* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.082s latency).
Scanned at 2024-06-26 21:19:55 EDT for 41s
PORT      STATE SERVICE        VERSION
139/tcp open netbios-ssn Microsoft Windows netbios-ssn
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
Host script results:
|_smb2-time: ERROR: Script execution failed (use -d to debug)
|_smb2-security-mode: SMB: Couldn't find a NetBIOS name that works for the server. Sorry!
# Nmap done at Wed Jun 26 21:20:36 2024 -- 1 IP address (1 host up) scanned in 42.78 seconds
```
## enum4linux 

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Wed Jun 26 21:19:54 2024

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
do_connect: Connection to TARGET failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
	IPC$            IPC       Remote IPC
	Shenzi          Disk
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available

```

![Pasted image 20240626214436.png](Evidence/Pasted%20image%2020240626214436.png)

![Pasted image 20240626214452.png](Evidence/Pasted%20image%2020240626214452.png)

![Pasted image 20240626214522.png](Evidence/Pasted%20image%2020240626214522.png)

![Pasted image 20240626214641.png](Evidence/Pasted%20image%2020240626214641.png)

![Pasted image 20240626214742.png](Evidence/Pasted%20image%2020240626214742.png)

versions for this database!!

![Pasted image 20240626214834.png](Evidence/Pasted%20image%2020240626214834.png)

![Pasted image 20240626214940.png](Evidence/Pasted%20image%2020240626214940.png)

![Pasted image 20240626215109.png](Evidence/Pasted%20image%2020240626215109.png)

