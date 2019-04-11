#analyticsprofile

Configuration for Analytics profile resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the analytics profile. Must begin with an ASCII alphabetic or underscore (_) character, and must contain only ASCII alphanumeric, underscore, hash (#), period (.), space, colon (:), at<br>(@), equals (=), and hyphen (-) characters.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my appflow profile" or 'my appflow profile').<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>collectors</td><td>&lt;String></td><td>Read-write</td><td>The collector can be an IP, an appflow collector name, a service or a vserver. If IP is specified, the transport is considered as logstream and default port of 5557 is taken. If collector name is specified, the collector properties are taken from the configured collector. If service is specified, the configured service is assumed as the collector. If vserver is specified, the services bound to it are considered as collectors and the records are load balanced.<br>Minimum length = 1</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>This option indicates what information needs to be collected and exported.<br>Possible values = global, webinsight, tcpinsight, securityinsight, videoinsight, hdxinsight, gatewayinsight, httpstream</td></tr><tr><td>httpclientsidemeasurements</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will insert a javascript into the HTTP response to collect the client side page-timings and will send the same to the configured collectors.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httppagetracking</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will link the embedded objects of a page together.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpurl</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log the URL in appflow records.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httphost</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log the Host header in appflow records.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log the method header in appflow records.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpreferer</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log the referer header in appflow records.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpuseragent</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log User-Agent header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpcookie</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log cookie header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httplocation</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log location header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>urlcategory</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will send the URL category record.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpcontenttype</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log content-length header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpauthentication</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log Authentication header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpvia</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will Via header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpxforwardedforheader</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log X-Forwarded-For header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpsetcookie</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log set-cookie header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpsetcookie2</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log set-cookie2 header.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpdomainname</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log domain name.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>httpurlquery</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log URL Query.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tcpburstreporting</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log TCP burst parameters.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cqareporting</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log TCP CQA parameters.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>integratedcache</td><td>&lt;String></td><td>Read-write</td><td>On enabling this option, the Citrix ADC will log the Integrated Caching appflow records.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>refcnt</td><td>&lt;Double></td><td>Read-only</td><td>The number of references to the profile.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"analyticsprofile":{<b>"name":<String_value>,</b>"collectors":<String_value>,<b>"type":<String_value>,</b>"httpclientsidemeasurements":<String_value>,"httppagetracking":<String_value>,"httpurl":<String_value>,"httphost":<String_value>,"httpmethod":<String_value>,"httpreferer":<String_value>,"httpuseragent":<String_value>,"httpcookie":<String_value>,"httplocation":<String_value>,"urlcategory":<String_value>,"httpcontenttype":<String_value>,"httpauthentication":<String_value>,"httpvia":<String_value>,"httpxforwardedforheader":<String_value>,"httpsetcookie":<String_value>,"httpsetcookie2":<String_value>,"httpdomainname":<String_value>,"httpurlquery":<String_value>,"tcpburstreporting":<String_value>,"cqareporting":<String_value>,"integratedcache":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"analyticsprofile":{<b>"name":<String_value>,</b>"collectors":<String_value>,"httpclientsidemeasurements":<String_value>,"httppagetracking":<String_value>,"httpurl":<String_value>,"httphost":<String_value>,"httpmethod":<String_value>,"httpreferer":<String_value>,"httpuseragent":<String_value>,"httpcookie":<String_value>,"httplocation":<String_value>,"urlcategory":<String_value>,"httpcontenttype":<String_value>,"httpauthentication":<String_value>,"httpvia":<String_value>,"httpxforwardedforheader":<String_value>,"httpsetcookie":<String_value>,"httpsetcookie2":<String_value>,"httpdomainname":<String_value>,"httpurlquery":<String_value>,"tcpburstreporting":<String_value>,"cqareporting":<String_value>,"integratedcache":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"analyticsprofile":{<b>"name":<String_value>,</b>"httpclientsidemeasurements":true,"httppagetracking":true,"httpurl":true,"httphost":true,"httpmethod":true,"httpreferer":true,"httpuseragent":true,"httpcookie":true,"httplocation":true,"urlcategory":true,"httpcontenttype":true,"httpauthentication":true,"httpvia":true,"httpxforwardedforheader":true,"httpsetcookie":true,"httpsetcookie2":true,"httpdomainname":true,"httpurlquery":true,"tcpburstreporting":true,"cqareporting":true,"integratedcache":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of analyticsprofile resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the analyticsprofile resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "analyticsprofile": [ {"name":<String_value>,"collectors":<String_value>,"refcnt":<Double_value>,"type":<String_value>,"httpclientsidemeasurements":<String_value>,"httppagetracking":<String_value>,"httpurl":<String_value>,"httphost":<String_value>,"httpmethod":<String_value>,"httpreferer":<String_value>,"httpuseragent":<String_value>,"httpcookie":<String_value>,"httplocation":<String_value>,"urlcategory":<String_value>,"httpcontenttype":<String_value>,"httpauthentication":<String_value>,"httpvia":<String_value>,"httpxforwardedforheader":<String_value>,"httpsetcookie":<String_value>,"httpsetcookie2":<String_value>,"httpdomainname":<String_value>,"httpurlquery":<String_value>,"tcpburstreporting":<String_value>,"cqareporting":<String_value>,"integratedcache":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "analyticsprofile": [ {"name":<String_value>,"collectors":<String_value>,"refcnt":<Double_value>,"type":<String_value>,"httpclientsidemeasurements":<String_value>,"httppagetracking":<String_value>,"httpurl":<String_value>,"httphost":<String_value>,"httpmethod":<String_value>,"httpreferer":<String_value>,"httpuseragent":<String_value>,"httpcookie":<String_value>,"httplocation":<String_value>,"urlcategory":<String_value>,"httpcontenttype":<String_value>,"httpauthentication":<String_value>,"httpvia":<String_value>,"httpxforwardedforheader":<String_value>,"httpsetcookie":<String_value>,"httpsetcookie2":<String_value>,"httpdomainname":<String_value>,"httpurlquery":<String_value>,"tcpburstreporting":<String_value>,"cqareporting":<String_value>,"integratedcache":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/analyticsprofile?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "analyticsprofile": [ { "__count": "#no"} ] }```



