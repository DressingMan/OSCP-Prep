## NMAP 

```bash
# Nmap 7.94SVN scan initiated Sat Jul 27 21:38:38 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.053s latency).
Scanned at 2024-07-27 21:38:39 EDT for 35s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 125 Apache httpd 2.4.48 ((Win64) OpenSSL/1.1.1k PHP/8.0.7)
|_http-server-header: Apache/2.4.48 (Win64) OpenSSL/1.1.1k PHP/8.0.7
|_http-title: Access The Event
| http-php-version: Logo query returned unknown hash b42d3147977e3c7d78cb765a2fd33682
|_Credits query returned unknown hash b42d3147977e3c7d78cb765a2fd33682
|_http-favicon: Unknown favicon MD5: FED84E16B6CCFE88EE7FFAAE5DFEFD34
|_http-exif-spider: ERROR: Script execution failed (use -d to debug)
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-date: Sun, 28 Jul 2024 01:38:46 GMT; -1s from local time.
| http-headers: 
|   Date: Sun, 28 Jul 2024 01:38:45 GMT
|   Server: Apache/2.4.48 (Win64) OpenSSL/1.1.1k PHP/8.0.7
|   Last-Modified: Mon, 11 Oct 2021 13:26:28 GMT
|   ETag: "c210-5ce13ad22e900"
|   Accept-Ranges: bytes
|   Content-Length: 49680
|   Connection: close
|   Content-Type: text/html
|   
|_  (Request type: HEAD)
| http-vhosts: 
|_128 names had status 200
| http-methods: 
|   Supported Methods: POST OPTIONS HEAD GET TRACE
|_  Potentially risky methods: TRACE
| http-fileupload-exploiter: 
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|     Failed to upload and execute a payload.
|   
|_    Failed to upload and execute a payload.
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 44
|     Comment: 
|         <!-- Uncomment below if you prefer to use a text logo -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 12
|     Comment: 
|         <!-- Favicons -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 944
|     Comment: 
|         <!-- End Buy Ticket Section -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 166
|     Comment: 
|         /*--------------------------------------------------------------
|         # Buy Tickets
|         --------------------------------------------------------------*/
|     

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     Path: http://TARGET:80/index.html
|     Line number: 730
|     Comment: 
|         <!-- End Sponsors Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 666
|     Comment: 
|         <!-- End Gallery Section -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 88
|     Comment: 
|         /* Sections Header
|         --------------------------------*/
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 19
|     Comment: 
|         <!-- Vendor CSS Files -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 827
|     Comment: 
|         <!-- End Subscribe Section -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 195
|     Comment: 
|         <!-- End  Footer -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 642
|     Comment: 
|         <!-- ======= Gallery Section ======= -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 83
|     Comment: 
|         <!-- End Header -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 29
|     Comment: 
|         
|         
|         
|         
|         
|           ======================================================== -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 946
|     Comment: 
|         <!-- ======= Contact Section ======= -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 124
|     Comment: 
|         <!-- ======= Footer ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 807
|     Comment: 
|         <!-- End  F.A.Q Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 399
|     Comment: 
|         <!-- Schdule Day 3 -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 871
|     Comment: 
|         /*--------------------------------------------------------------
|         # Hotels Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 8
|     Comment: 
|         /*--------------------------------------------------------------
|         # General
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 247
|     Comment: 
|         <!-- Schdule Day 1 -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 940
|     Comment: 
|         <!-- /.modal-content -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 829
|     Comment: 
|         <!-- ======= Buy Ticket Section ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 308
|     Comment: 
|         /**
|         * Mobile Navigation 
|         */
|     
|     Path: http://TARGET:80/assets/vendor/php-email-form/validate.js
|     Line number: 1
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/index.html
|     Line number: 576
|     Comment: 
|         <!-- ======= Hotels Section ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 198
|     Comment: 
|         /**
|         * Desktop Navigation 
|         */
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 1103
|     Comment: 
|         /*--------------------------------------------------------------
|         # Buy Tickets Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 327
|     Comment: 
|         <!-- Schdule Day 2 -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 39
|     Comment: 
|         <!-- ======= Header ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 1165
|     Comment: 
|         /*--------------------------------------------------------------
|         # Contact Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 881
|     Comment: 
|         <!-- Pro Tier -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 118
|     Comment: 
|         <!-- ======= Speakers Section ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 46
|     Comment: 
|         /* Prelaoder */
|     
|     Path: http://TARGET:80/index.html
|     Line number: 96
|     Comment: 
|         <!-- ======= About Section ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 668
|     Comment: 
|         <!-- ======= Supporters Section ======= -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 122
|     Comment: 
|         <!-- End #main -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 1
|     Comment: 
|         
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/index.html
|     Line number: 92
|     Comment: 
|         <!-- End Hero Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 220
|     Comment: 
|         <!-- End Speakers Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 640
|     Comment: 
|         <!-- End Hotels Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 477
|     Comment: 
|         <!-- ======= Venue Section ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 957
|     Comment: 
|         /*--------------------------------------------------------------
|         # Sponsors Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 942
|     Comment: 
|         <!-- /.modal -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 199
|     Comment: 
|         <!-- Vendor JS Files -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 919
|     Comment: 
|         /*--------------------------------------------------------------
|         # Gallery Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 206
|     Comment: 
|         <!-- Template Main JS File -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 475
|     Comment: 
|         <!-- End Schedule Section -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 45
|     Comment: 
|         <!-- <h1><a href="index.html">The<span>Event</span></a></h1>-->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 1292
|     Comment: 
|         /*--------------------------------------------------------------
|         # Footer
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 87
|     Comment: 
|         <!-- ======= Speaker Details Sectionn ======= -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 1041
|     Comment: 
|         /*--------------------------------------------------------------
|         # Subscribe Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 986
|     Comment: 
|         /*--------------------------------------------------------------
|         # F.A.Q Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 125
|     Comment: 
|         /*--------------------------------------------------------------
|         # Header
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 812
|     Comment: 
|         /*--------------------------------------------------------------
|         # Venue Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 16
|     Comment: 
|         <!-- Google Fonts -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 186
|     Comment: 
|         
|         
|         
|         
|         
|               -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 710
|     Comment: 
|         /*--------------------------------------------------------------
|         # Schedule Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 621
|     Comment: 
|         /*--------------------------------------------------------------
|         # Speakers Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 577
|     Comment: 
|         /*--------------------------------------------------------------
|         # About Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 809
|     Comment: 
|         <!-- ======= Subscribe Section ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 222
|     Comment: 
|         <!-- ======= Schedule Section ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 325
|     Comment: 
|         <!-- End Schdule Day 1 -->
|     
|     Path: http://TARGET:80/assets/vendor/swiper/swiper-bundle.min.js
|     Line number: 1
|     Comment: 
|         /**
|          * Swiper 7.0.8
|          * Most modern mobile touch slider and framework with hardware accelerated transitions
|          * https://swiperjs.com
|          *
|          * Copyright 2014-2021 Vladimir Kharlampidi
|          *
|          * Released under the MIT License
|          *
|          * Released on: October 4, 2021
|          */
|     
|     Path: http://TARGET:80/index.html
|     Line number: 85
|     Comment: 
|         <!-- ======= Hero Section ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 116
|     Comment: 
|         <!-- End About Section -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 941
|     Comment: 
|         <!-- /.modal-dialog -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 26
|     Comment: 
|         <!-- Template Main CSS File -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 59
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|         
|                 </li> -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 574
|     Comment: 
|         <!-- End Venue Section -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 401
|     Comment: 
|         /*--------------------------------------------------------------
|         # Hero Section
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/index.html
|     Line number: 732
|     Comment: 
|         <!-- =======  F.A.Q Section ======= -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 397
|     Comment: 
|         <!-- End Schdule Day 2 -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 908
|     Comment: 
|         <!-- Modal Order Form -->
|     
|     Path: http://TARGET:80/index.html
|     Line number: 1010
|     Comment: 
|         <!-- End Contact Section -->
|     
|     Path: http://TARGET:80/speaker-details.html
|     Line number: 79
|     Comment: 
|         <!-- .navbar -->
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 195
|     Comment: 
|         /*--------------------------------------------------------------
|         # Navigation Menu
|         --------------------------------------------------------------*/
|     
|     Path: http://TARGET:80/assets/css/style.css
|     Line number: 58
|     Comment: 
|         /*--------------------------------------------------------------
|         # Back to top button
|_        --------------------------------------------------------------*/
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /assets/css/
|       css: 1
|     /assets/img/gallery/
|       jpg: 4
|     /assets/img/hotels/
|       jpg: 1
|     /assets/img/speakers/
|       jpg: 3
|     /assets/img/supporters/
|       png: 1
|     /assets/img/venue-gallery/
|       jpg: 3
|     /assets/js/
|       js: 1
|     /assets/vendor/aos/
|       css: 1
|     /assets/vendor/bootstrap-icons/
|       css: 1
|     /assets/vendor/php-email-form/
|       js: 1
|     /assets/vendor/swiper/
|       js: 1
|     /forms/
|       php: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /assets/vendor/aos/
|   Total files found (by extension):
|_    Other: 1; css: 3; jpg: 11; js: 3; php: 1; png: 1
| http-trace: TRACE is enabled
| Headers:
| Date: Sun, 28 Jul 2024 01:38:46 GMT
| Server: Apache/2.4.48 (Win64) OpenSSL/1.1.1k PHP/8.0.7
| Connection: close
| Transfer-Encoding: chunked
| http-enum: 
|   /forms/: Potentially interesting directory w/ listing on 'apache/2.4.48 (win64) openssl/1.1.1k php/8.0.7'
|   /icons/: Potentially interesting folder w/ directory listing
|_  /uploads/: Potentially interesting directory w/ listing on 'apache/2.4.48 (win64) openssl/1.1.1k php/8.0.7'
| http-grep: 
|   (1) http://TARGET:80/: 
|     (1) email: 
|_      + info@example.com
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
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/
|     Form id: 
|     Form action: #
|     
|     Path: http://TARGET:80/
|     Form id: ticket-type
|     Form action: /Ticket.php
|     
|

_Trimmed for readability._
