
```
socat -ddd TCP-LISTEN:2345,fork TCP:TARGET:5432
```

```
socat TCP-LISTEN:2222,fork TCP:TARGET:22
```

