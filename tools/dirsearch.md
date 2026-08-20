
```
dirsearch -u http://capiclean.htb/ --exclude-status 403,404,400,401 -o dir
```


Directories
```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-large-directories.txt -x 404 -e html,htm,txt,php
```

```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/common.txt -x 404 -e html,htm,txt,php
```

Files:
```
dirsearch -u $URL -w /usr/share/seclists/Discovery/Web-Content/raft-small-files.txt -x 404
```

