#dnssoarec

Configuration for SOA record resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>domain</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to add the SOA record.<br>Minimum length = 1</td></tr><tr><td>originserver</td><td>&lt;String></td><td>Read-write</td><td>Domain name of the name server that responds authoritatively for the domain.<br>Minimum length = 1</td></tr><tr><td>contact</td><td>&lt;String></td><td>Read-write</td><td>Email address of the contact to whom domain issues can be addressed. In the email address, replace the @ sign with a period (.). For example, enter domainadmin.example.com instead of domainadmin@example.com.<br>Minimum length = 1</td></tr><tr><td>serial</td><td>&lt;Double></td><td>Read-write</td><td>The secondary server uses this parameter to determine whether it requires a zone transfer from the primary server.<br>Default value: 100<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>refresh</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, for which a secondary server must wait between successive checks on the value of the serial number.<br>Default value: 3600<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>retry</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, between retries if a secondary server's attempt to contact the primary server for a zone refresh fails.<br>Default value: 3<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>expire</td><td>&lt;Double></td><td>Read-write</td><td>Time, in seconds, after which the zone data on a secondary name server can no longer be considered authoritative because all refresh and retry attempts made during the period have failed. After the expiry period, the secondary server stops serving the zone. Typically one week. Not used by the primary server.<br>Default value: 3600<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>minimum</td><td>&lt;Double></td><td>Read-write</td><td>Default time to live (TTL) for all records in the zone. Can be overridden for individual records.<br>Default value: 5<br>Minimum value = 0<br>Maximum value = 2147483647</td></tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>Time to Live (TTL), in seconds, for the record. TTL is the time for which the record must be cached by DNS proxies. The specified TTL is applied to all the resource records that are of the same record type and belong to the specified domain name. For example, if you add an address record, with a TTL of 36000, to the domain name example.com, the TTLs of all the address records of example.com are changed to 36000. If the TTL is not specified, the Citrix ADC uses either the DNS zone's minimum TTL or, if the SOA record is not available on the appliance, the default value of 3600.<br>Default value: 3600<br>Minimum value = 0<br>Maximum value = 2147483647</td></tr><tr><td>ecssubnet</td><td>&lt;String></td><td>Read-write</td><td>Subnet for which the cached SOA record need to be removed.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of records to display. Available settings function as follows:<br>* ADNS - Display all authoritative address records.<br>* PROXY - Display all proxy address records.<br>* ALL - Display all address records.<br>Possible values = ALL, ADNS, PROXY</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>authtype</td><td>&lt;String></td><td>Read-only</td><td>Record type.<br>Possible values = ALL, ADNS, PROXY</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnssoarec":{<b>"domain":<String_value>,</b><b>"originserver":<String_value>,</b><b>"contact":<String_value>,</b>"serial":<Double_value>,"refresh":<Double_value>,"retry":<Double_value>,"expire":<Double_value>,"minimum":<Double_value>,"ttl":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnssoarec":{<b>"domain":<String_value>,</b>"originserver":<String_value>,"contact":<String_value>,"serial":<Double_value>,"refresh":<Double_value>,"retry":<Double_value>,"expire":<Double_value>,"minimum":<Double_value>,"ttl":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"dnssoarec":{<b>"domain":<String_value>,</b>"serial":true,"refresh":true,"retry":true,"expire":true,"minimum":true,"ttl":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>args=domain:&lt;String_value&gt;,type:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get dnssoarec resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of dnssoarec resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the dnssoarec resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnssoarec": [ {domain:<String_value>,type:<String_value>,nodeid:<Double_value>"originserver":<String_value>,"contact":<String_value>,"serial":<Double_value>,"refresh":<Double_value>,"retry":<Double_value>,"expire":<Double_value>,"minimum":<Double_value>,"ttl":<Double_value>,"authtype":<String_value>,"ecssubnet":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec/domain_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnssoarec": [ {domain:<String_value>,type:<String_value>,nodeid:<Double_value>"originserver":<String_value>,"contact":<String_value>,"serial":<Double_value>,"refresh":<Double_value>,"retry":<Double_value>,"expire":<Double_value>,"minimum":<Double_value>,"ttl":<Double_value>,"authtype":<String_value>,"ecssubnet":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/dnssoarec?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "dnssoarec": [ { "__count": "#no"} ] }```



