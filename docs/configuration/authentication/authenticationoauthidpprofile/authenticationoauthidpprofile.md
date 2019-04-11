#authenticationoauthidpprofile

Configuration for OAuth Identity Provider (IdP) profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the new OAuth Identity Provider (IdP) single sign-on profile. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after an action is created.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or 'my action').<br>Minimum length = 1</td></tr><tr><td>clientid</td><td>&lt;String></td><td>Read-write</td><td>Unique identity of the relying party requesting for authentication.<br>Minimum length = 1</td></tr><tr><td>clientsecret</td><td>&lt;String></td><td>Read-write</td><td>Unique secret string to authorize relying party at authorization server.<br>Minimum length = 1</td></tr><tr><td>redirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL endpoint on relying party to which the OAuth token is to be sent.<br>Minimum length = 1</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-write</td><td>The name to be used in requests sent from Citrix ADC to IdP to uniquely identify Citrix ADC.<br>Minimum length = 1</td></tr><tr><td>audience</td><td>&lt;String></td><td>Read-write</td><td>Audience for which token is being sent by Citrix ADC IdP. This is typically entity name or url that represents the recipient.</td></tr><tr><td>skewtime</td><td>&lt;Double></td><td>Read-write</td><td>This option specifies the duration for which the token sent by Citrix ADC IdP is valid. For example, if skewTime is 10, then token would be valid from (current time - 10) min to (current time + 10) min, ie 20min in all.<br>Default value: 5</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the group that is added to user sessions that match current IdP policy. It can be used in policies to identify relying party trust.</td></tr><tr><td>relyingpartymetadataurl</td><td>&lt;String></td><td>Read-write</td><td>This is the endpoint at which Citrix ADC IdP can get details about Relying Party (RP) being configured. Metadata response should include endpoints for jwks_uri for RP public key(s).</td></tr><tr><td>refreshinterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval at which Relying Party metadata is refreshed.<br>Default value: 50</td></tr><tr><td>encrypttoken</td><td>&lt;String></td><td>Read-write</td><td>Option to encrypt token when Citrix ADC IDP sends one.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>oauthstatus</td><td>&lt;String></td><td>Read-only</td><td>Describes status information of oauth idp metadata fetch process.<br>Default value: INIT<br>Possible values = INIT, CERTFETCH, AADFORGRAPH, GRAPH, AADFORMDM, MDMINFO, COMPLETE</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthidpprofile":{<b>"name":<String_value>,</b>"clientid":<String_value>,"clientsecret":<String_value>,"redirecturl":<String_value>,"issuer":<String_value>,"audience":<String_value>,"skewtime":<Double_value>,"defaultauthenticationgroup":<String_value>,"relyingpartymetadataurl":<String_value>,"refreshinterval":<Double_value>,"encrypttoken":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthidpprofile":{<b>"name":<String_value>,</b>"clientid":<String_value>,"clientsecret":<String_value>,"redirecturl":<String_value>,"issuer":<String_value>,"audience":<String_value>,"skewtime":<Double_value>,"defaultauthenticationgroup":<String_value>,"relyingpartymetadataurl":<String_value>,"refreshinterval":<Double_value>,"encrypttoken":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthidpprofile":{<b>"name":<String_value>,</b>"issuer":true,"audience":true,"skewtime":true,"defaultauthenticationgroup":true,"relyingpartymetadataurl":true,"refreshinterval":true,"encrypttoken":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationoauthidpprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationoauthidpprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthidpprofile": [ {"name":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"redirecturl":<String_value>,"issuer":<String_value>,"audience":<String_value>,"skewtime":<Double_value>,"defaultauthenticationgroup":<String_value>,"relyingpartymetadataurl":<String_value>,"refreshinterval":<Double_value>,"encrypttoken":<String_value>,"oauthstatus":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthidpprofile": [ {"name":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"redirecturl":<String_value>,"issuer":<String_value>,"audience":<String_value>,"skewtime":<Double_value>,"defaultauthenticationgroup":<String_value>,"relyingpartymetadataurl":<String_value>,"refreshinterval":<Double_value>,"encrypttoken":<String_value>,"oauthstatus":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthidpprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthidpprofile": [ { "__count": "#no"} ] }```



