## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 21 15:59:40 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-10-21 15:59:40 EDT for 46s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1688
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1899
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 24
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 5407
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2687
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2887
|     Comment: 
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/css/templatemo-lugx-gaming.css
|     Line number: 281
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2000
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 163
|     Comment: 
|         <!-- Scripts -->
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1408
|     Comment: 
|         
|         
|         
|         
|         
|         	 */

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     
|     Path: http://TARGET:80/assets/css/templatemo-lugx-gaming.css
|     Line number: 112
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2489
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 33
|     Comment: 
|         <!-- ***** Preloader Start ***** -->
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 65
|     Comment: 
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2880
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1064
|     Comment: 
|         
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1075
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2802
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1049
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 74
|     Comment: 
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1779
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 59
|     Comment: 
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 6
|     Comment: 
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3168
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 68
|     Comment: 
|         <!-- ***** Menu End ***** -->
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 975
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1040
|     Comment: 
|         
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 6682
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1174
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1009
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 8007
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2118
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1018
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1713
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 4160
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2846
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 663
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 541
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 7323
|     Comment: 
|         /* eslint-enable no-cond-assign */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2273
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
|         			*/
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1956
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1239
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 940
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 74
|     Comment: 
|         <!-- ***** Header Area End ***** -->
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2578
|     Comment: 
|         /* Internal Use Only */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 877
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 5447
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 4943
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 77
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 3233
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1544
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1786
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1342
|     Comment: 
|         
|         	---------------------------------------------------------------------- */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 3975
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 966
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3253
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 3979
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2632
|     Comment: 
|         
|         
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 84
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 6941
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1223
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 5593
|     Comment: 
|         /* eslint-disable max-len */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 500
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
|          */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2406
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/css/owl.css
|     Line number: 32
|     Comment: 
|         /* fix for flashing background */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3431
|     Comment: 
|         /* jshint -W053 */
|     
|     Path: http://TARGET:80/assets/css/templatemo-lugx-gaming.css
|     Line number: 1108
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1282
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2744
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 816
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1766
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 624
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 477
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 97
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2696
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 753
|     Comment: 
|         
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2313
|     Comment: 
|         
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/css/owl.css
|     Line number: 13
|     Comment: 
|         /* position relative and z-index fix webkit rendering fonts issue */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1044
|     Comment: 
|         
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2902
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2393
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/css/owl.css
|     Line number: 144
|     Comment: 
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 5514
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 164
|     Comment: 
|         <!-- Bootstrap core JavaScript -->
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 2181
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 4168
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1661
|     Comment: 
|         
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 6
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
|          */
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 72
|     Comment: 
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3034
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
|         		});*/
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 39
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1224
|     Comment: 
|         
|         	---------------------------------------------------------------------- */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1022
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/contact.html
|     Line number: 22
|     Comment: 
|         
|         
|         
|         
|         
|         
|         -->
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3243
|     Comment: 
|         
|         
|         
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 8216
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 77
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 1577
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 7336
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 1793
|     Comment: 
|         
|         
|         
|         
|         		 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 260
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 8220
|     Comment: 
|         
|         
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3180
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 3212
|     Comment: 
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 2608
|     Comment: 
|         
|         
|         
|         
|         
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/css/templatemo-lugx-gaming.css
|     Line number: 647
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 962
|     Comment: 
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/js/counter.js
|     Line number: 20
|     Comment: 
|         
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 898
|     Comment: 
|         
|         
|         
|         
|          */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 510
|     Comment: 
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/assets/css/templatemo-lugx-gaming.css
|     Line number: 23
|     Comment: 
|         
|         
|         
|         
|         */
|     
|     Path: http://TARGET:80/assets/js/owl-carousel.js
|     Line number: 726
|     Comment: 
|         
|         
|         
|         
|         
|         	 */
|     
|     Path: http://TARGET:80/vendor/jquery/jquery.slim.js
|     Line number: 3203
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

_Trimmed for readability._
