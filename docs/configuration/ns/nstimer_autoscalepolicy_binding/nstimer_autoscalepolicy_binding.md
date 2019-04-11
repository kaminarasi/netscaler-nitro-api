#nstimer_autoscalepolicy_binding

Binding object showing the autoscalepolicy that can be bound to nstimer.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>priority</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the priority of the timer policy.</td></tr><tr><td>gotopriorityexpression</td><td>&lt;String></td><td>Read-write</td><td>Expression specifying the priority of the next policy which will get evaluated if the current policy rule evaluates to TRUE.</td></tr><tr><td>policyname</td><td>&lt;String></td><td>Read-write</td><td>The timer policy associated with the timer.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Timer name.<br>Minimum length = 1</td></tr><tr><td>threshold</td><td>&lt;Double></td><td>Read-write</td><td>Denotes the threshold. If the rule of the policy in the binding relation evaluates 'threshold size' number of times in 'sample size' to true, then the corresponding action is taken. Its value needs to be less than or equal to the sample size value.<br>Default value: 3<br>Minimum value = 1<br>Maximum value = 32</td></tr><tr><td>samplesize</td><td>&lt;Double></td><td>Read-write</td><td>Denotes the sample size. Sample size value of 'x' means that previous '(x - 1)' policy's rule evaluation results and the current evaluation result are present with the binding. For example, sample size of 10 means that there is a state of previous 9 policy evaluation results and also the current policy evaluation result.<br>Default value: 3<br>Minimum value = 1<br>Maximum value = 32</td></tr><tr><td>vserver</td><td>&lt;String></td><td>Read-write</td><td>Name of the vserver which provides the context for the rule in timer policy. When not specified it is treated as a Global Default context.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD:]()| [DELETE:](#de)| [GET]()| [GET (ALL)](#ge)| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add:



<b>URL:</b>http://&lt;netscaler-ip-address/nitro/v1/config/nstimer_autoscalepolicy_binding
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nstimer_autoscalepolicy_binding":{<b>"name":<String_value>,</b><b>"policyname":<String_value>,</b><b>"priority":<Double_value>,</b>"gotopriorityexpression":<String_value>,"vserver":<String_value>,"samplesize":<Double_value>,"threshold":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete:



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;?<b>args=<b>policyname:&lt;String_value&gt;</b></b>



<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;?<b>filter=property-name1:property-value1,property-name2:property-value2</b>
Use this query-parameter to get the filtered set of nstimer_autoscalepolicy_binding resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the nstimer_autoscalepolicy_binding resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nstimer_autoscalepolicy_binding": [ {"priority":<Double_value>,"gotopriorityexpression":<String_value>,"policyname":<String_value>,"name":<String_value>,"threshold":<Double_value>,"samplesize":<Double_value>,"vserver":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding
<b>Query-parameters:</b>
<b>bulkbindings</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding?<b>bulkbindings=yes</b>
NITRO allows you to fetch bindings in bulk.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nstimer_autoscalepolicy_binding": [ {"priority":<Double_value>,"gotopriorityexpression":<String_value>,"policyname":<String_value>,"name":<String_value>,"threshold":<Double_value>,"samplesize":<Double_value>,"vserver":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nstimer_autoscalepolicy_binding/name_value&lt;String&gt;?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{"nstimer_autoscalepolicy_binding": [ { "__count": "#no"} ] }```



