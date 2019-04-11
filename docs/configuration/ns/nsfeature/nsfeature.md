#nsfeature

Configuration for feature resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>feature</td><td>&lt;String[]></td><td>Read-write</td><td>Feature to be enabled. Multiple features can be specified by providing a blank space between each feature.</td></tr><tr><td>wl</td><td>&lt;Boolean></td><td>Read-only</td><td>Web Logging.</td></tr><tr><td>sp</td><td>&lt;Boolean></td><td>Read-only</td><td>Surge Protection.</td></tr><tr><td>lb</td><td>&lt;Boolean></td><td>Read-only</td><td>Load Balancing.</td></tr><tr><td>cs</td><td>&lt;Boolean></td><td>Read-only</td><td>Content Switching.</td></tr><tr><td>cr</td><td>&lt;Boolean></td><td>Read-only</td><td>Cache Redirect.</td></tr><tr><td>sc</td><td>&lt;Boolean></td><td>Read-only</td><td>Sure Connect.</td></tr><tr><td>cmp</td><td>&lt;Boolean></td><td>Read-only</td><td>Compression.</td></tr><tr><td>pq</td><td>&lt;Boolean></td><td>Read-only</td><td>Priority Queuing.</td></tr><tr><td>ssl</td><td>&lt;Boolean></td><td>Read-only</td><td>Secure Sockets Layer.</td></tr><tr><td>gslb</td><td>&lt;Boolean></td><td>Read-only</td><td>Global Server Load Balancing.</td></tr><tr><td>hdosp</td><td>&lt;Boolean></td><td>Read-only</td><td>DOS Protection.</td></tr><tr><td>cf</td><td>&lt;Boolean></td><td>Read-only</td><td>Content Filter.</td></tr><tr><td>ic</td><td>&lt;Boolean></td><td>Read-only</td><td>Integrated Caching.</td></tr><tr><td>sslvpn</td><td>&lt;Boolean></td><td>Read-only</td><td>SSL VPN.</td></tr><tr><td>aaa</td><td>&lt;Boolean></td><td>Read-only</td><td>AAA.</td></tr><tr><td>ospf</td><td>&lt;Boolean></td><td>Read-only</td><td>OSPF Routing.</td></tr><tr><td>rip</td><td>&lt;Boolean></td><td>Read-only</td><td>RIP Routing.</td></tr><tr><td>bgp</td><td>&lt;Boolean></td><td>Read-only</td><td>BGP Routing.</td></tr><tr><td>rewrite</td><td>&lt;Boolean></td><td>Read-only</td><td>Rewrite.</td></tr><tr><td>ipv6pt</td><td>&lt;Boolean></td><td>Read-only</td><td>IPv6 protocol translation.</td></tr><tr><td>appfw</td><td>&lt;Boolean></td><td>Read-only</td><td>Application Firewall.</td></tr><tr><td>responder</td><td>&lt;Boolean></td><td>Read-only</td><td>Responder.</td></tr><tr><td>htmlinjection</td><td>&lt;Boolean></td><td>Read-only</td><td>HTML Injection.</td></tr><tr><td>push</td><td>&lt;Boolean></td><td>Read-only</td><td>Citrix ADC Push.</td></tr><tr><td>appflow</td><td>&lt;Boolean></td><td>Read-only</td><td>AppFlow.</td></tr><tr><td>cloudbridge</td><td>&lt;Boolean></td><td>Read-only</td><td>CloudBridge.</td></tr><tr><td>isis</td><td>&lt;Boolean></td><td>Read-only</td><td>ISIS Routing.</td></tr><tr><td>ch</td><td>&lt;Boolean></td><td>Read-only</td><td>Call Home.</td></tr><tr><td>appqoe</td><td>&lt;Boolean></td><td>Read-only</td><td>AppQoS.</td></tr><tr><td>contentaccelerator</td><td>&lt;Boolean></td><td>Read-only</td><td>Transparent Integrated Caching.</td></tr><tr><td>rise</td><td>&lt;Boolean></td><td>Read-only</td><td>RISE.</td></tr><tr><td>feo</td><td>&lt;Boolean></td><td>Read-only</td><td>Optimize Web content (HTML, CSS, JavaScript, images).</td></tr><tr><td>lsn</td><td>&lt;Boolean></td><td>Read-only</td><td>Large Scale NAT.</td></tr><tr><td>rdpproxy</td><td>&lt;Boolean></td><td>Read-only</td><td>RDPPROXY.</td></tr><tr><td>rep</td><td>&lt;Boolean></td><td>Read-only</td><td>Reputation Services.</td></tr><tr><td>urlfiltering</td><td>&lt;Boolean></td><td>Read-only</td><td>URL Filtering.</td></tr><tr><td>videooptimization</td><td>&lt;Boolean></td><td>Read-only</td><td>Video Optimization.</td></tr><tr><td>forwardproxy</td><td>&lt;Boolean></td><td>Read-only</td><td>Forward Proxy.</td></tr><tr><td>sslinterception</td><td>&lt;Boolean></td><td>Read-only</td><td>SSL Interception.</td></tr><tr><td>adaptivetcp</td><td>&lt;Boolean></td><td>Read-only</td><td>Adaptive TCP.</td></tr><tr><td>cqa</td><td>&lt;Boolean></td><td>Read-only</td><td>Connection Quality Analytics.</td></tr><tr><td>ci</td><td>&lt;Boolean></td><td>Read-only</td><td>Content Inspection.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ENABLE](#e)| [DISABLE](#di)| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###enable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsfeature?<b>action=enable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsfeature":{"feature":<String[]_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###disable



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsfeature?<b>action=disable</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsfeature":{"feature":<String[]_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsfeature
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsfeature": [ {"feature":<String[]_value>,"wl":<Boolean_value>,"sp":<Boolean_value>,"lb":<Boolean_value>,"cs":<Boolean_value>,"cr":<Boolean_value>,"sc":<Boolean_value>,"cmp":<Boolean_value>,"pq":<Boolean_value>,"ssl":<Boolean_value>,"gslb":<Boolean_value>,"hdosp":<Boolean_value>,"routing":<Boolean_value>,"cf":<Boolean_value>,"ic":<Boolean_value>,"sslvpn":<Boolean_value>,"aaa":<Boolean_value>,"ospf":<Boolean_value>,"rip":<Boolean_value>,"bgp":<Boolean_value>,"rewrite":<Boolean_value>,"ipv6pt":<Boolean_value>,"appfw":<Boolean_value>,"responder":<Boolean_value>,"htmlinjection":<Boolean_value>,"push":<Boolean_value>,"appflow":<Boolean_value>,"cloudbridge":<Boolean_value>,"isis":<Boolean_value>,"ch":<Boolean_value>,"appqoe":<Boolean_value>,"contentaccelerator":<Boolean_value>,"rise":<Boolean_value>,"feo":<Boolean_value>,"lsn":<Boolean_value>,"rdpproxy":<Boolean_value>,"rep":<Boolean_value>,"urlfiltering":<Boolean_value>,"videooptimization":<Boolean_value>,"forwardproxy":<Boolean_value>,"sslinterception":<Boolean_value>,"adaptivetcp":<Boolean_value>,"cqa":<Boolean_value>,"ci":<Boolean_value>}]}```



