#streamidentifier

Statistics for identifier resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the stream identifier.<br>Minimum length = 1</td></tr><tr><td>pattern</td><td>&lt;String[]></td><td>Read-write</td><td>Values on which grouping is performed are displayed in the output as row titles. If grouping is performed on two or more fields, their values are separated by a question mark in the row title.<br><br>For example, consider a selector that contains the expressions HTTP.REQ.URL and CLIENT.IP.SRC (in that order), on an appliance that has accumulated records of a number of requests for two URLs, example.com/page1.html and example.com/page2.html, from two client IP addresses, 192.0.2.10 and 192.0.2.11. <br><br>With a pattern of ? ?, the appliance performs grouping on both fields and displays statistics for the following:<br>* Requests for example.com/abc.html from 192.0.2.10, with a row title of example.com/abc.html?192.0.2.10.<br>* Requests for example.com/abc.html from 192.0.2.11, with a row title of example.com/abc.html?192.0.2.11.<br>* Requests for example.com/def.html from 192.0.2.10, with a row title of example.com/def.html?192.0.2.10.<br>* Requests for example.com/def.html from 192.0.2.11, with a row title of example.com/def.html?192.0.2.11.<br><br>With a pattern of * ?, the appliance performs grouping on only the client IP address values and displays statistics for the following requests:<br>* All requests from 192.0.2.10, with the IP address as the row title.<br>* All requests from 192.0.2.11, with the IP address as the row title.<br><br>With a pattern of ? *, the appliance performs grouping on only the URL values and displays statistics for the following requests:<br>* All requests for example.com/abc.html, with the URL as the row title.<br>* All requests for example.com/def.html, with the URL as the row title.<br><br>With a pattern of * *, the appliance displays one set of collective statistics for all the requests received, with no row title.<br><br>With a pattern of example.com/abc.html ?, the appliance displays statistics for requests for example.com/abc.html from each unique client IP address.<br><br>With a pattern of * 192.0.2.11, the appliance displays statistics for all requests from 192.0.2.11.</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>sortby</td><td>&lt;String></td><td>Read-write</td><td>use this argument to sort by specific key.<br>Possible values =</td></tr><tr><td>sortorder</td><td>&lt;String></td><td>Read-write</td><td>use this argument to specify sort order.<br>Default value: SORT_DESCENDING<br>Possible values = ascending, descending</td></tr><tr><td>streamobjreq</td><td>&lt;Double></td><td>Read-only</td><td>Total number of Stream Requests recieved.</td></tr><tr><td>streamobjbandw</td><td>&lt;Double></td><td>Read-only</td><td>Total Bandwidth consumed.</td></tr><tr><td>streamobjresptime</td><td>&lt;Double></td><td>Read-only</td><td>Average response time of the stream session.</td></tr><tr><td>streamobjconn</td><td>&lt;Double></td><td>Read-only</td><td>Current connections on the stream session.</td></tr><tr><td>streamobjbreachcnt</td><td>&lt;Double></td><td>Read-only</td><td>Total Breaching Transactions in configured interval.</td></tr><tr><td>streamobjpktcredits</td><td>&lt;Double></td><td>Read-only</td><td>Calculated Packet credits on current connection.</td></tr><tr><td>streamobjpktspersecond</td><td>&lt;Double></td><td>Read-only</td><td>Total packets recieved in configured interval.</td></tr><tr><td>streamobjdroppedconns</td><td>&lt;Double></td><td>Read-only</td><td>Total connections dropped.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#ge)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/streamidentifier
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/streamidentifier?<b>args=<b>name:&lt;String_value&gt;,</b>pattern:&lt;String[]_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;,sortby:&lt;String_value&gt;,sortorder:&lt;String_value&gt;,sortorder:&lt;String_value&gt;</b>
Use this query-parameter to get streamidentifier resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "streamidentifier": [ {"name":<String_value>,"streamobjconn":<Double_value>,"streamobjdroppedconns":<Double_value>,"streamobjbreachcnt":<Double_value>,"streamobjbandw":<Double_value>,"streamobjresptime":<Double_value>,"streamobjpktcredits":<Double_value>,"streamobjpktspersecond":<Double_value>,"streamobjreq":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/streamidentifier/name_value&gt;&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "streamidentifier": [ {"name":<String_value>,"streamobjconn":<Double_value>,"streamobjdroppedconns":<Double_value>,"streamobjbreachcnt":<Double_value>,"streamobjbandw":<Double_value>,"streamobjresptime":<Double_value>,"streamobjpktcredits":<Double_value>,"streamobjpktspersecond":<Double_value>,"streamobjreq":<Double_value>}]}```



