
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

```
gobuster dir -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30
```

```
gobuster dir -u TARGET -w /usr/share/wordlists/dirb/common.txt -t 5
```

```
gobuster dir -u http://TARGET:5002 -w /usr/share/wordlists/dirb/big.txt -p pattern
```

```
gobuster dir -u $URL -w /opt/SecLists/Discovery/Web-Content/raft-medium-directories.txt -k -t 30
```

```
gobuster dir -u $URL -w /opt/SecLists/Discovery/Web-Content/raft-medium-files.txt -k -t 30
```

```
gobuster dns -d domain.org -w /opt/SecLists/Discovery/DNS/subdomains-top1million-110000.txt -t 30
```

```
gobuster dir -u TARGET -w /usr/share/wordlists/dirb/common.txt -x pdf
```

```
gobuster dir -u http://TARGET:5002/users/v1/admin/ -w /usr/share/wordlists/dirb/small.txt
```

```
gobuster dir -u http://TARGET -w /usr/share/wordlists/dirb/common.txt -o mailsrv1/gobuster -x txt,pdf,config
```

