#sslaction

Configuration for SSL action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SSL action. Must begin with an ASCII alphanumeric or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at (@), equals (=), and hyphen (-) characters. Cannot be changed after the action is created.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my action" or 'my action').<br>Minimum length = 1</td></tr><tr><td>clientauth</td><td>&lt;String></td><td>Read-write</td><td>Perform client certificate authentication.<br>Possible values = DOCLIENTAUTH, NOCLIENTAUTH</td></tr><tr><td>ssllogprofile</td><td>&lt;String></td><td>Read-write</td><td>The name of the ssllogprofile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>clientcert</td><td>&lt;String></td><td>Read-write</td><td>Insert the entire client certificate into the HTTP header of the request being sent to the web server. The certificate is inserted in ASCII (PEM) format.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client certificate.</td></tr><tr><td>clientcertserialnumber</td><td>&lt;String></td><td>Read-write</td><td>Insert the entire client serial number into the HTTP header of the request being sent to the web server.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certserialheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client serial number.</td></tr><tr><td>clientcertsubject</td><td>&lt;String></td><td>Read-write</td><td>Insert the client certificate subject, also known as the distinguished name (DN), into the HTTP header of the request being sent to the web server.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certsubjectheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client certificate subject.</td></tr><tr><td>clientcerthash</td><td>&lt;String></td><td>Read-write</td><td>Insert the certificate's signature into the HTTP header of the request being sent to the web server. The signature is the value extracted directly from the X.509 certificate signature field. All X.509 certificates contain a signature field.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certhashheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client certificate signature (hash).</td></tr><tr><td>clientcertfingerprint</td><td>&lt;String></td><td>Read-write</td><td>Insert the certificate's fingerprint into the HTTP header of the request being sent to the web server. The fingerprint is derived by computing the specified hash value (SHA256, for example) of the DER-encoding of the client certificate.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certfingerprintheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client certificate fingerprint.</td></tr><tr><td>certfingerprintdigest</td><td>&lt;String></td><td>Read-write</td><td>Digest algorithm used to compute the fingerprint of the client certificate.<br>Possible values = SHA1, SHA224, SHA256, SHA384, SHA512</td></tr><tr><td>clientcertissuer</td><td>&lt;String></td><td>Read-write</td><td>Insert the certificate issuer details into the HTTP header of the request being sent to the web server.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certissuerheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the client certificate issuer details.</td></tr><tr><td>sessionid</td><td>&lt;String></td><td>Read-write</td><td>Insert the SSL session ID into the HTTP header of the request being sent to the web server. Every SSL connection that the client and the Citrix ADC share has a unique ID that identifies the specific connection.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>sessionidheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the Session ID.</td></tr><tr><td>cipher</td><td>&lt;String></td><td>Read-write</td><td>Insert the cipher suite that the client and the Citrix ADC negotiated for the SSL session into the HTTP header of the request being sent to the web server. The appliance inserts the cipher-suite name, SSL protocol, export or non-export string, and cipher strength bit, depending on the type of browser connecting to the SSL virtual server or service (for example, Cipher-Suite: RC4- MD5 SSLv3 Non-Export 128-bit).<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipherheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the name of the cipher suite.</td></tr><tr><td>clientcertnotbefore</td><td>&lt;String></td><td>Read-write</td><td>Insert the date from which the certificate is valid into the HTTP header of the request being sent to the web server. Every certificate is configured with the date and time from which it is valid.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certnotbeforeheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the date and time from which the certificate is valid.</td></tr><tr><td>clientcertnotafter</td><td>&lt;String></td><td>Read-write</td><td>Insert the date of expiry of the certificate into the HTTP header of the request being sent to the web server. Every certificate is configured with the date and time at which the certificate expires.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>certnotafterheader</td><td>&lt;String></td><td>Read-write</td><td>Name of the header into which to insert the certificate's expiry date.</td></tr><tr><td>owasupport</td><td>&lt;String></td><td>Read-write</td><td>If the appliance is in front of an Outlook Web Access (OWA) server, insert a special header field, FRONT-END-HTTPS: ON, into the HTTP requests going to the OWA server. This header communicates to the server that the transaction is HTTPS and not HTTP.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>forward</td><td>&lt;String></td><td>Read-write</td><td>This action takes an argument a vserver name, to this vserver one will be able to forward all the packets.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>cacertgrpname</td><td>&lt;String></td><td>Read-write</td><td>This action will allow to pick CA(s) from the specific CA group, to verify the client certificate.<br>Minimum length = 1<br>Maximum length = 31</td></tr><tr><td>hits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action has been taken.</td></tr><tr><td>undefhits</td><td>&lt;Double></td><td>Read-only</td><td>The number of times the action resulted in UNDEF.</td></tr><tr><td>referencecount</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the action.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-only</td><td>Description of the action.</td></tr><tr><td>builtin</td><td>&lt;String[]></td><td>Read-only</td><td>Flag to determine whether ssl action is built-in or not.<br>Possible values = MODIFIABLE, DELETABLE, IMMUTABLE, PARTITION_ALL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"sslaction":{<b>"name":<String_value>,</b>"clientauth":<String_value>,"ssllogprofile":<String_value>,"clientcert":<String_value>,"certheader":<String_value>,"clientcertserialnumber":<String_value>,"certserialheader":<String_value>,"clientcertsubject":<String_value>,"certsubjectheader":<String_value>,"clientcerthash":<String_value>,"certhashheader":<String_value>,"clientcertfingerprint":<String_value>,"certfingerprintheader":<String_value>,"certfingerprintdigest":<String_value>,"clientcertissuer":<String_value>,"certissuerheader":<String_value>,"sessionid":<String_value>,"sessionidheader":<String_value>,"cipher":<String_value>,"cipherheader":<String_value>,"clientcertnotbefore":<String_value>,"certnotbeforeheader":<String_value>,"clientcertnotafter":<String_value>,"certnotafterheader":<String_value>,"owasupport":<String_value>,"forward":<String_value>,"cacertgrpname":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of sslaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the sslaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslaction": [ {"name":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"certheader":<String_value>,"clientcertserialnumber":<String_value>,"certserialheader":<String_value>,"clientcertsubject":<String_value>,"certsubjectheader":<String_value>,"clientcerthash":<String_value>,"certhashheader":<String_value>,"clientcertfingerprint":<String_value>,"certfingerprintheader":<String_value>,"certfingerprintdigest":<String_value>,"clientcertissuer":<String_value>,"certissuerheader":<String_value>,"sessionid":<String_value>,"sessionidheader":<String_value>,"cipher":<String_value>,"cipherheader":<String_value>,"owasupport":<String_value>,"forward":<String_value>,"cacertgrpname":<String_value>,"clientcertnotbefore":<String_value>,"certnotbeforeheader":<String_value>,"clientcertnotafter":<String_value>,"certnotafterheader":<String_value>,"hits":<Double_value>,"undefhits":<Double_value>,"referencecount":<Double_value>,"description":<String_value>,"ssllogprofile":<String_value>,"builtin":<String[]_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslaction": [ {"name":<String_value>,"clientauth":<String_value>,"clientcert":<String_value>,"certheader":<String_value>,"clientcertserialnumber":<String_value>,"certserialheader":<String_value>,"clientcertsubject":<String_value>,"certsubjectheader":<String_value>,"clientcerthash":<String_value>,"certhashheader":<String_value>,"clientcertfingerprint":<String_value>,"certfingerprintheader":<String_value>,"certfingerprintdigest":<String_value>,"clientcertissuer":<String_value>,"certissuerheader":<String_value>,"sessionid":<String_value>,"sessionidheader":<String_value>,"cipher":<String_value>,"cipherheader":<String_value>,"owasupport":<String_value>,"forward":<String_value>,"cacertgrpname":<String_value>,"clientcertnotbefore":<String_value>,"certnotbeforeheader":<String_value>,"clientcertnotafter":<String_value>,"certnotafterheader":<String_value>,"hits":<Double_value>,"undefhits":<Double_value>,"referencecount":<Double_value>,"description":<String_value>,"ssllogprofile":<String_value>,"builtin":<String[]_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/sslaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "sslaction": [ { "__count": "#no"} ] }```



