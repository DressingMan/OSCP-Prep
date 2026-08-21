
```
ffuf -u http://TARGET/config/FUZZ -w /usr/share/seclists/SecLists-master/Discovery/Web-Content/quickhits.txt -fw 20
```

```
ffuf -c -w /usr/share/wordlists/seclists/Discovery/Web-Content/raft-medium-directories-lowercase.txt -b "ASP.NET_SessionId=kzvsjecvkfx15ee3fcu33vcy" -u http://TARGET:450/FUZZ
```

