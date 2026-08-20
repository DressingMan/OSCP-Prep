
```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/raft-large-directories.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/raft-large-files.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt --hh 0 "$URL"
```

FUZZ DATA AND CHECK FOR PARAMETERS:
```
export URL="https://example.com/?parameter=FUZZ
```
--> and/or some combination of...
```
export URL="https://example.com/?FUZZ=data
```

```
wfuzz -c -z file,/usr/share/secLists/Discovery/Web-Content/raft-large-words.txt --hc 404 "$URL"
```

```
wfuzz -c -z file,/opt/SecLists/Usernames/top-usernames-shortlist.txt --hc 404,403 "$URL"
```