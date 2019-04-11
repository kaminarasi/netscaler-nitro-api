#bridgegroup_nsip_binding

Binding object showing the nsip that can be bound to bridgegroup.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ownergroup</td><td>&lt;String></td><td>Read-write</td><td>The owner node group in a Cluster for this vlan.<br>Default value: DEFAULT_NG<br>Minimum length = 1</td></tr><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>The integer that uniquely identifies the bridge group.<br>Minimum value = 1<br>Maximum value = 1000</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>The network mask for the subnet defined for the bridge group.</td></tr><tr><td>td</td><td>&lt;Double></td><td>Read-write</td><td>Integer value that uniquely identifies the traffic domain in which you want to configure the entity. If you do not specify an ID, the entity becomes part of the default traffic domain, which has an ID of 0.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>The IP address assigned to the bridge group.</td></tr><tr><td>rnat</td><td>&lt;Boolean></td><td>Read-only</td><td>Temporary flag used for internal purpose.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/bridgegroup_nsip_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"bridgegroup_nsip_binding":{<b>"id":<Double_value>,</b>"ipaddress":<String_value>,"netmask":<String_value>,"td":<Double_value>,"ownergroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;?<b>args=ipaddress:&lt;String_value&gt;,netmask:&lt;String_value&gt;,td:&lt;Double_value&gt;,ownergroup:&lt;String_value&gt;</b>



<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of bridgegroup_nsip_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the bridgegroup_nsip_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "bridgegroup_nsip_binding": [ {"ownergroup":<String_value>,"id":<Double_value>,"netmask":<String_value>,"td":<Double_value>,"ipaddress":<String_value>,"rnat":<Boolean_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "bridgegroup_nsip_binding": [ {"ownergroup":<String_value>,"id":<Double_value>,"netmask":<String_value>,"td":<Double_value>,"ipaddress":<String_value>,"rnat":<Boolean_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/bridgegroup_nsip_binding/id_value&lt;Double&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"bridgegroup_nsip_binding": [ { "__count": "#no"} ] }```



