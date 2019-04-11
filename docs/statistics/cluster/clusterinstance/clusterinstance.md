#clusterinstance

Statistics for cluster instance resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clid</td><td>&lt;Double></td><td>Read-write</td><td>ID of the cluster instance for which to display statistics.<br>Minimum value = 1<br>Maximum value = 16</td></tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>clnumnodes</td><td>&lt;Double></td><td>Read-only</td><td>Number of nodes in the cluster.</td></tr><tr><td>clcurstatus</td><td>&lt;String></td><td>Read-only</td><td>State of the cluster.</td></tr><tr><td>clviewleader</td><td>&lt;String></td><td>Read-only</td><td>NSIP address of the Configuration Coordinator of the cluster.</td></tr><tr><td>totsteeredpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of packets steered on the cluster backplane.</td></tr><tr><td>clbkplanerx</td><td>&lt;Double></td><td>Read-only</td><td>Traffic received on backplane (in mbits)</td></tr><tr><td>clbkplanerxrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for clbkplanerx</td></tr><tr><td>clbkplanetx</td><td>&lt;Double></td><td>Read-only</td><td>Traffic transmitted from backplane (in mbits)</td></tr><tr><td>clbkplanetxrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for clbkplanetx</td></tr><tr><td>numdfddroppkts</td><td>&lt;Double></td><td>Read-only</td><td>Number of steered packets that are dropped.</td></tr><tr><td>totpropagationtimeout</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the update to the client timed-out.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#ge)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/clusterinstance
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/clusterinstance?<b>args=clid:&lt;Double_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get clusterinstance resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance": [ {"clid":<Double_value>,"totpropagationtimeout":<Double_value>,"clbkplanetx":<Double_value>,"clbkplanetxrate":<Double_value>,"totsteeredpkts":<Double_value>,"numdfddroppkts":<Double_value>,"clviewleader":<String_value>,"clbkplanerx":<Double_value>,"clcurstatus":<String_value>,"clnumnodes":<Double_value>,"clbkplanerxrate":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/clusterinstance/clid_value&gt;&lt;Double&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "clusterinstance": [ {"clid":<Double_value>,"totpropagationtimeout":<Double_value>,"clbkplanetx":<Double_value>,"clbkplanetxrate":<Double_value>,"totsteeredpkts":<Double_value>,"numdfddroppkts":<Double_value>,"clviewleader":<String_value>,"clbkplanerx":<Double_value>,"clcurstatus":<String_value>,"clnumnodes":<Double_value>,"clbkplanerxrate":<Double_value>}]}```



