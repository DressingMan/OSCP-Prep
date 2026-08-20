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

_Trimmed: original note was a full nmap/http-script dump. Open ports, titles, and attack notes are above._
