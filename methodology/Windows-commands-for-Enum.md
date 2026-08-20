
```
systeminfo
```

```
hostname
```

```
ipconfig /all
```

```
route print
```

```
netstat -ano
```

```
tasklist /svc
```

```
whoami /priv
```

```
net user
```

```
net localgroup administrators
```

```
net group /domain
```

```
net accounts
```

```
net user
```

```
dir /s
```

```
type
```

```
icacls
```

```
cacls
```

```
sc query
```

```
sc qc 
```

```
sc qprivs
```

```
 reg query HKLM\Software /s
```

```
reg query HKCU /s
```

```
reg query HKLM\SYSTEM\CurrentControlSet\Services /s
```

```
schtasks /query /fo LIST /v
```

```
net view
```

```
net use
```

```
wmic qfe list
```

```
wmic startup
```

```
PowerSploit
```



```
schtasks /query /fo csv > tasks.csv
```

Import the CSV file containing task information
```
$tasks = Import-Csv tasks.csv
```

Filter tasks where "RunAsUser" is SYSTEM or Administrators
```
$elevatedTasks = $tasks | Where-Object { $_.'Run As User' -eq "SYSTEM" -or $_.'Run As User' -eq "Administrators" }
```

Display filtered tasks
```
$elevatedTasks | Format-Table TaskName, NextRunTime, LastRunTime, Status, 'Run As User'
```

```
Get-History
```

```
(Get-PSReadlineOption).HistorySavePath
```


