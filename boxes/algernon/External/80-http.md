## NMAP 

```
# Nmap 7.94SVN scan initiated Mon Jun 24 23:04:21 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.074s latency).
Scanned at 2024-06-24 23:04:23 EDT for 205s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 125 Microsoft IIS httpd 10.0
|_http-malware-host: Host appears to be clean
|_http-feed: Couldn't find any feeds.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-headers: 
|   Content-Length: 696
|   Content-Type: text/html
|   Last-Modified: Thu, 30 Apr 2020 05:29:47 GMT
|   Accept-Ranges: bytes
|   ETag: "c692185db01ed61:0"
|   Server: Microsoft-IIS/10.0
|   X-Powered-By: ASP.NET
|   Date: Tue, 25 Jun 2024 03:04:30 GMT
|   Connection: close
|   
|_  (Request type: HEAD)
|_http-mobileversion-checker: No mobile version detected.
|_http-title: IIS Windows
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
| http-php-version: Logo query returned unknown hash f830d1e83d70eddcf08c5e3704237af0
|_Credits query returned unknown hash f830d1e83d70eddcf08c5e3704237af0
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-errors: Couldn't find any error pages.
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
|_http-date: Tue, 25 Jun 2024 03:04:31 GMT; -1s from local time.
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
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; png: 1
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    Other: 1; png: 1
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-server-header: Microsoft-IIS/10.0
| http-vhosts: 
|_128 names had status 200
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-devframework: ASP.NET detected. Found related header.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-chrono: Request times for /; avg: 231.96ms; min: 219.91ms; max: 258.65ms
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jun 24 23:07:48 2024 -- 1 IP address (1 host up) scanned in 206.96 seconds

```

## CURL 

```bash
HTTP/1.1 200 OK
Content-Type: text/html
Last-Modified: Thu, 30 Apr 2020 05:29:47 GMT
Accept-Ranges: bytes
ETag: "c692185db01ed61:0"
Server: Microsoft-IIS/10.0
X-Powered-By: ASP.NET
Date: Tue, 25 Jun 2024 03:04:20 GMT
Content-Length: 696

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
<title>IIS Windows</title>
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
/aspnet_client        (Status: 301) [Size: 162]
/Aspnet_client        (Status: 301) [Size: 162]
/aspnet_Client        (Status: 301) [Size: 162]
/ASPNET_CLIENT        (Status: 301) [Size: 162]

```

Files ->

```bash
/.                    (Status: 200) [Size: 696]
/iisstart.htm         (Status: 200) [Size: 696]

```
## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-06-24 23:04:24 (GMT-4)
---------------------------------------------------------------------------
+ Server: Microsoft-IIS/10.0
+ /: Retrieved x-powered-by header: ASP.NET.
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /tSsfr9vd.asmx: Retrieved x-aspnet-version header: 4.0.30319.
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ OPTIONS: Allowed HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST .
+ OPTIONS: Public HTTP Methods: OPTIONS, TRACE, GET, HEAD, POST .

```

## Whatweb

```
WhatWeb report for http://TARGET:80
Status    : 200 OK
Title     : IIS Windows
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
	Content-Encoding: gzip
	Last-Modified: Thu, 30 Apr 2020 05:29:47 GMT
	Accept-Ranges: bytes
	ETag: "c692185db01ed61:0"
	Vary: Accept-Encoding
	Server: Microsoft-IIS/10.0
	X-Powered-By: ASP.NET
	Date: Tue, 25 Jun 2024 03:04:26 GMT
	Connection: close
	Content-Length: 603



```
## Screenshot 

![Pasted image 20240624231022.png](Evidence/Pasted%20image%2020240624231022.png)

