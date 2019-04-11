#authenticationsamlaction

Configuration for AAA Saml action resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name for the SAML server profile (action). <br>Must begin with a letter, number, or the underscore character (_), and must contain only letters, numbers, and the hyphen (-), period (.) pound (#), space ( ), at (@), equals (=), colon (:), and underscore characters. Cannot be changed after SAML profile is created.<br><br>The following requirement applies only to the Citrix ADC CLI:<br>If the name includes one or more spaces, enclose the name in double or single quotation marks (for example, "my authentication action" or 'my authentication action').<br>Minimum length = 1</td></tr><tr><td>samlidpcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL certificate used to verify responses from SAML Identity Provider (IdP).<br>Minimum length = 1</td></tr><tr><td>samlsigningcertname</td><td>&lt;String></td><td>Read-write</td><td>Name of the SSL certificate to sign requests from ServiceProvider (SP) to Identity Provider (IdP).<br>Minimum length = 1</td></tr><tr><td>samlredirecturl</td><td>&lt;String></td><td>Read-write</td><td>URL to which users are redirected for authentication.<br>Minimum length = 1</td></tr><tr><td>samlacsindex</td><td>&lt;Double></td><td>Read-write</td><td>Index/ID of the metadata entry corresponding to this configuration.<br>Default value: 255<br>Minimum value = 0<br>Maximum value = 255</td></tr><tr><td>samluserfield</td><td>&lt;String></td><td>Read-write</td><td>SAML user ID, as given in the SAML assertion.<br>Minimum length = 1</td></tr><tr><td>samlrejectunsignedassertion</td><td>&lt;String></td><td>Read-write</td><td>Reject unsigned SAML assertions. ON option results in rejection of Assertion that is received without signature. STRICT option ensures that both Response and Assertion are signed. OFF allows unsigned Assertions.<br>Default value: ON<br>Possible values = ON, OFF, STRICT</td></tr><tr><td>samlissuername</td><td>&lt;String></td><td>Read-write</td><td>The name to be used in requests sent from Citrix ADC to IdP to uniquely identify Citrix ADC.<br>Minimum length = 1</td></tr><tr><td>samltwofactor</td><td>&lt;String></td><td>Read-write</td><td>Option to enable second factor after SAML.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>defaultauthenticationgroup</td><td>&lt;String></td><td>Read-write</td><td>This is the default group that is chosen when the authentication succeeds in addition to extracted groups.</td></tr><tr><td>attribute1</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute1. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute2</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute2. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute3</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute3. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute4</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute4. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute5</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute5. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute6</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute6. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute7</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute7. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute8</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute8. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute9</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute9. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute10</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute10. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute11</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute11. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute12</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute12. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute13</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute13. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute14</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute14. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute15</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute15. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>attribute16</td><td>&lt;String></td><td>Read-write</td><td>Name of the attribute in SAML Assertion whose value needs to be extracted and stored as attribute16. Maximum length of the extracted attribute is 239 bytes.</td></tr><tr><td>signaturealg</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to sign/verify SAML transactions.<br>Default value: RSA-SHA1<br>Possible values = RSA-SHA1, RSA-SHA256</td></tr><tr><td>digestmethod</td><td>&lt;String></td><td>Read-write</td><td>Algorithm to be used to compute/verify digest for SAML transactions.<br>Default value: SHA1<br>Possible values = SHA1, SHA256</td></tr><tr><td>requestedauthncontext</td><td>&lt;String></td><td>Read-write</td><td>This element specifies the authentication context requirements of authentication statements returned in the response.<br>Default value: exact<br>Possible values = exact, minimum, maximum, better</td></tr><tr><td>authnctxclassref</td><td>&lt;String[]></td><td>Read-write</td><td>This element specifies the authentication class types that are requested from IdP (IdentityProvider).<br>InternetProtocol: This is applicable when a principal is authenticated through the use of a provided IP address.<br>InternetProtocolPassword: This is applicable when a principal is authenticated through the use of a provided IP address, in addition to a username/password.<br>Kerberos: This is applicable when the principal has authenticated using a password to a local authentication authority, in order to acquire a Kerberos ticket.<br>MobileOneFactorUnregistered: This indicates authentication of the mobile device without requiring explicit end-user interaction.<br>MobileTwoFactorUnregistered: This indicates two-factor based authentication during mobile customer registration process, such as secure device and user PIN.<br>MobileOneFactorContract: Reflects mobile contract customer registration procedures and a single factor authentication.<br>MobileTwoFactorContract: Reflects mobile contract customer registration procedures and a two-factor based authentication.<br>Password: This class is applicable when a principal authenticates using password over unprotected http session.<br>PasswordProtectedTransport: This class is applicable when a principal authenticates to an authentication authority through the presentation of a password over a protected session.<br>PreviousSession: This class is applicable when a principal had authenticated to an authentication authority at some point in the past using any authentication context.<br>X509: This indicates that the principal authenticated by means of a digital signature where the key was validated as part of an X.509 Public Key Infrastructure.<br>PGP: This indicates that the principal authenticated by means of a digital signature where the key was validated as part of a PGP Public Key Infrastructure.<br>SPKI: This indicates that the principal authenticated by means of a digital signature where the key was validated via an SPKI Infrastructure.<br>XMLDSig: This indicates that the principal authenticated by means of a digital signature according to the processing rules specified in the XML Digital Signature specification.<br>Smartcard: This indicates that the principal has authenticated using smartcard.<br>SmartcardPKI: This class is applicable when a principal authenticates to an authentication authority through a two-factor authentication mechanism using a smartcard with enclosed private key and a PIN.<br>SoftwarePKI: This class is applicable when a principal uses an X.509 certificate stored in software to authenticate to the authentication authority.<br>Telephony: This class is used to indicate that the principal authenticated via the provision of a fixed-line telephone number, transported via a telephony protocol such as ADSL.<br>NomadTelephony: Indicates that the principal is "roaming" and authenticates via the means of the line number, a user suffix, and a password element.<br>PersonalTelephony: This class is used to indicate that the principal authenticated via the provision of a fixed-line telephone.<br>AuthenticatedTelephony: Indicates that the principal authenticated via the means of the line number, a user suffix, and a password element.<br>SecureRemotePassword: This class is applicable when the authentication was performed by means of Secure Remote Password.<br>TLSClient: This class indicates that the principal authenticated by means of a client certificate, secured with the SSL/TLS transport.<br>TimeSyncToken: This is applicable when a principal authenticates through a time synchronization token.<br>Unspecified: This indicates that the authentication was performed by unspecified means.<br>Windows: This indicates that Windows integrated authentication is utilized for authentication.<br>Possible values = InternetProtocol, InternetProtocolPassword, Kerberos, MobileOneFactorUnregistered, MobileTwoFactorUnregistered, MobileOneFactorContract, MobileTwoFactorContract, Password, PasswordProtectedTransport, PreviousSession, X509, PGP, SPKI, XMLDSig, Smartcard, SmartcardPKI, SoftwarePKI, Telephony, NomadTelephony, PersonalTelephony, AuthenticatedTelephony, SecureRemotePassword, TLSClient, TimeSyncToken, Unspecified, Windows</td></tr><tr><td>samlbinding</td><td>&lt;String></td><td>Read-write</td><td>This element specifies the transport mechanism of saml messages.<br>Default value: POST<br>Possible values = REDIRECT, POST, ARTIFACT</td></tr><tr><td>attributeconsumingserviceindex</td><td>&lt;Double></td><td>Read-write</td><td>Index/ID of the attribute specification at Identity Provider (IdP). IdP will locate attributes requested by SP using this index and send those attributes in Assertion.<br>Default value: 255<br>Minimum value = 0<br>Maximum value = 255</td></tr><tr><td>sendthumbprint</td><td>&lt;String></td><td>Read-write</td><td>Option to send thumbprint instead of x509 certificate in SAML request.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>enforceusername</td><td>&lt;String></td><td>Read-write</td><td>Option to choose whether the username that is extracted from SAML assertion can be edited in login page while doing second factor.<br>Default value: ON<br>Possible values = ON, OFF</td></tr><tr><td>logouturl</td><td>&lt;String></td><td>Read-write</td><td>SingleLogout URL on IdP to which logoutRequest will be sent on Citrix ADC session cleanup.</td></tr><tr><td>artifactresolutionserviceurl</td><td>&lt;String></td><td>Read-write</td><td>URL of the Artifact Resolution Service on IdP to which Citrix ADC will post artifact to get actual SAML token.</td></tr><tr><td>skewtime</td><td>&lt;Double></td><td>Read-write</td><td>This option specifies the allowed clock skew in number of minutes that Citrix ADC ServiceProvider allows on an incoming assertion. For example, if skewTime is 10, then assertion would be valid from (current time - 10) min to (current time + 10) min, ie 20min in all.<br>Default value: 5</td></tr><tr><td>logoutbinding</td><td>&lt;String></td><td>Read-write</td><td>This element specifies the transport mechanism of saml logout messages.<br>Default value: POST<br>Possible values = REDIRECT, POST</td></tr><tr><td>forceauthn</td><td>&lt;String></td><td>Read-write</td><td>Option that forces authentication at the Identity Provider (IdP) that receives Citrix ADC's request.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>groupnamefield</td><td>&lt;String></td><td>Read-write</td><td>Name of the tag in assertion that contains user groups.</td></tr><tr><td>audience</td><td>&lt;String></td><td>Read-write</td><td>Audience for which assertion sent by IdP is applicable. This is typically entity name or url that represents ServiceProvider.</td></tr><tr><td>metadataurl</td><td>&lt;String></td><td>Read-write</td><td>This URL is used for obtaining saml metadata.</td></tr><tr><td>metadatarefreshinterval</td><td>&lt;Double></td><td>Read-write</td><td>Interval in minutes for fetching metadata from specified metadata URL.<br>Default value: 36000</td></tr><tr><td>storesamlresponse</td><td>&lt;String></td><td>Read-write</td><td>Option to store entire SAML Response through the life of user session.<br>Default value: OFF<br>Possible values = ON, OFF</td></tr><tr><td>metadataimportstatus</td><td>&lt;String></td><td>Read-only</td><td>Describes metadata import status.<br>Default value: SUCCESS<br>Possible values = INIT, SUCCESS, FAIL</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-only</td><td>count parameter</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [UPDATE](#u)| [UNSET](#)| [GET (ALL)](#ge)| [GET]()| [COUNT](#)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationsamlaction":{<b>"name":<String_value>,</b>"samlidpcertname":<String_value>,"samlsigningcertname":<String_value>,"samlredirecturl":<String_value>,"samlacsindex":<Double_value>,"samluserfield":<String_value>,"samlrejectunsignedassertion":<String_value>,"samlissuername":<String_value>,"samltwofactor":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"requestedauthncontext":<String_value>,"authnctxclassref":<String[]_value>,"samlbinding":<String_value>,"attributeconsumingserviceindex":<Double_value>,"sendthumbprint":<String_value>,"enforceusername":<String_value>,"logouturl":<String_value>,"artifactresolutionserviceurl":<String_value>,"skewtime":<Double_value>,"logoutbinding":<String_value>,"forceauthn":<String_value>,"groupnamefield":<String_value>,"audience":<String_value>,"metadataurl":<String_value>,"metadatarefreshinterval":<Double_value>,"storesamlresponse":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 201 CreatedHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###delete



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;
<b>HTTP Method:</b>DELETE
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###update



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction
<b>HTTP Method:</b>PUT
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationsamlaction":{<b>"name":<String_value>,</b>"samlidpcertname":<String_value>,"samlsigningcertname":<String_value>,"samlredirecturl":<String_value>,"samlacsindex":<Double_value>,"samluserfield":<String_value>,"samlrejectunsignedassertion":<String_value>,"samlissuername":<String_value>,"samltwofactor":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"requestedauthncontext":<String_value>,"authnctxclassref":<String[]_value>,"samlbinding":<String_value>,"attributeconsumingserviceindex":<Double_value>,"sendthumbprint":<String_value>,"enforceusername":<String_value>,"logouturl":<String_value>,"artifactresolutionserviceurl":<String_value>,"skewtime":<Double_value>,"logoutbinding":<String_value>,"forceauthn":<String_value>,"groupnamefield":<String_value>,"audience":<String_value>,"metadataurl":<String_value>,"metadatarefreshinterval":<Double_value>,"storesamlresponse":<String_value>}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###unset



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>action=unset</b>
<b>HTTP Method:</b>POST
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Content-Type:application/json

<b>Request Payload: </b>```{"authenticationsamlaction":{<b>"name":<String_value>,</b>"samlidpcertname":true,"samlsigningcertname":true,"samlredirecturl":true,"samlacsindex":true,"samluserfield":true,"samlrejectunsignedassertion":true,"samlissuername":true,"samltwofactor":true,"defaultauthenticationgroup":true,"attribute1":true,"attribute2":true,"attribute3":true,"attribute4":true,"attribute5":true,"attribute6":true,"attribute7":true,"attribute8":true,"attribute9":true,"attribute10":true,"attribute11":true,"attribute12":true,"attribute13":true,"attribute14":true,"attribute15":true,"attribute16":true,"signaturealg":true,"digestmethod":true,"requestedauthncontext":true,"authnctxclassref":true,"samlbinding":true,"attributeconsumingserviceindex":true,"sendthumbprint":true,"enforceusername":true,"logouturl":true,"artifactresolutionserviceurl":true,"skewtime":true,"logoutbinding":true,"forceauthn":true,"groupnamefield":true,"audience":true,"metadataurl":true,"metadatarefreshinterval":true,"storesamlresponse":true}}```
<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error


###get (all)



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>filter</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>filter=property-name1:property-val1,property-name2:property-val2</b>
Use this query-parameter to get the filtered set of authenticationsamlaction resources configured on NetScaler.Filtering can be done on any of the properties of the resource.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).


<b>pagination</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>pagesize=#no;pageno=#no</b>
Use this query-parameter to get the authenticationsamlaction resources in chunks.



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationsamlaction": [ {"name":<String_value>,"samlidpcertname":<String_value>,"samlsigningcertname":<String_value>,"samlredirecturl":<String_value>,"samlacsindex":<Double_value>,"samluserfield":<String_value>,"samlrejectunsignedassertion":<String_value>,"samlissuername":<String_value>,"samltwofactor":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"requestedauthncontext":<String_value>,"authnctxclassref":<String[]_value>,"samlbinding":<String_value>,"attributeconsumingserviceindex":<Double_value>,"sendthumbprint":<String_value>,"enforceusername":<String_value>,"logouturl":<String_value>,"artifactresolutionserviceurl":<String_value>,"skewtime":<Double_value>,"logoutbinding":<String_value>,"forceauthn":<String_value>,"groupnamefield":<String_value>,"audience":<String_value>,"metadataurl":<String_value>,"metadatarefreshinterval":<Double_value>,"metadataimportstatus":<String_value>,"storesamlresponse":<String_value>}]}```



###get



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;
<b>Query-parameters:</b>
<b>attrs</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;?<b>attrs=property-name1,property-name2</b>
Use this query parameter to specify the resource details that you want to retrieve.


<b>view</b>
http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction/name_value&lt;String&gt;?<b>view=summary</b>
<b>Note:</b>By default, the retrieved results are displayed in detail view (?view=detail).



<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationsamlaction": [ {"name":<String_value>,"samlidpcertname":<String_value>,"samlsigningcertname":<String_value>,"samlredirecturl":<String_value>,"samlacsindex":<Double_value>,"samluserfield":<String_value>,"samlrejectunsignedassertion":<String_value>,"samlissuername":<String_value>,"samltwofactor":<String_value>,"defaultauthenticationgroup":<String_value>,"attribute1":<String_value>,"attribute2":<String_value>,"attribute3":<String_value>,"attribute4":<String_value>,"attribute5":<String_value>,"attribute6":<String_value>,"attribute7":<String_value>,"attribute8":<String_value>,"attribute9":<String_value>,"attribute10":<String_value>,"attribute11":<String_value>,"attribute12":<String_value>,"attribute13":<String_value>,"attribute14":<String_value>,"attribute15":<String_value>,"attribute16":<String_value>,"signaturealg":<String_value>,"digestmethod":<String_value>,"requestedauthncontext":<String_value>,"authnctxclassref":<String[]_value>,"samlbinding":<String_value>,"attributeconsumingserviceindex":<Double_value>,"sendthumbprint":<String_value>,"enforceusername":<String_value>,"logouturl":<String_value>,"artifactresolutionserviceurl":<String_value>,"skewtime":<Double_value>,"logoutbinding":<String_value>,"forceauthn":<String_value>,"groupnamefield":<String_value>,"audience":<String_value>,"metadataurl":<String_value>,"metadatarefreshinterval":<Double_value>,"metadataimportstatus":<String_value>,"storesamlresponse":<String_value>}]}```



###count



<b>URL:</b>http://&lt;netscaler-ip-address&gt;/nitro/v1/config/authenticationsamlaction?<b>count=yes</b>
<b>HTTP Method:</b>GET
<b>Request Headers:</b>

Cookie:NITRO_AUTH_TOKEN=&lt;tokenvalue&gt;Accept:application/json

<b>Response:</b>
HTTP Status Code on Success: 200 OKHTTP Status Code on Failure: 4xx &lt;string&gt; (for general HTTP errors) or 5xx &lt;string&gt; (for NetScaler-specific errors). The response payload provides details of the error<b>Response Headers:</b>

Content-Type:application/json

<b>Response Payload: </b>```{ "authenticationsamlaction": [ { "__count": "#no"} ] }```



