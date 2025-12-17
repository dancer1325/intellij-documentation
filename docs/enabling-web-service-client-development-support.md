[//]: # (Source: https://www.jetbrains.com/help/idea/enabling-web-service-client-development-support.html)
[//]: # (Downloaded: 2025-12-17 19:25:48)

# Enable web service client development support

To develop a web service client in IntelliJ IDEA, configure the corresponding module and supply all required libraries. The instructions on this page are applicable for developing a web service client of the following types:

  * GlassFish/JAXWS2.X RI/Netro 1.X/JWSDP2.0

  * Apache Axis

  * RESTful Web Service




### Install the Jakarta EE: Web Services (JAX-WS) plugin

This functionality relies on the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584) plugin, which you need to install and enable. 

The Jakarta EE: Web Services (JAX-WS) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Jakarta EE: Web Services (JAX-WS) plugin, and click Install (restart the IDE if prompted).




### Create a project for a web service client application

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the Web application project template.

  4. Select the Create Git repository option to place the new project under version control.

  5. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

![Creating new Jakarta EE project](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_1.png)
  6. On the next step of the wizard, select the Jakarta EE version to be supported.

From the Dependencies list, select XML Web Services.

![Add Web Services dependency to new project](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_2_web_services.png)
  7. Click Create.




### Enable web service client support for an existing project

  1. Open the build file in the editor (pom.xml or build.gradle depending on the build tool that you use in your project).

  2. Add the following dependency, but make sure to change the version according to your project's requirements:

Jakarta EE
    

<dependency> <groupId>jakarta.xml.ws</groupId> <artifactId>jakarta.xml.ws-api</artifactId> <version>3.0.1</version> <scope>provided</scope> </dependency>

Java EE
    

<dependency> <groupId>javax.xml.ws</groupId> <artifactId>jaxws-api</artifactId> <version>2.3.1</version> <scope>provided</scope> </dependency> <dependency> <groupId>javax.jws</groupId> <artifactId>javax.jws-api</artifactId> <version>1.1</version> <scope>provided</scope> </dependency>

Jakarta EE
    

compileOnly('jakarta.xml.ws:jakarta.xml.ws-api:3.0.1') 

Java EE
    

compileOnly('javax.xml.ws:jaxws-api:2.3.1') compileOnly('javax.jws:javax.jws-api:1.1') 

  3. Press `Ctrl+Shift+O` to import the changes.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

### Enable support for any web service engine

IntelliJ IDEA uses facets to enable support for the most common web service engines. However, you can enable any web service engine or implementation version, even if it is not supported by IntelliJ IDEA facets.

  1. Download the desired web service engine implementation.

  2. Press `Ctrl+Alt+S` to open settings and then select Tools | Web Services. Specify the path to the external web service engine, desired server name and port, and other options For more information, refer to [Web Services](web-services-settings.html).




17 June 2024

[Web service clients](web-service-clients.html)[Monitor SOAP messages](monitoring-soap-messages.html)
