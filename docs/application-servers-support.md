[//]: # (Source: https://www.jetbrains.com/help/idea/application-servers-support.html)
[//]: # (Downloaded: 2025-12-17 19:18:27)

# Application servers

IntelliJ IDEA with the Ultimate subscription provides integration with various application servers, enabling you to start and stop local servers, connect to running remote servers, and deploy your [artifacts](working-with-artifacts.html) on those servers. You can also debug your application right from the IDE.

By default, plugins that add support for the following application servers are bundled and enabled in IntelliJ IDEA with the Ultimate subscription:

  * [Tomcat](https://tomcat.apache.org/)

  * [TomEE](https://tomee.apache.org/)

  * [WildFly](https://wildfly.org/)




You can install additional plugins with support for other application servers, for example:

[GlassFish](https://projects.eclipse.org/projects/ee4j.glassfish)| [plugin](https://plugins.jetbrains.com/plugin/20220-glassfish)  
---|---  
[Jetty](https://www.eclipse.org/jetty/)| [plugin](https://plugins.jetbrains.com/plugin/18721-jetty)  
[WebLogic](https://www.oracle.com/ru/java/weblogic/)| [plugin](https://plugins.jetbrains.com/plugin/18722-weblogic)  
[WebSphere](https://www.ibm.com/cloud/websphere-application-server)| [plugin](https://plugins.jetbrains.com/plugin/18723-websphere)  
[Resin](https://caucho.com/products/resin)| [plugin](https://plugins.jetbrains.com/plugin/14598-resin)  
[Virgo](https://www.eclipse.org/virgo/) (previously dm Server)| [plugin](https://plugins.jetbrains.com/plugin/4542-virgo-dmserver)  
  
To get started with application servers in IntelliJ IDEA, refer to [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html).

### Enable the Jakarta EE: Application Servers plugin

This functionality relies on the Jakarta EE: Application Servers plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Jakarta EE: Application Servers plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Jakarta EE: Application Servers plugin, and select the checkbox next to the plugin name.




### Get started with an application server

  1. Let IntelliJ IDEA know where the server is installed.

For more information, refer to [Integration with application servers](configuring-and-managing-application-server-integration.html).

  2. Create and launch an application server run configuration.

For more information, refer to [Application server run configurations](creating-run-debug-configuration-for-application-server.html).




27 November 2025

[Flyway](flyway.html)[Integration with application servers](configuring-and-managing-application-server-integration.html)
