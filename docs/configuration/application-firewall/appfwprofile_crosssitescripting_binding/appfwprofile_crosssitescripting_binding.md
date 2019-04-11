#appfwprofile_crosssitescripting_binding

Binding object showing the crosssitescripting that can be bound to appfwprofile.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>crosssitescripting</td><td>&lt;String></td><td>Read-write</td><td>The web form field name.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the profile to which to bind an exemption or rule.<br>Minimum length = 1</td></tr><tr><td>isregex_xss</td><td>&lt;String></td><td>Read-write</td><td>Is the web form field name a regular expression?.<br>Possible values = REGEX, NOTREGEX</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Enabled.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>comment</td><td>&lt;String></td><td>Read-write</td><td>Any comments about the purpose of profile, or other useful information about the profile.</td></tr><tr><td>formactionurl_xss</td><td>&lt;String></td><td>Read-write</td><td>The web form action URL.</td></tr><tr><td>as_value_expr_xss</td><td>&lt;String></td><td>Read-write</td><td>The web form value expression.</td></tr><tr><td>as_scan_location_xss</td><td>&lt;String></td><td>Read-write</td><td>Location of cross-site scripting exception - form field, header or cookie.<br>Possible values = FORMFIELD, HEADER, COOKIE</td></tr><tr><td>as_value_type_xss</td><td>&lt;String></td><td>Read-write</td><td>The web form value type.<br>Possible values = Tag, Attribute, Pattern</td></tr><tr><td>isvalueregex_xss</td><td>&lt;String></td><td>Read-write</td><td>Is the web form field value a regular expression?.<br>Possible values = REGEX, NOTREGEX</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/appfwprofile_crosssitescripting_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"appfwprofile_crosssitescripting_binding":{<b>"name":<String_value>,</b>"crosssitescripting":<String_value>,"formactionurl_xss":<String_value>,"isregex_xss":<String_value>,"as_scan_location_xss":<String_value>,"as_value_type_xss":<String_value>,"as_value_expr_xss":<String_value>,"isvalueregex_xss":<String_value>,"comment":<String_value>,"state":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;?<b>args=crosssitescripting:&lt;String_value&gt;,formactionurl_xss:&lt;String_value&gt;,as_scan_location_xss:&lt;String_value&gt;,as_value_type_xss:&lt;String_value&gt;,as_value_expr_xss:&lt;String_value&gt;</b>



<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of appfwprofile_crosssitescripting_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the appfwprofile_crosssitescripting_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_crosssitescripting_binding": [ {"crosssitescripting":<String_value>,"name":<String_value>,"isregex_xss":<String_value>,"state":<String_value>,"comment":<String_value>,"formactionurl_xss":<String_value>,"as_value_expr_xss":<String_value>,"as_scan_location_xss":<String_value>,"as_value_type_xss":<String_value>,"isvalueregex_xss":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "appfwprofile_crosssitescripting_binding": [ {"crosssitescripting":<String_value>,"name":<String_value>,"isregex_xss":<String_value>,"state":<String_value>,"comment":<String_value>,"formactionurl_xss":<String_value>,"as_value_expr_xss":<String_value>,"as_scan_location_xss":<String_value>,"as_value_type_xss":<String_value>,"isvalueregex_xss":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/appfwprofile_crosssitescripting_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"appfwprofile_crosssitescripting_binding": [ { "__count": "#no"} ] }```



