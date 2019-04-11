#nsconfig

Configuration for system config resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>force</td><td>&lt;Boolean></td><td>Read-write</td><td>Configurations will be cleared without prompting for confirmation.</td></tr><tr><td>level</td><td>&lt;String></td><td>Read-write</td><td>Types of configurations to be cleared.<br>* basic: Clears all configurations except the following:<br>- NSIP, default route (gateway), MIPs, and SNIPs<br>- Network settings (DG, VLAN, RHI and DNS settings)<br>- Cluster settings<br>- HA node definitions<br>- Feature and mode settings<br>- nsroot password<br>* extended: Clears the same configurations as the 'basic' option. In addition, it clears the feature and mode settings.<br>* full: Clears all configurations except NSIP, default route, and interface settings.<br>Note: When you clear the configurations through the cluster IP address, by specifying the level as 'full', the cluster is deleted and all cluster nodes become standalone appliances. The 'basic' and 'extended' levels are propagated to the cluster nodes.<br>Possible values = basic, extended, full</td></tr><tr><td>rbaconfig</td><td>&lt;String></td><td>Read-write</td><td>RBA configurations and TACACS policies bound to system global will not be cleared if RBA is set to NO.This option is applicable only for BASIC level of clear configuration.Default is YES, which will clear rba configurations.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>ipaddress</td><td>&lt;String></td><td>Read-write</td><td>IP address of the Citrix ADC. Commonly referred to as NSIP address. This parameter is mandatory to bring up the appliance.<br>Minimum length = 1</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>Netmask corresponding to the IP address. This parameter is mandatory to bring up the appliance.</td></tr><tr><td>nsvlan</td><td>&lt;Double></td><td>Read-write</td><td>VLAN (NSVLAN) for the subnet on which the IP address resides.<br>Minimum value = 2<br>Maximum value = 4094</td></tr><tr><td>ifnum</td><td>&lt;String[]></td><td>Read-write</td><td>Interfaces of the appliances that must be bound to the NSVLAN.<br>Minimum length = 1</td></tr><tr><td>tagged</td><td>&lt;String></td><td>Read-write</td><td>Specifies that the interfaces will be added as 802.1q tagged interfaces. Packets sent on these interface on this VLAN will have an additional 4-byte 802.1q tag which identifies the VLAN.<br>To use 802.1q tagging, the switch connected to the appliance's interfaces must also be configured for tagging.<br>Default value: YES<br>Possible values = YES, NO</td></tr><tr><td>httpport</td><td>&lt;Integer[]></td><td>Read-write</td><td>The HTTP ports on the Web server. This allows the system to perform connection off-load for any client request that has a destination port matching one of these configured ports.<br>Minimum value = 1</td></tr><tr><td>maxconn</td><td>&lt;Double></td><td>Read-write</td><td>The maximum number of connections that will be made from the system to the web server(s) attached to it. The value entered here is applied globally to all attached servers.<br>Minimum value = 0<br>Maximum value = 4294967294</td></tr><tr><td>maxreq</td><td>&lt;Double></td><td>Read-write</td><td>The maximum number of requests that the system can pass on a particular connection between the system and a server attached to it. Setting this value to 0 allows an unlimited number of requests to be passed.<br>Minimum value = 0<br>Maximum value = 65535</td></tr><tr><td>cip</td><td>&lt;String></td><td>Read-write</td><td>The option to control (enable or disable) the insertion of the actual client IP address into the HTTP header request passed from the client to one, some, or all servers attached to the system.<br>The passed address can then be accessed through a minor modification to the server.<br>l If cipHeader is specified, it will be used as the client IP header.<br>l If it is not specified, then the value that has been set by the set ns config CLI command will be used as the client IP header.<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>cipheader</td><td>&lt;String></td><td>Read-write</td><td>The text that will be used as the client IP header.<br>Minimum length = 1</td></tr><tr><td>cookieversion</td><td>&lt;String></td><td>Read-write</td><td>The version of the cookie inserted by system.<br>Possible values = 0, 1</td></tr><tr><td>securecookie</td><td>&lt;String></td><td>Read-write</td><td>enable/disable secure flag for persistence cookie.<br>Default value: ENABLED<br>Possible values = ENABLED, DISABLED</td></tr><tr><td>pmtumin</td><td>&lt;Double></td><td>Read-write</td><td>The minimum Path MTU.<br>Default value: 576<br>Minimum value = 168<br>Maximum value = 1500</td></tr><tr><td>pmtutimeout</td><td>&lt;Double></td><td>Read-write</td><td>The timeout value in minutes.<br>Default value: 10<br>Minimum value = 1<br>Maximum value = 1440</td></tr><tr><td>ftpportrange</td><td>&lt;String></td><td>Read-write</td><td>Port range configured for FTP services.<br>Minimum length = 1024<br>Maximum length = 64000</td></tr><tr><td>crportrange</td><td>&lt;String></td><td>Read-write</td><td>Port range for cache redirection services.<br>Minimum length = 1<br>Maximum length = 65535</td></tr><tr><td>timezone</td><td>&lt;String></td><td>Read-write</td><td>Name of the timezone.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>grantquotamaxclient</td><td>&lt;Double></td><td>Read-write</td><td>The percentage of shared quota to be granted at a time for maxClient.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>exclusivequotamaxclient</td><td>&lt;Double></td><td>Read-write</td><td>The percentage of maxClient to be given to PEs.<br>Default value: 80<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>grantquotaspillover</td><td>&lt;Double></td><td>Read-write</td><td>The percentage of shared quota to be granted at a time for spillover.<br>Default value: 10<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>exclusivequotaspillover</td><td>&lt;Double></td><td>Read-write</td><td>The percentage of max limit to be given to PEs.<br>Default value: 80<br>Minimum value = 0<br>Maximum value = 100</td></tr><tr><td>config1</td><td>&lt;String></td><td>Read-write</td><td>Location of the configurations.</td></tr><tr><td>config2</td><td>&lt;String></td><td>Read-write</td><td>Location of the configurations.</td></tr><tr><td>outtype</td><td>&lt;String></td><td>Read-write</td><td>Format to display the difference in configurations.<br>Possible values = cli, xml</td></tr><tr><td>template</td><td>&lt;Boolean></td><td>Read-write</td><td>File that contains the commands to be compared.</td></tr><tr><td>ignoredevicespecific</td><td>&lt;Boolean></td><td>Read-write</td><td>Suppress device specific differences.</td></tr><tr><td>weakpassword</td><td>&lt;Boolean></td><td>Read-write</td><td>Option to list all weak passwords (not adhering to strong password requirements). Takes config file as input, if no input specified, running configuration is considered. Command =&gt; query ns config -weakpassword / query ns config -weakpassword /nsconfig/ns.conf.</td></tr><tr><td>config</td><td>&lt;String></td><td>Read-write</td><td>configuration File to be used to find weak passwords, if not specified, running config is taken as input.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr><tr><td>mappedip</td><td>&lt;String></td><td>Read-only</td><td>Mapped IP Address of the System.<br>Minimum length = 1</td></tr><tr><td>range</td><td>&lt;Double></td><td>Read-only</td><td>The range of Mapped IP addresses to be configured.<br>Minimum value = 1</td></tr><tr><td>systemtype</td><td>&lt;String></td><td>Read-only</td><td>The type of the System. Possible Values: Standalone, HA, Cluster.<br>Possible values = Stand-alone, HA, Cluster</td></tr><tr><td>primaryip</td><td>&lt;String></td><td>Read-only</td><td>HA Master Node IP address.</td></tr><tr><td>primaryip6</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr><tr><td>flags</td><td>&lt;Double></td><td>Read-only</td><td>The flags for this entry.</td></tr><tr><td>lastconfigchangedtime</td><td>&lt;String></td><td>Read-only</td><td>Time when the configuration was last modified.</td></tr><tr><td>lastconfigsavetime</td><td>&lt;String></td><td>Read-only</td><td>Time when the configuration was last saved through savensconfig.</td></tr><tr><td>currentsytemtime</td><td>&lt;String></td><td>Read-only</td><td>current system time in date format.</td></tr><tr><td>systemtime</td><td>&lt;Double></td><td>Read-only</td><td>current system time.</td></tr><tr><td>configchanged</td><td>&lt;Boolean></td><td>Read-only</td><td>returns True if configuration has changed since last saved config.</td></tr><tr><td>response</td><td>&lt;String></td><td>Read-only</td><td>.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[CLEAR](#)| [UPDATE](#u)| [UNSET](#)| [SAVE]()| [DIFF]()| [GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###clear



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig?<b>action=clear</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsconfig":{"force":<Boolean_value>,<b>"level":<String_value>,</b>"rbaconfig":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsconfig":{"ipaddress":<String_value>,"netmask":<String_value>,"nsvlan":<Double_value>,"ifnum":<String[]_value>,"tagged":<String_value>,"httpport":<Integer[]_value>,"maxconn":<Double_value>,"maxreq":<Double_value>,"cip":<String_value>,"cipheader":<String_value>,"cookieversion":<String_value>,"securecookie":<String_value>,"pmtumin":<Double_value>,"pmtutimeout":<Double_value>,"ftpportrange":<String_value>,"crportrange":<String_value>,"timezone":<String_value>,"grantquotamaxclient":<Double_value>,"exclusivequotamaxclient":<Double_value>,"grantquotaspillover":<Double_value>,"exclusivequotaspillover":<Double_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsconfig":{"nsvlan":true,"ftpportrange":true,"crportrange":true,"timezone":true,"ipaddress":true,"netmask":true,"ifnum":true,"tagged":true,"httpport":true,"maxconn":true,"maxreq":true,"cip":true,"cipheader":true,"cookieversion":true,"securecookie":true,"pmtumin":true,"pmtutimeout":true,"grantquotamaxclient":true,"exclusivequotamaxclient":true,"grantquotaspillover":true,"exclusivequotaspillover":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###save



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig?<b>action=save</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsconfig":{}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###diff



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig?<b>action=diff</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"nsconfig":{"config1":<String_value>,"config2":<String_value>,"outtype":<String_value>,"template":<Boolean_value>,"ignoredevicespecific":<Boolean_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Payload: </b>```{ "nsconfig": [ {"response":<String_value>}]}```



###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/nsconfig
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "nsconfig": [ {"ipaddress":<String_value>,"netmask":<String_value>,"mappedip":<String_value>,"range":<Double_value>,"nsvlan":<Double_value>,"ifnum":<String[]_value>,"tagged":<String_value>,"httpport":<Integer[]_value>,"maxconn":<Double_value>,"maxreq":<Double_value>,"cip":<String_value>,"cipheader":<String_value>,"cookieversion":<String_value>,"securecookie":<String_value>,"failover":<String_value>,"systemtype":<String_value>,"primaryip":<String_value>,"primaryip6":<String_value>,"pmtumin":<Double_value>,"pmtutimeout":<Double_value>,"ftpportrange":<String_value>,"crportrange":<String_value>,"flags":<Double_value>,"timezone":<String_value>,"lastconfigchangedtime":<String_value>,"lastconfigsavetime":<String_value>,"currentsytemtime":<String_value>,"systemtime":<Double_value>,"grantquotamaxclient":<Double_value>,"exclusivequotamaxclient":<Double_value>,"grantquotaspillover":<Double_value>,"exclusivequotaspillover":<Double_value>,"configchanged":<Boolean_value>}]}```



