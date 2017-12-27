#mapdomain

Statistics for MAP-T Map Domain resource.


##Properties 
<span>(click to see [Operations](#operations))</span>


<table><thead><tr><th>Name</th><th> Data Type</th><th> Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>An integer specifying the VLAN identification number (VID). Possible values: 1 through 4094.&lt;br>Minimum length = 1&lt;br>Maximum length = 127</td><tr><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.&lt;br>Possible values = basic, full</td><tr><tr><td>maptotv6rxpktstcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 TCP Recieved packets.</td><tr><tr><td>mapv6rxpktstcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxpktstcp</td><tr><tr><td>maptotv6txpktstcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 TCP Transmitted packets.</td><tr><tr><td>mapv6txpktstcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txpktstcp</td><tr><tr><td>maptotv6rxbytestcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 TCP Recieved Bytes.</td><tr><tr><td>mapv6rxbytestcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxbytestcp</td><tr><tr><td>maptotv6txbytestcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 TCP Transmitted Bytes.</td><tr><tr><td>mapv6txbytestcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txbytestcp</td><tr><tr><td>maptotv4rxpktstcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 TCP Recieved packets.</td><tr><tr><td>mapv4rxpktstcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxpktstcp</td><tr><tr><td>maptotv4txpktstcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 TCP Transmitted packets.</td><tr><tr><td>mapv4txpktstcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txpktstcp</td><tr><tr><td>maptotv4rxbytestcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 TCP Recieved Bytes.</td><tr><tr><td>mapv4rxbytestcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxbytestcp</td><tr><tr><td>maptotv4txbytestcp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 TCP Transmitted Bytes.</td><tr><tr><td>mapv4txbytestcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txbytestcp</td><tr><tr><td>maptotv6rxpktsudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 UDP Recieved packets.</td><tr><tr><td>mapv6rxpktsudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxpktsudp</td><tr><tr><td>maptotv6txpktsudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 UDP Transmitted packets.</td><tr><tr><td>mapv6txpktsudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txpktsudp</td><tr><tr><td>maptotv6rxbytesudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 UDP Recieved Bytes.</td><tr><tr><td>mapv6rxbytesudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxbytesudp</td><tr><tr><td>maptotv6txbytesudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 UDP Transmitted Bytes.</td><tr><tr><td>mapv6txbytesudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txbytesudp</td><tr><tr><td>maptotv4rxpktsudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 UDP Recieved packets.</td><tr><tr><td>mapv4rxpktsudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxpktsudp</td><tr><tr><td>maptotv4txpktsudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 UDP Transmitted packets.</td><tr><tr><td>mapv4txpktsudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txpktsudp</td><tr><tr><td>maptotv4rxbytesudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 UDP Recieved Bytes.</td><tr><tr><td>mapv4rxbytesudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxbytesudp</td><tr><tr><td>maptotv4txbytesudp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 UDP Transmitted Bytes.</td><tr><tr><td>mapv4txbytesudprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txbytesudp</td><tr><tr><td>maptotv6rxpktsicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 ICMP Recieved packets.</td><tr><tr><td>mapv6rxpktsicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxpktsicmp</td><tr><tr><td>maptotv6txpktsicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 ICMP Transmitted packets.</td><tr><tr><td>mapv6txpktsicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txpktsicmp</td><tr><tr><td>maptotv6rxbytesicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 ICMP Recieved Bytes.</td><tr><tr><td>mapv6rxbytesicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxbytesicmp</td><tr><tr><td>maptotv6txbytesicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv6 ICMP Transmitted Bytes.</td><tr><tr><td>mapv6txbytesicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txbytesicmp</td><tr><tr><td>maptotv4rxpktsicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 ICMP Recieved packets.</td><tr><tr><td>mapv4rxpktsicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxpktsicmp</td><tr><tr><td>maptotv4txpktsicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 ICMP Transmitted packets.</td><tr><tr><td>mapv4txpktsicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txpktsicmp</td><tr><tr><td>maptotv4rxbytesicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 ICMP Recieved Bytes.</td><tr><tr><td>mapv4rxbytesicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxbytesicmp</td><tr><tr><td>maptotv4txbytesicmp</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T IPv4 ICMP Transmitted Bytes.</td><tr><tr><td>mapv4txbytesicmprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txbytesicmp</td><tr><tr><td>maptotv6rxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T V6 Recieved packets.</td><tr><tr><td>mapv6rxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6rxpkts</td><tr><tr><td>maptotv6txpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T V6 Transmitted packets.</td><tr><tr><td>mapv6txpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv6txpkts</td><tr><tr><td>maptotv4rxpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T V4 Recieved packets.</td><tr><tr><td>mapv4rxpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4rxpkts</td><tr><tr><td>maptotv4txpkts</td><td>&lt;Double></td><td>Read-only</td><td>Total number of MAP-T V4 Transmitted packets.</td><tr><tr><td>mapv4txpktsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for maptotv4txpkts</td><tr></tbody></table>
##Operations 
<span>(click to see [Properties](#properties))</span>


[GET (ALL)](#get-(all)) | [GET](#get)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b> NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b> NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b> In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/mapdomain
Query-parameters:
args
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/mapdomain?args=name:&lt;String_value&gt;,detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;
Use this query-parameter to get mapdomain resources based on additional properties.



HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 



###get



URL: http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/mapdomain/name_value&gt;&lt;String&gt;
HTTP Method: GET
Request Headers:

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

Response:
HTTP Status Code on Success: 200 OK

Content-Type:application/json

Response Payload: 


