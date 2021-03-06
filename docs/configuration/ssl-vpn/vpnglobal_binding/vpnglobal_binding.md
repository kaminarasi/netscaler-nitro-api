#vpnglobal_binding

Binding object which returns the resources bound to vpnglobal.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vpnglobal_intranetip6_binding</td><td>&lt;vpnglobal_intranetip6_binding[]></td><td>Read-only</td><td>intranetip6 that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_auditnslogpolicy_binding</td><td>&lt;vpnglobal_auditnslogpolicy_binding[]></td><td>Read-only</td><td>auditnslogpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationpolicy_binding</td><td>&lt;vpnglobal_authenticationpolicy_binding[]></td><td>Read-only</td><td>authenticationpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationradiuspolicy_binding</td><td>&lt;vpnglobal_authenticationradiuspolicy_binding[]></td><td>Read-only</td><td>authenticationradiuspolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnsessionpolicy_binding</td><td>&lt;vpnglobal_vpnsessionpolicy_binding[]></td><td>Read-only</td><td>vpnsessionpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_domain_binding</td><td>&lt;vpnglobal_domain_binding[]></td><td>Read-only</td><td>domain that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpneula_binding</td><td>&lt;vpnglobal_vpneula_binding[]></td><td>Read-only</td><td>vpneula that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnclientlessaccesspolicy_binding</td><td>&lt;vpnglobal_vpnclientlessaccesspolicy_binding[]></td><td>Read-only</td><td>vpnclientlessaccesspolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_intranetip_binding</td><td>&lt;vpnglobal_intranetip_binding[]></td><td>Read-only</td><td>intranetip that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnnexthopserver_binding</td><td>&lt;vpnglobal_vpnnexthopserver_binding[]></td><td>Read-only</td><td>vpnnexthopserver that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationldappolicy_binding</td><td>&lt;vpnglobal_authenticationldappolicy_binding[]></td><td>Read-only</td><td>authenticationldappolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_sharefileserver_binding</td><td>&lt;vpnglobal_sharefileserver_binding[]></td><td>Read-only</td><td>sharefileserver that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpntrafficpolicy_binding</td><td>&lt;vpnglobal_vpntrafficpolicy_binding[]></td><td>Read-only</td><td>vpntrafficpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationlocalpolicy_binding</td><td>&lt;vpnglobal_authenticationlocalpolicy_binding[]></td><td>Read-only</td><td>authenticationlocalpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnintranetapplication_binding</td><td>&lt;vpnglobal_vpnintranetapplication_binding[]></td><td>Read-only</td><td>vpnintranetapplication that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_appcontroller_binding</td><td>&lt;vpnglobal_appcontroller_binding[]></td><td>Read-only</td><td>appcontroller that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationnegotiatepolicy_binding</td><td>&lt;vpnglobal_authenticationnegotiatepolicy_binding[]></td><td>Read-only</td><td>authenticationnegotiatepolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationtacacspolicy_binding</td><td>&lt;vpnglobal_authenticationtacacspolicy_binding[]></td><td>Read-only</td><td>authenticationtacacspolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnportaltheme_binding</td><td>&lt;vpnglobal_vpnportaltheme_binding[]></td><td>Read-only</td><td>vpnportaltheme that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationsamlpolicy_binding</td><td>&lt;vpnglobal_authenticationsamlpolicy_binding[]></td><td>Read-only</td><td>authenticationsamlpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_staserver_binding</td><td>&lt;vpnglobal_staserver_binding[]></td><td>Read-only</td><td>staserver that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_auditsyslogpolicy_binding</td><td>&lt;vpnglobal_auditsyslogpolicy_binding[]></td><td>Read-only</td><td>auditsyslogpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_authenticationcertpolicy_binding</td><td>&lt;vpnglobal_authenticationcertpolicy_binding[]></td><td>Read-only</td><td>authenticationcertpolicy that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_vpnurl_binding</td><td>&lt;vpnglobal_vpnurl_binding[]></td><td>Read-only</td><td>vpnurl that can be bound to vpnglobal.</td></tr><tr><td>vpnglobal_sslcertkey_binding</td><td>&lt;vpnglobal_sslcertkey_binding[]></td><td>Read-only</td><td>sslcertkey that can be bound to vpnglobal.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnglobal_binding
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnglobal_binding": [ {"vpnglobal_vpnintranetapplication_binding":<vpnglobal_vpnintranetapplication_binding[]_value>,"vpnglobal_sslcertkey_binding":<vpnglobal_sslcertkey_binding[]_value>,"vpnglobal_authenticationsamlpolicy_binding":<vpnglobal_authenticationsamlpolicy_binding[]_value>,"vpnglobal_intranetip_binding":<vpnglobal_intranetip_binding[]_value>,"vpnglobal_authenticationradiuspolicy_binding":<vpnglobal_authenticationradiuspolicy_binding[]_value>,"vpnglobal_staserver_binding":<vpnglobal_staserver_binding[]_value>,"vpnglobal_sharefileserver_binding":<vpnglobal_sharefileserver_binding[]_value>,"vpnglobal_intranetip6_binding":<vpnglobal_intranetip6_binding[]_value>,"vpnglobal_appcontroller_binding":<vpnglobal_appcontroller_binding[]_value>,"vpnglobal_authenticationtacacspolicy_binding":<vpnglobal_authenticationtacacspolicy_binding[]_value>,"vpnglobal_authenticationpolicy_binding":<vpnglobal_authenticationpolicy_binding[]_value>,"vpnglobal_vpntrafficpolicy_binding":<vpnglobal_vpntrafficpolicy_binding[]_value>,"vpnglobal_domain_binding":<vpnglobal_domain_binding[]_value>,"vpnglobal_vpnnexthopserver_binding":<vpnglobal_vpnnexthopserver_binding[]_value>,"vpnglobal_authenticationldappolicy_binding":<vpnglobal_authenticationldappolicy_binding[]_value>,"vpnglobal_vpnsessionpolicy_binding":<vpnglobal_vpnsessionpolicy_binding[]_value>,"vpnglobal_authenticationcertpolicy_binding":<vpnglobal_authenticationcertpolicy_binding[]_value>,"vpnglobal_authenticationnegotiatepolicy_binding":<vpnglobal_authenticationnegotiatepolicy_binding[]_value>,"vpnglobal_auditsyslogpolicy_binding":<vpnglobal_auditsyslogpolicy_binding[]_value>,"vpnglobal_vpneula_binding":<vpnglobal_vpneula_binding[]_value>,"vpnglobal_vpnurl_binding":<vpnglobal_vpnurl_binding[]_value>,"vpnglobal_vpnportaltheme_binding":<vpnglobal_vpnportaltheme_binding[]_value>,"vpnglobal_vpnclientlessaccesspolicy_binding":<vpnglobal_vpnclientlessaccesspolicy_binding[]_value>,"vpnglobal_authenticationlocalpolicy_binding":<vpnglobal_authenticationlocalpolicy_binding[]_value>,"vpnglobal_auditnslogpolicy_binding":<vpnglobal_auditnslogpolicy_binding[]_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnglobal_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnglobal_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vpnglobal_binding": [ {"vpnglobal_vpnintranetapplication_binding":<vpnglobal_vpnintranetapplication_binding[]_value>,"vpnglobal_sslcertkey_binding":<vpnglobal_sslcertkey_binding[]_value>,"vpnglobal_authenticationsamlpolicy_binding":<vpnglobal_authenticationsamlpolicy_binding[]_value>,"vpnglobal_intranetip_binding":<vpnglobal_intranetip_binding[]_value>,"vpnglobal_authenticationradiuspolicy_binding":<vpnglobal_authenticationradiuspolicy_binding[]_value>,"vpnglobal_staserver_binding":<vpnglobal_staserver_binding[]_value>,"vpnglobal_sharefileserver_binding":<vpnglobal_sharefileserver_binding[]_value>,"vpnglobal_intranetip6_binding":<vpnglobal_intranetip6_binding[]_value>,"vpnglobal_appcontroller_binding":<vpnglobal_appcontroller_binding[]_value>,"vpnglobal_authenticationtacacspolicy_binding":<vpnglobal_authenticationtacacspolicy_binding[]_value>,"vpnglobal_authenticationpolicy_binding":<vpnglobal_authenticationpolicy_binding[]_value>,"vpnglobal_vpntrafficpolicy_binding":<vpnglobal_vpntrafficpolicy_binding[]_value>,"vpnglobal_domain_binding":<vpnglobal_domain_binding[]_value>,"vpnglobal_vpnnexthopserver_binding":<vpnglobal_vpnnexthopserver_binding[]_value>,"vpnglobal_authenticationldappolicy_binding":<vpnglobal_authenticationldappolicy_binding[]_value>,"vpnglobal_vpnsessionpolicy_binding":<vpnglobal_vpnsessionpolicy_binding[]_value>,"vpnglobal_authenticationcertpolicy_binding":<vpnglobal_authenticationcertpolicy_binding[]_value>,"vpnglobal_authenticationnegotiatepolicy_binding":<vpnglobal_authenticationnegotiatepolicy_binding[]_value>,"vpnglobal_auditsyslogpolicy_binding":<vpnglobal_auditsyslogpolicy_binding[]_value>,"vpnglobal_vpneula_binding":<vpnglobal_vpneula_binding[]_value>,"vpnglobal_vpnurl_binding":<vpnglobal_vpnurl_binding[]_value>,"vpnglobal_vpnportaltheme_binding":<vpnglobal_vpnportaltheme_binding[]_value>,"vpnglobal_vpnclientlessaccesspolicy_binding":<vpnglobal_vpnclientlessaccesspolicy_binding[]_value>,"vpnglobal_authenticationlocalpolicy_binding":<vpnglobal_authenticationlocalpolicy_binding[]_value>,"vpnglobal_auditnslogpolicy_binding":<vpnglobal_auditnslogpolicy_binding[]_value>}]}```



