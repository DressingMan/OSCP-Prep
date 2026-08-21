## NMAP 

```
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

