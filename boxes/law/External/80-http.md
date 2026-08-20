## NMAP 

```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:39 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.074s latency).
Scanned at 2024-10-24 16:31:39 EDT for 36s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-malware-host: Host appears to be clean
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                                            method
|_  http://TARGET:80/htmLawed_README.txt  FORM
|_http-chrono: Request times for /; avg: 459.92ms; min: 385.29ms; max: 582.33ms
| http-headers: 
|   Date: Thu, 24 Oct 2024 20:31:47 GMT
|   Server: Apache/2.4.56 (Debian)
|   Set-Cookie: sid=g73kb4akr1f264tpjibo40u7r6; path=/
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: private, max-age=1800
|   Last-Modified: Tue, 22 Dec 2020 02:17:42 GMT
|   Set-Cookie: sid=vmf638idahlja5td28jabtlc3n; path=/
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: private, max-age=1800
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-grep: 
|   (1) http://TARGET:80/htmLawed_TESTCASE.txt: 
|     (1) email: 
|       + x@y.com
|   (1) http://TARGET:80/htmLawedTest.php: 
|     (1) ip: 
|       + TARGET
|   (2) http://TARGET:80/htmLawed_README.txt: 
|     (2) email: 
|       + a@b.com
|_      + def@abc.com
| http-php-version: Logo query returned unknown hash 62b70acd6aa85859782e36b9d3fd8418
|_Credits query returned unknown hash 112794c9b6b28eb69910c2766f965137
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|_    Couldn't find a file-type field.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-date: Thu, 24 Oct 2024 20:31:49 GMT; -1s from local time.
|_http-title: htmLawed (1.2.5) test
|_http-server-header: Apache/2.4.56 (Debian)
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; htm: 1; txt: 2
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    Other: 1; htm: 1; txt: 2
|_http-feed: Couldn't find any feeds.
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
| http-vhosts: 
|_128 names had status 200
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Form id: 
|     Form action: a
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Form id: 
|     Form action: b
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Form id: b
|_    Form action: a
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 404
|   	http://TARGET:80/htmLawedTest.php
|   
|   Error Code: 404
|   	http://TARGET:80/none
|   
|   Error Code: 404
|   	http://TARGET:80/x
|   
|   Error Code: 404
|   	http://TARGET:80/java%20script1alert1
|   
|   Error Code: 404
|   	http://TARGET:80/xxx
|   
|   Error Code: 404
|   	http://TARGET:80/javascript1alert1
|   
|   Error Code: 404
|   	http://TARGET:80/5
|   
|   Error Code: 404
|   	http://TARGET:80/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/link
|   
|   Error Code: 404
|   	http://TARGET:80/4
|   
|   Error Code: 404
|   	http://TARGET:80/home.htm
|   
|   Error Code: 404
|   	http://TARGET:80/b
|   
|   Error Code: 404
|   	http://TARGET:80/b.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/s
|   
|   Error Code: 404
|   	http://TARGET:80/3
|   
|   Error Code: 404
|   	http://TARGET:80/h
|   
|   Error Code: 404
|   	http://TARGET:80/%5CxE2%5Cx80%5Cx83javascript1alert11231
|   
|   Error Code: 404
|   	http://TARGET:80/Psych0tr1a1
|   
|   Error Code: 404
|   	http://TARGET:80/a.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/c.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/1
|   
|   Error Code: 404

_Trimmed: original note was a full nmap/http-script dump. Open ports, titles, and attack notes are above._
