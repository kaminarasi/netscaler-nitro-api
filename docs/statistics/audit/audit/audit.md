#audit

Statistics for audit.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>auditsyslogmsgsent</td><td>&lt;Double></td><td>Read-only</td><td>Syslog messages sent to the syslog server(s) over UDP.</td></tr><tr><td>auditsyslogmsgsentrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditsyslogmsgsent</td></tr><tr><td>auditsyslogmsggen</td><td>&lt;Double></td><td>Read-only</td><td>Syslog messages about to be sent to the syslog server.</td></tr><tr><td>auditsyslogmsggenrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditsyslogmsggen</td></tr><tr><td>auditsyslogmsgsenttcp</td><td>&lt;Double></td><td>Read-only</td><td>Syslog messages sent to the syslog server(s) over TCP.</td></tr><tr><td>auditsyslogmsgsenttcprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditsyslogmsgsenttcp</td></tr><tr><td>auditnsballocfail</td><td>&lt;Double></td><td>Read-only</td><td>NAT allocation failed.</td></tr><tr><td>auditnsballocfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditnsballocfail</td></tr><tr><td>auditlog32errsyslogallocnsbfail</td><td>&lt;Double></td><td>Read-only</td><td>Nsb allocation failed.</td></tr><tr><td>auditlog32errsyslogallocnsbfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditlog32errsyslogallocnsbfail</td></tr><tr><td>auditmemallocfail</td><td>&lt;Double></td><td>Read-only</td><td>Failures in allocation of Access Gateway context structure. When an Access Gateway session is established, the Citrix ADC creates an internal context structure , which identifies the user and the IP address from which the user has logged in.</td></tr><tr><td>auditmemallocfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditmemallocfail</td></tr><tr><td>auditportallocfail</td><td>&lt;Double></td><td>Read-only</td><td>Number of times the Citrix ADC failed to allocate a port when sending a syslog message to the syslog server(s).</td></tr><tr><td>auditportallocfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditportallocfail</td></tr><tr><td>auditcontextnotfound</td><td>&lt;Double></td><td>Read-only</td><td>Failures in finding the context structure for an Access Gateway session during attempts to send session-specific audit messages. During an Access Gateway session, audit messages related to the session are queued up in the auditlog buffer for transmission to the audit log server(s). If the session is killed before the messages are sent, the context structure allocated at session creation is removed. This structure is needed for sending the queued auditlog messages. If it is not found, this counter is incremented.</td></tr><tr><td>auditcontextnotfoundrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for auditcontextnotfound</td></tr><tr><td>nsbchainallocfail</td><td>&lt;Double></td><td>Read-only</td><td>Nsb Chain allocation failed.</td></tr><tr><td>nsbchainallocfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for nsbchainallocfail</td></tr><tr><td>clientconnfail</td><td>&lt;Double></td><td>Read-only</td><td>Failures in establishment of a connection between the Citrix ADC and the auditserver tool (the Citrix ADC's custom logging tool).</td></tr><tr><td>clientconnfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for clientconnfail</td></tr><tr><td>flushcmdcnt</td><td>&lt;Double></td><td>Read-only</td><td>Auditlog buffer flushes. In a multiprocessor Citrix ADC, both the main processor and the co-processor can generate auditlog messages and fill up the auditlog buffers. But only the primary processor can free up the buffers by sending auditlog messages to the auditlog server(s). The number of auditlog buffers is fixed. If the co-processor detects that all the auditlog buffers are full, it issues a flush command to the main processor.</td></tr><tr><td>flushcmdcntrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for flushcmdcnt</td></tr><tr><td>systcpconnfail</td><td>&lt;Double></td><td>Read-only</td><td>Failures in establishment of a connection between the Citrix ADC and the syslog server.</td></tr><tr><td>systcpconnfailrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for systcpconnfail</td></tr><tr><td>logunsentlbsys</td><td>&lt;Double></td><td>Read-only</td><td>Total auditlog messages which are not delivered to load balanced syslog servers</td></tr><tr><td>logunsentlbsysrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for logunsentlbsys</td></tr><tr><td>logsdropped</td><td>&lt;Double></td><td>Read-only</td><td>Total number of log messages dropped by Citrix ADC after max hold limit is reached</td></tr><tr><td>logsdroppedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for logsdropped</td></tr><tr><td>logsdroppedtxminnsbs</td><td>&lt;Double></td><td>Read-only</td><td>Total number of log messages dropped by Citrix ADC when NSBQ length is less than TX min NSBs</td></tr><tr><td>logsdroppedtxminnsbsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for logsdroppedtxminnsbs</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/audit
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/audit?<b>args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get audit resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "audit": [ {"auditportallocfailrate":<Double_value>,"auditnsballocfailrate":<Double_value>,"auditsyslogmsgsenttcprate":<Double_value>,"auditcontextnotfoundrate":<Double_value>,"logsdroppedtxminnsbs":<Double_value>,"clientconnfail":<Double_value>,"flushcmdcntrate":<Double_value>,"auditlog32errsyslogallocnsbfailrate":<Double_value>,"auditnsballocfail":<Double_value>,"auditsyslogmsgsentrate":<Double_value>,"clientconnfailrate":<Double_value>,"auditmemallocfailrate":<Double_value>,"auditlog32errsyslogallocnsbfail":<Double_value>,"logsdroppedrate":<Double_value>,"auditportallocfail":<Double_value>,"nsbchainallocfail":<Double_value>,"logunsentlbsys":<Double_value>,"systcpconnfailrate":<Double_value>,"systcpconnfail":<Double_value>,"auditmemallocfail":<Double_value>,"logunsentlbsysrate":<Double_value>,"auditsyslogmsggenrate":<Double_value>,"logsdropped":<Double_value>,"auditsyslogmsgsent":<Double_value>,"auditcontextnotfound":<Double_value>,"flushcmdcnt":<Double_value>,"logsdroppedtxminnsbsrate":<Double_value>,"auditsyslogmsggen":<Double_value>,"nsbchainallocfailrate":<Double_value>,"auditsyslogmsgsenttcp":<Double_value>}]}```



