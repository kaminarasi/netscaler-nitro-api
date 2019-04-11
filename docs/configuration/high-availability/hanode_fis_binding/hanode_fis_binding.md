#hanode_fis_binding

Binding object showing the fis that can be bound to hanode.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Node Name.</td></tr><tr><td>routemonitor</td><td>&lt;String></td><td>Read-write</td><td>A route that you want the Citrix ADC to monitor in its internal routing table. You can specify an IPv4 address or network, or an IPv6 address or network prefix. If you specify an IPv4 network address or IPv6 network prefix, the appliance monitors any route that matches the network or prefix.<br>Minimum length = 1</td></tr><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>Number that uniquely identifies the local node. The ID of the local node is always 0.<br>Minimum value = 0<br>Maximum value = 64</td></tr><tr><td>enaifaces</td><td>&lt;String></td><td>Read-only</td><td>Enabled interfaces.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding/id_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding/id_value&lt;Double&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of hanode_fis_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding/id_value&lt;Double&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the hanode_fis_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "hanode_fis_binding": [ {"name":<String_value>,"routemonitor":<String_value>,"id":<Double_value>,"enaifaces":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "hanode_fis_binding": [ {"name":<String_value>,"routemonitor":<String_value>,"id":<Double_value>,"enaifaces":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/hanode_fis_binding/id_value&lt;Double&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"hanode_fis_binding": [ { "__count": "#no"} ] }```



