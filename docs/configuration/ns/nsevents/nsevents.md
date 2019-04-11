#nsevents

Configuration for events resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>eventno</td><td>&lt;Double></td><td>Read-write</td><td>Event number starting from which events must be shown.</td></tr><tr><td>time</td><td>&lt;Double></td><td>Read-only</td><td>Event no.</td></tr><tr><td>eventcode</td><td>&lt;Double></td><td>Read-only</td><td>event Code.</td></tr><tr><td>devid</td><td>&lt;Double></td><td>Read-only</td><td>Device Name.</td></tr><tr><td>devname</td><td>&lt;String></td><td>Read-only</td><td>Device Name.</td></tr><tr><td>text</td><td>&lt;String></td><td>Read-only</td><td>Event no.</td></tr><tr><td>data0</td><td>&lt;Double></td><td>Read-only</td><td>additional event information.</td></tr><tr><td>data1</td><td>&lt;Double></td><td>Read-only</td><td>additional event information.</td></tr><tr><td>data2</td><td>&lt;Double></td><td>Read-only</td><td>additional event information.</td></tr><tr><td>data3</td><td>&lt;Double></td><td>Read-only</td><td>additional event information.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>args=eventno:&lt;Double_value&gt;</b>
Use this query-parameter to get nsevents resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of nsevents resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nsevents resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsevents": [ {eventno:<Double_value>"time":<Double_value>,"eventcode":<Double_value>,"devid":<Double_value>,"devname":<String_value>,"text":<String_value>,"data0":<Double_value>,"data1":<Double_value>,"data2":<Double_value>,"data3":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsevents?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsevents": [ { "__count": "#no"} ] }```



