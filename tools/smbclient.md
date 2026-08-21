

```
smbclient \\TARGET\ -N
```

```
smbclient \\\\TARGET\\dev
```

```
smbclient -L \\\\TARGET\\ -N
```

```
smbclient \\\\TARGET\\SYSVOL -U "hutch.offsec\fmcsorley"
recurse on
prompt off
mget *
```

```
smbclient \\\\TARGET\\SYSVOL -U "hutch.offsec\fmcsorley"
```

```
smbclient //TARGET/share -c 'put config.Library-ms
```

```
smbclient -p 4455 -L //TARGET/ -U hr_admin --password=Welcome1234
```

```
smbclient -p 4455 //TARGET/scripts -U hr_admin --password=Welcome1234
```

```
smbclient -L //TARGET/ -U hr_admin --password=Welcome1234
```

```
smbclient \\\\TARGET\\secrets -U Administrator --pw-nt-hash 7a38310ea6f0027ee955abed1762964b
```

