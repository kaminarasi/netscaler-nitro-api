#sslcertbundle

Configuration for Imported Certbundle resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name to assign to the imported certificate bundle. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. The following requirement applies only to the NetScaler CLI: If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my file" or my file).&lt;br>Minimum length = 1&lt;br>Maximum length = 31</td><tr><tr><td>src</td><td>&lt;String></td><td>Read-write</td><td>URL specifying the protocol, host, and path, including file name, to the certificate bundle to be imported or exported. For example, http://www.example.com/cert_bundle_file.&lt;br>NOTE: The import fails if the object to be imported is on an HTTPS server that requires client certificate authentication for access.&lt;br>Minimum length = 1&lt;br>Maximum length = 2047</td><tr><tr><td>inuse</td><td>&lt;String></td><td>Read-only</td><td>.&lt;br>Possible values = YES, NO</td><tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[IMPORT](#import) | [DELETE](#delete) | [APPLY](#apply) | [EXPORT](#export) | [GET (ALL)](#get-(all)) | [COUNT](#count)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###Import



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?action=Import
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###delete



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle
HTTP Method: DELETE
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK


###apply



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?action=apply
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###export



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?action=export
HTTP Method: POST
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Request Payload: 
Response:
HTTP Status Code on Success: 200 OK


###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle
Query-parameters:
attrs
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?attrs=property-name1,property-name2
Use this query parameter to specify the resource details that you want to retrieve.


filter
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?filter=property-name1:property-val1,property-name2:property-val2
Use this query-parameter to get the filtered set of sslcertbundle resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


view
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?view=summary
Note: By default, the retrieved results are displayed in detail view (?view=detail).


pagination
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?pagesize=#no;pageno=#no
Use this query-parameter to get the sslcertbundle resources in chunks.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###count



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslcertbundle?count=yes
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 


