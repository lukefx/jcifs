Fork of jCifs library: http://jcifs.samba.org

Addiction:

Possibility to blacklist some IPs to bypass NTLM:

Example of web.xml

````xml
<filter>
 <filter-name>NtlmHttpFilter</filter-name>
	<filter-class>jcifs.http.NtlmHttpFilter</filter-class>
	<init-param>
		<param-name>jcifs.smb.client.domain</param-name>
		<param-value>DOMAIN</param-value>
	</init-param>
	<init-param>
		<param-name>jcifs.http.domainController</param-name>
		<param-value>192.168.1.2</param-value>
	</init-param>
	<init-param>
		<param-name>jcifs.smb.blacklist</param-name>
		<param-value>10.33.0.0,10.8.0.0,10.120.0.0</param-value>
	</init-param>
</filter>

<filter-mapping>
	<filter-name>NtlmHttpFilter</filter-name>
	<url-pattern>/*</url-pattern>
</filter-mapping>
````
