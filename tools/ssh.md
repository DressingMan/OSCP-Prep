
```
ssh offsec@IP
password = password
```

```
ssh offsec@IP
```

```
ssh support@MS01
```

```
ssh administrator@MS01
```

```
ssh user@192.168.XXX.147 -D9090 -R :7777:localhost:7777 -R:8888:localhost:8888
```

```
ssh -i id_ecdsa anita@TARGET -p 2222
```

```
ssh -o StrictHostKeyChecking=no -i id_rsa tom@$IP -p 22 -t "bash --noprofile"
```

```
ssh user@127.0.0.1 "/bin/sh"
```

```
ssh user@127.0.0.1
```

```
ssh fox@$IP
```

```
ssh -i root root@127.0.0.1 -o IdentitiesOnly=yes
```

```
ssh user@$IP
```

```
ssh -i id_rsa root@localhost
```

```
ssh sysadmin@TARGET
```

```
ssh database_admin@TARGET -p2222
```

```
ssh -N -R 9998 kali@TARGET
```

```
ssh database_admin@TARGET -p2222
```

```
ssh -N -R 127.0.0.1:2345:TARGET:5432 kali@TARGET
```

```
ssh -N -L 0.0.0.0:4455:TARGET:445 database_admin@TARGET
```

```
ssh -N -D 0.0.0.0:9999 database_admin@TARGET
```

```
ssh -i id_rsa daniela@TARGET
```

```
ssh -o ProxyCommand='ncat --proxy-type socks5 --proxy 127.0.0.1:1080 %h %p' database_admin@TARGET
```

