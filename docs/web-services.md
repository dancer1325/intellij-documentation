[//]: # (Source: https://www.jetbrains.com/help/idea/web-services.html)
[//]: # (Downloaded: 2025-12-17 20:06:56)

# Web services

IntelliJ IDEA supports the development, packaging, and deployment of web services according to the following standards:

  * [Java API for XML-Based Web Services (JAX-WS)](https://jcp.org/en/jsr/detail?id=224)

  * [JAX-RS: The JavaTM API for RESTful Web Services](http://jcp.org/en/jsr/detail?id=311)

  * [Apache Axis](http://axis.apache.org/axis/)




### Install the Jakarta EE: WebServices (JAX-WS) plugin

This functionality relies on the [Jakarta EE: WebServices (JAX-WS)](https://plugins.jetbrains.com/plugin/18584) plugin, which you need to install and enable. 

The Jakarta EE: WebServices (JAX-WS) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Jakarta EE: WebServices (JAX-WS) plugin, and click Install (restart the IDE if prompted).




IntelliJ IDEA provides the following development and packaging features:

  * Setting up the relevant module structure and downloading all the necessary resources based on the dedicated web services facet you specify.

  * Generating the necessary deployment descriptors, mapping and manifest files.

  * Packaging the web service files, with the EAR file structure following the rules defined by the Enterprise Web Services 1.1 specification.




### Develop a web service with IntelliJ IDEA

  1. In a Java module, [enable support](preparing-to-develop-a-web-service.html) of the relevant web service.

  2. Populate the module with the necessary classes and methods.

  3. [Compile](compiling-applications.html) the developed classes and [expose](exposing-code-as-web-service.html) them as a web service.

To develop the client side of the web service before deploying the web service itself, generate a [WSDL document](generating-wsdl-document-from-java-code.html).

  4. Configure the [artifacts](working-with-artifacts.html) to deploy.

Do not forget to include the Web facet resources in the artifact.

  5. [Create a run configuration](run-debug-configuration.html#createExplicitly) specifying the list of artifacts to deploy, each with the corresponding application context.

  6. Run the application.

  7. [View and manage deployed web services](managing-deployed-web-services.html) in the [Deployment console](deployment-console.html) of the [Run](run-tool-window.html) tool window.




17 June 2024

[Generate Client-side XML-Java binding](generating-client-side-xml-java-binding.html)[Enable web service development](preparing-to-develop-a-web-service.html)
