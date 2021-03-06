#aaaldapparams

Configuration for LDAP parameter resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>serverip</td><td>&lt;String></td><td>Read-write</td><td>IP address of your LDAP server.</td></tr><tr><td>serverport</td><td>&lt;Integer></td><td>Read-write</td><td>Port number on which the LDAP server listens for connections.<br>Default value: 389<br>Minimum value = 1</td></tr><tr><td>authtimeout</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of seconds that the Citrix ADC waits for a response from the LDAP server.<br>Default value: 3<br>Minimum value = 1</td></tr><tr><td>ldapbase</td><td>&lt;String></td><td>Read-write</td><td>Base (the server and location) from which LDAP search commands should start. <br>If the LDAP server is running locally, the default value of base is dc=netscaler, dc=com.</td></tr><tr><td>ldapbinddn</td><td>&lt;String></td><td>Read-write</td><td>Complete distinguished name (DN) string used for binding to the LDAP server.</td></tr><tr><td>ldapbinddnpassword</td><td>&lt;String></td><td>Read-write</td><td>Password for binding to the LDAP server.<br>Minimum length = 1</td></tr><tr><td>ldaploginname</td><td>&lt;String></td><td>Read-write</td><td>Name attribute that the Citrix ADC uses to query the external LDAP server or an Active Directory.</td></tr><tr><td>searchfilter</td><td>&lt;String></td><td>Read-write</td><td>String to be combined with the default LDAP user search string to form the value to use when executing an LDAP search. <br>For example, the following values:<br>vpnallowed=true,<br>ldaploginame=""samaccount""<br>when combined with the user-supplied username ""bob"", yield the following LDAP search string:<br>""(;(vpnallowed=true)(samaccount=bob)"".<br>Minimum length = 1</td></tr><tr><td>groupattrname</td><td>&lt;String></td><td>Read-write</td><td>Attribute name used for group extraction from the LDAP server.</td></tr><tr><td>subattributename</td><td>&lt;String></td><td>Read-write</td><td>Subattribute name used for group extraction from the LDAP server.</td></tr><tr><td>sectype</td><td>&lt;String></td><td>Read-write</td><td>Type of security used for communications between the Citrix ADC and the LDAP server. For the PLAINTEXT setting, no encryption is required.<br>Default value: PLAINTEXT<br>Possible values = PLAINTEXT, TLS, SSL</td></tr><tr><td>svrtype</td><td>&lt;String></td><td>Read-write</td><td>The type of LDAP server.<br>Default value: AAA_LDAP_SERVER_TYPE_DEFAULT<br>Possible values = AD, NDS</td></tr><tr><td>ssonameattribute</td><td>&lt;String></td><td>Read-write</td><td>Attribute used by the Citrix ADC to query an external LDAP server or Active Directory for an alternative username. <br>This alternative username is then used for single sign-on (SSO).</td></tr><tr><td>passwdchange</td><td>&lt;String></td><td>Read-write</td><td>Accept password change requests.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>nestedgroupextraction</td><td>&lt;String></td><td>Read-write</td><td>Queries the external LDAP server to determine whether the specified group belongs to another group.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>maxnestinglevel</td><td>&lt;Double></td><td>Read-write</td><td>Number of levels up to which the system can query nested LDAP groups.<br>Default value: 2<br>Minimum value = 2</td></tr><tr><td>groupnameidentifier</td><td>&lt;String></td><td>Read-write</td><td>LDAP-group attribute that uniquely identifies the group. No two groups on one LDAP server can have the same group name identifier.</td></tr><tr><td>groupsearchattribute</td><td>&lt;String></td><td>Read-write</td><td>LDAP-group attribute that designates the parent group of the specified group. Use this attribute to search for a group's parent group.</td></tr><tr><td>groupsearchsubattribute</td><td>&lt;String></td><td>Read-write</td><td>LDAP-group subattribute that designates the parent group of the specified group. Use this attribute to search for a group's parent group.</td></tr><tr><td>groupsearchfilter</td><td>&lt;String></td><td>Read-write</td><td>Search-expression that can be specified for sending group-search requests to the LDAP server.</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.<br>Maximum length = 64</td></tr><tr><td>groupauthname</td><td>&lt;String></td><td>Read-only</td><td>To associate AAA users with an AAA group, use the command<br><br>"bind AAA group ... -username ...".<br><br>You can bind different policies to each AAA group. Use the command<br><br>"bind AAA group ... -policy ...".</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Indicates that a variable is a built-in (SYSTEM INTERNAL) type.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaldapparams
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaaldapparams":{"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"ldapbase":<String_value>,"ldapbinddn":<String_value>,"ldapbinddnpassword":<String_value>,"ldaploginname":<String_value>,"searchfilter":<String_value>,"groupattrname":<String_value>,"subattributename":<String_value>,"sectype":<String_value>,"svrtype":<String_value>,"ssonameattribute":<String_value>,"passwdchange":<String_value>,"nestedgroupextraction":<String_value>,"maxnestinglevel":<Double_value>,"groupnameidentifier":<String_value>,"groupsearchattribute":<String_value>,"groupsearchsubattribute":<String_value>,"groupsearchfilter":<String_value>,"defaultauthenticationgroup":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaldapparams?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"aaaldapparams":{"serverip":true,"serverport":true,"authtimeout":true,"ldapbase":true,"ldapbinddn":true,"ldapbinddnpassword":true,"ldaploginname":true,"searchfilter":true,"groupattrname":true,"subattributename":true,"sectype":true,"svrtype":true,"ssonameattribute":true,"passwdchange":true,"nestedgroupextraction":true,"maxnestinglevel":true,"groupnameidentifier":true,"groupsearchattribute":true,"groupsearchsubattribute":true,"groupsearchfilter":true,"defaultauthenticationgroup":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/aaaldapparams
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "aaaldapparams": [ {"serverip":<String_value>,"serverport":<Integer_value>,"authtimeout":<Double_value>,"ldapbinddn":<String_value>,"ldaploginname":<String_value>,"ldapbase":<String_value>,"sectype":<String_value>,"svrtype":<String_value>,"ssonameattribute":<String_value>,"searchfilter":<String_value>,"groupattrname":<String_value>,"subattributename":<String_value>,"groupauthname":<String_value>,"passwdchange":<String_value>,"nestedgroupextraction":<String_value>,"maxnestinglevel":<Double_value>,"groupnameidentifier":<String_value>,"groupsearchattribute":<String_value>,"groupsearchsubattribute":<String_value>,"groupsearchfilter":<String_value>,"defaultauthenticationgroup":<String_value>,"builtin":<String[]_value>}]}```



