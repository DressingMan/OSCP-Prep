## NMAP 

```
# Nmap 7.94SVN scan initiated Wed Jun 26 21:19:54 2024 as: nmap -vv --reason -Pn -T4 -sV -p 443 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.083s latency).
Scanned at 2024-06-26 21:19:55 EDT for 117s

PORT    STATE SERVICE  REASON          VERSION
443/tcp open  ssl/http syn-ack ttl 125 Apache httpd 2.4.43 ((Win64) OpenSSL/1.1.1g PHP/7.4.6)
|_http-server-header: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|_http-malware-host: Host appears to be clean
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://TARGET:443/dashboard/javascripts/modernizr.js
|   https://TARGET:443/dashboard/javascripts/all.js
|_  https://code.jquery.com:443/jquery-1.10.2.min.js
| http-trace: TRACE is enabled
| Headers:
| Date: Thu, 27 Jun 2024 01:20:11 GMT
| Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
| Connection: close
| Transfer-Encoding: chunked
|_Content-Type: message/http
| ssl-enum-ciphers: 
|   TLSv1.0: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_256_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_128_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_128_CBC_SHA (rsa 1024) - F
|       TLS_DHE_RSA_WITH_SEED_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_SEED_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_IDEA_CBC_SHA (rsa 1024) - F
|     compressors: 
|       NULL
|     cipher preference: server
|     warnings: 
|       64-bit block cipher IDEA vulnerable to SWEET32 attack
|       Insecure certificate signature (SHA1), score capped at F
|   TLSv1.1: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_256_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_128_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_128_CBC_SHA (rsa 1024) - F
|       TLS_DHE_RSA_WITH_SEED_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_SEED_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_IDEA_CBC_SHA (rsa 1024) - F
|     compressors: 
|       NULL
|     cipher preference: server
|     warnings: 
|       64-bit block cipher IDEA vulnerable to SWEET32 attack
|       Insecure certificate signature (SHA1), score capped at F
|   TLSv1.2: 
|     ciphers: 
|       TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_CHACHA20_POLY1305_SHA256 (dh 1024) - F
|       TLS_DHE_RSA_WITH_AES_256_CCM_8 (dh 1024) - F
|       TLS_DHE_RSA_WITH_AES_256_CCM (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_ARIA_256_GCM_SHA384 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_ARIA_256_GCM_SHA384 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 (dh 1024) - F
|       TLS_DHE_RSA_WITH_AES_128_CCM_8 (dh 1024) - F
|       TLS_DHE_RSA_WITH_AES_128_CCM (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_ARIA_128_GCM_SHA256 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_ARIA_128_GCM_SHA256 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_CAMELLIA_256_CBC_SHA384 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA256 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 (ecdh_x25519) - F

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|       TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_CAMELLIA_128_CBC_SHA256 (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA256 (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_256_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_256_CBC_SHA (dh 1024) - F
|       TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA (ecdh_x25519) - F
|       TLS_DHE_RSA_WITH_AES_128_CBC_SHA (dh 1024) - F
|       TLS_DHE_RSA_WITH_CAMELLIA_128_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_AES_256_GCM_SHA384 (rsa 1024) - F
|       TLS_RSA_WITH_AES_256_CCM_8 (rsa 1024) - F
|       TLS_RSA_WITH_AES_256_CCM (rsa 1024) - F
|       TLS_RSA_WITH_ARIA_256_GCM_SHA384 (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_GCM_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CCM_8 (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CCM (rsa 1024) - F
|       TLS_RSA_WITH_ARIA_128_GCM_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_AES_256_CBC_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_256_CBC_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CBC_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_128_CBC_SHA256 (rsa 1024) - F
|       TLS_RSA_WITH_AES_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_256_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_AES_128_CBC_SHA (rsa 1024) - F
|       TLS_RSA_WITH_CAMELLIA_128_CBC_SHA (rsa 1024) - F
|       TLS_DHE_RSA_WITH_SEED_CBC_SHA (dh 1024) - F
|       TLS_RSA_WITH_SEED_CBC_SHA (rsa 1024) - F
|     compressors: 
|       NULL
|     cipher preference: server
|     warnings: 
|       Insecure certificate signature (SHA1), score capped at F
|   TLSv1.3: 
|     ciphers: 
|       TLS_AKE_WITH_AES_256_GCM_SHA384 (ecdh_x25519) - A
|       TLS_AKE_WITH_CHACHA20_POLY1305_SHA256 (ecdh_x25519) - A
|       TLS_AKE_WITH_AES_128_GCM_SHA256 (ecdh_x25519) - A
|     cipher preference: server
|_  least strength: F
| http-headers: 
|   Date: Thu, 27 Jun 2024 01:20:10 GMT
|   Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
|   Last-Modified: Mon, 18 May 2020 06:55:42 GMT
|   ETag: "1d98-5a5e6a6bcb780"
|   Accept-Ranges: bytes
|   Content-Length: 7576
|   Connection: close
|   Content-Type: text/html
|   
|_  (Request type: HEAD)
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: https://TARGET:443/dashboard/
|     Line number: 10
|     Comment: 
|         <!-- Use title if it's in the page YAML frontmatter -->
|     
|     Path: https://TARGET:443/dashboard/
|     Line number: 163
|     Comment: 
|         <!-- JS Libraries -->
|     
|     Path: https://TARGET:443/dashboard/
|     Line number: 50
|     Comment: 
|         <!-- Right Nav Section -->
|     
|     Path: https://TARGET:443/dashboard/
|     Line number: 6
|     Comment: 
|_        <!-- Always force latest IE rendering engine or request Chrome Frame -->
| http-waf-detect: IDS/IPS/WAF detected:
| http-grep: 
|   (1) https://TARGET:443/dashboard/: 
|     (1) email: 
|_      + fastly-logo@2x.png
| http-sitemap-generator: 
|   Directory structure:
|     /dashboard/
|       Other: 1
|   Longest directory structure:
|     Depth: 1
|     Dir: /dashboard/
|   Total files found (by extension):
|_    Other: 1
| http-php-version: Logo query returned unknown hash 468aa6f6356253cc88b73c33cfb48b5b
| http-security-headers: 
|   Strict_Transport_Security: 
|_    HSTS not configured in HTTPS Server
| http-title: Welcome to XAMPP
| http-vhosts: 
| ssl-dh-params: 
|   VULNERABLE:
|   Diffie-Hellman Key Exchange Insufficient Group Strength
|     State: VULNERABLE
|       Transport Layer Security (TLS) services that use Diffie-Hellman groups
|       of insufficient strength, especially those using one of a few commonly
|       shared groups, may be susceptible to passive eavesdropping attacks.
|     Check results:
|       WEAK DH GROUP 1
|             Cipher Suite: TLS_DHE_RSA_WITH_AES_256_GCM_SHA384
|             Modulus Type: Safe prime
|             Modulus Source: RFC2409/Oakley Group 2
|             Modulus Length: 1024
|             Generator Length: 8
|             Public Key Length: 1024
|     References:
|_      https://weakdh.org
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a4:4cc9:9e84:b26f:9e63:9f9e:d229:dee0
| SHA-1: b023:8c54:7a90:5bfa:119c:4e8b:acca:eacf:3649:1ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Redirected To: https://TARGET/dashboard/
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
| http-enum: 
|   /icons/: Potentially interesting folder w/ directory listing
|_  /img/: Potentially interesting directory w/ listing on 'apache/2.4.43 (win64) openssl/1.1.1g php/7.4.6'
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Jun 26 21:21:52 2024 -- 1 IP address (1 host up) scanned in 118.03 seconds

```

## CURL 

```
HTTP/1.1 302 Found
Date: Thu, 27 Jun 2024 01:19:53 GMT
Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
X-Powered-By: PHP/7.4.6
Location: https://TARGET/dashboard/
Content-Length: 0
Content-Type: text/html; charset=UTF-8



```

## Gobuster 

```

/img                  (Status: 301) [Size: 340]
/webalizer            (Status: 403) [Size: 1040]
/phpmyadmin           (Status: 403) [Size: 1199]
/dashboard            (Status: 301) [Size: 346]
/examples             (Status: 503) [Size: 1054]
/IMG                  (Status: 301) [Size: 340]
/Img                  (Status: 301) [Size: 340]
/xampp                (Status: 301) [Size: 342]
/licenses             (Status: 403) [Size: 1199]
/server-status        (Status: 403) [Size: 1199]
/Dashboard            (Status: 301) [Size: 346]
/con                  (Status: 403) [Size: 1040]
/Webalizer            (Status: 301) [Size: 346]
/aux                  (Status: 403) [Size: 1040]
/WEBALIZER            (Status: 301) [Size: 346]
/prn                  (Status: 403) [Size: 1040]
/server-info          (Status: 403) [Size: 1199]

```

```
/index.php            (Status: 302) [Size: 0]
/favicon.ico          (Status: 200) [Size: 30894]
/.htaccess            (Status: 403) [Size: 1040]
/.                    (Status: 302) [Size: 0]
/.html                (Status: 403) [Size: 1040]
/.htpasswd            (Status: 403) [Size: 1040]
/.htm                 (Status: 403) [Size: 1040]
/.htpasswds           (Status: 403) [Size: 1040]
/.htgroup             (Status: 403) [Size: 1040]
/Index.php            (Status: 302) [Size: 0]
/.htaccess.bak        (Status: 403) [Size: 1040]
/applications.html    (Status: 200) [Size: 3607]
/.htuser              (Status: 403) [Size: 1040]
/Favicon.ico          (Status: 200) [Size: 30894]
/.ht                  (Status: 403) [Size: 1040]
/.htc                 (Status: 403) [Size: 1040]
/favicon.ICO     
```


## Nikto

```
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        443
---------------------------------------------------------------------------
+ SSL Info:        Subject:  /CN=localhost
                   Ciphers:  TLS_AES_256_GCM_SHA384
                   Issuer:   /CN=localhost
+ Start Time:         2024-06-26 21:19:57 (GMT-4)
---------------------------------------------------------------------------
+ Server: Apache/2.4.43 (Win64) OpenSSL/1.1.1g PHP/7.4.6
+ /: Retrieved x-powered-by header: PHP/7.4.6.

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
```
## Whatweb
```
```
## Screenshot 
