#authenticationpushservice

Configuration for Service details for sending push notifications resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the push service. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at sign (@), equal sign (=), and hyphen (-) characters. Cannot be changed after the profile is created.<br>CLI Users: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my push service" or 'my push service'). .<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>Namespace</td><td>&lt;String></td><td>Read-write</td><td>Namespace of the push notification service. This can either be just the namespace without dot (.) or complete namespace uri with http protocol or uri elements. For citrix type push service, this is fully qualified domain name of the service in the cloud. .<br>Minimum length = 1<br>Maximum length = 63</td></tr><tr><td>pushservicetype</td><td>&lt;String></td><td>Read-write</td><td>Type of the Push server implementation. Default value is Azure.<br>Default value: AZURE<br>Possible values = AZURE, CITRIX</td></tr><tr><td>hubname</td><td>&lt;String></td><td>Read-write</td><td>Name of the hub within a namespace. This is used to classify different identities within a namespace.<br>Minimum length = 1</td></tr><tr><td>servicekey</td><td>&lt;String></td><td>Read-write</td><td>Key to be used to compute signature necessary for accessing notification service.<br>Minimum length = 1</td></tr><tr><td>servicekeyname</td><td>&lt;String></td><td>Read-write</td><td>Friendly name of the Key to be used to compute signature necessary for accessing notification service.<br>Minimum length = 1</td></tr><tr><td>certendpoint</td><td>&lt;String></td><td>Read-write</td><td>URL of the endpoint that contains JWKs (Json Web Key) for JWT (Json Web Token) verification. This is used at cloud instance that offers push service.</td></tr><tr><td>clientid</td><td>&lt;String></td><td>Read-write</td><td>Unique identity of the relying party for communicating with Citrix Push server in cloud.<br>Minimum length = 1</td></tr><tr><td>clientsecret</td><td>&lt;String></td><td>Read-write</td><td>Unique secret of the relying party for communicating with Citrix Push server in cloud.<br>Minimum length = 1</td></tr><tr><td>customerid</td><td>&lt;String></td><td>Read-write</td><td>Customer id/name of the account in cloud that is used to create clientid/secret pair.<br>Minimum length = 1</td></tr><tr><td>refreshinterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval at which certificates or idtoken is refreshed.<br>Default value: 50</td></tr><tr><td>trustservice</td><td>&lt;String></td><td>Read-write</td><td>URL of the service that generates tokens for cloud access.<br>Minimum length = 1</td></tr><tr><td>pushservicestatus</td><td>&lt;String></td><td>Read-only</td><td>Describes status of push service.<br>Default value: INIT<br>Possible values = INIT, CERTFETCH, CCTOKEN, COMPLETE</td></tr><tr><td>pushcloudserverstatus</td><td>&lt;String></td><td>Read-only</td><td>Describes status of the cloud service that does push.<br>Possible values = UP, DOWN</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationpushservice":{<b>"name":<String_value>,</b><b>"Namespace":<String_value>,</b>"pushservicetype":<String_value>,"hubname":<String_value>,"servicekey":<String_value>,"servicekeyname":<String_value>,"certendpoint":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"customerid":<String_value>,"refreshinterval":<Double_value>,"trustservice":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationpushservice":{<b>"name":<String_value>,</b>"Namespace":<String_value>,"pushservicetype":<String_value>,"hubname":<String_value>,"servicekey":<String_value>,"servicekeyname":<String_value>,"certendpoint":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"customerid":<String_value>,"refreshinterval":<Double_value>,"trustservice":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationpushservice":{<b>"name":<String_value>,</b>"refreshinterval":true,"trustservice":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationpushservice resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationpushservice resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationpushservice": [ {"name":<String_value>,"Namespace":<String_value>,"hubname":<String_value>,"servicekey":<String_value>,"servicekeyname":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"pushservicetype":<String_value>,"customerid":<String_value>,"certendpoint":<String_value>,"refreshinterval":<Double_value>,"pushservicestatus":<String_value>,"trustservice":<String_value>,"pushcloudserverstatus":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationpushservice": [ {"name":<String_value>,"Namespace":<String_value>,"hubname":<String_value>,"servicekey":<String_value>,"servicekeyname":<String_value>,"clientid":<String_value>,"clientsecret":<String_value>,"pushservicetype":<String_value>,"customerid":<String_value>,"certendpoint":<String_value>,"refreshinterval":<Double_value>,"pushservicestatus":<String_value>,"trustservice":<String_value>,"pushcloudserverstatus":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationpushservice?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationpushservice": [ { "__count": "#no"} ] }```



