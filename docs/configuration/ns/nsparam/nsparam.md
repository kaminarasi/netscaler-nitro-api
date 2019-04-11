#nsparam

Configuration for Citrix ADC parameters resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>httpport</td><td>&lt;Integer[]></td><td>Read-write</td><td>HTTP ports on the web server. This allows the system to perform connection off-load for any client request that has a destination port matching one of these configured ports.<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>maxconn</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of connections that will be made from the appliance to the web server(s) attached to it. The value entered here is applied globally to all attached servers.<br>Default value: 0<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>maxreq</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of requests that the system can pass on a particular connection between the appliance and a server attached to it. Setting this value to 0 allows an unlimited number of requests to be passed. This value is overridden by the maximum number of requests configured on the individual service.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>cip</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the insertion of the actual client IP address into the HTTP header request passed from the client to one, some, or all servers attached to the system. The passed address can then be accessed through a minor modification to the server.<br>* If the CIP header is specified, it will be used as the client IP header.<br>* If the CIP header is not specified, the value that has been set will be used as the client IP header.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipheader</td><td>&lt;String></td><td>Read-write</td><td>Text that will be used as the client IP address header.<br>Minimum length = 1</td></tr><tr><td>cookieversion</td><td>&lt;String></td><td>Read-write</td><td>Version of the cookie inserted by the system.<br>Possible values = 0, 1</td></tr><tr><td>securecookie</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable secure flag for persistence cookie.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>pmtumin</td><td>&lt;Double></td><td>Read-write</td><td>Minimum path MTU value that Citrix ADC will process in the ICMP fragmentation needed message. If the ICMP message contains a value less than this value, then this value is used instead.<br>Default value: 576<br>Minimum value = 168<br>Maximum value = 1500</td></tr><tr><td>pmtutimeout</td><td>&lt;Double></td><td>Read-write</td><td>Interval, in minutes, for flushing the PMTU entries.<br>Default value: 10<br>Minimum value = 1<br>Maximum value = 1440</td></tr><tr><td>ftpportrange</td><td>&lt;String></td><td>Read-write</td><td>Minimum and maximum port (port range) that FTP services are allowed to use.<br>Minimum length = 1024<br>Maximum length = 64000</td></tr><tr><td>crportrange</td><td>&lt;String></td><td>Read-write</td><td>Port range for cache redirection services.<br>Minimum length = 1<br>Maximum length = 65535</td></tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Time zone for the Citrix ADC. Name of the time zone should be specified as argument.<br>Minimum length = 1<br>Maximum length = 63</td></tr><tr><td>grantquotamaxclient</td><td>&lt;Double></td><td>Read-write</td><td>Percentage of shared quota to be granted at a time for maxClient.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>exclusivequotamaxclient</td><td>&lt;Double></td><td>Read-write</td><td>Percentage of maxClient to be given to PEs.<br>Default value: 80<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>grantquotaspillover</td><td>&lt;Double></td><td>Read-write</td><td>Percentage of shared quota to be granted at a time for spillover.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>exclusivequotaspillover</td><td>&lt;Double></td><td>Read-write</td><td>Percentage of maximum limit to be given to PEs.<br>Default value: 80<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>useproxyport</td><td>&lt;String></td><td>Read-write</td><td>Enable/Disable use_proxy_port setting.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>internaluserlogin</td><td>&lt;String></td><td>Read-write</td><td>Enables/disables the internal user from logging in to the appliance. Before disabling internal user login, you must have key-based authentication set up on the appliance. The file name for the key pair must be "ns_comm_key".<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>aftpallowrandomsourceport</td><td>&lt;String></td><td>Read-write</td><td>Allow the FTP server to come from a random source port for active FTP data connections.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>icaports</td><td>&lt;Integer[]></td><td>Read-write</td><td>The ICA ports on the Web server. This allows the system to perform connection off-load for any<br>client request that has a destination port matching one of these configured ports.<br>Minimum value = 1</td></tr><tr><td>tcpcip</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable the insertion of the client TCP/IP header in TCP payload passed from the client to one, some, or all servers attached to the system. The passed address can then be accessed through a minor modification to the server.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>servicepathingressvlan</td><td>&lt;Double></td><td>Read-write</td><td>VLAN on which the subscriber traffic arrives on the appliance.<br>Minimum value = 1</td></tr><tr><td>secureicaports</td><td>&lt;Integer[]></td><td>Read-write</td><td>The Secure ICA ports on the Web server. This allows the system to perform connection off-load for any<br>client request that has a destination port matching one of these configured ports.<br>Minimum value = 1</td></tr><tr><td>mgmthttpport</td><td>&lt;Integer></td><td>Read-write</td><td>This allow the configuration of management HTTP port.<br>Default value: 80<br>Minimum value = 1<br>Maximum value = 65534</td></tr><tr><td>mgmthttpsport</td><td>&lt;Integer></td><td>Read-write</td><td>This allows the configuration of management HTTPS port.<br>Default value: 443<br>Minimum value = 1<br>Maximum value = 65534</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsparam
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsparam":{"httpport":<Integer[]_value>,"maxconn":<Double_value>,"maxreq":<Double_value>,"cip":<String_value>,"cipheader":<String_value>,"cookieversion":<String_value>,"securecookie":<String_value>,"pmtumin":<Double_value>,"pmtutimeout":<Double_value>,"ftpportrange":<String_value>,"crportrange":<String_value>,"timezone":<String_value>,"grantquotamaxclient":<Double_value>,"exclusivequotamaxclient":<Double_value>,"grantquotaspillover":<Double_value>,"exclusivequotaspillover":<Double_value>,"useproxyport":<String_value>,"internaluserlogin":<String_value>,"aftpallowrandomsourceport":<String_value>,"icaports":<Integer[]_value>,"tcpcip":<String_value>,"servicepathingressvlan":<Double_value>,"secureicaports":<Integer[]_value>,"mgmthttpport":<Integer_value>,"mgmthttpsport":<Integer_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsparam?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsparam":{"ftpportrange":true,"crportrange":true,"aftpallowrandomsourceport":true,"httpport":true,"maxconn":true,"maxreq":true,"cip":true,"cipheader":true,"cookieversion":true,"securecookie":true,"pmtumin":true,"pmtutimeout":true,"timezone":true,"grantquotamaxclient":true,"exclusivequotamaxclient":true,"grantquotaspillover":true,"exclusivequotaspillover":true,"useproxyport":true,"internaluserlogin":true,"icaports":true,"tcpcip":true,"servicepathingressvlan":true,"secureicaports":true,"mgmthttpport":true,"mgmthttpsport":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsparam
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsparam": [ {"httpport":<Integer[]_value>,"maxconn":<Double_value>,"maxreq":<Double_value>,"cip":<String_value>,"cipheader":<String_value>,"cookieversion":<String_value>,"securecookie":<String_value>,"pmtumin":<Double_value>,"pmtutimeout":<Double_value>,"ftpportrange":<String_value>,"crportrange":<String_value>,"timezone":<String_value>,"grantquotamaxclient":<Double_value>,"exclusivequotamaxclient":<Double_value>,"grantquotaspillover":<Double_value>,"exclusivequotaspillover":<Double_value>,"useproxyport":<String_value>,"internaluserlogin":<String_value>,"aftpallowrandomsourceport":<String_value>,"icaports":<Integer[]_value>,"tcpcip":<String_value>,"servicepathingressvlan":<Double_value>,"secureicaports":<Integer[]_value>,"mgmthttpport":<Integer_value>,"mgmthttpsport":<Integer_value>}]}```



