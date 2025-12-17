[//]: # (Source: https://www.jetbrains.com/help/idea/web-services-settings.html)
[//]: # (Downloaded: 2025-12-17 20:06:54)

# Web Services

Use this dialog to specify the default server name and port for generating URL addresses of Web services, as well as the paths to installation directories of Web service engines that cannot be enabled directly via dedicated facets.

Item| Description  
---|---  
External engines| In this section, specify the paths to the installation directories of external Web service engines. Enter the path manually, or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the path in the dialog that opens. The following external engines are supported:

  * [GlassFish](https://glassfish.java.net/)/[JAX-WS 2.2 RI](https://jax-ws.java.net/2.2/)/[Metro 1.X](https://metro.java.net/)/[JWSDP 2.2](https://java.net/projects/jax-ws/lists/users/archive/2007-05/message/6)
  * [Apache Axis 2](http://axis.apache.org/axis2/java/core/)
  * [CXF](http://cxf.apache.org/)
  * [JBoss](http://jbossws.jboss.org/docs/)
  * [XMLBeans](http://xmlbeans.apache.org/)

  
Server name| In this field, specify the default name of the server to be used in URL addresses. IntelliJ IDEA suggests localhost.  
Server port| In this field, specify the default port number to be used in URL addresses. IntelliJ IDEA suggests 8080.  
Prefix path for web services URL| In this field, specify the default prefix to be used in URL addresses of Web services. IntelliJ IDEA suggests /services.  
Maximum VM heap size when launching tools (Mb)| In this field, specify the default maximum heap size in Mbs that will be used when a Web service is launched.  
  
28 June 2024

[XPath Viewer](xpath-viewer.html)[Advanced Settings](advanced-settings.html)
