[//]: # (Source: https://www.jetbrains.com/help/idea/generating-java-code-from-xml-schema.html)
[//]: # (Downloaded: 2025-12-17 19:27:45)

# Generate Java Code from XML Schema

This topic describes how to get a Java representation of an [XML Schema](https://www.w3schools.com/xml/schema_intro.asp), which involves mapping the elements of the XML Schema to members of a Java class. With IntelliJ IDEA, this transformation can be done using one of the following data binders:

  * [JAXB](#jaxb) generates classes and groups them in Java packages. A package consists of a Java class name and an `ObjectFactory` class. The latter is a factory that is used to return instances of a bound Java class.

  * [XMLBeans](#xmlbeans) converts an XML Schema into a Java class, compiles it, and places in the specified output jar file.




### Install the Jakarta EE: Web Services (JAX-WS) plugin

This functionality relies on the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws) plugin, which you need to install and enable. 

The Jakarta EE: Web Services (JAX-WS) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Jakarta EE: Web Services (JAX-WS) plugin, and click Install (restart the IDE if prompted).




### Generate a Java class from an XML Schema using JAXB

  1. In the active editor tab, open a Schema .xsd file or an XML document, which contains the Schema you need.

  2. In the main menu, go to Tools | XML Actions | Generate Java Code From XML Schema Using JAXB.

  3. In the [Generate Java from Xml Schema using JAXB](generate-java-from-xml-schema-using-jaxb-dialog.html) dialog, configure the generation procedure:

     * In the Schema/DTD/WSDL Path list, specify the file to be used as the basis for code generation. By default, the field shows the full path to the current file. Accept this suggestion or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select a file in the Select XML Schema File for JAXB Generation that opens.

     * From the Output Path list, select the module source directory to place the generated Java class in.

     * In the Package Prefix list, specify the package to include the generated stubs in.

     * Using the checkboxes, configure additional options, such as generating annotation, setting the read-only status, downloading and installing additional libraries.




### Generate and compile a Java class from an XML Schema using XMLBeans

  1. In the active editor tab, open a Schema .xsd file or an XML document, which contains the Schema you need.

  2. In the main menu, go to Tools | XML Actions | Generate Java Code From XML Schema Using XmlBeans.

  3. In the [Generate Java Code From XML Schema using XMLBeans](generate-java-code-from-xml-schema-using-xmlbeans-dialog.html) dialog, configure the generation procedure:

     * In the Schema Path list, specify the file to be used as the basis for code generation. By default, the field shows the full path to the current file. Accept this suggestion or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select a file in the Select XML Schema /WSDL File for Generation dialog that opens.

     * In the Output Path list, specify the name of the jar file to place the generated and compiled Java code in. By default, IntelliJ IDEA suggests creating a new file types.jar. To overwrite an existing file, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and choose the desired file in the Select XML Schema / Wsdl File for generation dialog that opens.

     * To have missing libraries downloaded and installed automatically, select the Add necessary libraries in order for generated code compile and work checkbox.




18 July 2025

[XML-Java Binding](xml-java-binding.html)[Generate an XML Schema from Java Code](generating-xml-schema-from-java-code.html)
