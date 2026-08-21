## NMAP 

```
# Nmap 7.94SVN scan initiated Fri Jun 21 08:57:42 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.062s latency).
Scanned at 2024-06-21 08:57:43 EDT for 34s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-date: Fri, 21 Jun 2024 12:57:56 GMT; 0s from local time.
| http-php-version: Logo query returned unknown hash 130946e51b01b931b1c277f8e3fc55f5
|_Credits query returned unknown hash 10e437bf2871f151781815ed688c5c4a
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 1
|     Comment: 
|         /*
|         # ------------------ BEGIN LICENSE BLOCK ------------------
|         #
|         # This file is part of PluXml : https://www.pluxml.org
|         #
|         # Package:		theme.css
|         # Copyright (c) 2017-2019 PluXml
|         # Authors		Stephane F., Pedro "P3ter" CADETE., Thomas "sudwebdesign" Ingles.
|         # Licensed under the GPL license.
|         # See http://www.gnu.org/licenses/gpl.html
|         #
|         # ------------------- END LICENSE BLOCK -------------------
|         */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 99
|     Comment: 
|         /* hide sub menu */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 865
|     Comment: 
|         /* Dialog Content */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 455
|     Comment: 
|         /* ---------- NAVIGATION ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 971
|     Comment: 
|         /*for firefox*/
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 952
|     Comment: 
|         /* ---------- GRID, GALLERY, AND HELPER ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 921
|     Comment: 
|         /* ---- select pour fichiers (folding) --- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 667
|     Comment: 
|         /* pour la fen\xC3\xAAtre modale de la visionneuse d'image */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 15
|     Comment: 
|         /* ---------- Authentication ---------- */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 458
|     Comment: 
|         /* Lush Meadow */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 140
|     Comment: 
|         /*	cursor: pointer;*/
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 531
|     Comment: 
|         /* fix old android browser */
|     

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 908
|     Comment: 
|         /* Remove offsets & enlarge (screens>767px) */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 286
|     Comment: 
|         /* ------- Comments ------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 843
|     Comment: 
|         /* Hidden by default */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 537
|     Comment: 
|         /* fix old android browser : good position*/
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 296
|     Comment: 
|         /* Chrome/Opera/Safari */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 179
|     Comment: 
|         /* ------- Pagination ------- */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 593
|     Comment: 
|         /* sub menu icon */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 446
|     Comment: 
|         /* Warm Taupe */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 542
|     Comment: 
|         /* fix hidden sub-menu */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 247
|     Comment: 
|         /* Fontello */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 623
|     Comment: 
|         /*		color: #000;*/
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 129
|     Comment: 
|         /* pluCss1.3.1 fix : plxMyshop 0.13.x, maybe more */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 428
|     Comment: 
|         /* Airy Blue  */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 378
|     Comment: 
|         /* ------- Sidebar ------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 344
|     Comment: 
|         /*Chrome & Safari */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 464
|     Comment: 
|         /* Spicy Mustard */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 573
|     Comment: 
|         /* Pagination */
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 6
|     Comment: 
|          // Safari<1.2, Konqueror
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 976
|     Comment: 
|         /*for IE10*/
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 16
|     Comment: 
|         /* ---------- RESET CSS ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 876
|     Comment: 
|         /* The Close Button */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 847
|     Comment: 
|         /* Sit on top */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 970
|     Comment: 
|         /*for chrome*/
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 342
|     Comment: 
|         /* Mozilla, since 1999 */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 931
|     Comment: 
|         /* Fonctionne uniquement avec Firefox */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 915
|     Comment: 
|         /* ----------- Drag and Drop for sorting table rows ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 521
|     Comment: 
|         /* fix old android browser (always open) */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 115
|     Comment: 
|         /* ---------- Section ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 861
|     Comment: 
|         /* Black w/ opacity */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 859
|     Comment: 
|         /* Fallback color */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 899
|     Comment: 
|         /* ---------- HELPER ---------- */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 470
|     Comment: 
|         /* Potter's Clay */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 849
|     Comment: 
|         /* Location of the box */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 761
|     Comment: 
|         /* gestion des themes */
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 7
|     Comment: 
|          // Older Mozilla and Firefox
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 855
|     Comment: 
|         /* Full height */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 853
|     Comment: 
|         /* Full width */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 857
|     Comment: 
|         /* Enable scroll if needed */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 486
|     Comment: 
|         /* ---------- Footer ---------- */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 119
|     Comment: 
|         /* \/ menu */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 35
|     Comment: 
|         /* ---------- Header ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 313
|     Comment: 
|         /* ---------- TABLE ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 308
|     Comment: 
|         /* Firefox 18- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 840
|     Comment: 
|         /* The Dialog (background) */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 34
|     Comment: 
|         /* ---------- Main ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 794
|     Comment: 
|         /* champs de recherche */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 300
|     Comment: 
|         /* Firefox 19+ */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 784
|     Comment: 
|         /* image d'accroche */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 510
|     Comment: 
|         /*Removes default chrome and safari style*/
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 1
|     Comment: 
|         /* Visual Effects */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 434
|     Comment: 
|         /* Sharkskin  */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 515
|     Comment: 
|         /*Position of the background-image*/
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 418
|     Comment: 
|         /* https://www.w3schools.com/colors/colors_trends.asp (The 10 Hottest Fall Colors for 2016) */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 609
|     Comment: 
|         /* pour l'indentation des commentaires */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 508
|     Comment: 
|         /*Removes border*/
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 350
|     Comment: 
|         /* css-3 */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 452
|     Comment: 
|         /* Dusty Cedar */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 390
|     Comment: 
|         /* masquer */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 352
|     Comment: 
|         /* Internet Explorer 5.5+ */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 397
|     Comment: 
|         /* afficher */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 348
|     Comment: 
|         /* Opera 7 */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 482
|     Comment: 
|         /* Snorkel Blue */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 213
|     Comment: 
|         /* ------- Article ------- */
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 5
|     Comment: 
|          // IE/Win
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 422
|     Comment: 
|         /* Riverside  */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 40
|     Comment: 
|         /* ---------- Aside ---------- */
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 8
|     Comment: 
|          // Safari 1.2, newer Firefox and Mozilla, CSS3
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 90
|     Comment: 
|         /* sub menu */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 573
|     Comment: 
|         /* responsive slide is in 3 */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 803
|     Comment: 
|         /* gestionnaire de m\xC3\xA9dias */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 155
|     Comment: 
|         /*	background-color: rgba(255,255,255,.55);*/
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 396
|     Comment: 
|         /* --------- tags ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 1
|     Comment: 
|         /*
|         # ------------------ BEGIN LICENSE BLOCK ------------------
|         #
|         # This file is part of PluXml : https://www.pluxml.org
|         #
|         # Package:		theme.css
|         # Copyright (c) 2019 PluXml
|         # Authors		Jos, Stephane F., Pedro "P3ter" CADETE
|         # Licensed under the GPL license.
|         # See http://www.gnu.org/licenses/gpl.html
|         #
|         # ------------------- END LICENSE BLOCK -------------------
|         */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 1
|     Comment: 
|         /*
|         # ------------------ BEGIN LICENSE BLOCK ------------------
|         #
|         # This file is part of PluXml : http://www.pluxml.org
|         #
|         # Package		plucss.css
|         # Version		1.3.1
|         # Copyright (c)	2014-2019 PluXml
|         # Authors		Jos, St\xC3\xA9phane F, sudwebdesign, Pedro "P3ter" CADETE
|         # Licensed under the GPL license.
|         # See http://www.gnu.org/licenses/gpl.html
|         #
|         # ------------------- END LICENSE BLOCK -------------------
|         */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 476
|     Comment: 
|         /* Aurora Red */
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 616
|     Comment: 
|         /*		text-decoration: underline; */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 200
|     Comment: 
|         /* ---------- TYPOGRAPHY ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 512
|     Comment: 
|         /*Removes default style Firefox*/
|     
|     Path: http://TARGET:80/themes/defaut/css/theme.css?v=5.8.7
|     Line number: 440
|     Comment: 
|         /* Bodacious */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 304
|     Comment: 
|         /* IE 10+ */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 845
|     Comment: 
|         /* Stay in place */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 327
|     Comment: 
|         /* ---------- FORM ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 980
|     Comment: 
|         /* ---- parametres_plugins ---- */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 604
|     Comment: 
|         /* ---------- OTHER COMPONENTS ---------- */
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 654
|     Comment: 
|         /* This will render the 'X' */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 346
|     Comment: 
|         /* Opera 4-6 */
|     
|     Path: http://TARGET:80/core/lib/visual.js?v=5.8.7
|     Line number: 3
|     Comment: 
|          // hack IE
|     
|     Path: http://TARGET:80/core/admin/theme/plucss.css?v=5.8.7
|     Line number: 810
|     Comment: 
|         /* -- Tooltip -- */
|     
|     Path: http://TARGET:80/core/admin/theme/theme.css?v=5.8.7
|     Line number: 892
|     Comment: 
|_        /* ------- Popup Medias Manager ------ */
| http-headers: 
|   Date: Fri, 21 Jun 2024 12:57:56 GMT
|   Server: Apache/2.4.56 (Debian)
|   Set-Cookie: PHPSESSID=REDACTED; path=/; domain=TARGET; HttpOnly
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: no-cache
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: 
|     Header: Pragma: no-cache
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-vhosts: 
| http-enum: 
|   /core/: Potentially interesting folder
|   /data/: Potenti

_Trimmed for readability._
