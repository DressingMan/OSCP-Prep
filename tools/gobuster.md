
```
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30 > Dir.txt
```

```
gobuster dir -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30 --exclude-length 162
```

```
gobuster dir -u $URL -w /usr/share/SecLists/Discovery/Web-Content/raft-medium-files.txt -k -t 30 > Files.txt
```

**`-b` to exclude status codes** 
-k for https 



**BUST SUB-DOMAINS:**
```
gobuster dns -d someDomain.com -w /opt/SecLists/Discovery/DNS/subdomains-top1million-110000.txt -t 30
```
**--> Make sure any DNS name you find resolves to an in-scope address before you test it.**