## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:51 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-10-14 10:32:52 EDT for 94s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.38 ((Debian))
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: 
|     Header: Pragma: no-cache
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-title: SuiteCRM
|_Requested resource was index.php?action=Login&module=Users
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-favicon: Unknown favicon MD5: ED9A8C7810E8C9FB7035B6C3147C9A3A
| http-headers: 
|   Date: Mon, 14 Oct 2024 14:33:05 GMT
|   Server: Apache/2.4.38 (Debian)
|   Set-Cookie: PHPSESSID=REDACTED; path=/
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: no-cache
|   Set-Cookie: sugar_user_theme=SuiteP; expires=Tue, 14-Oct-2025 14:33:05 GMT; Max-Age=31536000; HttpOnly
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
| http-vhosts: 
|_128 names had status 301
| http-waf-detect: IDS/IPS/WAF detected:
|_192.168.158.146:80/?p4yl04d3=<script>alert(document.cookie)</script>
| http-php-version: Logo query returned unknown hash 76f37b38832eb32b2da1546fa338bb6c
|_Credits query returned unknown hash 76f37b38832eb32b2da1546fa338bb6c
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-robots.txt: 1 disallowed entry 
|_/
| http-sql-injection: 
|   Possible sqli for queries:
|     http://TARGET:80/cache/include/javascript/index.php?themeName=%27%20OR%20sqlspider&entryPoint=getImage
|     http://TARGET:80/cache/include/javascript/index.php?themeName=&entryPoint=getImage%27%20OR%20sqlspider
|     http://TARGET:80/vendor/tinymce/tinymce/Xt._addCacheSuffix1t11o.onload1function11%7Ba.remove1i11o111o.onreadystatechange1o.onload1o1null11n11%7D1o.onerror1function11%7BAi1r1?r%28%29%3A%22undefined%22%21=typeof%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/Selector.getters.rel1Selector.getters.href;if(Selector.useNative&&Y_DOC.querySelector){Selector.shorthand["\\.([^\\s\\\\(\\[:]*)"]="[class~=$1]";}Selector._reNth=/^(?%3A%28%5B%5C-%5D%3F%5Cd%2A%29%28n%29%7B1%7D%7C%28odd%7Ceven%29%24%29%2A%28%5B%5C-%2B%5D%3F%5Cd%2A%29%24%2F%3BSelector._getNth=function%28d%2Co%2Cq%2Ch%29%7BSelector._reNth.test%28o%29%3Bvar%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=D%3BO%3DA%27%20OR%20sqlspider
|_    http://TARGET:80/cache/include/javascript/?C=M%3BO%3DA%27%20OR%20sqlspider
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-date: Mon, 14 Oct 2024 14:33:06 GMT; -1s from local time.
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/
|     Form id: form
|     Form action: index.php
|     
|     Path: http://TARGET:80/index.php
|     Form id: form
|_    Form action: index.php
|_http-malware-host: Host appears to be clean
|_http-server-header: Apache/2.4.38 (Debian)
|_http-mobileversion-checker: No mobile version detected.
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|_    Couldn't find a file-type field.
| http-grep: 
|   (1) http://TARGET:80/include/javascript/calendar.js?v=WWrZLHR9Ay2yH7WcEIhRuA: 
|     (1) email: 
|       + contact@sugarcrm.com
|   (1) http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA: 
|     (1) email: 
|       + carl.ogren@gmail.com
|   (1) http://TARGET:80/cache/include/javascript/: 
|     (1) ip: 
|_      + TARGET
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Redirected To: index.php?action=Login&module=Users
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
|_http-chrono: Request times for /; avg: 1910.66ms; min: 544.84ms; max: 5416.42ms
|_http-feed: Couldn't find any feeds.
| http-enum: 
|   /robots.txt: Robots file
|   /crossdomain.xml: Adobe Flash crossdomain policy
|   /cache/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /custom/: Potentially interesting folder
|   /data/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /include/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /install/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /lib/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /modules/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /service/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /soap/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /themes/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /upload/: Potentially interesting folder
|_  /vendor/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://oss.maxcdn.com:443/respond/1.4.2/respond.min.js
|_  https://oss.maxcdn.com:443/html5shiv/3.7.2/html5shiv.min.js
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                                  method
|   http://TARGET:80/           FORM
|_  http://TARGET:80/index.php  FORM
|_http-errors: Couldn't find any error pages.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /cache/include/javascript/
|       Other: 1; js: 4
|     /include/javascript/
|       js: 1
|     /include/javascript/qtip/
|       css: 1
|     /modules/Users/
|       css: 1; js: 1
|     /themes/SuiteP/css/
|       css: 4; php: 1
|     /themes/SuiteP/images/
|       ico: 1
|     /themes/SuiteP/js/
|       js: 1
|     /themes/default/images/
|       png: 1
|     /vendor/tinymce/tinymce/
|       js: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /themes/SuiteP/css/
|   Total files found (by extension):
|_    Other: 2; css: 6; ico: 1; js: 8; php: 1; png: 1
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 3557
|     Comment: 
|         /**
|         			 * Whether or not this is a hidden filter.
|         			 * @instance
|         			 * @type {boolean}

_Trimmed: original note was a full nmap/http-script dump. Open ports, titles, and attack notes are above._
