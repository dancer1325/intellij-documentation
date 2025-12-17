[//]: # (Source: https://www.jetbrains.com/help/idea/preparing-to-develop-a-web-service.html)
[//]: # (Downloaded: 2025-12-17 19:34:09)

# Enable web service development

To develop a web service in IntelliJ IDEA, configure the corresponding module and provide all the required libraries and servlet references. This page describes how to meet these requirements.

### Install the Jakarta EE: WebServices (JAX-WS) plugin

This functionality relies on the [Jakarta EE: WebServices (JAX-WS)](https://plugins.jetbrains.com/plugin/18584) plugin, which you need to install and enable. 

The Jakarta EE: WebServices (JAX-WS) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Jakarta EE: WebServices (JAX-WS) plugin, and click Install (restart the IDE if prompted).




These instructions apply to the following types of web services:

  * GlassFish

  * JAXWS2.X RI

  * Netro 1.X

  * JWSDP2.0

  * Apache Axis




### Create a new project with web services

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the Web application project template.

  4. Select the Create Git repository option to place the new project under version control.

  5. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  6. On the next step of the wizard, select the Java EE version to be supported.

  7. From the Dependencies list, select Web Profile.

  8. Click Create.




### Add web services to an existing module

This information is valid for projects that are built with the native IntelliJ IDEA builder. If you're using a build tool, such as [Maven](maven-support.html) or [Gradle](gradle.html), make all changes using the build file.

  1. In the Project tool window `Alt+1`, select the necessary module.

  2. Press `Ctrl+Shift+A` and type `Add Framework Support`.

Once the action is found, click it to open the Add Framework Support dialog.

  3. In the dialog that opens, select Web Application and select a version of the Servlet specification.

  4. If you want the deployment descriptor web.xml file to be created, select the Create web.xml checkbox.

Click OK.


![Adding support for a framework](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_framework_support.png)

### Add the necessary libraries

This approach is applicable if the necessary libraries have been previously downloaded.

  1. In the main menu, go to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. From the panel on the left, select Modules, select the required module and open the Dependencies tab on the right.

  3. To enable Web development, click the Add button and select JARs or Directories... from the context menu. In the dialog that opens, select the javaee.jar library and click OK.

  4. Click the Add button again, then select JARs or Directories... from the context menu. In the dialog that opens, select the javaee.jar library and the required web service-specific libraries.

     * The location of the javaee.jar library is defined during the installation of IntelliJ IDEA.

     * The location of the Web-service specific libraries is defined during their download.

  5. Click OK when ready.




11 October 2024

[Web services](web-services.html)[Expose code as Web service](exposing-code-as-web-service.html)
