#csvserver_domain_binding

Binding object showing the domain that can be bound to csvserver.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>backupip</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Minimum length = 1</td><tr><tr><td>ttl</td><td>&lt;Double></td><td>Read-write</td><td>.&lt;br>Minimum value = 1</td><tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the content switching virtual server to which the content switching policy applies.&lt;br>Minimum length = 1</td><tr><tr><td>domainname</td><td>&lt;String></td><td>Read-write</td><td>Domain name for which to change the time to live (TTL) and/or backup service IP address.&lt;br>Minimum length = 1</td><tr><tr><td>sitedomainttl</td><td>&lt;Double></td><td>Read-write</td><td>.&lt;br>Minimum value = 1</td><tr><tr><td>cookiedomain</td><td>&lt;String></td><td>Read-write</td><td>.&lt;br>Minimum length = 1</td><tr><tr><td>cookietimeout</td><td>&lt;Double></td><td>Read-write</td><td>.&lt;br>Minimum value = 0&lt;br>Maximum value = 1440</td><tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-only</td><td>Enable logging appflow flow information.&lt;br>Default value: ENABLED&lt;br>Possible values = ENABLED, DISABLED</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD:](#add:) | [DELETE:](#delete:) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



URL: http://&lt;netscaler-ip-address/nitro/v1/config/csvserver_domain_binding
HTTP Method: PUT
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 

HTTP Status Code on Success: 201 Created


###delete:



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/csvserver_domain_binding/name_value&lt;String&gt;
HTTP Method: null



###get



URL:
HTTP Method: null
Request Payload: 



###count



URL:
HTTP Method: null
Request Payload: 


