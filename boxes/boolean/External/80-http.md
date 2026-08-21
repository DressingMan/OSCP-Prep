## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jun 29 20:52:26 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-06-29 20:52:26 EDT for 208s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61
| http-vhosts: 
|_128 names had status 403
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/register
|     Line number: 57
|     Comment: 
|         <!-- The only True wisdom is in knowing you know nothing -->
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 12
|     Comment: 
|         /* line 12, app/assets/stylesheets/files.scss */
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 1
|     Comment: 
|         /* line 4, app/assets/stylesheets/files.scss */
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 47
|     Comment: 
|         /*# sourceMappingURL=application.css-a5c95786551d4f70c1e84965bbf10e50b1a22344def987b650b199691410c040.map */
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 22
|     Comment: 
|         /*
|          * This is a manifest file that'll be compiled into application.css, which will include all the files
|          * listed below.
|          *
|          * Any CSS and SCSS file within this directory, lib/assets/stylesheets, or any plugin's
|          * vendor/assets/stylesheets directory can be referenced here using a relative path.
|          *
|          * You're free to add application-wide styles to this file and they'll appear at the bottom of the
|          * compiled file so the styles you add here take precedence over styles defined in any other CSS/SCSS
|          * files in this directory. Styles in this file should be added after the last require_* statement.
|          * It is generally better to create a new file per style scope.
|          *
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 7
|     Comment: 
|         /* line 8, app/assets/stylesheets/files.scss */
|     
|     Path: http://TARGET:80/assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css
|     Line number: 17
|     Comment: 
|_        /* line 16, app/assets/stylesheets/files.scss */
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                                 method
|   http://TARGET:80/login     FORM
|   http://TARGET:80/login     FORM
|_  http://TARGET:80/register  FORM
| http-security-headers: 
|   X_Frame_Options: 
|     Header: X-Frame-Options: SAMEORIGIN
|     Description: The browser must not display this content in any frame from a page of different origin than the content itself.
|   X_XSS_Protection: 
|     Header: X-XSS-Protection: 1; mode=block
|     Description: The browser will prevent the rendering of the page when XSS is detected.
|   X_Content_Type_Options: 
|     Header: X-Content-Type-Options: nosniff
|     Description: Will prevent the browser from MIME-sniffing a response away from the declared content-type. 
|   X_Permitted_Cross_Domain_Policies: 
|     Header: X-Permitted-Cross-Domain-Policies: none
|     Description: No policy files are allowed anywhere on the target server, including this master policy file. 
|   Cache_Control: 
|_    Header: Cache-Control: max-age=0, private, must-revalidate
|_http-chrono: Request times for /login; avg: 883.79ms; min: 339.60ms; max: 1797.05ms
|_http-referer-checker: Couldn't find any cross-domain scripts.
| http-headers: 

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|   X-Frame-Options: SAMEORIGIN
|   X-XSS-Protection: 1; mode=block
|   X-Content-Type-Options: nosniff
|   X-Download-Options: noopen
|   X-Permitted-Cross-Domain-Policies: none
|   Referrer-Policy: strict-origin-when-cross-origin
|   Link: </assets/application.debug-4922c2e84f8c272c2f1c5a4699cd704175e279c1c7d601e53b1fdb863182d098.css>; rel=preload; as=style; nopush,</packs/js/application-1110badc63879de6d3dd.js>; rel=preload; as=script; nopush
|   Content-Type: text/html; charset=utf-8
|   ETag: W/"75fc5fc3aeb86a31e80ff449bd1d1535"
|   Cache-Control: max-age=0, private, must-revalidate
|   Set-Cookie: _boolean_session=OIhZRDcwpCT60sFs8BI%2FyJIZB3ABP4kKhYHIbcYu%2BiSmq5iS%2BKXCwhOsYng%2ByF1Wi%2FsKyEsZIfIIqZ%2FQc%2BhQYVLi6z80VrfGhJVQ3VKDsAN4w5fU9aWOs%2BjeLun%2BXSeIKQS8iaqbjWT4CFLX4j4ZFb7UvxQ7Csh%2FfUog5RUbzMGPWbxXw1vC8EIKjOYfQayl5oDcmksggdYh9uisWL8RdNF%2BA5zRi3UGj8ky6gAiDPiwF6gxgzrEvTe7IUt0J%2BAlU0kMgAJUeXkz%2F6LNcJGwZqXLDX5uStfw--U4RZzML0QQOS4imG--6oPIdyx0XfvQbsl7lPz3lg%3D%3D; path=/; HttpOnly; SameSite=Lax
|   X-Request-Id: 901e72e1-2381-4928-b46e-e8defafca6a3
|   X-Runtime: 0.010257
|   Connection: close
|   
|_  (Request type: HEAD)
| fingerprint-strings: 
|   DNSStatusRequestTCP, DNSVersionBindReqTCP, GenericLines, Help, JavaRMI, Kerberos, LANDesk-RC, LDAPBindReq, LDAPSearchReq, LPDString, NCP, NotesRPC, RPCCheck, RTSPRequest, SIPOptions, SMBProgNeg, SSLSessionReq, TLSSessionReq, TerminalServer, TerminalServerCookie, WMSRequest, X11Probe, afp, giop, ms-sql-s, oracle-tns: 
|     HTTP/1.1 400 Bad Request
|   FourOhFourRequest, GetRequest, HTTPOptions: 
|     HTTP/1.0 403 Forbidden
|     Content-Type: text/html; charset=UTF-8
|_    Content-Length: 0
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Redirected To: http://TARGET/login
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
| http-title: Boolean
| http-waf-detect: IDS/IPS/WAF detected:
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 2
|     /assets/
|       css: 1
|     /packs/js/
|       js: 1
|   Longest directory structure:
|     Depth: 2
|     Dir: /packs/js/
|   Total files found (by extension):
|_    Other: 2; css: 1; js: 1
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-php-version: Logo query returned unknown hash 6b286ea14583550e43517a524a40f1db
| http-enum: 
|   /login.stm: Belkin G Wireless Router
|   /login.php: Possible admin folder
|   /login.html: Possible admin folder
|   /login.cfm: Possible admin folder
|   /login.asp: Possible admin folder
|   /login.aspx: Possible admin folder
|   /login.jsp: Possible admin folder
|   /login/: Login page
|   /login.htm: Login page
|   /login.jsp: Login page
|   /robots.txt: Robots file
|_  /register/: Potentially interesting folder
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Jun 29 20:55:54 2024 -- 1 IP address (1 host up) scanned in 208.40 seconds

```

## CURL 

```
HTTP/1.1 302 Found
X-Frame-Options: SAMEORIGIN
X-XSS-Protection: 1; mode=block
X-Content-Type-Options: nosniff
X-Download-Options: noopen
X-Permitted-Cross-Domain-Policies: none
Referrer-Policy: strict-origin-when-cross-origin
Location: http://TARGET/login
Content-Type: text/html; charset=utf-8
Cache-Control: no-cache
X-Request-Id: 64f47077-6a15-42b1-9c0b-e17a9181a8cf
X-Runtime: 0.001515
Transfer-Encoding: chunked

<html><body>You are being <a href="http://TARGET/login">redirected</a>.</body></html>

```

## Gobuster 

Self Enumerate these!

Directories -> 

```
/register             (Status: 200) [Size: 2765]
/login                (Status: 200) [Size: 2413]
/404                  (Status: 200) [Size: 1722]
/500                  (Status: 200) [Size: 1635]
/filemanager          (Status: 302) [Size: 94] [--> http://TARGET/login]
/422                  (Status: 200) [Size: 1705]

```

Files ->

```
/register.php         (Status: 200) [Size: 2765]
/login.php            (Status: 200) [Size: 2413]
/favicon.ico          (Status: 200) [Size: 0]
/login.html           (Status: 200) [Size: 2413]
/404.html             (Status: 200) [Size: 1722]
/login.asp            (Status: 200) [Size: 2413]
/login.aspx           (Status: 200) [Size: 2413]
/register.aspx        (Status: 200) [Size: 2765]
/robots.txt           (Status: 200) [Size: 99]
/register.html        (Status: 200) [Size: 2765]
/register.asp         (Status: 200) [Size: 2765]
/login.cfm            (Status: 200) [Size: 2413]
/500.html             (Status: 200) [Size: 1635]
/login.htm            (Status: 200) [Size: 2413]
/login.jsp            (Status: 200) [Size: 2413]
/register.htm         (Status: 200) [Size: 2765]
/login.cgi            (Status: 200) [Size: 2413]
/register.cfm         (Status: 200) [Size: 2765]
/register.jsp         (Status: 200) [Size: 2765]
/register.cgi         (Status: 200) [Size: 2765]
/login.phtml          (Status: 200) [Size: 2413]
/422.html             (Status: 200) [Size: 1705]
/login.shtml          (Status: 200) [Size: 2413]
/login.action         (Status: 200) [Size: 2413]
/login.php3           (Status: 200) [Size: 2413]
/register.shtml       (Status: 200) [Size: 2765]
/login.jhtml          (Status: 200) [Size: 2413]
/filemanager.php      (Status: 302) [Size: 94] [--> http://TARGET/login]
/register.action      (Status: 200) [Size: 2765]
/register.php3        (Status: 200) [Size: 2765]
/login.php5           (Status: 200) [Size: 2413]
/login.jsf            (Status: 200) [Size: 2413]
/register.phtml       (Status: 200) [Size: 2765]
/register.jhtml       (Status: 200) [Size: 2765]

```

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
## Nikto
```
```
## Whatweb
```
```
## Screenshot 
```
```
```
```
```
```
