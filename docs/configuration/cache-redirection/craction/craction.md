#craction

Configuration for cache redirection action resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the action for which to display detailed information.&lt;br>Minimum length = 1</td><tr><tr><td>crtype</td><td>&lt;String></td><td>Read-only</td><td>Type to decide where to redirect the requests if the cache redirection policy is hit. The valid options are as follows: *CACHE - Directs all the requests to the cache if cache redirection policy is hit. *ORIGIN - Directs all requests to the origin server if the cache redirection policy is hit.&lt;br>Possible values = origin, cache</td><tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether CRACTION is default or not.&lt;br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td><tr><tr><td>isdefault</td><td>&lt;Boolean></td><td>Read-only</td><td>A value of true is returned if it is a default cr action.</td><tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td><tr><tr><td>referencecount</td><td>&lt;String></td><td>Read-only</td><td>The number of references to the action.</td><tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td><tr><tr><td>comment</td><td>&lt;String></td><td>Read-only</td><td>Comment. Any type of information about this responder action.</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;NSIP&gt;/nitro/v1/config/craction
Query-parameters:
filter
http://&lt;NSIP&gt;/nitro/v1/config/craction?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of craction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;NS_IP&gt;/nitro/v1/config/craction?view=summary
Use this query-parameter to get the summary output of craction resources configured on NetScaler.


pagesize=#no;pageno=#no
http://&lt;NS_IP&gt;/nitro/v1/config/craction?pagesize=#no;pageno=#no
Use this query-parameter to get the craction resources in chunks.


warning
http://&lt;NS_IP&gt;/nitro/v1/config/craction?warning=yes
Use this query parameter to get warnings in nitro response. If this field is set to YES, warning message will be sent in 'message' field and 'WARNING' value is set in severity field of the response in case there is a



HTTP Method: GET
Response Payload: 



###get



URL: http://&lt;NS_IP&gt;/nitro/v1/config/craction/name_value&lt;String&gt;
HTTP Method: GET
Response Payload: 



###count



URL: http://&lt;NS_IP&gt;/nitro/v1/config/craction?count=yes
HTTP Method: GET
Response Payload: 


