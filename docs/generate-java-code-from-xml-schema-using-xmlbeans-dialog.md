[//]: # (Source: https://www.jetbrains.com/help/idea/generate-java-code-from-xml-schema-using-xmlbeans-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:29)

# Generate Java Code from XML Schema using XmlBeans Dialog

Use this dialog to configure generation of Java code stubs based on an XML Schema via the [XmlBeans](http://xmlbeans.apache.org/) data binder.

  * This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

  * The menu item and the dialog are available when an XML Schema is opened in the active editor tab.




Item| Description  
---|---  
Schema path| In this field, specify the file to be used as the generation basis. By default, the field shows the full path to the current file. To use another Schema, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and choose the desired file in the Select XML Schema / Wsdl File for generation dialog, that opens.  
Output path| Use this field to specify the name of the jar to place the generated and complied Java code in. By default, IntelliJ IDEA suggests creating a new types.jar. To overwrite an existing jar, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and choose the desired jar in the dialog that opens.  
Add necessary libraries in order for generated code compile and work| Select this checkbox to have additional XmlBeans libraries automatically added to the classpath of the module where the generated source code will be placed.These are libraries the generated stubs depend on.  
Status| View the information in this read-only field to track and improve discrepancies when configuring the generation procedure.  
  
08 October 2024

[Generate XML Schema From Java Using JAXB Dialog](generate-xml-schema-from-java-using-jaxb-dialog.html)[Generate Instance Document from Schema Dialog](generate-instance-document-from-schema-dialog.html)
