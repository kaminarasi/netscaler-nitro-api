#gslbservice_lbmonitor_binding

Binding object showing the lbmonitor that can be bound to gslbservice.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>servicename</td><td>&lt;String></td><td>Read-write</td><td>Name of the GSLB service.<br>Minimum length = 1</td></tr><tr><td>weight</td><td>&lt;Double></td><td>Read-write</td><td>Weight to assign to the monitor-service binding. A larger number specifies a greater weight. Contributes to the monitoring threshold, which determines the state of the service.<br>Minimum value = 1<br>Maximum value = 100</td></tr><tr><td>monitor_name</td><td>&lt;String></td><td>Read-write</td><td>Monitor name.</td></tr><tr><td>monstate</td><td>&lt;String></td><td>Read-write</td><td>State of the monitor bound to gslb service.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>monstatparam2</td><td>&lt;Integer></td><td>Read-only</td><td>Second parameter for use with message code.</td></tr><tr><td>monstatcode</td><td>&lt;Integer></td><td>Read-only</td><td>The code indicating the monitor response.</td></tr><tr><td>lastresponse</td><td>&lt;String></td><td>Read-only</td><td>Displays the gslb monitor status in string format.</td></tr><tr><td>failedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Number of the current failed monitoring probes.</td></tr><tr><td>monstatparam3</td><td>&lt;Integer></td><td>Read-only</td><td>Third parameter for use with message code.</td></tr><tr><td>monitor_state</td><td>&lt;String></td><td>Read-only</td><td>The running state of the monitor on this service.<br>Possible values = UP, DOWN, UNKNOWN, BUSY, OUT OF SERVICE, GOING OUT OF SERVICE, DOWN WHEN GOING OUT OF SERVICE, NS_EMPTY_STR, Unknown, DISABLED</td></tr><tr><td>monitortotalprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of probes sent to monitor this service.</td></tr><tr><td>monstatparam1</td><td>&lt;Integer></td><td>Read-only</td><td>First parameter for use with message code.</td></tr><tr><td>responsetime</td><td>&lt;Double></td><td>Read-only</td><td>Response time of this monitor.</td></tr><tr><td>monitortotalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of failed probes.</td></tr><tr><td>monitorcurrentfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>Total number of currently failed probes.</td></tr><tr><td>totalfailedprobes</td><td>&lt;Double></td><td>Read-only</td><td>The total number of failed probs.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/gslbservice_lbmonitor_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"gslbservice_lbmonitor_binding":{<b>"servicename":<String_value>,</b>"monitor_name":<String_value>,"monstate":<String_value>,"weight":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;?<b>args=monitor_name:&lt;String_value&gt;</b>



<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of gslbservice_lbmonitor_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the gslbservice_lbmonitor_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbservice_lbmonitor_binding": [ {"servicename":<String_value>,"weight":<Double_value>,"monitor_name":<String_value>,"monstate":<String_value>,"monstatparam2":<Integer_value>,"monstatcode":<Integer_value>,"lastresponse":<String_value>,"failedprobes":<Double_value>,"monstatparam3":<Integer_value>,"monitor_state":<String_value>,"monitortotalprobes":<Double_value>,"monstatparam1":<Integer_value>,"responsetime":<Double_value>,"monitortotalfailedprobes":<Double_value>,"monitorcurrentfailedprobes":<Double_value>,"totalfailedprobes":<Double_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "gslbservice_lbmonitor_binding": [ {"servicename":<String_value>,"weight":<Double_value>,"monitor_name":<String_value>,"monstate":<String_value>,"monstatparam2":<Integer_value>,"monstatcode":<Integer_value>,"lastresponse":<String_value>,"failedprobes":<Double_value>,"monstatparam3":<Integer_value>,"monitor_state":<String_value>,"monitortotalprobes":<Double_value>,"monstatparam1":<Integer_value>,"responsetime":<Double_value>,"monitortotalfailedprobes":<Double_value>,"monitorcurrentfailedprobes":<Double_value>,"totalfailedprobes":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/gslbservice_lbmonitor_binding/servicename_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"gslbservice_lbmonitor_binding": [ { "__count": "#no"} ] }```



