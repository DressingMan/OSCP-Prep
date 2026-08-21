## NMAP 

```
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-06-29 20:52:26 EDT for 208s
PORT      STATE SERVICE        VERSION
80/tcp open http
| http-title: Boolean
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
