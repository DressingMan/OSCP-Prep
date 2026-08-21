## NMAP 

```
```

## CURL 

```
HTTP/1.1 302 Found
Date: Thu, 27 Jun 2024 01:19:53 GMT
Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
X-Powered-By: PHP/7.4.6
Location: https://TARGET/dashboard/
Content-Length: 0
Content-Type: text/html; charset=UTF-8

```

## Gobuster 

```

/img                  (Status: 301) [Size: 340]
/webalizer            (Status: 403) [Size: 1040]
/phpmyadmin           (Status: 403) [Size: 1199]
/dashboard            (Status: 301) [Size: 346]
/examples             (Status: 503) [Size: 1054]
/IMG                  (Status: 301) [Size: 340]
/Img                  (Status: 301) [Size: 340]
/xampp                (Status: 301) [Size: 342]
/licenses             (Status: 403) [Size: 1199]
/server-status        (Status: 403) [Size: 1199]
/Dashboard            (Status: 301) [Size: 346]
/con                  (Status: 403) [Size: 1040]
/Webalizer            (Status: 301) [Size: 346]
/aux                  (Status: 403) [Size: 1040]
/WEBALIZER            (Status: 301) [Size: 346]
/prn                  (Status: 403) [Size: 1040]
/server-info          (Status: 403) [Size: 1199]

```

```
/index.php            (Status: 302) [Size: 0]
/favicon.ico          (Status: 200) [Size: 30894]
/.htaccess            (Status: 403) [Size: 1040]
/.                    (Status: 302) [Size: 0]
/.html                (Status: 403) [Size: 1040]
/.htpasswd            (Status: 403) [Size: 1040]
/.htm                 (Status: 403) [Size: 1040]
/.htpasswds           (Status: 403) [Size: 1040]
/.htgroup             (Status: 403) [Size: 1040]
/Index.php            (Status: 302) [Size: 0]
/.htaccess.bak        (Status: 403) [Size: 1040]
/applications.html    (Status: 200) [Size: 3607]
/.htuser              (Status: 403) [Size: 1040]
/Favicon.ico          (Status: 200) [Size: 30894]
/.ht                  (Status: 403) [Size: 1040]
/.htc                 (Status: 403) [Size: 1040]
/favicon.ICO     
```

## Nikto

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        443
---------------------------------------------------------------------------
+ SSL Info:        Subject:  /CN=localhost
                   Ciphers:  TLS_AES_256_GCM_SHA384
                   Issuer:   /CN=localhost
+ Start Time:         2024-06-26 21:19:57 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
+ /: Retrieved x-powered-by header: PHP/7.4.6.

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
```
## Whatweb
```
```
## Screenshot 
