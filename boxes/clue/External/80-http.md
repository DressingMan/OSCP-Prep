## NMAP 

```
Nmap scan report for TARGET
Host is up, received user-set (0.091s latency).
Scanned at 2024-06-21 13:31:10 EDT for 28s
PORT      STATE SERVICE        VERSION
80/tcp open http Apache httpd 2.4.38
|_http-title: 403 Forbidden
Service Info: Host: 127.0.0.1
# Nmap done at Fri Jun 21 13:31:38 2024 -- 1 IP address (1 host up) scanned in 29.23 seconds
```

## CURL 

```
HTTP/1.1 403 Forbidden
Date: Fri, 21 Jun 2024 17:46:24 GMT
Server: Apache/2.4.38 (Debian)
Content-Length: 280
Content-Type: text/html; charset=iso-8859-1

<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>403 Forbidden</title>
</head><body>
<h1>Forbidden</h1>
<p>You don't have permission to access this resource.</p>
<hr>
<address>Apache/2.4.38 (Debian) Server at TARGET Port 80</address>
</body></html>

```

## Gobuster 

Self Enumerate these!

Directories -> 

```
/backup               (Status: 301) [Size: 319]
/server-status        (Status: 403) [Size: 280]

```

Files ->

```
/.htaccess            (Status: 403) [Size: 280]
/.                    (Status: 403) [Size: 280]
/.html                (Status: 403) [Size: 280]
/.php                 (Status: 403) [Size: 280]
/.htpasswd            (Status: 403) [Size: 280]
/.htm                 (Status: 403) [Size: 280]
/.htpasswds           (Status: 403) [Size: 280]
/.htgroup             (Status: 403) [Size: 280]
/wp-forum.phps        (Status: 403) [Size: 280]
/.htaccess.bak        (Status: 403) [Size: 280]
/.htuser              (Status: 403) [Size: 280]
/.ht                  (Status: 403) [Size: 280]
/.htc                 (Status: 403) [Size: 280]

```
## Nikto

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-06-21 13:31:14 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.38 (Debian)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.38 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ OPTIONS: Allowed HTTP Methods: GET, POST, OPTIONS, HEAD .
+ /icons/README: Apache default file found. See: https://www.vntweb.co.uk/apache-restricting-access-to-iconsreadme/

```

## Whatweb

```
WhatWeb report for http://TARGET:80
Status    : 403 Forbidden
Title     : 403 Forbidden
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.38], HTTPServer[Debian Linux][Apache/2.4.38 (Debian)]

Detected Plugins:
[ Apache ]
	The Apache HTTP Server Project is an effort to develop and
	maintain an open-source HTTP server for modern operating
	systems including UNIX and Windows NT. The goal of this
	project is to provide a secure, efficient and extensible
	server that provides HTTP services in sync with the current
	HTTP standards.

	Version      : 2.4.38 (from HTTP Server Header)
	Google Dorks: (3)
	Website     : http://httpd.apache.org/

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Debian Linux
	String       : Apache/2.4.38 (Debian) (from server string)

HTTP Headers:
	HTTP/1.1 403 Forbidden
	Date: Fri, 21 Jun 2024 17:46:30 GMT
	Server: Apache/2.4.38 (Debian)
	Content-Length: 280
	Connection: close
	Content-Type: text/html; charset=iso-8859-1

```
## Screenshot 

![Pasted image 20240621133558.png](Evidence/Pasted%20image%2020240621133558.png)
