#nsdhcpparams

Configuration for DHCP parameters resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>dhcpclient</td><td>&lt;String></td><td>Read-write</td><td>Enables DHCP client to acquire IP address from the DHCP server in the next boot. When set to OFF, disables the DHCP client in the next boot.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>saveroute</td><td>&lt;String></td><td>Read-write</td><td>DHCP acquired routes are saved on the Citrix ADC.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-only</td><td>DHCP acquired IP.</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-only</td><td>DHCP acquired Netmask.</td></tr><tr><td>hostrtgw</td><td>&lt;String></td><td>Read-only</td><td>DHCP acquired Gateway.</td></tr><tr><td>running</td><td>&lt;Boolean></td><td>Read-only</td><td>DHCP mode.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsdhcpparams
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsdhcpparams":{"dhcpclient":<String_value>,"saveroute":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsdhcpparams?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsdhcpparams":{"dhcpclient":true,"saveroute":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsdhcpparams
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsdhcpparams": [ {"dhcpclient":<String_value>,"ipaddress":<String_value>,"netmask":<String_value>,"hostrtgw":<String_value>,"running":<Boolean_value>,"saveroute":<String_value>}]}```



