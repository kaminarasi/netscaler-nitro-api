#lsnclient_binding

Binding object which returns the resources bound to lsnclient.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clientname</td><td>&lt;String></td><td>Read-write</td><td>Name for the LSN client entity. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the LSN client is created. The following requirement applies only to the Citrix ADC CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "lsn client1" or 'lsn client1'). .<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>lsnclient_network_binding</td><td>&lt;lsnclient_network_binding[]></td><td>Read-only</td><td>network that can be bound to lsnclient.</td></tr><tr><td>lsnclient_network6_binding</td><td>&lt;lsnclient_network6_binding[]></td><td>Read-only</td><td>network6 that can be bound to lsnclient.</td></tr><tr><td>lsnclient_nsacl6_binding</td><td>&lt;lsnclient_nsacl6_binding[]></td><td>Read-only</td><td>nsacl6 that can be bound to lsnclient.</td></tr><tr><td>lsnclient_nsacl_binding</td><td>&lt;lsnclient_nsacl_binding[]></td><td>Read-only</td><td>nsacl that can be bound to lsnclient.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnclient_binding/clientname_value&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnclient_binding": [ {"clientname":<String_value>,"lsnclient_nsacl6_binding":<lsnclient_nsacl6_binding[]_value>,"lsnclient_network_binding":<lsnclient_network_binding[]_value>,"lsnclient_network6_binding":<lsnclient_network6_binding[]_value>,"lsnclient_nsacl_binding":<lsnclient_nsacl_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnclient_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/lsnclient_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "lsnclient_binding": [ {"clientname":<String_value>,"lsnclient_nsacl6_binding":<lsnclient_nsacl6_binding[]_value>,"lsnclient_network_binding":<lsnclient_network_binding[]_value>,"lsnclient_network6_binding":<lsnclient_network6_binding[]_value>,"lsnclient_nsacl_binding":<lsnclient_nsacl_binding[]_value>}]}```



