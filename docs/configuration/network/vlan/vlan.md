#vlan

Configuration for "VLAN" resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;Double></td><td>Read-write</td><td>A positive integer that uniquely identifies a VLAN.<br>Minimum value = 1<br>Maximum value = 4094</td></tr><tr><td>aliasname</td><td>&lt;String></td><td>Read-write</td><td>A name for the VLAN. Must begin with a letter, a number, or the underscore symbol, and can consist of from 1 to 31 letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at sign (@), equals (=), colon (:), and underscore (_) characters. You should choose a name that helps identify the VLAN. However, you cannot perform any VLAN operation by specifying this name instead of the VLAN ID.<br>Maximum length = 31</td></tr><tr><td>dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable dynamic routing on this VLAN.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>ipv6dynamicrouting</td><td>&lt;String></td><td>Read-write</td><td>Enable all IPv6 dynamic routing protocols on this VLAN. Note: For the ENABLED setting to work, you must configure IPv6 dynamic routing protocols from the VTYSH command line.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>mtu</td><td>&lt;Double></td><td>Read-write</td><td>Specifies the maximum transmission unit (MTU), in bytes. The MTU is the largest packet size, excluding 14 bytes of ethernet header and 4 bytes of crc, that can be transmitted and received over this VLAN.<br>Default value: 0<br>Minimum value = 500<br>Maximum value = 9216</td></tr><tr><td>sharing</td><td>&lt;String></td><td>Read-write</td><td>If sharing is enabled, then this vlan can be shared across multiple partitions by binding it to all those partitions. If sharing is disabled, then this vlan can be bound to only one of the partitions.<br>Default value: DISABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>linklocalipv6addr</td><td>&lt;String></td><td>Read-only</td><td>The link-local IP address assigned to the VLAN.</td></tr><tr><td>rnat</td><td>&lt;Boolean></td><td>Read-only</td><td>Temporary flag used for internal purpose.</td></tr><tr><td>portbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Member interfaces of this vlan.</td></tr><tr><td>lsbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Member linksets of this vlan.</td></tr><tr><td>tagbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Tagged members of this vlan.</td></tr><tr><td>lstagbitmap</td><td>&lt;Double></td><td>Read-only</td><td>Tagged linksets of this vlan.</td></tr><tr><td>ifaces</td><td>&lt;String></td><td>Read-only</td><td>Names of all member interfaces of this vlan.</td></tr><tr><td>tagifaces</td><td>&lt;String></td><td>Read-only</td><td>Names of all tagged member interfaces of this vlan.</td></tr><tr><td>ifnum</td><td>&lt;String></td><td>Read-only</td><td>The interface to be bound to the VLAN, specified in slot/port notation (for example, 1/3).<br>Minimum length = 1</td></tr><tr><td>tagged</td><td>&lt;Boolean></td><td>Read-only</td><td>Make the interface an 802.1q tagged interface. Packets sent on this interface on this VLAN have an additional 4-byte 802.1q tag, which identifies the VLAN. To use 802.1q tagging, you must also configure the switch connected to the appliance's interfaces.</td></tr><tr><td>vlantd</td><td>&lt;Double></td><td>Read-only</td><td>Traffic domain associated with vlan.<br>Minimum value = 0<br>Maximum value = 4094</td></tr><tr><td>sdxvlan</td><td>&lt;String></td><td>Read-only</td><td>SDX vlan.<br>Default value: NO<br>Possible values = YES, NO</td></tr><tr><td>partitionname</td><td>&lt;String></td><td>Read-only</td><td>Name of the Partition to which this vlan bound to.<br>Minimum length = 1</td></tr><tr><td>vxlan</td><td>&lt;Double></td><td>Read-only</td><td>The VXLAN that extends this vlan.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vlan":{<b>"id":<Double_value>,</b>"aliasname":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>,"mtu":<Double_value>,"sharing":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vlan":{<b>"id":<Double_value>,</b>"aliasname":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>,"mtu":<Double_value>,"sharing":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"vlan":{<b>"id":<Double_value>,</b>"aliasname":true,"dynamicrouting":true,"ipv6dynamicrouting":true,"mtu":true,"sharing":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of vlan resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the vlan resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vlan": [ {"id":<Double_value>,"aliasname":<String_value>,"linklocalipv6addr":<String_value>,"rnat":<Boolean_value>,"portbitmap":<Double_value>,"lsbitmap":<Double_value>,"tagbitmap":<Double_value>,"lstagbitmap":<Double_value>,"ifaces":<String_value>,"tagifaces":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>,"ifnum":<String_value>,"tagged":<Boolean_value>,"vlantd":<Double_value>,"sdxvlan":<String_value>,"mtu":<Double_value>,"sharing":<String_value>,"partitionname":<String_value>,"vxlan":<Double_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan/id_value&lt;Double&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vlan": [ {"id":<Double_value>,"aliasname":<String_value>,"linklocalipv6addr":<String_value>,"rnat":<Boolean_value>,"portbitmap":<Double_value>,"lsbitmap":<Double_value>,"tagbitmap":<Double_value>,"lstagbitmap":<Double_value>,"ifaces":<String_value>,"tagifaces":<String_value>,"dynamicrouting":<String_value>,"ipv6dynamicrouting":<String_value>,"ifnum":<String_value>,"tagged":<Boolean_value>,"vlantd":<Double_value>,"sdxvlan":<String_value>,"mtu":<Double_value>,"sharing":<String_value>,"partitionname":<String_value>,"vxlan":<Double_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/vlan?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "vlan": [ { "__count": "#no"} ] }```



