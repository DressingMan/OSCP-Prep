## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.075s latency).
Scanned at 2024-06-26 21:19:55 EDT for 136s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
| http-vhosts: 
|_128 names had status 302
| http-trace: TRACE is enabled
| Headers:
| Date: Thu, 27 Jun 2024 01:20:06 GMT
| Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
| Connection: close
| Transfer-Encoding: chunked
|_Content-Type: message/http
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-headers: 
|   Date: Thu, 27 Jun 2024 01:20:03 GMT
|   Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|   Last-Modified: Mon, 18 May 2020 06:55:42 GMT
|   ETag: "1d98-5a5e6a6bcb780"
|   Accept-Ranges: bytes
|   Content-Length: 7576
|   Connection: close
|   Content-Type: text/html
|   
|_  (Request type: HEAD)
| http-php-version: Logo query returned unknown hash 468aa6f6356253cc88b73c33cfb48b5b
|_Credits query returned unknown hash 468aa6f6356253cc88b73c33cfb48b5b
| http-waf-detect: IDS/IPS/WAF detected:
|_192.168.158.55:80/?p4yl04d3=<script>alert(document.cookie)</script>
|_http-favicon: Unknown favicon MD5: 56F7C04657931F2D0B79371B2D6E9820
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-malware-host: Host appears to be clean
| http-sql-injection: 
|   Possible sqli for queries:
|     http://TARGET:80/dashboard/javascripts/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/dashboard/javascripts/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/dashboard/javascripts/?C=D%3BO%3DA%27%20OR%20sqlspider
|_    http://TARGET:80/dashboard/javascripts/?C=M%3BO%3DA%27%20OR%20sqlspider
|_http-date: Thu, 27 Jun 2024 01:20:04 GMT; -2s from local time.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Redirected To: http://TARGET/dashboard/
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
|_http-mobileversion-checker: No mobile version detected.
| http-title: Welcome to XAMPP
|_Requested resource was http://TARGET/dashboard/
| http-enum: 
|   /icons/: Potentially interesting folder w/ directory listing
|_  /img/: Potentially interesting directory w/ listing on 'apache/2.4.43 (win64) openssl/1.1.1g php/7.4.6'
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|_  http://code.jquery.com:80/jquery-1.10.2.min.js
|_http-dombased-xss: Couldn't find any DOM based XSS.
| http-grep: 
|   (1) http://TARGET:80/dashboard/: 
|     (1) email: 
|       + fastly-logo@2x.png
|   (1) http://TARGET:80/dashboard/faq.html: 

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     (1) email: 
|       + your-gmail-username@gmail.com
|   (3) http://TARGET:80/dashboard/phpinfo.php: 
|     (2) ip: 
|       + TARGET
|       + ATTACKER
|     (1) email: 
|       + license@php.net
|   (2) http://TARGET:80/dashboard/stylesheets/all.css: 
|     (2) email: 
|       + social-icons@2x.png
|_      + social-icons-large@2x.png
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 403
|_  	http://TARGET:80/phpmyadmin/
| http-sitemap-generator: 
|   Directory structure:
|     /
|       css: 1; html: 1
|     /dashboard/
|       Other: 1; html: 3; php: 1
|     /dashboard/docs/
|       html: 1
|     /dashboard/images/
|       png: 3; svg: 1
|     /dashboard/images/screenshots/
|       jpg: 1
|     /dashboard/javascripts/
|       Other: 1; js: 2
|     /dashboard/stylesheets/
|       css: 2
|   Longest directory structure:
|     Depth: 3
|     Dir: /dashboard/images/screenshots/
|   Total files found (by extension):
|_    Other: 2; css: 3; html: 5; jpg: 1; js: 2; php: 1; png: 3; svg: 1
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7353
|     Comment: 
|         /* line 33, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 3441
|     Comment: 
|         /* line 135, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_dropdown.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8373
|     Comment: 
|         /* line 443, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 273
|     Comment: 
|         /* line 367, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1082
|     Comment: 
|         /**
|                  * Returns the value of `html5.elements` as an array.
|                  * @private
|                  * @returns {Array} An array of shived element node names.
|                  */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/normalize.css
|     Line number: 229
|     Comment: 
|         /*
|          * Addresses margin not present in IE 8/9 and Safari 5.
|          */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 600
|     Comment: 
|          // The non-literal . in this regex is intentional:
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8185
|     Comment: 
|         /* line 383, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 329
|     Comment: 
|         /* line 438, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 726
|     Comment: 
|          //   It was also live in Safari 4.0.0 - 4.0.4, but fixed in 4.0.5
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8072
|     Comment: 
|         /* line 345, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 551
|     Comment: 
|          //  occurrences of "url(" is a reliable method for detecting ACTUAL support for this!
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 470
|     Comment: 
|          // Using !!navigator.geolocation does two things we don't want. It:
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 4084
|     Comment: 
|         /* line 182, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_global.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 5053
|     Comment: 
|         /* line 149, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_reveal.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7336
|     Comment: 
|         /* line 20, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1025
|     Comment: 
|         /** Detect whether the browser supports default html5 styles */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 157
|     Comment: 
|         /* line 216, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 6627
|     Comment: 
|         /* line 282, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_offcanvas.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 9024
|     Comment: 
|         /* line 741, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 4735
|     Comment: 
|         /* line 289, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_orbit.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1342
|     Comment: 
|          // Modernizr.testProp() investigates whether a given style property is recognized
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7270
|     Comment: 
|         /* ========================================================================== Links ========================================================================== */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8943
|     Comment: 
|         /* line 713, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 48
|     Comment: 
|         /* line 73, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 4223
|     Comment: 
|         /* line 461, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_forms.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7968
|     Comment: 
|         /* line 320, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7766
|     Comment: 
|         /* line 257, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 943
|     Comment: 
|          // todo: hypothetically we could be doing an array of tests and use a basic loop here.
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8121
|     Comment: 
|         /* line 362, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1401
|     Comment: 
|          // Add the new classes to the <html> element.
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 3092
|     Comment: 
|         /* line 80, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_button-groups.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8413
|     Comment: 
|         /* line 460, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 9050
|     Comment: 
|         /* line 769, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/all.js
|     Line number: 108
|     Comment: 
|          // http://paulirish.com/2011/requestanimationframe-for-smart-animating/
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 363
|     Comment: 
|         /* line 491, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/all.js
|     Line number: 3320
|     Comment: 
|          // should we animate the background?
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 912
|     Comment: 
|          // Spec doesn't define any special parsing or detectable UI
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 233
|     Comment: 
|         /* footer */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 321
|     Comment: 
|         /* line 426, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/all.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 985
|     Comment: 
|          //   docElement.className = docElement.className.replace( re, '' );
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7981
|     Comment: 
|         /* line 324, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 333
|     Comment: 
|         /* downloads list */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1138
|     Comment: 
|          //   is inserted into a document/fragment
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7892
|     Comment: 
|         /* line 297, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 724
|     Comment: 
|          // Note: in some older browsers, "no" was a return value instead of empty string.
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 3388
|     Comment: 
|         /* line 170, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_clearing.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 937
|     Comment: 
|          // End of test definitions
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8715
|     Comment: 
|         /* line 617, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 4469
|     Comment: 
|         /* line 95, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_labels.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 5439
|     Comment: 
|         /* line 300, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_switch.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7182
|     Comment: 
|         /* line 637, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_visibility.scss */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 8792
|     Comment: 
|         /* line 662, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 3703
|     Comment: 
|         /* line 81, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_forms.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 1007
|     Comment: 
|         /*>>shiv*/
|     
|     Path: http://TARGET:80/phpmyadmin/
|     Line number: 8
|     Comment: 
|         
|         
|         
|         
|         
|         /*]]>*/-->
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 7618
|     Comment: 
|         /* line 191, /home/bitnami/projects/apachefriends-web/source-xampp-windows/stylesheets/asciidoctor.css */
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 6298
|     Comment: 
|         /* line 324, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_top-bar.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/all.js
|     Line number: 1946
|     Comment: 
|          // skip non-existant targets
|     
|     Path: http://TARGET:80/dashboard/stylesheets/all.css
|     Line number: 978
|     Comment: 
|         /* line 168, /home/bitnami/projects/apachefriends-web/bower_components/foundation/scss/foundation/components/_grid.scss */
|     
|     Path: http://TARGET:80/dashboard/javascripts/modernizr.js
|     Line number: 93
|     Comment: 
|          // used in testing loop
|     
|     Path: http://TARGET:80/dashboard/docs/increase-php-file-upload-limit.html
|     Li

_Trimmed for readability._
