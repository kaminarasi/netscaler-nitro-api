#vpnvserver_authenticationoauthidppolicy_binding

Binding object showing the authenticationoauthidppolicy that can be bound to vpnvserver.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Integer specifying the policy's priority. The lower the number, the higher the priority. Policies are evaluated in the order of their priority numbers. Maximum value for default syntax policies is 2147483647 and for classic policies is 64000.<br>Minimum value = 0<br>Maximum value = 2147483647</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Next priority expression.</td></tr><tr><td>policy</td><td>&lt;String></td><td>Read-write</td><td>The name of the policy, if any, bound to the VPN virtual server.</td></tr><tr><td>groupextraction</td><td>&lt;Boolean></td><td>Read-write</td><td>Binds the authentication policy to a tertiary chain which will be used only for group extraction. The user will not authenticate against this server, and this will only be called if primary and/or secondary authentication has succeeded.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the virtual server.<br>Minimum length = 1</td></tr><tr><td>secondary</td><td>&lt;Boolean></td><td>Read-write</td><td>Binds the authentication policy as the secondary policy to use in a two-factor configuration. A user must then authenticate not only via a primary authentication method but also via a secondary authentication method. User groups are aggregated across both. The user name must be exactly the same for both authentication methods, but they can require different passwords.</td></tr><tr><td>bindpoint</td><td>&lt;String></td><td>Read-write</td><td>Bind point to which to bind the policy. Applies only to rewrite and cache policies. If you do not set this parameter, the policy is bound to REQ_DEFAULT or RES_DEFAULT, depending on whether the policy rule is a response-time or a request-time expression.<br>Possible values = REQUEST, RESPONSE, ICA_REQUEST, OTHERTCP_REQUEST</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#get-)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Request Payload: </b>
<b>Response:</b>
HTTP Status Code on Success: 201 Created


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of vpnvserver_authenticationoauthidppolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vpnvserver_authenticationoauthidppolicy_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vpnvserver_authenticationoauthidppolicy_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OK

Content-Type:application/json

<b>Response Payload: </b>


