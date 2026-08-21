## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Jul 15 15:25:29 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.063s latency).
Scanned at 2024-07-15 15:25:31 EDT for 201s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 125 Microsoft IIS httpd 10.0
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-vhosts: 
|_128 names had status 200
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     Python-urllib/2.5
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     HTTP::Lite
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
|_http-errors: Couldn't find any error pages.
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-feed: Couldn't find any feeds.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; png: 1
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    Other: 1; png: 1
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-chrono: Request times for /; avg: 231.01ms; min: 219.59ms; max: 255.04ms
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
| http-php-version: Logo query returned unknown hash 242c23ea412530c7d94b77a7a978c176
|_Credits query returned unknown hash 242c23ea412530c7d94b77a7a978c176
| http-headers: 
|   Content-Length: 703
|   Content-Type: text/html
|   Last-Modified: Wed, 04 Nov 2020 05:35:35 GMT
|   Accept-Ranges: bytes
|   ETag: "965c9516cb2d61:0"
|   Server: Microsoft-IIS/10.0
|   X-Powered-By: ASP.NET
|   Date: Mon, 15 Jul 2024 19:25:41 GMT
|   Connection: close
|   
|_  (Request type: HEAD)
|_http-iis-webdav-vuln: Could not determine vulnerability, since root folder is password protected
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-title: IIS Windows Server
| http-webdav-scan: 
|   Server Type: Microsoft-IIS/10.0
|   Server Date: Mon, 15 Jul 2024 19:25:40 GMT
|   Allowed Methods: OPTIONS, TRACE, GET, HEAD, POST, COPY, PROPFIND, DELETE, MOVE, PROPPATCH, MKCOL, LOCK, UNLOCK
|   Public Options: OPTIONS, TRACE, GET, HEAD, POST, PROPFIND, PROPPATCH, MKCOL, PUT, DELETE, COPY, MOVE, LOCK, UNLOCK
|_  WebDAV type: Unknown
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST COPY PROPFIND DELETE MOVE PROPPATCH MKCOL LOCK UNLOCK PUT
|_  Potentially risky methods: TRACE COPY PROPFIND DELETE MOVE PROPPATCH MKCOL LOCK UNLOCK PUT
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/
|     Line number: 7
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|_        -->
|_http-server-header: Microsoft-IIS/10.0
|_http-malware-host: Host appears to be clean
|_http-mobileversion-checker: No mobile version detected.
|_http-devframework: ASP.NET detected. Found related header.
|_http-date: Mon, 15 Jul 2024 19:25:42 GMT; -1s from local time.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul 15 15:28:52 2024 -- 1 IP address (1 host up) scanned in 203.25 seconds

```

## CURL 

```bash
HTTP/1.1 200 OK
Content-Type: text/html
Last-Modified: Wed, 04 Nov 2020 05:35:35 GMT
Accept-Ranges: bytes
ETag: "965c9516cb2d61:0"
Server: Microsoft-IIS/10.0
X-Powered-By: ASP.NET
Date: Mon, 15 Jul 2024 19:25:29 GMT
Content-Length: 703

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
<title>IIS Windows Server</title>
<style type="text/css">
<!--
body {
	color:#000000;
	background-color:#0072C6;
	margin:0;
}

#container {
	margin-left:auto;
	margin-right:auto;
	text-align:center;
	}

a img {
	border:none;
}

-->
</style>
</head>
<body>
<div id="container">
<a href="http://go.microsoft.com/fwlink/?linkid=66138&amp;clcid=0x409"><img src="iisstart.png" alt="IIS" width="960" height="600" /></a>
</div>
</body>
</html>

```

## Gobuster

Self Enumerate these!

Directories -> 

```bash
/aspnet_client        (Status: 301) [Size: 160] [--> http://TARGET/aspnet_client/]
/Aspnet_client        (Status: 301) [Size: 160] [--> http://TARGET/Aspnet_client/]
/aspnet_Client        (Status: 301) [Size: 160] [--> http://TARGET/aspnet_Client/]
/ASPNET_CLIENT        (Status: 301) [Size: 160] [--> http://TARGET/ASPNET_CLIENT/]

```

Files ->

```bash
/index.aspx           (Status: 500) [Size: 3420]
/Index.aspx           (Status: 500) [Size: 3420]
/iisstart.htm         (Status: 200) [Size: 703]

```
## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-07-15 15:25:32 (GMT-4)
---------------------------------------------------------------------------
+ Server: Microsoft-IIS/10.0
+ /: Retrieved x-powered-by header: ASP.NET.
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /qdrki8Z1.asmx: Retrieved x-aspnet-version header: 4.0.30319.
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ OPTIONS: Allowed HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST, PROPFIND, PROPPATCH, MKCOL, PUT, DELETE, COPY, MOVE, LOCK, UNLOCK .
+ HTTP method ('Allow' Header): 'PUT' method could allow clients to save files on the web server.
+ HTTP method ('Allow' Header): 'DELETE' may allow clients to remove files on the web server.
+ HTTP method ('Allow' Header): 'MOVE' may allow clients to change file locations on the web server.
+ OPTIONS: Public HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST, PROPFIND, PROPPATCH, MKCOL, PUT, DELETE, COPY, MOVE, LOCK, UNLOCK .
+ HTTP method ('Public' Header): 'PUT' method could allow clients to save files on the web server.
+ HTTP method ('Public' Header): 'DELETE' may allow clients to remove files on the web server.
+ HTTP method ('Public' Header): 'MOVE' may allow clients to change file locations on the web server.
+ OPTIONS: WebDAV enabled (UNLOCK PROPFIND COPY MKCOL PROPPATCH LOCK listed as allowed).
+ 7881 requests: 0 error(s) and 13 item(s) reported on remote host
+ End Time:           2024-07-15 15:36:10 (GMT-4) (638 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```

## Whatweb

```bash
WhatWeb report for http://TARGET:80
Status    : 200 OK
Title     : IIS Windows Server
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : HTTPServer[Microsoft-IIS/10.0], Microsoft-IIS[10.0], X-Powered-By[ASP.NET]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : Microsoft-IIS/10.0 (from server string)

[ Microsoft-IIS ]
	Microsoft Internet Information Services (IIS) for Windows
	Server is a flexible, secure and easy-to-manage Web server
	for hosting anything on the Web. From media streaming to
	web application hosting, IIS's scalable and open
	architecture is ready to handle the most demanding tasks.

	Version      : 10.0
	Website     : http://www.iis.net/

[ X-Powered-By ]
	X-Powered-By HTTP header

	String       : ASP.NET (from x-powered-by string)

HTTP Headers:
	HTTP/1.1 200 OK
	Content-Type: text/html
	Last-Modified: Wed, 04 Nov 2020 05:35:35 GMT
	Accept-Ranges: bytes
	ETag: "965c9516cb2d61:0"
	Server: Microsoft-IIS/10.0
	X-Powered-By: ASP.NET
	Date: Mon, 15 Jul 2024 19:25:36 GMT
	Connection: close
	Content-Length: 703



```
## Screenshot 

![Pasted image 20240715172452.png](Evidence/Pasted%20image%2020240715172452.png)