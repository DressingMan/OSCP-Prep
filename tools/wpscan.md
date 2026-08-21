
```
wpscan --url $URL --disable-tls-checks --enumerate p --enumerate t --enumerate u
```

```
wpscan --url $URL --disable-tls-checks -U users -P /usr/share/wordlists/rockyou.txt
```

```
wpscan --url $URL --enumerate p --plugins-detection aggressive
```

```
WPScan Brute Forceing:
```

```
wpscan --url http://TARGET --enumerate p --plugins-detection aggressive -o websrv1/wpscan
```

