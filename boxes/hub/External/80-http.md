## NMAP 

```
# Nmap 7.94SVN scan initiated Mon Jul  1 17:33:43 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.11s latency).
Scanned at 2024-07-01 17:33:45 EDT for 57s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 nginx 1.18.0
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-headers: 
|   Server: nginx/1.18.0
|   Date: Mon, 01 Jul 2024 21:33:58 GMT
|   Content-Type: text/html
|   Content-Length: 153
|   Connection: close
|   
|_  (Request type: GET)
|_http-feed: Couldn't find any feeds.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-date: Mon, 01 Jul 2024 21:33:54 GMT; -1s from local time.
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 403
|_  	http://TARGET:80/
| http-sitemap-generator: 
|   Directory structure:
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-csrf: Couldn't find any CSRF vulnerabilities.
| http-vhosts: 
|_128 names had status 403
|_http-mobileversion-checker: No mobile version detected.
|_http-title: 403 Forbidden
|_http-malware-host: Host appears to be clean
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_http-chrono: Request times for /; avg: 265.35ms; min: 248.98ms; max: 285.15ms
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
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-comments-displayer: Couldn't find any comments.
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Jul  1 17:34:42 2024 -- 1 IP address (1 host up) scanned in 59.24 seconds

```

## CURL 

```
HTTP/1.1 403 Forbidden
Server: nginx/1.18.0
Date: Mon, 01 Jul 2024 21:33:43 GMT
Content-Type: text/html
Content-Length: 153
Connection: keep-alive

<html>
<head><title>403 Forbidden</title></head>
<body>
<center><h1>403 Forbidden</h1></center>
<hr><center>nginx/1.18.0</center>
</body>
</html>

```

## Dirbuster

Self Enumerate these!

Directories -> 

```
http://TARGET:80/LICENSE.txt          (Status: 200) [Size: 87]
http://TARGET:80/applications         (Status: 403) [Size: 153]
http://TARGET:80/cache                (Status: 403) [Size: 153]
http://TARGET:80/data                 (Status: 403) [Size: 153]
http://TARGET:80/disk                 (Status: 403) [Size: 153]
http://TARGET:80/readme.txt           (Status: 200) [Size: 18730]
http://TARGET:80/themes               (Status: 403) [Size: 153]
http://TARGET:80/trace                (Status: 403) [Size: 153]

```

Files ->

```

```
## Nikto

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-07-01 17:33:47 (GMT-4)
---------------------------------------------------------------------------
+ Server: nginx/1.18.0
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ /readme.txt: This might be interesting.
+ /LICENSE.txt: License file found may identify site software.
+ 7733 requests: 3 error(s) and 4 item(s) reported on remote host
+ End Time:           2024-07-01 17:46:55 (GMT-4) (788 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```

## Whatweb

```
WhatWeb report for http://TARGET:80
Status    : 403 Forbidden
Title     : 403 Forbidden
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : HTTPServer[nginx/1.18.0], nginx[1.18.0]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : nginx/1.18.0 (from server string)

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 403 Forbidden
	Server: nginx/1.18.0
	Date: Mon, 01 Jul 2024 21:33:50 GMT
	Content-Type: text/html
	Transfer-Encoding: chunked
	Connection: close
	Content-Encoding: gzip



```
## Screenshot 

![Pasted image 20240701181726.png](Evidence/Pasted%20image%2020240701181726.png)