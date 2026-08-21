## NMAP 

```
# Nmap 7.94SVN scan initiated Fri Jun 21 13:31:09 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.091s latency).
Scanned at 2024-06-21 13:31:10 EDT for 28s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.38
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-chrono: Request times for /; avg: 243.22ms; min: 172.91ms; max: 288.71ms
|_http-server-header: Apache/2.4.38 (Debian)
| http-vhosts: 
|_128 names had status 403
|_http-mobileversion-checker: No mobile version detected.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-title: 403 Forbidden
|_http-date: Fri, 21 Jun 2024 17:46:33 GMT; +15m15s from local time.
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-malware-host: Host appears to be clean
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
| http-grep: 
|   (1) http://TARGET:80/: 
|     (1) ip: 
|_      + TARGET
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 403
|_  	http://TARGET:80/
| http-useragent-tester: 
|   Status for browser useragent: 403
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
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-headers: 
|   Date: Fri, 21 Jun 2024 17:46:42 GMT
|   Server: Apache/2.4.38 (Debian)
|   Content-Length: 280
|   Connection: close
|   Content-Type: text/html; charset=iso-8859-1
|   
|_  (Request type: GET)
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-sitemap-generator: 
|   Directory structure:
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-feed: Couldn't find any feeds.
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-comments-displayer: Couldn't find any comments.
Service Info: Host: 127.0.0.1

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
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