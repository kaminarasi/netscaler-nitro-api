#authenticationoauthaction

Configuration for OAuth authentication action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the OAuth Authentication action. Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the profile is created. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or my authentication action).&lt;br>Minimum length = 1</td><tr><tr><td>authorizationendpoint</td><td>&lt;String></td><td>Read-write</td><td>Authorization endpoint/url to which unauthenticated user will be redirected. Netscaler appliance redirects user to this endpoint by adding query parameters including clientid.</td><tr><tr><td>tokenendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL to which OAuth token will be posted to verify its authenticity. User obtains this token from Authorization server upon successful authentication. Netscaler appliance will validate presented token by posting it to the URL configured.</td><tr><tr><td>idtokendecryptendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL to which obtained idtoken will be posted to get a decrypted user identity. Encrypted idtoken will be obtained by posting OAuth token to token endpoint. In order to decrypt idtoken, Netscaler appliance posts request to the URL configured.</td><tr><tr><td>clientid</td><td>&lt;String></td><td>Read-write</td><td>Unique identity of the client/user who is getting authenticated. Authorization server infers client configuration using this ID.</td><tr><tr><td>clientsecret</td><td>&lt;String></td><td>Read-write</td><td>Secret string established by user and authorization server.</td><tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td><tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute1 from the oauth response.</td><tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute2 from the oauth response.</td><tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute3 from the oauth response.</td><tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute4 from the oauth response.</td><tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute5 from the oauth response.</td><tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute6 from the oauth response.</td><tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute7 from the oauth response.</td><tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute8 from the oauth response.</td><tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute9 from the oauth response.</td><tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute10 from the oauth response.</td><tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute11 from the oauth response.</td><tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute12 from the oauth response.</td><tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute13 from the oauth response.</td><tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute14 from the oauth response.</td><tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute15 from the oauth response.</td><tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Expression that would be evaluated to extract attribute16 from the oauth response.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[ADD](#add) | [DELETE](#delete) | [UPDATE](#update) | [UNSET](#unset) | [GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: 
Response Payload: 



###delete



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;
Query-parameters:
warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: DELETE
Response Payload: 



###update



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: PUT
Request Payload: 
Response Payload: 



###unset



URL: http://&lt;NSIP&gt;/nitro/v1/config/
HTTP Method: POST
Request Payload: 
Response Payload: 



###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/authenticationoauthaction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/authenticationoauthaction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of authenticationoauthaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction?view=summary
Use this query-parameter to get the summary output of authenticationoauthaction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction?pagesize=#no;pageno=#no
Use this query-parameter to get the authenticationoauthaction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: 



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: 



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/authenticationoauthaction?count=yes
HTTP Method: GET
Response Payload: 


