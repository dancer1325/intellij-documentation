[//]: # (Source: https://www.jetbrains.com/help/idea/generate-java-from-xml-schema-using-jaxb-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:31)

# Generate Java from XML Schema using JAXB Dialog

Use this dialog to configure generation of Java code stubs based on an XML Schema via the [JAXB](https://javaee.github.io/jaxb-v2/) data binder.

  * This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

  * The menu item and the dialog are available when an XML Schema is opened in the active editor tab.




Item| Description  
---|---  
Schema/WSDL/DTD path| In this field, specify the file to be used as the generation basis. By default, the field shows the full path to the current file. To use another Schema, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and choose the desired file in the Select XML Schema File for JAXB Generation dialog, that opens.  
Output path| Select the module source directory to place the generated Java code stubs in.  
Package prefix| Use this list to specify the package to place the generated Java files in.  
Generate package level annotations| Do one of the following: 

  * Select this checkbox to have a package-info.java with annotations generated.
  * Clear this checkbox to have annotations internalized into other generated classes.

  
Mark generated code with 'generated' annotation| Select this checkbox to have generated code supplied with the `javax.annotation.Generated` annotations.  
Make generated file read-only| Select this checkbox to force the XJC binding compiler to mark the generated Java source code as read-only.  
Add necessary libraries in order for generated code compile and work| Select this checkbox to have additional JAXB client libraries automatically added to the classpath of the module where the generated source code will be placed.These are the libraries the generated code stubs depend on.  
Do not generate header| Select this checkbox to pass `no-header` parameter to the corresponding command.  
Add external binding file/dir| Select this checkbox to specify an external binding file or an output directory where the generated file is located.  
Status| View the information in this read-only field to track and improve discrepancies when configuring the generation procedure.  
  
13 November 2025

[XML-Java Binding Reference](xml-java-binding-reference.html)[Generate XML Schema From Java Using JAXB Dialog](generate-xml-schema-from-java-using-jaxb-dialog.html)
