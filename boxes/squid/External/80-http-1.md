## NMAP 

```bash

```

## CURL 

```bash
HTTP/1.1 400 Bad Request
Server: squid/4.14
Mime-Version: 1.0
Date: Wed, 24 Jul 2024 22:01:46 GMT
Content-Type: text/html;charset=utf-8
Content-Length: 3394
X-Squid-Error: ERR_INVALID_URL 0
Vary: Accept-Language
Content-Language: en
X-Cache: MISS from SQUID
Via: 1.1 localhost (squid/4.14)
Connection: close

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html><head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>ERROR: The requested URL could not be retrieved</title>
<style type="text/css"><!--
 /*
 * Copyright (C) 1996-2021 The Squid Software Foundation and contributors
 *
 * Squid software is distributed under GPLv2+ license and includes
 * contributions from numerous individuals and organizations.
 * Please see the COPYING and CONTRIBUTORS files for details.
 */

/*
 Stylesheet for Squid Error pages
 Adapted from design by Free CSS Templates
 http://www.freecsstemplates.org
 Released for free under a Creative Commons Attribution 2.5 License
*/

/* Page basics */
* {
	font-family: verdana, sans-serif;
}

html body {
	margin: 0;
	padding: 0;
	background: #efefef;
	font-size: 12px;
	color: #1e1e1e;
}

/* Page displayed title area */
#titles {
	margin-left: 15px;
	padding: 10px;
	padding-left: 100px;
	background: url('/squid-internal-static/icons/SN.png') no-repeat left;
}

/* initial title */
#titles h1 {
	color: #000000;
}
#titles h2 {
	color: #000000;
}

/* special event: FTP success page titles */
#titles ftpsuccess {
	background-color:#00ff00;
	width:100%;
}

/* Page displayed body content area */
#content {
	padding: 10px;
	background: #ffffff;
}

/* General text */
p {
}

/* error brief description */
#error p {
}

/* some data which may have caused the problem */
#data {
}

/* the error message received from the system or other software */
#sysmsg {
}

pre {
}

/* special event: FTP / Gopher directory listing */
#dirmsg {
    font-family: courier, monospace;
    color: black;
    font-size: 10pt;
}
#dirlisting {
    margin-left: 2%;
    margin-right: 2%;
}
#dirlisting tr.entry td.icon,td.filename,td.size,td.date {
    border-bottom: groove;
}
#dirlisting td.size {
    width: 50px;
    text-align: right;
    padding-right: 5px;
}

/* horizontal lines */
hr {
	margin: 0;
}

/* page displayed footer area */
#footer {
	font-size: 9px;
	padding-left: 10px;
}

body
:lang(fa) { direction: rtl; font-size: 100%; font-family: Tahoma, Roya, sans-serif; float: right; }
:lang(he) { direction: rtl; }
 --></style>
</head><body id=ERR_INVALID_URL>
<div id="titles">
<h1>ERROR</h1>
<h2>The requested URL could not be retrieved</h2>
</div>
<hr>

<div id="content">
<p>The following error was encountered while trying to retrieve the URL: <a href="/">/</a></p>

<blockquote id="error">
<p><b>Invalid URL</b></p>
</blockquote>

<p>Some aspect of the requested URL is incorrect.</p>

<p>Some possible problems are:</p>
<ul>
<li><p>Missing or incorrect access protocol (should be <q>http://</q> or similar)</p></li>
<li><p>Missing hostname</p></li>
<li><p>Illegal double-escape in the URL-Path</p></li>
<li><p>Illegal character in hostname; underscores are not allowed.</p></li>
</ul>

<p>Your cache administrator is <a href="mailto:webmaster?subject=CacheErrorInfo%20-%20ERR_INVALID_URL&amp;body=CacheHost%3A%20SQUID%0D%0AErrPage%3A%20ERR_INVALID_URL%0D%0AErr%3A%20%5Bnone%5D%0D%0ATimeStamp%3A%20Wed,%2024%20Jul%202024%2022%3A01%3A46%20GMT%0D%0A%0D%0AClientIP%3A%20192.168.45.159%0D%0A%0D%0AHTTP%20Request%3A%0D%0A%0D%0A%0D%0A">webmaster</a>.</p>
<br>
</div>

<hr>
<div id="footer">
<p>Generated Wed, 24 Jul 2024 22:01:46 GMT by SQUID (squid/4.14)</p>
<!-- ERR_INVALID_URL -->
</div>
</body></html>

```

## Gobuster

Self Enumerate these!

Directories -> 

```bash

```

Files ->

```bash

```
## Nikto

```bash
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Target IP:          TARGET
+ Target Hostname:    TARGET
+ Target Port:        3128
+ Start Time:         2024-07-24 18:01:50 (GMT-4)
---------------------------------------------------------------------------
+ Server: squid/4.14
+ /: Retrieved via header: 1.1 localhost (squid/4.14).
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: Uncommon header 'x-squid-error' found, with contents: ERR_INVALID_URL 0.
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ /robots.txt: Entry '<li><p>Illegal character in hostname; underscores are not ed.</p></li>' is returned a non-forbidden or redirect HTTP code (400). See: https://portswigger.net/kb/issues/00600600_robots-txt-file
+ /robots.txt: contains 1 entry which should be manually viewed. See: https://developer.mozilla.org/en-US/docs/Glossary/Robots.txt
+ /splashAdmin.php: Cobalt Qube 3 admin is running. This may have multiple security problems which could not be tested remotely. See: https://seclists.org/bugtraq/2002/Jul/262
+ /_vti_bin/shtml.exe: Attackers may be able to crash FrontPage by requesting a DOS device, like shtml.exe/aux.htm -- a DoS was not attempted. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2000-0709
+ /~root/: Allowed to browse root's home directory. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2001-1013
+ /cgi-bin/wrap: comes with IRIX 6.2; allows to view directories.
+ /forums//admin/config.php: PHP Config file may contain database IDs and passwords.
+ /forums//adm/config.php: PHP Config file may contain database IDs and passwords.
+ /forums//administrator/config.php: PHP Config file may contain database IDs and passwords.
+ /forums/config.php: PHP Config file may contain database IDs and passwords.
+ /guestbook/guestbookdat: PHP-Gastebuch 1.60 Beta reveals sensitive information about its configuration.
+ /guestbook/pwd: PHP-Gastebuch 1.60 Beta reveals the md5 hash of the admin password.
+ /help/: Help directory should not be accessible.
+ /hola/admin/cms/htmltags.php?datei=./sec/data.php: hola-cms-1.2.9-10 may reveal the administrator ID and password. See: https://vulners.com/exploitdb/EDB-ID:23027
+ /global.inc: PHP-Survey's include file should not be available via the web. Configure the web server to ignore .inc files or change this to global.inc.php. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-0614
+ /geeklog/users.php: Geeklog prior to 1.3.8-1sr2 contains a SQL injection vulnerability that lets a remote attacker reset admin password. See: https://vulners.com/osvdb/OSVDB:2703
+ /gb/index.php?login=true: gBook may allow admin login by setting the value 'login' equal to 'true'. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1560
+ /guestbook/admin.php: Guestbook admin page available without authentication.
+ /getaccess: This may be an indication that the server is running getAccess for SSO.
+ /cfdocs/expeval/openfile.cfm: Can use to expose the system/server path.
+ /tsweb/: Microsoft TSAC found. See: https://web.archive.org/web/20040910030506/http://www.dslwebserver.com/main/fr_index.html?/main/sbs-Terminal-Services-Advanced-Client-Configuration.html
+ /vgn/performance/TMT: Vignette CMS admin/maintenance script available.
+ /vgn/performance/TMT/Report: Vignette CMS admin/maintenance script available.
+ /vgn/performance/TMT/Report/XML: Vignette CMS admin/maintenance script available.
+ /vgn/performance/TMT/reset: Vignette CMS admin/maintenance script available.
+ /vgn/ppstats: Vignette CMS admin/maintenance script available.
+ /vgn/previewer: Vignette CMS admin/maintenance script available.
+ /vgn/record/previewer: Vignette CMS admin/maintenance script available.
+ /vgn/stylepreviewer: Vignette CMS admin/maintenance script available.
+ /vgn/vr/Deleting: Vignette CMS admin/maintenance script available.
+ /vgn/vr/Editing: Vignette CMS admin/maintenance script available.
+ /vgn/vr/Saving: Vignette CMS admin/maintenance script available.
+ /vgn/vr/Select: Vignette CMS admin/maintenance script available.
+ /scripts/iisadmin/bdir.htr: This default script shows host info, may allow file browsing and buffer a overrun in the Chunked Encoding data transfer mechanism, request /scripts/iisadmin/bdir.htr??c:\<dir>. See: https://docs.microsoft.com/en-us/security-updates/securitybulletins/2002/MS02-028
+ /scripts/iisadmin/ism.dll: Allows you to mount a brute force attack on passwords.
+ /scripts/tools/ctss.idc: This CGI allows remote users to view and modify SQL DB contents, server paths, docroot and more.
+ /bigconf.cgi: BigIP Configuration CGI.
+ /blah_badfile.shtml: Allaire ColdFusion allows JSP source viewed through a vulnerable SSI call.
+ /vgn/style: Vignette server may reveal system information through this file. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2003-0401
+ /SiteServer/Admin/commerce/foundation/domain.asp: Displays known domains of which that server is involved. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1769
+ /SiteServer/Admin/commerce/foundation/driver.asp: Displays a list of installed ODBC drivers. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1769
+ /SiteServer/Admin/commerce/foundation/DSN.asp: Displays all DSNs configured for selected ODBC drivers. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1769
+ /SiteServer/admin/findvserver.asp: Gives a list of installed Site Server components. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1769
+ /SiteServer/Admin/knowledge/dsmgr/default.asp: Used to view current search catalog configurations.
+ /bb-dnbd/faxsurvey: This may allow arbitrary command execution.
+ /cartcart.cgi: If this is Dansie Shopping Cart 3.0.8 or earlier, it contains a backdoor to allow attackers to execute arbitrary commands.
+ /scripts/Carello/Carello.dll: Carello 1.3 may allow commands to be executed on the server by replacing hidden form elements. This could not be tested by Nikto. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2001-0614
+ /scripts/tools/dsnform.exe: Allows creation of ODBC Data Source.
+ /scripts/tools/dsnform: Allows creation of ODBC Data Source.
+ /SiteServer/Admin/knowledge/dsmgr/users/GroupManager.asp: Microsoft Site Server script used to create, modify, and potentially delete LDAP users and groups. See: https://securitytracker.com/id/1003420
+ /SiteServer/Admin/knowledge/dsmgr/users/UserManager.asp: Microsoft Site Server used to create, modify, and potentially delete LDAP users and groups. See: https://securitytracker.com/id/1003420
+ /prd.i/pgen/: Has MS Merchant Server 1.0.
+ /readme.eml: Remote server may be infected with the Nimda virus.
+ /scripts/httpodbc.dll: Possible IIS backdoor found.
+ /scripts/proxy/w3proxy.dll: MSProxy v1.0 installed.
+ /SiteServer/admin/: Site Server components admin. Default account may be 'LDAP_Anonymous', pass is 'LdapPassword_1'. See: https://github.com/sullo/advisory-archives/blob/master/RFP2201.txt
+ /siteseed/: Siteseed pre 1.4.2 have 'major' security problems.
+ /pccsmysqladm/incs/dbconnect.inc: This file should not be accessible, as it contains database connectivity information. Upgrade to version 1.2.5 or higher.
+ /iisadmin/: Access to /iisadmin should be restricted to localhost or allowed hosts only.
+ /PDG_Cart/order.log: PDG Commerce log found. See: http://zodi.com/cgi-bin/shopper.cgi?display=intro&template=Intro/commerce.html
+ /ows/restricted%2eshow: OWS may allow restricted files to be viewed by replacing a character with its encoded equivalent.
+ /view_source.jsp: Resin 2.1.2 view_source.jsp allows any file on the system to be viewed by using \..\ directory traversal. This script may be vulnerable.
+ /w-agora/: w-agora pre 4.1.4 may allow a remote user to execute arbitrary PHP scripts via URL includes in include/*.php and user/*.php files. Default account is 'admin' but password set during install.
+ /vider.php3: MySimpleNews may allow deleting of news items without authentication. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-2320
+ /officescan/cgi/cgiChkMasterPwd.exe: Trend Micro Officescan allows you to skip the login page and access some CGI programs directly. See: https://web.archive.org/web/20030607054822/http://support.microsoft.com/support/exchange/content/whitepapers/owaguide.doc
+ /pbserver/pbserver.dll: This may contain a buffer overflow. See: https://docs.microsoft.com/en-us/security-updates/securitybulletins/2000/MS00-094
+ /administrator/gallery/uploadimage.php: Mambo PHP Portal/Server 4.0.12 BETA and below may allow upload of any file type simply putting '.jpg' before the real file extension.
+ /pafiledb/includes/team/file.php: paFileDB 3.1 and below may allow file upload without authentication.
+ /phpEventCalendar/file_upload.php: phpEventCalendar 1.1 and prior are vulnerable to file upload bug.
+ /servlet/com.unify.servletexec.UploadServlet: This servlet allows attackers to upload files to the server.
+ /scripts/cpshost.dll: Posting acceptor possibly allows you to upload files.
+ /upload.asp: An ASP page that allows attackers to upload files to server.
+ /uploadn.asp: An ASP page that allows attackers to upload files to server.
+ /uploadx.asp: An ASP page that allows attackers to upload files to server.
+ /wa.exe: An ASP page that allows attackers to upload files to server.
+ /basilix/compose-attach.php3: BasiliX webmail application prior to 1.1.1 contains a non-descript security vulnerability in compose-attach.php3 related to attachment uploads.
+ /server/: Possibly Macromedia JRun or CRX WebDAV upload.
+ /vgn/ac/data: Vignette CMS admin/maintenance script available.
+ /vgn/ac/delete: Vignette CMS admin/maintenance script available.
+ /vgn/ac/edit: Vignette CMS admin/maintenance script available.
+ /vgn/ac/esave: Vignette CMS admin/maintenance script available.
+ /vgn/ac/fsave: Vignette CMS admin/maintenance script available.
+ /vgn/ac/index: Vignette CMS admin/maintenance script available.
+ /vgn/asp/MetaDataUpdate: Vignette CMS admin/maintenance script available.
+ /vgn/asp/previewer: Vignette CMS admin/maintenance script available.
+ /vgn/asp/status: Vignette CMS admin/maintenance script available.
+ /vgn/asp/style: Vignette CMS admin/maintenance script available.
+ /vgn/errors: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/controller: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/errorpage: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/initialize: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/jspstatus: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/jspstatus56: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/metadataupdate: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/previewer: Vignette CMS admin/maintenance script available.
+ /vgn/jsp/style: Vignette CMS admin/maintenance script available.
+ /vgn/legacy/edit: Vignette CMS admin/maintenance script available.
+ /vgn/login: Vignette server may allow user enumeration based on the login attempts to this file.
+ /forum/admin/wwforum.mdb: Web Wiz Forums password database found. See: https://seclists.org/bugtraq/2003/Apr/238
+ /fpdb/shop.mdb: MetaCart2 is an ASP shopping cart. The database of customers is available via the web. See: https://packetstormsecurity.com/files/32406/xmas.txt.html
+ /guestbook/admin/o12guest.mdb: Ocean12 ASP Guestbook Manager allows download of SQL database which contains admin password. See: https://www.exploit-db.com/exploits/22484
+ /midicart.mdb: MIDICART database is available for browsing. This should not be allowed via the web server. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1432
+ /MIDICART/midicart.mdb: MIDICART database is available for browsing. This should not be allowed via the web server. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1432
+ /mpcsoftweb_guestbook/database/mpcsoftweb_guestdata.mdb: MPCSoftWeb Guest Book passwords retrieved. See: https://www.exploit-db.com/exploits/22513
+ /news/news.mdb: Web Wiz Site News release v3.06 admin password database is available and unencrypted.
+ /shopping300.mdb: VP-ASP shopping cart application allows .mdb files (which may include customer data) to be downloaded via the web. These should not be available. See: https://securitytracker.com/id/1004382
+ /shopping400.mdb: VP-ASP shopping cart application allows .mdb files (which may include customer data) to be downloaded via the web. These should not be available. See: https://securitytracker.com/id/1004382
+ /shoppingdirectory/midicart.mdb: MIDICART database is available for browsing. This should not be allowed via the web server. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-1432
+ /database/db2000.mdb: Max Web Portal database is available remotely. It should be moved from the default location to a directory outside the web root. See: https://www.medae.co/en/max/web-app
+ /admin/config.php: PHP Config file may contain database IDs and passwords.
+ /adm/config.php: PHP Config file may contain database IDs and passwords.
+ /administrator/config.php: PHP Config file may contain database IDs and passwords.
+ /contents.php?new_language=elvish&mode=select: Requesting a file with an invalid language selection from DC Portal may reveal the system path.
+ /pw/storemgr.pw: Encrypted ID/Pass for Mercantec's SoftCart. See: http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-1999-0609
+ /servlet/com.livesoftware.jrun.plugins.ssi.SSIFilter: Allaire ColdFusion allows JSP source viewed through a vulnerable SSI call.
+ /shopa_sessionlist.asp: VP-ASP shopping cart test application is available from the web. This page may give the location of .mdb files which may also be available.
+ /si

_Trimmed for readability._
