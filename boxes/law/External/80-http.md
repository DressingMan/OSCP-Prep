## NMAP 

```bash
# Nmap 7.94SVN scan initiated Thu Oct 24 16:31:39 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.074s latency).
Scanned at 2024-10-24 16:31:39 EDT for 36s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.56 ((Debian))
|_http-malware-host: Host appears to be clean
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                                            method
|_  http://TARGET:80/htmLawed_README.txt  FORM
|_http-chrono: Request times for /; avg: 459.92ms; min: 385.29ms; max: 582.33ms
| http-headers: 
|   Date: Thu, 24 Oct 2024 20:31:47 GMT
|   Server: Apache/2.4.56 (Debian)
|   Set-Cookie: sid=g73kb4akr1f264tpjibo40u7r6; path=/
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: private, max-age=1800
|   Last-Modified: Tue, 22 Dec 2020 02:17:42 GMT
|   Set-Cookie: sid=vmf638idahlja5td28jabtlc3n; path=/
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: private, max-age=1800
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-grep: 
|   (1) http://TARGET:80/htmLawed_TESTCASE.txt: 
|     (1) email: 
|       + x@y.com
|   (1) http://TARGET:80/htmLawedTest.php: 
|     (1) ip: 
|       + TARGET
|   (2) http://TARGET:80/htmLawed_README.txt: 
|     (2) email: 
|       + a@b.com
|_      + def@abc.com
| http-php-version: Logo query returned unknown hash 62b70acd6aa85859782e36b9d3fd8418
|_Credits query returned unknown hash 112794c9b6b28eb69910c2766f965137
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|_    Couldn't find a file-type field.
|_http-fetch: Please enter the complete path of the directory to save data in.
|_http-date: Thu, 24 Oct 2024 20:31:49 GMT; -1s from local time.
|_http-title: htmLawed (1.2.5) test
|_http-server-header: Apache/2.4.56 (Debian)
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1; htm: 1; txt: 2
|   Longest directory structure:
|     Depth: 0
|     Dir: /
|   Total files found (by extension):
|_    Other: 1; htm: 1; txt: 2
|_http-feed: Couldn't find any feeds.
|_http-referer-checker: Couldn't find any cross-domain scripts.
|_http-drupal-enum: Nothing found amongst the top 100 resources,use --script-args number=<number|all> for deeper analysis)
| http-vhosts: 
|_128 names had status 200
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Form id: 
|     Form action: a
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Form id: 
|     Form action: b
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     Form id: b
|_    Form action: a
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Allowed User Agents: 
|     Mozilla/5.0 (compatible; Nmap Scripting Engine; https://nmap.org/book/nse.html)
|     libwww
|     lwp-trivial
|     libcurl-agent/1.0
|     PHP/
|     GT::WWW
|     Snoopy
|     MFC_Tear_Sample
|     PHPCrawl
|     URI::Fetch
|     Zend_Http_Client
|     http client
|     PECL::HTTP
|     Wget/1.13.4 (linux-gnu)
|_    WWW-Mechanize/1.34
| http-errors: 
| Spidering limited to: maxpagecount=40; withinhost=TARGET
|   Found the following error pages: 
|   
|   Error Code: 404
|   	http://TARGET:80/htmLawedTest.php
|   
|   Error Code: 404
|   	http://TARGET:80/none
|   
|   Error Code: 404
|   	http://TARGET:80/x
|   
|   Error Code: 404
|   	http://TARGET:80/java%20script1alert1
|   
|   Error Code: 404
|   	http://TARGET:80/xxx
|   
|   Error Code: 404
|   	http://TARGET:80/javascript1alert1
|   
|   Error Code: 404
|   	http://TARGET:80/5
|   
|   Error Code: 404
|   	http://TARGET:80/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/link
|   
|   Error Code: 404
|   	http://TARGET:80/4
|   
|   Error Code: 404
|   	http://TARGET:80/home.htm
|   
|   Error Code: 404
|   	http://TARGET:80/b
|   
|   Error Code: 404
|   	http://TARGET:80/b.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/s
|   
|   Error Code: 404
|   	http://TARGET:80/3
|   
|   Error Code: 404
|   	http://TARGET:80/h
|   
|   Error Code: 404
|   	http://TARGET:80/%5CxE2%5Cx80%5Cx83javascript1alert11231
|   
|   Error Code: 404
|   	http://TARGET:80/Psych0tr1a1
|   
|   Error Code: 404
|   	http://TARGET:80/a.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/c.com/d.f
|   
|   Error Code: 404
|   	http://TARGET:80/1
|   
|   Error Code: 404
|_  	http://TARGET:80/3.4.9
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Line number: 424
|     Comment: 
|         /****/
|     
|     Path: http://TARGET:80/htmLawed_README.txt
|     Line number: 1249
|     Comment: 
|          // Remove any duplicate element
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Line number: 428
|     Comment: 
|         /*/*/
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Line number: 205
|     Comment: 
|         <!--check -->
|     
|     Path: http://TARGET:80/htmLawed_TESTCASE.txt
|     Line number: 51
|     Comment: 
|         <!-- comment -->
|     
|     Path: http://TARGET:80/
|     Line number: 37
|     Comment: 
|         <!-- 
|         window.name = 'hlmain';
|         function hl(i){
|           var e = document.getElementById(i);
|          if(!e){return;}
|          run(e, '</[a-z1-6]+>', 'ctag');
|          run(e, '<[a-z]+(?:[^>]*)/>', 'etag');
|          run(e, '<[a-z1-6]+(?:[^>]*)>', 'otag');
|          run(e, '&[#a-z0-9]+;', 'ent');
|          run(e, '<!(?:(?:--(?:.|\n)*?--)|(?:\\[CDATA\\[(?:.|\n)*?\\]\\]))>', 'cmtcdata');
|         }
|         function sndProc(){
|          var f = document.getElementById('testform');
|          if(!f){return;}
|          var e = document.createElement('input');
|          e.type = 'hidden';
|          e.name = 'sid';
|          e.id = 'sid';
|          e.value = readCookie('sid');
|          f.appendChild(e);
|          f.submit();
|         }
|         function readCookie(n){
|          var ne = n + '=';
|          var ca = document.cookie.split(';');
|          for(var i=0;i < ca.length;i++){
|           var c = ca[i];
|           while(c.charAt(0)==' '){
|            c = c.substring(1,c.length);
|           }
|           if(c.indexOf(ne) == 0){
|            return c.substring(ne.length,c.length);
|           }
|          }
|          return null;
|         }
|         function run(e, q, c){
|          var q = new RegExp(q);
|          if(e.firstChild == null){
|           var m = q.exec(e.data);
|           if(m){
|            var v = m[0];
|            var k2 = e.splitText(m.index);
|            var k3 = k2.splitText(v.length);
|            var s = e.ownerDocument.createElement('span');
|            e.parentNode.replaceChild(s, k2);
|            s.className = c; s.appendChild(k2);
|           }
|          }
|          for(var k = e.firstChild; k != null; k = k.nextSibling){
|           if(k.nodeType == 3){     
|            var m = q.exec(k.data);
|            if(m){
|             var v = m[0];
|             var k2 = k.splitText(m.index);
|             var k3 = k2.splitText(v.length);
|             var s = k.ownerDocument.createElement('span');
|             k.parentNode.replaceChild(s, k2);
|             s.className = c; s.appendChild(k2);
|            }
|           }
|           else if(c == 'ent' && k.nodeType == 1){
|            var d = k.firstChild;
|            if(d){
|             var m = q.exec(d.data);
|             if(m){
|              var v = m[0];
|              var d2 = d.splitText(m.index);
|              var d3 = d2.splitText(v.length);
|              var s = d.ownerDocument.createElement('span');
|              d.parentNode.replaceChild(s, d2);
|              s.className = c; s.appendChild(d2);
|             }
|            }
|           }
|          }
|         }
|         function toggle(i){  
|          var e = document.getElementById(i);  
|          if(!e){return;}
|          if(e.style){
|           var a = e.style.display;   
|           if(a == 'block'){e.style.display = 'none'; return;}
|           if(a == 'none'){e.style.display = 'block';}
|           else{e.style.display = 'none';}
|           return;   
|          }
|          var a = e.visibility;
|          if(a == 'hidden'){e.visibility = 'show'; return;}
|          if(a == 'show'){e.visibility = 'hidden';}
|         }
|         function sndProc2(){
|          var i = document.getElementById('text2');
|          if(!i){return;}
|          i = i.value;
|          var w = window.open('htmLawedTest.php?pre=1', 'hlposthtm');
|          var f = document.createElement('form');
|          f.enctype = 'application/x-www-form-urlencoded';
|          f.method = 'post';
|          f.acceptCharset = 'utf-8';
|          if(f.style){f.style.display = 'none';}
|          else{f.visibility = 'hidden';}
|          f.innerHTML = '<p style="display:none;"><input style="display:none;" type="hidden" name="token" id="token" value="e9c88b11a79d2435a273713bddf667d8" /><input style="display:none;" type="hidden" name="sid" id="sid" value="' + readCookie('sid') + '" /></p>';
|          f.action = 'htmLawedTest.php?pre=1';
|          f.target = 'hlposthtm';
|          f.method = 'post';
|          var t = document.createElement('textarea');
|          t.name = 'outputH';
|          t.value = i;
|          f.appendChild(t);
|          var b = document.getElementsByTagName('body')[0];
|          b.appendChild(f);
|          f.submit();
|          w.focus;
|         }
|         function sndUnproc(){
|          var i = document.getElementById('text');
|          if(!i){return;}
|          i = i.value;
|          var w = window.open('htmLawedTest.php?pre=1', 'hlprehtm');
|          var f = document.createElement('form');
|          f.enctype = 'application/x-www-form-urlencoded';
|          f.method = 'post';
|          f.acceptCharset = 'utf-8';
|          if(f.style){f.style.display = 'none';}
|          else{f.visibility = 'hidden';}
|          f.innerHTML = '<p style="display:none;"><input style="display:none;" type="hidden" name="token" id="token" value="e9c88b11a79d2435a273713bddf667d8" /><input style="display:none;" type="hidden" name="sid" id="sid" value="' + readCookie('sid') + '" /></p>';
|          f.action = 'htmLawedTest.php?pre=1';
|          f.target = 'hlprehtm';
|          f.method = 'post';
|          var t = document.createElement('textarea');
|          t.name = 'inputH';
|          t.value = i;
|          f.appendChild(t);
|          var b = document.getElementsByTagName('body')[0];
|          b.appendChild(f);
|          f.submit();
|          w.focus;
|         }
|         function sndValidn(id, type){
|          var i = document.getElementById(id);
|          if(!i){return;}
|          i = i.value;
|          var w = window.open('http://validator.w3.org/check', 'validate'+id+type);
|          var f = document.createElement('form');
|          f.enctype = 'application/x-www-form-urlencoded';
|          f.method = 'post';
|          f.acceptCharset = 'utf-8';
|          if(f.style){f.style.display = 'none';}
|          else{f.visibility = 'hidden';}
|          f.innerHTML = '<p style="display:none;"><input style="display:none;" type="hidden" name="prefill" id="prefill" value="1" /><input style="display:none;" type="hidden" name="prefill_doctype" id="prefill_doctype" value="'+ type+ '" /><input style="display:none;" type="hidden" name="group" id="group" value="1" /><input type="hidden" name="ss" id="ss" value="1" /></p>';
|          f.action = 'http://validator.w3.org/check';
|          f.target = 'validate'+id+type;
|          var t = document.createElement('textarea');
|          t.name = 'fragment';
|          t.value = i;
|          f.appendChild(t);
|          var b = document.getElementsByTagName('body')[0];
|          b.appendChild(f);
|          f.submit();
|          w.focus;
|         }
|         tRs = {
|          formEl: null,
|          resizeClass: 'textarea',
|          adEv: function(t,ev,fn){
|           if(typeof document.addEventListener != 'undefined'){
|            t.addEventListener(ev,fn,false);
|           }else{
|            t.attachEvent('on' + ev, fn);
|           }
|          },
|          rmEv: function(t,ev,fn){
|           if(typeof document.removeEventListener != 'undefined'){
|            t.removeEventListener(ev,fn,false);
|           }else
|           {
|            t.detachEvent('on' + ev, fn);
|           }
|          },
|          adBtn: function(){
|           var textareas = document.getElementsByTagName('textarea');
|           for(var i = 0; i < textareas.length; i++){	
|            var txtclass=textareas[i].className;
|            if(txtclass.substring(0,tRs.resizeClass.length)==tRs.resizeClass ||
|            txtclass.substring(txtclass.length -tRs.resizeClass.length)==tRs.resizeClass){
|             var a = document.createElement('a');
|             a.appendChild(document.createTextNode("\u2195"));
|             a.style.cursor = 'n-resize';
|             a.className= 'resizer';
|             a.title = 'click-drag to resize textarea'
|             tRs.adEv(a, 'mousedown', tRs.initResize);
|             textareas[i].parentNode.appendChild(a);
|            }	
|           }
|          },
|          initResize: function(event){
|           if(typeof event == 'undefined'){
|            event = window.event;
|           }
|           if(event.srcElement){
|            var target = event.srcElement.previousSibling;
|           }else{
|            var target = event.target.previousSibling;
|           }
|           if(target.nodeName.toLowerCase() == 'textarea' || (target.nodeName.toLowerCase() == 'input' && target.type == 'text')){
|            tRs.formEl = target;
|            tRs.formEl.startHeight = tRs.formEl.clientHeight;
|            tRs.formEl.startY = event.clientY;
|            tRs.adEv(document, 'mousemove', tRs.resize);
|            tRs.adEv(document, 'mouseup', tRs.stopResize);
|            tRs.formEl.parentNode.style.cursor = 'n-resize';
|            tRs.formEl.style.cursor = 'n-resize';
|            try{
|             event.preventDefault();
|            }catch(e){
|            }
|           }
|          },
|          resize: function(event){
|           if(typeof event == 'undefined'){
|            event = window.event;
|           }
|         	if(tRs.formEl.nodeName.toLowerCase() == 'textarea'){
|            tRs.formEl.style.height = event.clientY - tRs.formEl.startY + tRs.formEl.startHeight + 'px';
|           }
|          },
|          stopResize: function(event){
|           tRs.rmEv(document, 'mousedown', tRs.initResize);
|           tRs.rmEv(document, 'mousemove', tRs.resize);
|           tRs.formEl.style.cursor = 'text';
|           tRs.formEl.parentNode.style.cursor = 'auto';
|           return false;
|          }
|         };
|         tRs.adEv(window, 'load', tRs.adBtn);
|         // Diff Match and Patch javascript code by Neil Fraser; Apache license 2.0; http://code.google.com/p/google-diff-match-patch/
|         (function(){function diff_match_patch(){this.Diff_Timeout=1;this.Diff_EditCost=4;this.Match_Threshold=0.5;this.Match_Distance=1E3;this.Patch_DeleteThreshold=0.5;this.Patch_Margin=4;this.Match_MaxBits=32}
|         diff_match_patch.prototype.diff_main=function(a,b,c,d){"undefined"==typeof d&&(d=0>=this.Diff_Timeout?Number.MAX_VALUE:(new Date).getTime()+1E3*this.Diff_Timeout);if(null==a||null==b)throw Error("Null input. (diff_main)");if(a==b)return a?0,a:[];"undefined"==typeof c&&(c=!0);var e=c,f=this.diff_commonPrefix(a,b),c=a.substring(0,f),a=a.substring(f),b=b.substring(f),f=this.diff_commonSuffix(a,b),g=a.substring(a.length-f),a=a.substring(0,a.length-f),b=b.substring(0,b.length-f),a=this.diff_compute_(a,
|         b,e,d);c&&a.unshift([0,c]);g&&a.push([0,g]);this.diff_cleanupMerge(a);return a};
|         diff_match_patch.prototype.diff_compute_=function(a,b,c,d){if(!a)return1,b;if(!b)return-1,a;var e=a.length>b.length?a:b,f=a.length>b.length?b:a,g=e.indexOf(f);if(-1!=g)return c=[[1,e.substring(0,g)],[0,f],[1,e.substring(g+f.length)]],a.length>b.length&&(c[0][0]=c[2][0]=-1),c;if(1==f.length)return[[-1,a],[1,b]];return(e=this.diff_halfMatch_(a,b))?(f=e[0],a=e[1],g=e[2],b=e[3],e=e[4],f=this.diff_main(f,g,c,d),c=this.diff_main(a,b,c,d),f.concat(0,e,c)):c&&100<a.length&&100<b.length?this.diff_lineMode_(a,
|         b,d):this.diff_bisect_(a,b,d)};
|         diff_match_patch.prototype.diff_lineMode_=function(a,b,c){var d=this.diff_linesToChars_(a,b),a=d.chars1,b=d.chars2,d=d.lineArray,a=this.diff_main(a,b,!1,c);this.diff_charsToLines_(a,d);this.diff_cleanupSemantic(a);a.push([0,""]);for(var e=d=b=0,f="",g="";b<a.length;){switch(a[b][0]){case 1:e++;g+=a[b][1];break;case -1:d++;f+=a[b][1];break;case 0:if(1<=d&&1<=e){a.splice(b-d-e,d+e);b=b-d-e;d=this.diff_main(f,g,!1,c);for(e=d.length-1;0<=e;e--)a.splice(b,0,d[e]);b+=d.length}d=e=0;g=f=""}b++}a.pop();return a};
|         diff_match_patch.prototype.diff_bisect_=function(a,b,c){for(var d=a.

_Trimmed for readability._
