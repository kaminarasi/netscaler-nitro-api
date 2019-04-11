#cacheobject

Configuration for cache object resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of the particular object whose details is required. Parameter "host" must be specified along with the URL.<br>Minimum length = 1</td></tr><tr><td>locator</td><td>&lt;Double></td><td>Read-write</td><td>ID of the cached object.</td></tr><tr><td>httpstatus</td><td>&lt;Double></td><td>Read-write</td><td>HTTP status of the object.</td></tr><tr><td>host</td><td>&lt;String></td><td>Read-write</td><td>Host name of the object. Parameter "url" must be specified.<br>Minimum length = 1</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Host port of the object. You must also set the Host parameter.<br>Default value: 80<br>Minimum value = 1</td></tr><tr><td>groupname</td><td>&lt;String></td><td>Read-write</td><td>Name of the content group to which the object belongs. It will display only the objects belonging to the specified content group. You must also set the Host parameter.</td></tr><tr><td>httpmethod</td><td>&lt;String></td><td>Read-write</td><td>HTTP request method that caused the object to be stored.<br>Default value: GET<br>Possible values = GET, POST</td></tr><tr><td>group</td><td>&lt;String></td><td>Read-write</td><td>Name of the content group whose objects should be listed.</td></tr><tr><td>ignoremarkerobjects</td><td>&lt;String></td><td>Read-write</td><td>Ignore marker objects. Marker objects are created when a response exceeds the maximum or minimum response size for the content group or has not yet received the minimum number of hits for the content group.<br>Possible values = ON, OFF</td></tr><tr><td>includenotreadyobjects</td><td>&lt;String></td><td>Read-write</td><td>Include responses that have not yet reached a minimum number of hits before being cached.<br>Possible values = ON, OFF</td></tr><tr><td>nodeid</td><td>&lt;Double></td><td>Read-write</td><td>Unique number that identifies the cluster node.<br>Minimum value = 0<br>Maximum value = 31</td></tr><tr><td>tosecondary</td><td>&lt;String></td><td>Read-write</td><td>Object will be saved onto Secondary.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>cacheressize</td><td>&lt;Double></td><td>Read-only</td><td>Cache response size of the object.</td></tr><tr><td>cachereshdrsize</td><td>&lt;Double></td><td>Read-only</td><td>Cache response header size of the object.</td></tr><tr><td>cacheetag</td><td>&lt;String></td><td>Read-only</td><td>Cache ETag of the object.</td></tr><tr><td>httpstatusoutput</td><td>&lt;Double></td><td>Read-only</td><td>HTTP status of the object.</td></tr><tr><td>cachereslastmod</td><td>&lt;String></td><td>Read-only</td><td>Value of "Last-modified" header.</td></tr><tr><td>cachecontrol</td><td>&lt;String></td><td>Read-only</td><td>Cache-Control header of the object.</td></tr><tr><td>cacheresdate</td><td>&lt;String></td><td>Read-only</td><td>Value of "Date" header.</td></tr><tr><td>contentgroup</td><td>&lt;String></td><td>Read-only</td><td>Name of the contentgroup in which it is stored.</td></tr><tr><td>destipv46</td><td>&lt;String></td><td>Read-only</td><td>Destination IP.</td></tr><tr><td>destport</td><td>&lt;Integer></td><td>Read-only</td><td>Destination Port.<br>Range 1 - 65535<br>* in CLI is represented as 65535 in NITRO API</td></tr><tr><td>cachecellcomplex</td><td>&lt;String></td><td>Read-only</td><td>The state of the parameterized caching on this cell.<br>Possible values = YES, NO</td></tr><tr><td>hitparams</td><td>&lt;String[]></td><td>Read-only</td><td>Parameterized hit evaluation of an object.</td></tr><tr><td>hitvalues</td><td>&lt;String[]></td><td>Read-only</td><td>Values of hitparams for this object.</td></tr><tr><td>cachecellreqtime</td><td>&lt;Double></td><td>Read-only</td><td>Required time of the cache cell object.</td></tr><tr><td>cachecellrestime</td><td>&lt;Double></td><td>Read-only</td><td>Response time to the cache cell object.</td></tr><tr><td>cachecurage</td><td>&lt;Double></td><td>Read-only</td><td>Current age of the cache object.</td></tr><tr><td>cachecellexpires</td><td>&lt;Double></td><td>Read-only</td><td>Expiry time of the cache cell object in seconds.</td></tr><tr><td>cachecellexpiresmillisec</td><td>&lt;Double></td><td>Read-only</td><td>Expiry time of the cache cell object in milliseconds.</td></tr><tr><td>flushed</td><td>&lt;String></td><td>Read-only</td><td>Specifies whether the object is flushed.<br>Possible values = YES, NO</td></tr><tr><td>prefetch</td><td>&lt;String></td><td>Read-only</td><td>Specifies whether Integrated Cache should attempt to refresh an object immediately before it goes stale.<br>Possible values = YES, NO</td></tr><tr><td>prefetchperiod</td><td>&lt;Double></td><td>Read-only</td><td>The duration in seconds of the period during which prefetch should be attempted, immediately before the object's calculated expiry time.</td></tr><tr><td>prefetchperiodmillisec</td><td>&lt;Double></td><td>Read-only</td><td>The duration in milliseconds of the period during which prefetch should be attempted, immediately before the object's calculated expiry time.</td></tr><tr><td>cachecellcurreaders</td><td>&lt;Double></td><td>Read-only</td><td>Current readers of the cache cell object.</td></tr><tr><td>cachecellcurmisses</td><td>&lt;Double></td><td>Read-only</td><td>Current misses of the cache cell object.</td></tr><tr><td>cachecellhits</td><td>&lt;Double></td><td>Read-only</td><td>Cache cell hits.</td></tr><tr><td>cachecellmisses</td><td>&lt;Double></td><td>Read-only</td><td>Cache cell misses.</td></tr><tr><td>cachecelldhits</td><td>&lt;Double></td><td>Read-only</td><td>Cache cell disk hits.</td></tr><tr><td>cachecellcompressionformat</td><td>&lt;String></td><td>Read-only</td><td>Compression format of this object. Identity means not compressed.</td></tr><tr><td>cachecellappfwmetadataexists</td><td>&lt;String></td><td>Read-only</td><td>AppFirewall cache object.<br>Possible values = YES, NO</td></tr><tr><td>cachecellhttp11</td><td>&lt;String></td><td>Read-only</td><td>The state of the response to be HTTP/1.1.<br>Possible values = YES, NO</td></tr><tr><td>cachecellweaketag</td><td>&lt;String></td><td>Read-only</td><td>The state of the weak HTTP Entity Tag in the cell.<br>Possible values = YES, NO</td></tr><tr><td>cachecellresbadsize</td><td>&lt;String></td><td>Read-only</td><td>The marked state of the cell.<br>Possible values = YES, NO</td></tr><tr><td>markerreason</td><td>&lt;String></td><td>Read-only</td><td>Reason for marking the cell.<br>Possible values = Waiting for min hit, Response header is too big, Content-length header said response size is not in group size limit, Content-length response received more data, Content-length response received less data, Content-length response data is not in group size limit, Chunk response received more data, Chunk response data is not in group size limit, Bad chunk format, Fin terminated response data is not in group size limit</td></tr><tr><td>cachecellpolleverytime</td><td>&lt;String></td><td>Read-only</td><td>The state to poll every time on object.<br>Possible values = YES, NO</td></tr><tr><td>cachecelletaginserted</td><td>&lt;String></td><td>Read-only</td><td>The state of the ETag to be inserted by IC for this object.<br>Possible values = YES, NO</td></tr><tr><td>cachecellreadywithlastbyte</td><td>&lt;String></td><td>Read-only</td><td>The state of the complete arrived response.<br>Possible values = YES, NO</td></tr><tr><td>cacheinmemory</td><td>&lt;String></td><td>Read-only</td><td>The cache data is available in memory.<br>Possible values = YES, NO</td></tr><tr><td>cacheindisk</td><td>&lt;String></td><td>Read-only</td><td>The cache data is available in disk.<br>Possible values = YES, NO</td></tr><tr><td>cacheinsecondary</td><td>&lt;String></td><td>Read-only</td><td>The cache data is available in secondary in HA deployment.<br>Possible values = YES, NO</td></tr><tr><td>cachedirname</td><td>&lt;String></td><td>Read-only</td><td>The directory name used if saved.</td></tr><tr><td>cachefilename</td><td>&lt;String></td><td>Read-only</td><td>The filename used if saved.</td></tr><tr><td>cachecelldestipverified</td><td>&lt;String></td><td>Read-only</td><td>The state of DNS verification.<br>Possible values = YES, NO</td></tr><tr><td>cachecellfwpxyobj</td><td>&lt;String></td><td>Read-only</td><td>The state of the object to be stored on a request to a forward proxy.<br>Possible values = YES, NO</td></tr><tr><td>cachecellbasefile</td><td>&lt;String></td><td>Read-only</td><td>The state of delta being used as a basefile.<br>Possible values = YES, NO</td></tr><tr><td>cachecellminhitflag</td><td>&lt;String></td><td>Read-only</td><td>The state of the minhit feature on this cell.<br>Possible values = YES, NO</td></tr><tr><td>cachecellminhit</td><td>&lt;Integer></td><td>Read-only</td><td>Min hit value for the object.</td></tr><tr><td>policy</td><td>&lt;Integer></td><td>Read-only</td><td>Policy info for the object.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-only</td><td>Policy which created the object.</td></tr><tr><td>selectorname</td><td>&lt;String[]></td><td>Read-only</td><td>The hit selector for the object.</td></tr><tr><td>rule</td><td>&lt;String[]></td><td>Read-only</td><td>Selectors for this object.</td></tr><tr><td>selectorvalue</td><td>&lt;String[]></td><td>Read-only</td><td>The HTTP request method that caused the object to be stored.</td></tr><tr><td>cacheurls</td><td>&lt;String></td><td>Read-only</td><td>List of cache object URLs.</td></tr><tr><td>warnbucketskip</td><td>&lt;Double></td><td>Read-only</td><td>Bucket skipped warning.</td></tr><tr><td>totalobjs</td><td>&lt;Double></td><td>Read-only</td><td>Total objects.</td></tr><tr><td>httpcalloutcell</td><td>&lt;String></td><td>Read-only</td><td>Is it a http callout cell ?.<br>Possible values = YES, NO</td></tr><tr><td>httpcalloutname</td><td>&lt;String></td><td>Read-only</td><td>Name of the http callout.</td></tr><tr><td>returntype</td><td>&lt;String></td><td>Read-only</td><td>Return type of the http callout.<br>Possible values = BOOL, NUM, TEXT</td></tr><tr><td>httpcalloutresult</td><td>&lt;String></td><td>Read-only</td><td>First few bytes of http callout response.</td></tr><tr><td>locatorshow</td><td>&lt;Double></td><td>Read-only</td><td>ID of the cached object.</td></tr><tr><td>ceflags</td><td>&lt;Double></td><td>Read-only</td><td>Indicates state and type of cached cell.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[EXPIRE](#e)| [FLUSH](#)| [SAVE]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###expire



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>action=expire</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cacheobject":{"locator":<Double_value>,"url":<String_value>,"host":<String_value>,"port":<Integer_value>,"groupname":<String_value>,"httpmethod":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###flush



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>action=flush</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cacheobject":{"locator":<Double_value>,"url":<String_value>,"host":<String_value>,"port":<Integer_value>,"groupname":<String_value>,"httpmethod":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###save



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>action=save</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"cacheobject":{"locator":<Double_value>,"tosecondary":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>args=url:&lt;String_value&gt;,locator:&lt;Double_value&gt;,httpstatus:&lt;Double_value&gt;,host:&lt;String_value&gt;,port:&lt;Integer_value&gt;,groupname:&lt;String_value&gt;,httpmethod:&lt;String_value&gt;,group:&lt;String_value&gt;,ignoremarkerobjects:&lt;String_value&gt;,includenotreadyobjects:&lt;String_value&gt;,nodeid:&lt;Double_value&gt;</b>
Use this query-parameter to get cacheobject resources based on additional properties.


<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of cacheobject resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the cacheobject resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "cacheobject": [ {url:<String_value>,locator:<Double_value>,httpstatus:<Double_value>,host:<String_value>,port:<Integer_value>,groupname:<String_value>,httpmethod:<String_value>,group:<String_value>,ignoremarkerobjects:<String_value>,includenotreadyobjects:<String_value>,nodeid:<Double_value>"cacheressize":<Double_value>,"cachereshdrsize":<Double_value>,"cacheetag":<String_value>,"httpstatusoutput":<Double_value>,"cachereslastmod":<String_value>,"cachecontrol":<String_value>,"cacheresdate":<String_value>,"contentgroup":<String_value>,"destip":<Double_value>,"destipv46":<String_value>,"destport":<Integer_value>,"cachecellcomplex":<String_value>,"hitparams":<String[]_value>,"hitvalues":<String[]_value>,"cachecellreqtime":<Double_value>,"cachecellrestime":<Double_value>,"cachecurage":<Double_value>,"cachecellexpires":<Double_value>,"cachecellexpiresmillisec":<Double_value>,"flushed":<String_value>,"prefetch":<String_value>,"prefetchperiod":<Double_value>,"prefetchperiodmillisec":<Double_value>,"cachecellcurreaders":<Double_value>,"cachecellcurmisses":<Double_value>,"cachecellhits":<Double_value>,"cachecellmisses":<Double_value>,"cachecelldhits":<Double_value>,"cachecellgzipcompressed":<String_value>,"cachecelldeflatecompressed":<String_value>,"cachecellcompressionformat":<String_value>,"cachecellappfwmetadataexists":<String_value>,"cachecellhttp11":<String_value>,"cachecellweaketag":<String_value>,"cachecellresbadsize":<String_value>,"markerreason":<String_value>,"cachecellpolleverytime":<String_value>,"cachecelletaginserted":<String_value>,"cachecellreadywithlastbyte":<String_value>,"cacheinmemory":<String_value>,"cacheindisk":<String_value>,"cacheinsecondary":<String_value>,"cachedirname":<String_value>,"cachefilename":<String_value>,"cachecelldestipverified":<String_value>,"cachecellfwpxyobj":<String_value>,"cachecellbasefile":<String_value>,"cachecellminhitflag":<String_value>,"cachecellminhit":<Integer_value>,"policy":<Integer_value>,"policyname":<String_value>,"selectorname":<String[]_value>,"rule":<String[]_value>,"selectorvalue":<String[]_value>,"cacheurls":<String_value>,"warnbucketskip":<Double_value>,"totalobjs":<Double_value>,"httpcalloutcell":<String_value>,"httpcalloutname":<String_value>,"returntype":<String_value>,"httpcalloutresult":<String_value>,"locatorshow":<Double_value>,"ceflags":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/cacheobject?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "cacheobject": [ { "__count": "#no"} ] }```



