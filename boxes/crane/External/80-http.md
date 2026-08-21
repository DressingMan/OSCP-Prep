## NMAP 

```bash
# Nmap 7.94SVN scan initiated Mon Oct 14 10:32:51 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.059s latency).
Scanned at 2024-10-14 10:32:52 EDT for 94s

PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 61 Apache httpd 2.4.38 ((Debian))
| http-security-headers: 
|   Cache_Control: 
|     Header: Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: 
|     Header: Pragma: no-cache
|   Expires: 
|_    Header: Expires: Thu, 19 Nov 1981 08:52:00 GMT
| http-title: SuiteCRM
|_Requested resource was index.php?action=Login&module=Users
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
|_http-favicon: Unknown favicon MD5: ED9A8C7810E8C9FB7035B6C3147C9A3A
| http-headers: 
|   Date: Mon, 14 Oct 2024 14:33:05 GMT
|   Server: Apache/2.4.38 (Debian)
|   Set-Cookie: PHPSESSID=REDACTED; path=/
|   Expires: Thu, 19 Nov 1981 08:52:00 GMT
|   Cache-Control: no-store, no-cache, must-revalidate
|   Pragma: no-cache
|   Set-Cookie: sugar_user_theme=SuiteP; expires=Tue, 14-Oct-2025 14:33:05 GMT; Max-Age=31536000; HttpOnly
|   Connection: close
|   Content-Type: text/html; charset=UTF-8
|   
|_  (Request type: HEAD)
|_http-vuln-cve2017-1001000: ERROR: Script execution failed (use -d to debug)
| http-vhosts: 
|_128 names had status 301
| http-waf-detect: IDS/IPS/WAF detected:
|_192.168.158.146:80/?p4yl04d3=<script>alert(document.cookie)</script>
| http-php-version: Logo query returned unknown hash 76f37b38832eb32b2da1546fa338bb6c
|_Credits query returned unknown hash 76f37b38832eb32b2da1546fa338bb6c
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
| http-robots.txt: 1 disallowed entry 
|_/
| http-sql-injection: 
|   Possible sqli for queries:
|     http://TARGET:80/cache/include/javascript/index.php?themeName=%27%20OR%20sqlspider&entryPoint=getImage
|     http://TARGET:80/cache/include/javascript/index.php?themeName=&entryPoint=getImage%27%20OR%20sqlspider
|     http://TARGET:80/vendor/tinymce/tinymce/Xt._addCacheSuffix1t11o.onload1function11%7Ba.remove1i11o111o.onreadystatechange1o.onload1o1null11n11%7D1o.onerror1function11%7BAi1r1?r%28%29%3A%22undefined%22%21=typeof%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/Selector.getters.rel1Selector.getters.href;if(Selector.useNative&&Y_DOC.querySelector){Selector.shorthand["\\.([^\\s\\\\(\\[:]*)"]="[class~=$1]";}Selector._reNth=/^(?%3A%28%5B%5C-%5D%3F%5Cd%2A%29%28n%29%7B1%7D%7C%28odd%7Ceven%29%24%29%2A%28%5B%5C-%2B%5D%3F%5Cd%2A%29%24%2F%3BSelector._getNth=function%28d%2Co%2Cq%2Ch%29%7BSelector._reNth.test%28o%29%3Bvar%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=S%3BO%3DA%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=N%3BO%3DD%27%20OR%20sqlspider
|     http://TARGET:80/cache/include/javascript/?C=D%3BO%3DA%27%20OR%20sqlspider
|_    http://TARGET:80/cache/include/javascript/?C=M%3BO%3DA%27%20OR%20sqlspider
|_http-fetch: Please enter the complete path of the directory to save data in.
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-devframework: Couldn't determine the underlying framework or CMS. Try increasing 'httpspider.maxpagecount' value to spider more pages.
|_http-date: Mon, 14 Oct 2024 14:33:06 GMT; -1s from local time.
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://TARGET:80/
|     Form id: form
|     Form action: index.php
|     
|     Path: http://TARGET:80/index.php
|     Form id: form
|_    Form action: index.php
|_http-malware-host: Host appears to be clean
|_http-server-header: Apache/2.4.38 (Debian)
|_http-mobileversion-checker: No mobile version detected.
| http-fileupload-exploiter: 
|   
|     Couldn't find a file-type field.
|   
|_    Couldn't find a file-type field.
| http-grep: 
|   (1) http://TARGET:80/include/javascript/calendar.js?v=WWrZLHR9Ay2yH7WcEIhRuA: 
|     (1) email: 
|       + contact@sugarcrm.com
|   (1) http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA: 
|     (1) email: 
|       + carl.ogren@gmail.com
|   (1) http://TARGET:80/cache/include/javascript/: 
|     (1) ip: 
|_      + TARGET

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
| http-useragent-tester: 
|   Status for browser useragent: 200
|   Redirected To: index.php?action=Login&module=Users
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
|   /robots.txt: Robots file
|   /crossdomain.xml: Adobe Flash crossdomain policy
|   /cache/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /custom/: Potentially interesting folder
|   /data/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /include/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /install/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /lib/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /modules/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /service/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /soap/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /themes/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
|   /upload/: Potentially interesting folder
|_  /vendor/: Potentially interesting directory w/ listing on 'apache/2.4.38 (debian)'
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
| http-referer-checker: 
| Spidering limited to: maxpagecount=30
|   https://oss.maxcdn.com:443/respond/1.4.2/respond.min.js
|_  https://oss.maxcdn.com:443/html5shiv/3.7.2/html5shiv.min.js
| http-auth-finder: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|   url                                  method
|   http://TARGET:80/           FORM
|_  http://TARGET:80/index.php  FORM
| http-sitemap-generator: 
|   Directory structure:
|     /
|       Other: 1
|     /cache/include/javascript/
|       Other: 1; js: 4
|     /include/javascript/
|       js: 1
|     /include/javascript/qtip/
|       css: 1
|     /modules/Users/
|       css: 1; js: 1
|     /themes/SuiteP/css/
|       css: 4; php: 1
|     /themes/SuiteP/images/
|       ico: 1
|     /themes/SuiteP/js/
|       js: 1
|     /themes/default/images/
|       png: 1
|     /vendor/tinymce/tinymce/
|       js: 1
|   Longest directory structure:
|     Depth: 3
|     Dir: /themes/SuiteP/css/
|   Total files found (by extension):
|_    Other: 2; css: 6; ico: 1; js: 8; php: 1; png: 1
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 3557
|     Comment: 
|         /**
|         			 * Whether or not this is a hidden filter.
|         			 * @instance
|         			 * @type {boolean}
|         			 */
|     
|     Path: http://TARGET:80/index.php
|     Line number: 205
|     Comment: 
|          // fix for campaign wizard
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4697
|     Comment: 
|         /**
|         			 * The destroy.ft.sorting event is raised before its UI is removed.
|         			 * Calling preventDefault on this event will prevent the component from being destroyed.
|         			 * @event FooTable.Sorting#"destroy.ft.sorting"
|         			 * @param {jQuery.Event} e - The jQuery.Event object for the event.
|         			 * @param {FooTable.Table} ft - The instance of the plugin raising the event.
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4469
|     Comment: 
|         /**
|         	 * Whether or not the column can be used during filtering. Added by the {@link FooTable.Filtering} component.
|         	 * @type {boolean}
|         	 * @default true
|         	 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 3625
|     Comment: 
|         /**
|         			 * The delay in milliseconds before the query is auto applied after a change.
|         			 * @instance
|         			 * @type {number}
|         			 */
|     
|     Path: http://TARGET:80/themes/SuiteP/css/normalize.css
|     Line number: 69
|     Comment: 
|         /* 1 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 6549
|     Comment: 
|         /**
|         	 * Updates a row in the underlying {@link FooTable.Rows#all} array.
|         	 * @param {(number|FooTable.Row)} indexOrRow - The index to update or the actual {@link FooTable.Row} object.
|         	 * @param {object} data - A hash containing the new row values.
|         	 * @param {boolean} [redraw=true] - Whether or not to redraw the table, defaults to true but for bulk operations this
|         	 * can be set to false and then followed by a call to the {@link FooTable.Table#draw} method.
|         	 */
|     
|     Path: http://TARGET:80/index.php
|     Line number: 160
|     Comment: 
|         /**
|            * Password reset screen validation
|            */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 684
|     Comment: 
|         /**
|         	 * Escapes a string for use in a regular expression.
|         	 * @memberof FooTable.str
|         	 * @function escapeRegExp
|         	 * @param {string} str - The string to escape.
|         	 * @returns {string}
|         	 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 5864
|     Comment: 
|         /**
|         			 * The text that appears in the view button. This can contain HTML.
|         			 * @type {string}
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 1026
|     Comment: 
|         /**
|         		 * The cell class containing all the properties for cells.
|         		 * @constructs
|         		 * @extends FooTable.Class
|         		 * @param {FooTable.Table} table -  The root {@link FooTable.Table} this cell belongs to.
|         		 * @param {FooTable.Row} row - The parent {@link FooTable.Row} this cell belongs to.
|         		 * @param {FooTable.Column} column - The {@link FooTable.Column} this cell falls under.
|         		 * @param {(*|HTMLElement|jQuery)} valueOrElement - Either the value or the element for the cell.
|         		 * @returns {FooTable.Cell}
|         		 * @this FooTable.Cell
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 7299
|     Comment: 
|          //look for all subnavs and set them up
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 6691
|     Comment: 
|         /**
|         		 * Clears the state value for the specified key for this table.
|         		 * @instance
|         		 * @param {string} key - The key to clear the value for.
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4652
|     Comment: 
|         /**
|         		 * Initializes the sorting component for the plugin using the supplied table and options.
|         		 * @instance
|         		 * @protected
|         		 * @fires FooTable.Sorting#"init.ft.sorting"
|         		 * @this FooTable.Sorting
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4397
|     Comment: 
|         /**
|         		 * Parses a single part of a query into an object to use during matching.
|         		 * @param {string} str - The string representation of the part.
|         		 * @returns {{query: string, negate: boolean, phrase: boolean, exact: boolean}}
|         		 * @private
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4902
|     Comment: 
|         /**
|         	 * The direction to sort if the {@link FooTable.Column#sorted} property is set to true. Can be "ASC", "DESC" or NULL. Added by the {@link FooTable.Sorting} component.
|         	 * @type {string}
|         	 * @default null
|         	 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 4305
|     Comment: 
|         /**
|         		 * Matches this queries parts array against the supplied string.
|         		 * @param {string} str - The string to test.
|         		 * @param {boolean} def - The default value to return based on the operand.
|         		 * @returns {boolean}
|         		 * @private
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 7633
|     Comment: 
|         /* End of File include/javascript/jquery/jquery.showLoading.js */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 1183
|     Comment: 
|         /**
|         		 * Helper method to call this cell's column formatter function using the supplied value and any additional required parameters.
|         		 * @instance
|         		 * @protected
|         		 * @param {*} value - The value to format.
|         		 * @returns {(string|HTMLElement|jQuery)}
|         		 * @see FooTable.Column#formatter
|         		 * @this FooTable.Cell
|         		 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 3318
|     Comment: 
|         /**
|         			 * The preinit.ft.rows event is raised before any UI is created and provides the tables jQuery data object for additional options parsing.
|         			 * Calling preventDefault on this event will disable the entire plugin.
|         			 * @event FooTable.Rows#"preinit.ft.rows"
|         			 * @param {jQuery.Event} e - The jQuery.Event object for the event.
|         			 * @param {FooTable.Table} ft - The instance of the plugin raising the event.
|         			 * @param {object} data - The jQuery data object of the table raising the event.
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 500
|     Comment: 
|         /**
|         	 * This is a simple check to determine if an object is a jQuery promise object. It simply checks the object has a "then" and "promise" function defined.
|         	 * The promise object is created as an object literal inside of jQuery.Deferred.
|         	 * It has no prototype, nor any other truly unique properties that could be used to distinguish it.
|         	 * This method should be a little more accurate than the internal jQuery one that simply checks for a "promise" method.
|         	 * @memberof FooTable.is
|         	 * @function promise
|         	 * @param {object} obj - The object to check.
|         	 * @returns {boolean}
|         	 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 6623
|     Comment: 
|         /**
|         			 * Whether or not to allow the paging component to store it's state.
|         			 * @type {boolean}
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 3833
|     Comment: 
|         /**
|         			 * The destroy.ft.filtering event is raised before its UI is removed.
|         			 * Calling preventDefault on this event will prevent the component from being destroyed.
|         			 * @event FooTable.Filtering#"destroy.ft.filtering"
|         			 * @param {jQuery.Event} e - The jQuery.Event object for the event.
|         			 * @param {FooTable.Table} ft - The instance of the plugin raising the event.
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 1345
|     Comment: 
|         /**
|         			 * The name of the column. This name must correspond to the property name of the JSON row data.
|         			 * @type {string}
|         			 * @default null
|         			 */
|     
|     Path: http://TARGET:80/cache/include/javascript/sugar_grp1_jquery.js?v=WWrZLHR9Ay2yH7WcEIhRuA
|     Line number: 1413
|     Comment: 
|         /**
|         		 * Creates a cell for this column from the supplied {@link FooTable.Row} object. This allows different column types to return different types of cells.
|         		 * @instance
|         		 * @protected
|         		 * @param {FooTable.Row} row - The row to create the cell from.
|         

_Trimmed for readability._
