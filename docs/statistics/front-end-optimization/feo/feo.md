#feo

Statistics for feo.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clearstats</td><td>&lt;String></td><td>Read-write</td><td>Clear the statsistics / counters.<br>Possible values = basic, full</td></tr><tr><td>optcacheobjects</td><td>&lt;Double></td><td>Read-only</td><td>Total number of optimized cache objects ready to be served.</td></tr><tr><td>optcacheobjectsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for optcacheobjects</td></tr><tr><td>origcacheobjects</td><td>&lt;Double></td><td>Read-only</td><td>Total number of original cache objects ready to be served.</td></tr><tr><td>origcacheobjectsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for origcacheobjects</td></tr><tr><td>totalimgsdomainsharded</td><td>&lt;Double></td><td>Read-only</td><td>Total no of images whose domain has been set from shards.</td></tr><tr><td>imgsdomainshardedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgsdomainsharded</td></tr><tr><td>totalimgslazyloaded</td><td>&lt;Double></td><td>Read-only</td><td>Total number of images modified for lazy loading.</td></tr><tr><td>imgslazyloadedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgslazyloaded</td></tr><tr><td>toturireplaced</td><td>&lt;Double></td><td>Read-only</td><td>Total number of URI replaced.</td></tr><tr><td>urireplacedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for toturireplaced</td></tr><tr><td>totalimgsinlinedincss</td><td>&lt;Double></td><td>Read-only</td><td>Total number of images inlined in CSS.</td></tr><tr><td>imgsinlinedincssrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgsinlinedincss</td></tr><tr><td>totalinlinedjs</td><td>&lt;Double></td><td>Read-only</td><td>Total number of inlined JS files.</td></tr><tr><td>inlinedjsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalinlinedjs</td></tr><tr><td>totalinlinedcss</td><td>&lt;Double></td><td>Read-only</td><td>Total number of inlined CSS files.</td></tr><tr><td>inlinedcssrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalinlinedcss</td></tr><tr><td>totalinlinedimgs</td><td>&lt;Double></td><td>Read-only</td><td>Total number of inlined images in HTML.</td></tr><tr><td>inlinedimgsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalinlinedimgs</td></tr><tr><td>totaldatasavings</td><td>&lt;Double></td><td>Read-only</td><td>Total data savings in bytes.</td></tr><tr><td>datasavingsrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaldatasavings</td></tr><tr><td>htmlcommentsremoved</td><td>&lt;Double></td><td>Read-only</td><td>The total number of HTML comments removed.</td></tr><tr><td>htmlcommentsremovedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for htmlcommentsremoved</td></tr><tr><td>totalcacheextended</td><td>&lt;Double></td><td>Read-only</td><td>The total number of objects cache extended.</td></tr><tr><td>cacheextendedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalcacheextended</td></tr><tr><td>totalcsscombined</td><td>&lt;Double></td><td>Read-only</td><td>The total number of CSS combined.</td></tr><tr><td>csscombinedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalcsscombined</td></tr><tr><td>totalimporttolink</td><td>&lt;Double></td><td>Read-only</td><td>The total number of CSS imports converted to links</td></tr><tr><td>importtolinkrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimporttolink</td></tr><tr><td>totaljsmoved</td><td>&lt;Double></td><td>Read-only</td><td>The total number of JS moved to end.</td></tr><tr><td>jsmovedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaljsmoved</td></tr><tr><td>totalcssmoved</td><td>&lt;Double></td><td>Read-only</td><td>The total number of CSS moved to head.</td></tr><tr><td>cssmovedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalcssmoved</td></tr><tr><td>totaljsmin</td><td>&lt;Double></td><td>Read-only</td><td>The total number of JS files minified.</td></tr><tr><td>jsminrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaljsmin</td></tr><tr><td>totalcssmin</td><td>&lt;Double></td><td>Read-only</td><td>The total number of CSS files minified.</td></tr><tr><td>cssminrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalcssmin</td></tr><tr><td>totalimgstojxr</td><td>&lt;Double></td><td>Read-only</td><td>The total number of images converted to JPEGXR format.</td></tr><tr><td>imgstojxrrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgstojxr</td></tr><tr><td>totalimgstowebp</td><td>&lt;Double></td><td>Read-only</td><td>The total number of images converted to WEBP format.</td></tr><tr><td>imgstowebprate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgstowebp</td></tr><tr><td>totaljpegsoptimized</td><td>&lt;Double></td><td>Read-only</td><td>The total number of JPEG format images optimized.</td></tr><tr><td>jpegsoptimizedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totaljpegsoptimized</td></tr><tr><td>totalgifstopng</td><td>&lt;Double></td><td>Read-only</td><td>The total number of images converted from GIF to PNG format.</td></tr><tr><td>gifstopngrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalgifstopng</td></tr><tr><td>totalimgsresized</td><td>&lt;Double></td><td>Read-only</td><td>The total number of images resized to dimensions in the &lt;img&gt; tag.</td></tr><tr><td>imgsresizedrate</td><td>&lt;Double></td><td>Read-only</td><td>Rate (/s) counter for totalimgsresized</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#ge)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/feo
<b>Query-parameters:</b>
<b>args</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/stat/feo?<b>args=detail:&lt;Boolean_value&gt;,fullvalues:&lt;Boolean_value&gt;,ntimes:&lt;Double_value&gt;,logfile:&lt;String_value&gt;,clearstats:&lt;String_value&gt;</b>
Use this query-parameter to get feo resources based on additional properties.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "feo": [ {"totaljsmoved":<Double_value>,"totalimgslazyloaded":<Double_value>,"htmlcommentsremovedrate":<Double_value>,"urireplacedrate":<Double_value>,"cssmovedrate":<Double_value>,"htmlcommentsremoved":<Double_value>,"jsmovedrate":<Double_value>,"totalimgsinlinedincss":<Double_value>,"totalinlinedcss":<Double_value>,"inlinedimgsrate":<Double_value>,"toturireplaced":<Double_value>,"imgstowebprate":<Double_value>,"totalinlinedjs":<Double_value>,"totalcssmoved":<Double_value>,"csscombinedrate":<Double_value>,"imgslazyloadedrate":<Double_value>,"totaljsmin":<Double_value>,"optcacheobjects":<Double_value>,"totalgifstopng":<Double_value>,"totalimgsresized":<Double_value>,"imgsinlinedincssrate":<Double_value>,"inlinedcssrate":<Double_value>,"totalimgstowebp":<Double_value>,"inlinedjsrate":<Double_value>,"origcacheobjectsrate":<Double_value>,"cssminrate":<Double_value>,"totalimgsdomainsharded":<Double_value>,"imgsdomainshardedrate":<Double_value>,"gifstopngrate":<Double_value>,"importtolinkrate":<Double_value>,"totalcsscombined":<Double_value>,"totalimgstojxr":<Double_value>,"imgsresizedrate":<Double_value>,"optcacheobjectsrate":<Double_value>,"totaljpegsoptimized":<Double_value>,"totalcacheextended":<Double_value>,"origcacheobjects":<Double_value>,"jsminrate":<Double_value>,"jpegsoptimizedrate":<Double_value>,"totaldatasavings":<Double_value>,"imgstojxrrate":<Double_value>,"datasavingsrate":<Double_value>,"cacheextendedrate":<Double_value>,"totalcssmin":<Double_value>,"totalinlinedimgs":<Double_value>,"totalimporttolink":<Double_value>}]}```



