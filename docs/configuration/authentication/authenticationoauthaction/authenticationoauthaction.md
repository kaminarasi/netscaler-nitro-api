#authenticationoauthaction

Configuration for OAuth authentication action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the OAuth Authentication action. <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the profile is created.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or 'my authentication action').<br>Minimum length = 1</td></tr><tr><td>oauthtype</td><td>&lt;String></td><td>Read-write</td><td>Type of the OAuth implementation. Default value is generic implementation that is applicable for most deployments.<br>Default value: GENERIC<br>Possible values = GENERIC, INTUNE</td></tr><tr><td>authorizationendpoint</td><td>&lt;String></td><td>Read-write</td><td>Authorization endpoint/url to which unauthenticated user will be redirected. Citrix ADC redirects user to this endpoint by adding query parameters including clientid. If this parameter not specified then as default value we take Token Endpoint/URL value. Please note that Authorization Endpoint or Token Endpoint is mandatory for oauthAction.</td></tr><tr><td>tokenendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL to which OAuth token will be posted to verify its authenticity. User obtains this token from Authorization server upon successful authentication. Citrix ADC will validate presented token by posting it to the URL configured.</td></tr><tr><td>idtokendecryptendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL to which obtained idtoken will be posted to get a decrypted user identity. Encrypted idtoken will be obtained by posting OAuth token to token endpoint. In order to decrypt idtoken, Citrix ADC posts request to the URL configured.</td></tr><tr><td>clientid</td><td>&lt;String></td><td>Read-write</td><td>Unique identity of the client/user who is getting authenticated. Authorization server infers client configuration using this ID.<br>Minimum length = 1</td></tr><tr><td>clientsecret</td><td>&lt;String></td><td>Read-write</td><td>Secret string established by user and authorization server.<br>Minimum length = 1</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td></tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute1 from the oauth response.</td></tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute2 from the oauth response.</td></tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute3 from the oauth response.</td></tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute4 from the oauth response.</td></tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute5 from the oauth response.</td></tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute6 from the oauth response.</td></tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute7 from the oauth response.</td></tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute8 from the oauth response.</td></tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute9 from the oauth response.</td></tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute10 from the oauth response.</td></tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute11 from the oauth response.</td></tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute12 from the oauth response.</td></tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute13 from the oauth response.</td></tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute14 from the oauth response.</td></tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute15 from the oauth response.</td></tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute16 from the oauth response.</td></tr><tr><td>tenantid</td><td>&lt;String></td><td>Read-write</td><td>TenantID of the application. This is usually specific to providers such as Microsoft and usually refers to the deployment identifier.</td></tr><tr><td>graphendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL of the Graph API service to learn Enterprise Mobility Services (EMS) endpoints.</td></tr><tr><td>refreshinterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval at which services are monitored for necessary configuration.<br>Default value: 1440</td></tr><tr><td>certendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL of the endpoint that contains JWKs (Json Web Key) for JWT (Json Web Token) verification.</td></tr><tr><td>audience</td><td>&lt;String></td><td>Read-write</td><td>Audience for which token sent by Authorization server is applicable. This is typically entity name or url that represents the recipient.</td></tr><tr><td>usernamefield</td><td>&lt;String></td><td>Read-write</td><td>Attribute in the token from which username should be extracted.<br>Minimum length = 1</td></tr><tr><td>skewtime</td><td>&lt;Double></td><td>Read-write</td><td>This option specifies the allowed clock skew in number of minutes that Citrix ADC allows on an incoming token. For example, if skewTime is 10, then token would be valid from (current time - 10) min to (current time + 10) min, ie 20min in all.<br>Default value: 5</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-write</td><td>Identity of the server whose tokens are to be accepted.</td></tr><tr><td>userinfourl</td><td>&lt;String></td><td>Read-write</td><td>URL to which OAuth access token will be posted to obtain user information.</td></tr><tr><td>certfilepath</td><td>&lt;String></td><td>Read-write</td><td>Path to the file that contains JWKs (Json Web Key) for JWT (Json Web Token) verification.</td></tr><tr><td>granttype</td><td>&lt;String></td><td>Read-write</td><td>Grant type support. value can be code or password.<br>Default value: CODE<br>Possible values = CODE, PASSWORD</td></tr><tr><td>oauthstatus</td><td>&lt;String></td><td>Read-only</td><td>Describes status information of oauth server.<br>Default value: INIT<br>Possible values = INIT, CERTFETCH, AADFORGRAPH, GRAPH, AADFORMDM, MDMINFO, COMPLETE</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthaction":{<b>"name":<String_value>,</b>"oauthtype":<String_value>,"authorizationendpoint":<String_value>,"tokenendpoint":<String_value>,"idtokendecryptendpoint":<String_value>,<b>"clientid":<String_value>,</b><b>"clientsecret":<String_value>,</b>"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"tenantid":<String_value>,"graphendpoint":<String_value>,"refreshinterval":<Double_value>,"certendpoint":<String_value>,"audience":<String_value>,"usernamefield":<String_value>,"skewtime":<Double_value>,"issuer":<String_value>,"userinfourl":<String_value>,"certfilepath":<String_value>,"granttype":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthaction":{<b>"name":<String_value>,</b>"oauthtype":<String_value>,"authorizationendpoint":<String_value>,"tokenendpoint":<String_value>,"idtokendecryptendpoint":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"tenantid":<String_value>,"graphendpoint":<String_value>,"refreshinterval":<Double_value>,"certendpoint":<String_value>,"audience":<String_value>,"usernamefield":<String_value>,"skewtime":<Double_value>,"issuer":<String_value>,"userinfourl":<String_value>,"certfilepath":<String_value>,"granttype":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationoauthaction":{<b>"name":<String_value>,</b>"oauthtype":true,"idtokendecryptendpoint":true,"defaultauthenticationgroup":true,"attribute1":true,"attribute2":true,"attribute3":true,"attribute4":true,"attribute5":true,"attribute6":true,"attribute7":true,"attribute8":true,"attribute9":true,"attribute10":true,"attribute11":true,"attribute12":true,"attribute13":true,"attribute14":true,"attribute15":true,"attribute16":true,"graphendpoint":true,"refreshinterval":true,"certendpoint":true,"audience":true,"usernamefield":true,"skewtime":true,"issuer":true,"userinfourl":true,"certfilepath":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationoauthaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationoauthaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthaction": [ {"name":<String_value>,"authorizationendpoint":<String_value>,"tokenendpoint":<String_value>,"idtokendecryptendpoint":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"tenantid":<String_value>,"graphendpoint":<String_value>,"refreshinterval":<Double_value>,"certendpoint":<String_value>,"oauthtype":<String_value>,"audience":<String_value>,"usernamefield":<String_value>,"skewtime":<Double_value>,"issuer":<String_value>,"oauthstatus":<String_value>,"userinfourl":<String_value>,"certfilepath":<String_value>,"granttype":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthaction": [ {"name":<String_value>,"authorizationendpoint":<String_value>,"tokenendpoint":<String_value>,"idtokendecryptendpoint":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"tenantid":<String_value>,"graphendpoint":<String_value>,"refreshinterval":<Double_value>,"certendpoint":<String_value>,"oauthtype":<String_value>,"audience":<String_value>,"usernamefield":<String_value>,"skewtime":<Double_value>,"issuer":<String_value>,"oauthstatus":<String_value>,"userinfourl":<String_value>,"certfilepath":<String_value>,"granttype":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationoauthaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationoauthaction": [ { "__count": "#no"} ] }```



