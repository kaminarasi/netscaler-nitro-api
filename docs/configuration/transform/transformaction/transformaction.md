#transformaction

Configuration for transform action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the URL transformation action.<br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after the URL Transformation action is added.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, ?my transform action? or ?my transform action).<br>Minimum length = 1</td></tr><tr><td>profilename</td><td>&lt;String></td><td>Read-write</td><td>Name of the URL Transformation profile with which to associate this action.<br>Minimum length = 1</td></tr><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Positive integer specifying the priority of the action within the profile. A lower number specifies a higher priority. Must be unique within the list of actions bound to the profile. Policies are evaluated in the order of their priority numbers, and the first policy that matches is applied.<br>Minimum value = 1<br>Maximum value = 2147483647</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enable or disable this action.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>requrlfrom</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the request URL pattern to be transformed.<br>Minimum length = 1</td></tr><tr><td>requrlinto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on URLs that match the reqUrlFrom pattern.<br>Minimum length = 1</td></tr><tr><td>resurlfrom</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the response URL pattern to be transformed.<br>Minimum length = 1</td></tr><tr><td>resurlinto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on URLs that match the resUrlFrom pattern.<br>Minimum length = 1</td></tr><tr><td>cookiedomainfrom</td><td>&lt;String></td><td>Read-write</td><td>Pattern that matches the domain to be transformed in Set-Cookie headers.<br>Minimum length = 1</td></tr><tr><td>cookiedomaininto</td><td>&lt;String></td><td>Read-write</td><td>PCRE-format regular expression that describes the transformation to be performed on cookie domains that match the cookieDomainFrom pattern. <br>NOTE: The cookie domain to be transformed is extracted from the request.<br>Minimum length = 1</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments to preserve information about this URL Transformation action.</td></tr><tr><td>continuematching</td><td>&lt;String></td><td>Read-only</td><td>Continue transforming using the next rule in the list.<br>Possible values = ON, OFF</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"transformaction":{<b>"name":<String_value>,</b><b>"profilename":<String_value>,</b><b>"priority":<Double_value>,</b>"state":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"transformaction":{<b>"name":<String_value>,</b>"priority":<Double_value>,"requrlfrom":<String_value>,"requrlinto":<String_value>,"resurlfrom":<String_value>,"resurlinto":<String_value>,"cookiedomainfrom":<String_value>,"cookiedomaininto":<String_value>,"state":<String_value>,"comment":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"transformaction":{<b>"name":<String_value>,</b>"requrlfrom":true,"requrlinto":true,"resurlfrom":true,"resurlinto":true,"cookiedomainfrom":true,"cookiedomaininto":true,"state":true,"comment":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of transformaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the transformaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "transformaction": [ {"name":<String_value>,"profilename":<String_value>,"priority":<Double_value>,"requrlfrom":<String_value>,"requrlinto":<String_value>,"resurlfrom":<String_value>,"resurlinto":<String_value>,"cookiedomainfrom":<String_value>,"cookiedomaininto":<String_value>,"continuematching":<String_value>,"state":<String_value>,"comment":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "transformaction": [ {"name":<String_value>,"profilename":<String_value>,"priority":<Double_value>,"requrlfrom":<String_value>,"requrlinto":<String_value>,"resurlfrom":<String_value>,"resurlinto":<String_value>,"cookiedomainfrom":<String_value>,"cookiedomaininto":<String_value>,"continuematching":<String_value>,"state":<String_value>,"comment":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/transformaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "transformaction": [ { "__count": "#no"} ] }```



