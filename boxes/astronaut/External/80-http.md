## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 19 22:52:53 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.061s latency).
Scanned at 2024-06-19 22:52:53 EDT for 29s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-grep: 
|   (1) http://TARGET:80/: 
|     (1) ip: 
|       + TARGET
|   (5) http://TARGET:80/grav-admin/: 
|     (5) ip: 
|       + 5.1.87.66
|       + 7.74.96.9
|       + 3.65.02.05
|       + 04.1.07.14
|_      + 07.1.13.14
|_http-comments-displayer: Couldn't find any comments.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /grav-admin/
|       Other: 2
|     /icons/
|       gif: 2
|   Longest directory structure:
|     Depth: 1
|     Dir: /grav-admin/
|   Total files found (by extension):
|_    Other: 3; gif: 2
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-ls: Volume /
| SIZE  TIME              FILENAME
| -     2021-03-17 17:46  grav-admin/
|_
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-php-version: Logo query returned unknown hash ed1edca388359919e3da6869af09ba0f
|_Credits query returned unknown hash ed1edca388359919e3da6869af09ba0f
|_http-malware-host: Host appears to be clean
| http-vhosts: 
|_128 names had status 200
|_http-title: Index of /
|_http-date: Thu, 20 Jun 2024 02:53:07 GMT; -1s from local time.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-headers: 
|   Date: Thu, 20 Jun 2024 02:53:05 GMT
|   Server: Apache/2.4.41 (Ubuntu)
|   Connection: close
|   Content-Type: text/html;charset=UTF-8
|   
|_  (Request type: HEAD)
| http-methods: 
|_  Supported Methods: HEAD GET POST OPTIONS
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-errors: Couldn't find any error pages.
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
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
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-csrf: Couldn't find any CSRF vulnerabilities.
|_http-mobileversion-checker: No mobile version detected.
| http-sql-injection: 
|   Possible sqli for queries:
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=N%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/?C=D%3BO%3DA%27%20OR%20sqlspider
|_    http://TARGET:80/?C=M%3BO%3DA%27%20OR%20sqlspider
|_http-chrono: Request times for /; avg: 313.12ms; min: 245.85ms; max: 411.77ms
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
| http-enum: 
|_  /: Root directory w/ listing on 'apache/2.4.41 (ubuntu)'
|_http-feed: Couldn't find any feeds.
Service Info: Host: 127.0.0.1

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 19 22:53:22 2024 -- 1 IP address (1 host up) scanned in 28.99 seconds

```

## CURL 

```
HTTP/1.1 200 OK
Date: Thu, 20 Jun 2024 02:52:53 GMT
Server: Apache/2.4.41 (Ubuntu)
Vary: Accept-Encoding
Content-Length: 758
Content-Type: text/html;charset=UTF-8

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<html>
 <head>
  <title>Index of /</title>
 </head>
 <body>
<h1>Index of /</h1>
  <table>
   <tr><th valign="top"><img src="/icons/blank.gif" alt="[ICO]"></th><th><a href="?C=N;O=D">Name</a></th><th><a href="?C=M;O=A">Last modified</a></th><th><a href="?C=S;O=A">Size</a></th><th><a href="?C=D;O=A">Description</a></th></tr>
   <tr><th colspan="5"><hr></th></tr>
<tr><td valign="top"><img src="/icons/folder.gif" alt="[DIR]"></td><td><a href="grav-admin/">grav-admin/</a></td><td align="right">2021-03-17 17:46  </td><td align="right">  - </td><td>&nbsp;</td></tr>
   <tr><th colspan="5"><hr></th></tr>
</table>
<address>Apache/2.4.41 (Ubuntu) Server at TARGET Port 80</address>
</body></html>


```

## Gobuster 

Self Enumerate these!

Directories -> 

```
/server-status        (Status: 403) [Size: 279]
```

Files ->

```
/.htaccess            (Status: 403) [Size: 279]
/.                    (Status: 200) [Size: 758]
/.html                (Status: 403) [Size: 279]
/.php                 (Status: 403) [Size: 279]
/.htpasswd            (Status: 403) [Size: 279]
/.htm                 (Status: 403) [Size: 279]
/.htpasswds           (Status: 403) [Size: 279]
/.htgroup             (Status: 403) [Size: 279]
/wp-forum.phps        (Status: 403) [Size: 279]
/.htaccess.bak        (Status: 403) [Size: 279]
/.htuser              (Status: 403) [Size: 279]
/.ht                  (Status: 403) [Size: 279]
/.htc                 (Status: 403) [Size: 279]

```

## Gobuster /grav-admin/

Directories ->
```bash
/cache                (Status: 301) [Size: 327]
/images               (Status: 301) [Size: 328]
/tmp                  (Status: 301) [Size: 325]
/user                 (Status: 301) [Size: 326]
/bin                  (Status: 301) [Size: 325]
/logs                 (Status: 301) [Size: 326]
/login                (Status: 200) [Size: 13967]
/admin                (Status: 200) [Size: 15508]
/backup               (Status: 301) [Size: 328]
/assets               (Status: 301) [Size: 328]
/home                 (Status: 200) [Size: 14014]
/system               (Status: 301) [Size: 328]
/vendor               (Status: 301) [Size: 328]
/forgot_password      (Status: 200) [Size: 12383]
/user_profile         (Status: 200) [Size: 13974]
/activate_user        (Status: 302) [Size: 0]
```

Files ->
```bash
/LICENSE.txt          (Status: 403) [Size: 279]
/login.html           (Status: 200) [Size: 13967]
/.htaccess            (Status: 403) [Size: 279]
/robots.txt           (Status: 200) [Size: 274]
/home.html            (Status: 200) [Size: 14014]
/.html                (Status: 403) [Size: 279]
/admin.html           (Status: 200) [Size: 15508]
/login.htm            (Status: 200) [Size: 13967]
/.php                 (Status: 403) [Size: 279]
/home.htm             (Status: 200) [Size: 14014]
/admin.htm            (Status: 403) [Size: 0]
/.htpasswd            (Status: 403) [Size: 279]
/.xml                 (Status: 200) [Size: 14014]
/.htm                 (Status: 403) [Size: 279]
/.txt                 (Status: 200) [Size: 14014]
/.htpasswds           (Status: 403) [Size: 279]
/.htgroup             (Status: 403) [Size: 279]
/forgot_password.htm  (Status: 200) [Size: 12383]
/wp-forum.phps        (Status: 403) [Size: 279]
/.htaccess.bak        (Status: 403) [Size: 279]
/.htuser              (Status: 403) [Size: 279]
/.htc                 (Status: 403) [Size: 279]
/.ht                  (Status: 403) [Size: 279]
/user_profile.html    (Status: 200) [Size: 13974]

```



## Nikto

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-06-19 22:52:58 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.41 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ /: Directory indexing found.
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.41 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ OPTIONS: Allowed HTTP Methods: HEAD, GET, POST, OPTIONS .
+ /./: Directory indexing found.
+ /./: Appending '/./' to a directory allows indexing.
+ //: Directory indexing found.
+ //: Apache on Red Hat Linux release 9 reveals the root directory listing by default if there is no index page.
+ /%2e/: Directory indexing found.
+ /%2e/: Weblogic allows source code or directory listing, upgrade to v6.0 SP1 or higher. See: http://www.securityfocus.com/bid/2513
+ ///: Directory indexing found.
+ /?PageServices: The remote server may allow directory listings through Web Publisher by forcing the server to show all files via 'open directory browsing'. Web Publisher should be disabled. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0269
+ /?wp-cs-dump: The remote server may allow directory listings through Web Publisher by forcing the server to show all files via 'open directory browsing'. Web Publisher should be disabled. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0269
+ ///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////: Directory indexing found.
+ ///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////: Abyss 1.03 reveals directory listing when multiple /'s are requested. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1078
+ 7731 requests: 0 error(s) and 16 item(s) reported on remote host
+ End Time:           2024-06-19 23:02:06 (GMT-4) (548 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

```

## Whatweb

```
WhatWeb report for http://TARGET:80
Status    : 200 OK
Title     : Index of /
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)], Index-Of

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

[ Index-Of ]
	Index of

	Google Dorks: (1)

HTTP Headers:
	HTTP/1.1 200 OK
	Date: Thu, 20 Jun 2024 02:52:58 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Vary: Accept-Encoding
	Content-Encoding: gzip
	Content-Length: 416
	Connection: close
	Content-Type: text/html;charset=UTF-8



```
## Screenshot 

![Pasted image 20240619231531.png](Evidence/Pasted%20image%2020240619231531.png)


![Pasted image 20240619232058.png](Evidence/Pasted%20image%2020240619232058.png)

Exploit
