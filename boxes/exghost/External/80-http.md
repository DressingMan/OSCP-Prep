## NMAP 

```bash
# Nmap 7.94SVN scan initiated Wed Oct  9 20:56:41 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.069s latency).
Scanned at 2024-10-09 20:56:42 EDT for 26s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 403
|_  	http://TARGET:80/
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-vhosts: 
|_128 names had status 403
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-server-header: Apache/2.4.41 (Ubuntu)
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
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-date: Thu, 10 Oct 2024 00:56:53 GMT; -1s from local time.
|_http-title: 403 Forbidden
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-mobileversion-checker: No mobile version detected.
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-malware-host: Host appears to be clean
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
| http-grep: 
|   (1) http://TARGET:80/: 
|     (1) ip: 
|_      + TARGET
|_http-comments-displayer: Couldn't find any comments.
|_http-chrono: Request times for /; avg: 226.69ms; min: 215.68ms; max: 241.65ms
| http-sitemap-generator: 
|   Directory structure:
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    
| http-headers: 
|   Date: Thu, 10 Oct 2024 00:56:56 GMT
|   Server: Apache/2.4.41 (Ubuntu)
|   Content-Length: 280
|   Connection: close
|   Content-Type: text/html; charset=iso-8859-1
|   
|_  (Request type: GET)
|_http-feed: Couldn't find any feeds.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
Service Info: Host: 127.0.0.1

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Oct  9 20:57:08 2024 -- 1 IP address (1 host up) scanned in 26.71 seconds

```

## CURL 

```bash
HTTP/1.1 403 Forbidden
Date: Thu, 10 Oct 2024 00:56:41 GMT
Server: Apache/2.4.41 (Ubuntu)
Content-Length: 280
Content-Type: text/html; charset=iso-8859-1

<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>403 Forbidden</title>
</head><body>
<h1>Forbidden</h1>
<p>You don't have permission to access this resource.</p>
<hr>
<address>Apache/2.4.41 (Ubuntu) Server at TARGET Port 80</address>
</body></html>


```


## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-10-09 20:56:47 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.41 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.41 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ OPTIONS: Allowed HTTP Methods: OPTIONS, HEAD, GET, POST .

```

## Whatweb

```bash
WhatWeb report for http://TARGET:80
Status    : 403 Forbidden
Title     : 403 Forbidden
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)]

Detected Plugins:
[ Apache ]
	The Apache HTTP Server Project is an effort to develop and
	maintain an open-source HTTP server for modern operating
	systems including UNIX and Windows NT. The goal of this
	project is to provide a secure, efficient and extensible
	server that provides HTTP services in sync with the current
	HTTP standards.

	Version      : 2.4.41 (from HTTP Server Header)
	Google Dorks: (3)
	Website     : http://httpd.apache.org/

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.4.41 (Ubuntu) (from server string)

HTTP Headers:
	HTTP/1.1 403 Forbidden
	Date: Thu, 10 Oct 2024 00:56:48 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Content-Length: 280
	Connection: close
	Content-Type: text/html; charset=iso-8859-1



```
## Screenshot 


![Pasted image 20241009200441.png](Evidence/Pasted%20image%2020241009200441.png)

## Gobuster

Self Enumerate these!

Directories -> 

```bash
/uploads              (Status: 301) [Size: 320] [--> http://TARGET/uploads/]
/server-status        (Status: 403) [Size: 280]
```

Files ->

```bash
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