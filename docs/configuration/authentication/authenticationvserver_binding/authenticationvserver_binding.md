#authenticationvserver_binding

Binding object which returns the resources bound to authenticationvserver.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the authentication virtual server.<br>Minimum length = 1</td></tr><tr><td>authenticationvserver_auditnslogpolicy_binding</td><td>&lt;authenticationvserver_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationpolicy_binding</td><td>&lt;authenticationvserver_authenticationpolicy_binding[]></td><td>Read-only</td><td>authenticationpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationradiuspolicy_binding</td><td>&lt;authenticationvserver_authenticationradiuspolicy_binding[]></td><td>Read-only</td><td>authenticationradiuspolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationldappolicy_binding</td><td>&lt;authenticationvserver_authenticationldappolicy_binding[]></td><td>Read-only</td><td>authenticationldappolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationsamlidppolicy_binding</td><td>&lt;authenticationvserver_authenticationsamlidppolicy_binding[]></td><td>Read-only</td><td>authenticationsamlidppolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationwebauthpolicy_binding</td><td>&lt;authenticationvserver_authenticationwebauthpolicy_binding[]></td><td>Read-only</td><td>authenticationwebauthpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationlocalpolicy_binding</td><td>&lt;authenticationvserver_authenticationlocalpolicy_binding[]></td><td>Read-only</td><td>authenticationlocalpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationnegotiatepolicy_binding</td><td>&lt;authenticationvserver_authenticationnegotiatepolicy_binding[]></td><td>Read-only</td><td>authenticationnegotiatepolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationtacacspolicy_binding</td><td>&lt;authenticationvserver_authenticationtacacspolicy_binding[]></td><td>Read-only</td><td>authenticationtacacspolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_vpnportaltheme_binding</td><td>&lt;authenticationvserver_vpnportaltheme_binding[]></td><td>Read-only</td><td>vpnportaltheme that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationsamlpolicy_binding</td><td>&lt;authenticationvserver_authenticationsamlpolicy_binding[]></td><td>Read-only</td><td>authenticationsamlpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_cspolicy_binding</td><td>&lt;authenticationvserver_cspolicy_binding[]></td><td>Read-only</td><td>cspolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_auditsyslogpolicy_binding</td><td>&lt;authenticationvserver_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationloginschemapolicy_binding</td><td>&lt;authenticationvserver_authenticationloginschemapolicy_binding[]></td><td>Read-only</td><td>authenticationloginschemapolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationcertpolicy_binding</td><td>&lt;authenticationvserver_authenticationcertpolicy_binding[]></td><td>Read-only</td><td>authenticationcertpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_tmsessionpolicy_binding</td><td>&lt;authenticationvserver_tmsessionpolicy_binding[]></td><td>Read-only</td><td>tmsessionpolicy that can be bound to authenticationvserver.</td></tr><tr><td>authenticationvserver_authenticationoauthidppolicy_binding</td><td>&lt;authenticationvserver_authenticationoauthidppolicy_binding[]></td><td>Read-only</td><td>authenticationoauthidppolicy that can be bound to authenticationvserver.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver_binding/name_value&lt;String&gt;
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationvserver_binding": [ {"name":<String_value>,"authenticationvserver_authenticationlocalpolicy_binding":<authenticationvserver_authenticationlocalpolicy_binding[]_value>,"authenticationvserver_tmsessionpolicy_binding":<authenticationvserver_tmsessionpolicy_binding[]_value>,"authenticationvserver_cspolicy_binding":<authenticationvserver_cspolicy_binding[]_value>,"authenticationvserver_auditsyslogpolicy_binding":<authenticationvserver_auditsyslogpolicy_binding[]_value>,"authenticationvserver_authenticationsamlidppolicy_binding":<authenticationvserver_authenticationsamlidppolicy_binding[]_value>,"authenticationvserver_auditnslogpolicy_binding":<authenticationvserver_auditnslogpolicy_binding[]_value>,"authenticationvserver_authenticationldappolicy_binding":<authenticationvserver_authenticationldappolicy_binding[]_value>,"authenticationvserver_authenticationcertpolicy_binding":<authenticationvserver_authenticationcertpolicy_binding[]_value>,"authenticationvserver_authenticationsamlpolicy_binding":<authenticationvserver_authenticationsamlpolicy_binding[]_value>,"authenticationvserver_authenticationpolicy_binding":<authenticationvserver_authenticationpolicy_binding[]_value>,"authenticationvserver_vpnportaltheme_binding":<authenticationvserver_vpnportaltheme_binding[]_value>,"authenticationvserver_authenticationoauthidppolicy_binding":<authenticationvserver_authenticationoauthidppolicy_binding[]_value>,"authenticationvserver_authenticationradiuspolicy_binding":<authenticationvserver_authenticationradiuspolicy_binding[]_value>,"authenticationvserver_authenticationloginschemapolicy_binding":<authenticationvserver_authenticationloginschemapolicy_binding[]_value>,"authenticationvserver_authenticationtacacspolicy_binding":<authenticationvserver_authenticationtacacspolicy_binding[]_value>,"authenticationvserver_authenticationwebauthpolicy_binding":<authenticationvserver_authenticationwebauthpolicy_binding[]_value>,"authenticationvserver_authenticationnegotiatepolicy_binding":<authenticationvserver_authenticationnegotiatepolicy_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationvserver_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationvserver_binding": [ {"name":<String_value>,"authenticationvserver_authenticationlocalpolicy_binding":<authenticationvserver_authenticationlocalpolicy_binding[]_value>,"authenticationvserver_tmsessionpolicy_binding":<authenticationvserver_tmsessionpolicy_binding[]_value>,"authenticationvserver_cspolicy_binding":<authenticationvserver_cspolicy_binding[]_value>,"authenticationvserver_auditsyslogpolicy_binding":<authenticationvserver_auditsyslogpolicy_binding[]_value>,"authenticationvserver_authenticationsamlidppolicy_binding":<authenticationvserver_authenticationsamlidppolicy_binding[]_value>,"authenticationvserver_auditnslogpolicy_binding":<authenticationvserver_auditnslogpolicy_binding[]_value>,"authenticationvserver_authenticationldappolicy_binding":<authenticationvserver_authenticationldappolicy_binding[]_value>,"authenticationvserver_authenticationcertpolicy_binding":<authenticationvserver_authenticationcertpolicy_binding[]_value>,"authenticationvserver_authenticationsamlpolicy_binding":<authenticationvserver_authenticationsamlpolicy_binding[]_value>,"authenticationvserver_authenticationpolicy_binding":<authenticationvserver_authenticationpolicy_binding[]_value>,"authenticationvserver_vpnportaltheme_binding":<authenticationvserver_vpnportaltheme_binding[]_value>,"authenticationvserver_authenticationoauthidppolicy_binding":<authenticationvserver_authenticationoauthidppolicy_binding[]_value>,"authenticationvserver_authenticationradiuspolicy_binding":<authenticationvserver_authenticationradiuspolicy_binding[]_value>,"authenticationvserver_authenticationloginschemapolicy_binding":<authenticationvserver_authenticationloginschemapolicy_binding[]_value>,"authenticationvserver_authenticationtacacspolicy_binding":<authenticationvserver_authenticationtacacspolicy_binding[]_value>,"authenticationvserver_authenticationwebauthpolicy_binding":<authenticationvserver_authenticationwebauthpolicy_binding[]_value>,"authenticationvserver_authenticationnegotiatepolicy_binding":<authenticationvserver_authenticationnegotiatepolicy_binding[]_value>}]}```



