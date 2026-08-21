## NMAP 

```
# Nmap 7.94SVN scan initiated Sat Jun 29 17:51:47 2024 as: nmap -vv --reason -Pn -T4 -sV -p 80 "--script=banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN /home/kali/... -oX /home/kali/... TARGET
Nmap scan report for TARGET
Host is up, received user-set (0.058s latency).
Scanned at 2024-06-29 17:51:48 EDT for 297s

Bug in http-security-headers: no string output.
PORT   STATE SERVICE REASON          VERSION
80/tcp open  http    syn-ack ttl 125 Microsoft IIS httpd 10.0
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
| http-comments-displayer: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=TARGET
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1550
|     Comment: 
|          // the trigger was dropped
|     
|     Path: http://TARGET:80/html/navigation.js
|     Line number: 140
|     Comment: 
|          // skip anything inside a <script> block
|     
|     Path: http://TARGET:80/html/grammar.html
|     Line number: 51
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="datetimeFields">
|             <a href="#${item.link}">${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 179
|     Comment: 
|         <!-- analytics -->
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1536
|     Comment: 
|          // initialize the trigger object is necessary
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 23
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="commandsDML">
|             <a href="#${item.link}">${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/grammar.html
|     Line number: 23
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="literals">
|             <a href="#${item.link}">${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/
|     Line number: 7
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
|         -->
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1043
|     Comment: 
|         
|         // Application 1:

_Trimmed verbose nmap/http-script dump; open ports and versions kept._
|     
|     Path: http://TARGET:80/html/navigation.js
|     Line number: 138
|     Comment: 
|          // skip anything inside an HTML tag
|     
|     Path: http://TARGET:80/html/datatypes.html
|     Line number: 22
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="dataTypes">
|             <a href="#${item.link}" >${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/navigation.js
|     Line number: 1
|     Comment: 
|         /*
|          * Copyright 2004-2019 H2 Group. Multiple-Licensed under the MPL 2.0,
|          * and the EPL 1.0 (http://h2database.com/html/license.html).
|          *  * Initial Developer: H2 Group
|          */
|     
|     Path: http://TARGET:80/html/navigation.js
|     Line number: 33
|     Comment: 
|          // name of the frameset page
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 48
|     Comment: 
|         <!-- railroad-end -->
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1046
|     Comment: 
|         
|         // Application 2:
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 179
|     Comment: 
|         <!-- [close] { -->
|     
|     Path: http://TARGET:80/html/tutorial.html
|     Line number: 468
|     Comment: 
|          // add application code here
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 122
|     Comment: 
|         <!-- syntax-start
|         <pre>
|         ${item.syntax}
|         </pre>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/grammar.html
|     Line number: 79
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="otherGrammar">
|             <a href="#${item.link}" >${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1542
|     Comment: 
|          // the trigger is fired
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 177
|     Comment: 
|         <!--[if lte IE 7]><script language="javascript">switchBnf(null);</script><![endif]-->
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 1123
|     Comment: 
|         /**/
|     
|     Path: http://TARGET:80/html/tutorial.html
|     Line number: 352
|     Comment: 
|         /*rnd*/
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 79
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="commandsOther">
|             <a href="#${item.link}">${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/commands.html
|     Line number: 51
|     Comment: 
|         <!-- syntax-start
|         <p class="notranslate">
|         <c:forEach var="item" items="commandsDDL">
|             <a href="#${item.link}">${item.topic}</a><br />
|         </c:forEach>
|         </p>
|         syntax-end -->
|     
|     Path: http://TARGET:80/html/advanced.html
|     Line number: 1606
|     Comment: 
|         /* PUBLIC.GEO_TABLE_SPATIAL_INDEX:
|             THE_GEOM &amp;&amp;
|             'POLYGON ((490 490, 536 490, 536 515, 490 515, 490 490))'::Geometry */
|     
|     Path: http://TARGET:80/html/tutorial.html
|     Line number: 587
|     Comment: 
|         
|         // start the TCP Server
|     
|     Path: http://TARGET:80/html/features.html
|     Line number: 762
|     Comment: 
|         /*
|         </td><td>
|             Directory containing one file for each<br />
|             BLOB or CLOB value larger than a certain size.<br />
|             Format: <code>&lt;id&gt;.t&lt;tableId&gt;.lob.db</code>
|         </td><td>
|             1 per large object
|         </td></tr>
|         <tr><td class="notranslate">
|             test.123.temp.db
|         </td><td>
|             Temporary file.<br />
|             Contains a temporary blob or a large result set.<br />
|             Format: <code>&lt;database&gt;.&lt;id&gt;.temp.db</code>
|         </td><td>
|             1 per object
|         </td></tr>
|         </table>
|         
|         <h3>Moving and Renaming Database Files</h3>
|         <p>
|         Database name and location are not stored inside the database files.
|         </p><p>
|         While a database is closed, the files can be moved to another directory, and they can
|         be renamed as well (as long as all files of the same database start with the same
|         name and the respective extensions are unchanged).
|         </p><p>
|         As there is no platform specific data in the files, they can be moved to other operating systems
|         without problems.
|         </p>
|         
|         <h3>Backup</h3>
|         <p>
|         When the database is closed, it is possible to backup the database files.
|         </p><p>
|         To backup data while the database is running,
|         the SQL commands <code>SCRIPT</code> and <code>BACKUP</code> can be used.
|         </p>
|         
|         <h2 id="logging_recovery">Logging and Recovery</h2>
|         <p>
|         Whenever data is modified in the database and those changes are committed, the changes are written
|         to the transaction log (except for in-memory objects). The changes to the main data area itself are usually written
|         later on, to optimize disk access. If there is a power failure, the main data area is not up-to-date,
|         but because the changes are in the transaction log, the next time the database is opened, the changes
|         are re-applied automatically.
|         </p>
|         
|         <h2 id="compatibility">Compatibility</h2>
|         <p>
|         All database engines behave a little bit different. Where possible, H2 supports the ANSI SQL standard,
|         and tries to be compatible to other databases. There are still a few differences however:
|         </p>
|         <p>
|         In MySQL text columns are case insensitive by default, while in H2 they are case sensitive. However
|         H2 supports case insensitive columns as well. To create the tables with case insensitive texts, append
|         <code>IGNORECASE=TRUE</code> to the database URL
|         (example: <code>jdbc:h2:~/test;IGNORECASE=TRUE</code>).
|         </p>
|         
|         <h3>Compatibility Modes</h3>
|         <p>
|         For certain features, this database can emulate the behavior of specific databases.
|         However, only a small subset of the differences between databases are implemented in this way.
|         Here is the list of currently supported modes and the differences to the regular mode:
|         </p>
|         
|         <h3>DB2 Compatibility Mode</h3>
|         <p>
|         To use the IBM DB2 mode, use the database URL <code>jdbc:h2:~/test;MODE=DB2</code>
|         or the SQL statement <code>SET MODE DB2</code>.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>Concatenating <code>NULL</code> with another value
|             results in the other value.
|         </li><li>Support the pseudo-table SYSIBM.SYSDUMMY1.
|         </li><li>Timestamps with dash between date and time are supported.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         
|         <h3>Derby Compatibility Mode</h3>
|         <p>
|         To use the Apache Derby mode, use the database URL <code>jdbc:h2:~/test;MODE=Derby</code>
|         or the SQL statement <code>SET MODE Derby</code>.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>For unique indexes, <code>NULL</code> is distinct.
|             That means only one row with <code>NULL</code> in one of the columns is allowed.
|         </li><li>Concatenating <code>NULL</code> with another value
|             results in the other value.
|         </li><li>Support the pseudo-table SYSIBM.SYSDUMMY1.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         
|         <h3>HSQLDB Compatibility Mode</h3>
|         <p>
|         To use the HSQLDB mode, use the database URL <code>jdbc:h2:~/test;MODE=HSQLDB</code>
|         or the SQL statement <code>SET MODE HSQLDB</code>.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>When converting the scale of decimal data, the number is only converted if the new scale is
|             smaller than the current scale. Usually, the scale is converted and 0s are added if required.
|         </li><li>For unique indexes, <code>NULL</code> is distinct.
|             That means only one row with <code>NULL</code> in one of the columns is allowed.
|         </li><li>Text can be concatenated using '+'.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         
|         <h3>MS SQL Server Compatibility Mode</h3>
|         <p>
|         To use the MS SQL Server mode, use the database URL <code>jdbc:h2:~/test;MODE=MSSQLServer</code>
|         or the SQL statement <code>SET MODE MSSQLServer</code>.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>Identifiers may be quoted using square brackets as in <code>[Test]</code>.
|         </li><li>For unique indexes, <code>NULL</code> is distinct.
|             That means only one row with <code>NULL</code> in one of the columns is allowed.
|         </li><li>Concatenating <code>NULL</code> with another value
|             results in the other value.
|         </li><li>Text can be concatenated using '+'.
|         </li><li>MONEY data type is treated like NUMERIC(19, 4) data type. SMALLMONEY data type is treated like NUMERIC(10, 4)
|             data type.
|         </li><li><code>IDENTITY</code> can be used for automatic id generation on column level.
|         </li><li>Table hints are discarded. Example: <code>SELECT * FROM table WITH (NOLOCK)</code>.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         
|         <h3>MySQL Compatibility Mode</h3>
|         <p>
|         To use the MySQL mode, use the database URL <code>jdbc:h2:~/test;MODE=MySQL;DATABASE_TO_LOWER=TRUE</code>.
|         Use this mode for compatibility with MariaDB too.
|         When case-insensitive identifiers are needed append <code>;CASE_INSENSITIVE_IDENTIFIERS=TRUE</code> to URL.
|         Do not change value of DATABASE_TO_LOWER after creation of database.
|         </p>
|         <ul><li>When inserting data, if a column is defined to be <code>NOT NULL</code>
|             and <code>NULL</code> is inserted,
|             then a 0 (or empty string, or the current timestamp for timestamp columns) value is used.
|             Usually, this operation is not allowed and an exception is thrown.
|         </li><li>Creating indexes in the <code>CREATE TABLE</code> statement is allowed using
|             <code>INDEX(..)</code> or <code>KEY(..)</code>.
|             Example: <code>create table test(id int primary key, name varchar(255), key idx_name(name));</code>
|         </li><li>When converting a floating point number to an integer, the fractional
|             digits are not truncated, but the value is rounded.
|         </li><li>Concatenating <code>NULL</code> with another value
|             results in the other value.
|         </li><li>ON DUPLICATE KEY UPDATE is supported in INSERT statements, due to this feature VALUES has special non-standard
|             meaning is some contexts.
|         </li><li>INSERT IGNORE is partially supported and may be used to skip rows with duplicate keys if ON DUPLICATE KEY
|             UPDATE is not specified.
|         </li><li>REGEXP_REPLACE() uses \ for back-references for compatibility with MariaDB.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         <p>
|         Text comparison in MySQL is case insensitive by default, while in H2 it is case sensitive (as in most other databases).
|         H2 does support case insensitive text comparison, but it needs to be set separately,
|         using <code>SET IGNORECASE TRUE</code>.
|         This affects comparison using <code>=, LIKE, REGEXP</code>.
|         </p>
|         
|         <h3>Oracle Compatibility Mode</h3>
|         <p>
|         To use the Oracle mode, use the database URL <code>jdbc:h2:~/test;MODE=Oracle</code>
|         or the SQL statement <code>SET MODE Oracle</code>.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>When using unique indexes, multiple rows with <code>NULL</code>
|             in all columns are allowed, however it is not allowed to have multiple rows with the
|             same values otherwise.
|         </li><li>Concatenating <code>NULL</code> with another value
|             results in the other value.
|         </li><li>Empty strings are treated like <code>NULL</code> values.
|         </li><li>REGEXP_REPLACE() uses \ for back-references.
|         </li><li>DATE data type is treated like TIMESTAMP(0) data type.
|         </li><li>Datetime value functions return the same value within a command.
|         </li></ul>
|         
|         <h3>PostgreSQL Compatibility Mode</h3>
|         <p>
|         To use the PostgreSQL mode, use the database URL <code>jdbc:h2:~/test;MODE=PostgreSQL;DATABASE_TO_LOWER=TRUE</code>.
|         Do not change value of DATABASE_TO_LOWER after creation of database.
|         </p>
|         <ul><li>For aliased columns, <code>ResultSetMetaData.getColumnName()</code>
|             returns the alias name and <code>getTableName()</code> returns
|             <code>null</code>.
|         </li><li>When converting a floating point number to an integer, the fractional
|             digits are not be truncated, but the value is rounded.
|         </li><li>The system columns <code>CTID</code> and
|             <code>OID</code> are supported.
|         </li><li>LOG(x) is base 10 in this mode.
|         </li><li>REGEXP_REPLACE():
|             <ul>
|             <li>uses \ for back-references;</li>
|             <li>does not throw an exception when the <code>flagsString</code> parameter contains a 'g';</li>


_Trimmed for readability._
