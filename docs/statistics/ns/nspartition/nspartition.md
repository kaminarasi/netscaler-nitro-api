#nspartition

Statistics for admin partition resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>partitionname</td><td>&lt;String></td><td>Read-write</td><td>Name of the partition.&lt;br>Minimum length = 1</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>minbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Minimum Bandwidth required by the partition.</td><tr><tr><td>maxbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Banwidth allowed for the partition.</td><tr><tr><td>maxconnection</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Connection allowed for the partition.</td><tr><tr><td>maxmemory</td><td>&lt;Double></td><td>Read-only</td><td>Maximum memory limit for the partition.</td><tr><tr><td>currentbandwidth</td><td>&lt;Double></td><td>Read-only</td><td>Current Bandwidth usage for the partition.</td><tr><tr><td>currentconnections</td><td>&lt;Double></td><td>Read-only</td><td>Current Connections on this partition.</td><tr><tr><td>memoryusagepcnt</td><td>&lt;Double></td><td>Read-only</td><td>Memory usage(%) on this partition.</td><tr><tr><td>totaldrops</td><td>&lt;Double></td><td>Read-only</td><td>Total packet drops for the partition.</td><tr><tr><td>dropsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaldrops</td><tr><tr><td>totaltokendrops</td><td>&lt;Double></td><td>Read-only</td><td>Total drops(KB) for the partition.</td><tr><tr><td>tokendropsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaltokendrops</td><tr><tr><td>totalconnectiondrops</td><td>&lt;Double></td><td>Read-only</td><td>Total connection drops for the partition.</td><tr><tr><td>connectiondropsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalconnectiondrops</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://NS_IP/nitro/v1/stat/nspartition
Query-parameters:
args
http://&lt;NSIP&gt;/nitro/v1/stat/nspartition?args=
Use this query-parameter to get nspartition resources based on additional properties.



HTTP Method: GET
Response Payload: 



###get



URL: http://NS_IP/nitro/v1/stat/nspartition/partitionname_value&lt;String&gt;
HTTP Method: GET
Response Payload: 


