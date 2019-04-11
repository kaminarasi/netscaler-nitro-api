#streamidentifier

Configuration for identifier resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>The name of stream identifier.</td></tr><tr><td>selectorname</td><td>&lt;String></td><td>Read-write</td><td>Name of the selector to use with the stream identifier.<br>Minimum length = 1</td></tr><tr><td>interval</td><td>&lt;Double></td><td>Read-write</td><td>Number of minutes of data to use when calculating session statistics (number of requests, bandwidth, and response times). The interval is a moving window that keeps the most recently collected data. Older data is discarded at regular intervals.<br>Default value: 1<br>Minimum value = 1</td></tr><tr><td>samplecount</td><td>&lt;Double></td><td>Read-write</td><td>Size of the sample from which to select a request for evaluation. The smaller the sample count, the more accurate is the statistical data. To evaluate all requests, set the sample count to 1. However, such a low setting can result in excessive consumption of memory and processing resources.<br>Default value: 1<br>Minimum value = 1<br>Maximum value = 65535</td></tr><tr><td>sort</td><td>&lt;String></td><td>Read-write</td><td>Sort stored records by the specified statistics column, in descending order. Performed during data collection, the sorting enables real-time data evaluation through Citrix ADC policies (for example, compression and caching policies) that use functions such as IS_TOP(n).<br>Default value: REQUESTS<br>Possible values = REQUESTS, CONNECTIONS, RESPTIME, BANDWIDTH, RESPTIME_BREACHES, NONE</td></tr><tr><td>snmptrap</td><td>&lt;String></td><td>Read-write</td><td>Enable/disable SNMP trap for stream identifier.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>appflowlog</td><td>&lt;String></td><td>Read-write</td><td>Enable/disable Appflow logging for stream identifier.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>trackackonlypackets</td><td>&lt;String></td><td>Read-write</td><td>Track ack only packets as well. This setting is applicable only when packet rate limiting is being used.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>tracktransactions</td><td>&lt;String></td><td>Read-write</td><td>Track transactions exceeding configured threshold. Transaction tracking can be enabled for following metric: ResponseTime.<br>By default transaction tracking is disabled.<br>Default value: NONE<br>Possible values = RESPTIME, NONE</td></tr><tr><td>maxtransactionthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Maximum per transcation value of metric. Metric to be tracked is specified by tracktransactions attribute.<br>Default value: 0</td></tr><tr><td>mintransactionthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Minimum per transcation value of metric. Metric to be tracked is specified by tracktransactions attribute.<br>Default value: 0</td></tr><tr><td>acceptancethreshold</td><td>&lt;String></td><td>Read-write</td><td>Non-Breaching transactions to Total transactions threshold expressed in percent.<br>Maximum of 6 decimal places is supported.<br>Default value: 0.000000<br>Maximum length = 10</td></tr><tr><td>breachthreshold</td><td>&lt;Double></td><td>Read-write</td><td>Breaching transactions threshold calculated over interval.<br>Default value: 0</td></tr><tr><td>rule</td><td>&lt;String[]></td><td>Read-only</td><td>Rule.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [UPDATE](#u)| [UNSET](#)| [DELETE](#d)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"streamidentifier":{<b>"name":<String_value>,</b><b>"selectorname":<String_value>,</b>"interval":<Double_value>,"samplecount":<Double_value>,"sort":<String_value>,"snmptrap":<String_value>,"appflowlog":<String_value>,"trackackonlypackets":<String_value>,"tracktransactions":<String_value>,"maxtransactionthreshold":<Double_value>,"mintransactionthreshold":<Double_value>,"acceptancethreshold":<String_value>,"breachthreshold":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"streamidentifier":{<b>"name":<String_value>,</b>"selectorname":<String_value>,"interval":<Double_value>,"samplecount":<Double_value>,"sort":<String_value>,"snmptrap":<String_value>,"appflowlog":<String_value>,"trackackonlypackets":<String_value>,"tracktransactions":<String_value>,"maxtransactionthreshold":<Double_value>,"mintransactionthreshold":<Double_value>,"acceptancethreshold":<String_value>,"breachthreshold":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"streamidentifier":{<b>"name":<String_value>,</b>"selectorname":true,"interval":true,"samplecount":true,"sort":true,"snmptrap":true,"appflowlog":true,"trackackonlypackets":true,"tracktransactions":true,"maxtransactionthreshold":true,"mintransactionthreshold":true,"acceptancethreshold":true,"breachthreshold":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of streamidentifier resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the streamidentifier resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "streamidentifier": [ {"name":<String_value>,"selectorname":<String_value>,"rule":<String[]_value>,"interval":<Double_value>,"samplecount":<Double_value>,"sort":<String_value>,"snmptrap":<String_value>,"appflowlog":<String_value>,"trackackonlypackets":<String_value>,"tracktransactions":<String_value>,"maxtransactionthreshold":<Double_value>,"mintransactionthreshold":<Double_value>,"acceptancethreshold":<String_value>,"breachthreshold":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "streamidentifier": [ {"name":<String_value>,"selectorname":<String_value>,"rule":<String[]_value>,"interval":<Double_value>,"samplecount":<Double_value>,"sort":<String_value>,"snmptrap":<String_value>,"appflowlog":<String_value>,"trackackonlypackets":<String_value>,"tracktransactions":<String_value>,"maxtransactionthreshold":<Double_value>,"mintransactionthreshold":<Double_value>,"acceptancethreshold":<String_value>,"breachthreshold":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/streamidentifier?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "streamidentifier": [ { "__count": "#no"} ] }```



