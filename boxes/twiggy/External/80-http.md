## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jun 29 16:34:23 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-29 16:34:24 EDT for 910s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 nginx 1.16.1
| http-methods: 
|_  Supported Methods: GET HEAD OPTIONS
|_http-devframework: Django detected. Found Django admin login page on /admin/
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-date: Sat, 29 Jun 2024 20:34:41 GMT; 0s from local time.
| http-feed: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following feeds: 
|     Atom: http://TARGET:80/blog/feeds/atom/
|     Atom: /blog/feeds/atom/
|     RSS (version 2.0): http://TARGET:80/blog/feeds/rss/
|_    RSS (version 2.0): /blog/feeds/rss/
|_http-errors: Couldn't find any error pages.
| http-vhosts: 
| smtp
| blog
| info
|_125 names had status 200
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
| http-security-headers: 
|   X_Frame_Options: 
|     Header: X-Frame-Options: SAMEORIGIN
|_    Description: The browser must not display this content in any frame from a page of different origin than the content itself.
| http-headers: 
|   Server: nginx/1.16.1
|   Date: Sat, 29 Jun 2024 20:34:39 GMT
|   Content-Type: text/html; charset=utf-8
|   Content-Length: 6927
|   Connection: close
|   X-Frame-Options: SAMEORIGIN
|   Vary: Cookie
|   
|_  (Request type: HEAD)
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-title: Home | Mezzanine
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-wordpress-enum: Nothing found amongst the top 100 resources,use --script-args search-limit=<number|all> for deeper analysis)
|_http-chrono: Request times for /; avg: 1271.91ms; min: 937.51ms; max: 1539.09ms
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/gallery/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/contact/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/about/team/
|     Form id: 
|     Form action: /search/
|     

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     Path: http://TARGET:80/contact/legals/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/about/history/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/search/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/blog/
|     Form id: 
|     Form action: /search/
|     
|     Path: http://TARGET:80/about/
|     Form id: 
|_    Form action: /search/
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                              method
|_  http://TARGET:80/admin/  FORM
| http-php-version: Logo query returned unknown hash e2d05cb54f0c980109f3fdab35c8404b
| http-fileupload-exploiter: 
|   
|_    Couldn't find a file-type field.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /about/
|       Other: 1
|     /about/history/
|       Other: 1
|     /about/team/
|       Other: 1
|     /admin/
|       Other: 1
|     /blog/
|       Other: 1
|     /blog/feeds/atom/
|       Other: 1
|     /blog/feeds/rss/
|       Other: 1
|     /contact/
|       Other: 1
|     /contact/legals/
|       Other: 1
|     /gallery/
|       Other: 1
|     /search/
|       Other: 1
|     /static/css/
|       css: 2
|     /static/img/
|       ico: 1
|     /static/js/
|       js: 4
|     /static/mezzanine/js/
|       js: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /static/mezzanine/js/
|   Total files found (by extension):
|_    Other: 12; css: 2; ico: 1; js: 5
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1963
|     Comment: 
|          // TAB DATA-API
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 497
|     Comment: 
|         /* ========================================================================
|          * Bootstrap: collapse.js v3.2.0
|          * http://getbootstrap.com/javascript/#collapse
|          * ========================================================================
|          * Copyright 2011-2014 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|          * ======================================================================== */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 230
|     Comment: 
|          // BUTTON PLUGIN DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 703
|     Comment: 
|          // if mobile we use a backdrop because click events don't delegate
|     
|     Path: http://TARGET:80/admin/
|     Line number: 84
|     Comment: 
|         <!-- HEADER -->
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1432
|     Comment: 
|         /* placement == 'right' */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 810
|     Comment: 
|          // ===================================
|     
|     Path: http://TARGET:80/static/js/bootstrap-extras.js
|     Line number: 59
|     Comment: 
|          // Prevent link on first touch
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1332
|     Comment: 
|          // so we use setOffset directly with our own function B-0
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 106
|     Comment: 
|         /* Style error messages as danger alerts */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 97
|     Comment: 
|          // strip for ie7
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 460
|     Comment: 
|         /*========================================
|                   MEZZANINE ACCOUNTS
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1673
|     Comment: 
|         /* ========================================================================
|          * Bootstrap: scrollspy.js v3.2.0
|          * http://getbootstrap.com/javascript/#scrollspy
|          * ========================================================================
|          * Copyright 2011-2014 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|          * ======================================================================== */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1320
|     Comment: 
|          // manually read margins because getBoundingClientRect includes difference
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 509
|     Comment: 
|          // COLLAPSE PUBLIC CLASS DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 162
|     Comment: 
|         /* ========================================================================
|          * Bootstrap: button.js v3.2.0
|          * http://getbootstrap.com/javascript/#buttons
|          * ========================================================================
|          * Copyright 2011-2014 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|          * ======================================================================== */
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 2
|     Comment: 
|         /*========================================
|                 MEZZANINE GENERAL STYLES
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1115
|     Comment: 
|          // ===============================
|     
|     Path: http://TARGET:80/static/js/bootstrap-extras.js
|     Line number: 54
|     Comment: 
|          // Prevent touch events within dropdown bubbling down to document
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1804
|     Comment: 
|          // ===========================
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 472
|     Comment: 
|         /* Display dropdowns on hover only in desktops (md and lg classes) */
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 400
|     Comment: 
|         /*========================================
|                   MEZZANINE GENERIC
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 886
|     Comment: 
|          // don't move modals dom position
|     
|     Path: http://TARGET:80/static/js/bootstrap-extras.js
|     Line number: 64
|     Comment: 
|          // Hide other open dropdowns
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 128
|     Comment: 
|         /*========================================
|                   MULTI-LEVEL DROP-DOWN NAV
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1344
|     Comment: 
|          // check to see if placing tip in new offset caused the tip to resize itself
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 377
|     Comment: 
|         /* We apply the clearfix hack to .form-actions because we often
|         float the buttons inside it. This prevents collapsing. */
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 389
|     Comment: 
|         /*========================================
|                   MEZZANINE GALLERY
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 2068
|     Comment: 
|          // AFFIX PLUGIN DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 459
|     Comment: 
|          // ====================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1550
|     Comment: 
|          // ===================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 201
|     Comment: 
|          // push to event loop to allow forms to submit
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1607
|     Comment: 
|          // we use append for html objects to maintain js events
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 156
|     Comment: 
|          // ==============
|     
|     Path: http://TARGET:80/static/js/bootstrap-extras.js
|     Line number: 40
|     Comment: 
|         /**
|              * Touch events
|              *
|              * @description Support click to open if we're dealing with a touchscreen
|              */
|     
|     Path: http://TARGET:80/static/css/mezzanine.css
|     Line number: 176
|     Comment: 
|         /*========================================
|                     MEZZANINE BLOG
|         ==========================================*/
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1590
|     Comment: 
|          // NOTE: POPOVER EXTENDS tooltip.js
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1954
|     Comment: 
|          // TAB NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1528
|     Comment: 
|          // TOOLTIP PLUGIN DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1912
|     Comment: 
|          // reflow for transition
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 252
|     Comment: 
|          // BUTTON NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 40
|     Comment: 
|          // explicit for ie8 (  ._.)
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 947
|     Comment: 
|          // guard against infinite focus loop
|     
|     Path: http://TARGET:80/static/js/bootstrap-extras.js
|     Line number: 16
|     Comment: 
|          // Mouseenter (used with .hover()) does not trigger when user enters from outside document window
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 82
|     Comment: 
|          // ======================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 175
|     Comment: 
|          // ==============================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 155
|     Comment: 
|          // ALERT DATA-API
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1823
|     Comment: 
|          // SCROLLSPY NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1685
|     Comment: 
|          // SCROLLSPY CLASS DEFINITION
|     
|     Path: http://TARGET:80/static/css/bootstrap.css
|     Line number: 6203
|     Comment: 
|         /*# sourceMappingURL=bootstrap.css.map */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1446
|     Comment: 
|          // top overflow
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1049
|     Comment: 
|          // MODAL PLUGIN DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1549
|     Comment: 
|          // TOOLTIP NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 634
|     Comment: 
|          // COLLAPSE NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1454
|     Comment: 
|          // left overflow
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1844
|     Comment: 
|         /* ========================================================================
|          * Bootstrap: tab.js v3.2.0
|          * http://getbootstrap.com/javascript/#tabs
|          * ========================================================================
|          * Copyright 2011-2014 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|          * ======================================================================== */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1856
|     Comment: 
|          // TAB CLASS DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 231
|     Comment: 
|          // ========================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1091
|     Comment: 
|          // only register focus restorer if modal will actually get shown
|     
|     Path: http://TARGET:80/admin/
|     Line number: 7
|     Comment: 
|         <!-- LOADING -->
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 146
|     Comment: 
|          // ALERT NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 800
|     Comment: 
|          // DROPDOWN NO CONFLICT
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 128
|     Comment: 
|          // =======================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 435
|     Comment: 
|          // CAROUSEL PLUGIN DEFINITION
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 668
|     Comment: 
|         /* ========================================================================
|          * Bootstrap: dropdown.js v3.2.0
|          * http://getbootstrap.com/javascript/#dropdowns
|          * ========================================================================
|          * Copyright 2011-2014 Twitter, Inc.
|          * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|          * ======================================================================== */
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1324
|     Comment: 
|          // we must check for NaN for ie 8/9
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 436
|     Comment: 
|          // ==========================
|     
|     Path: http://TARGET:80/static/js/bootstrap.js
|     Line number: 1824
|     Comment: 
|          // =====================
|     
|     Path: http://TARGET:80/admin/
|     Line number: 51
|     Comment: 
|          // Ensures jQuery does not pollute the global namespace
|     
|     Path: http://TARGET:80/admin/
|     Line number: 97
|     Comment: 
|         <!-- BREADCRUMBS -->
|     
|     Path: http://TARGET:80/static/js/b

_Trimmed for readability._
