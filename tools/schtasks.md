
```
schtasks /query /fo LIST /v /TN "[taskname]"
```

```
schtasks /query /fo LIST /v > schtasks.txt
```

```
schtasks /create /ru SYSTEM /sc MINUTE /MO 5 /tn RUNME /tr "\"C:\Tools\sirenMaint.exe\""
```

```
schtasks /RUN /TN "RUNME"
```

```
schtasks /query /fo LIST /v > schtask.txt
```

```
schtasks /query /fo LIST /v
```

```
schtasks /query /fo csv > tasks.csv
```

```
schtasks /query /fo LIST /v | Select-String -Pattern "Administrator" -Context 100
```

```
schtasks /query /fo LIST /v | Select-String -Pattern "" -Context 100
```

