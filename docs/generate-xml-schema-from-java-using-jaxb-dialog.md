[//]: # (Source: https://www.jetbrains.com/help/idea/generate-xml-schema-from-java-using-jaxb-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:38)

# Generate XML Schema From Java Using JAXB Dialog

Use this dialog to configure XML Schema generation based on the existing Java code.

  * This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

  * The menu item and the dialog are available when a Java class is opened in the active editor tab.




Item| Description  
---|---  
Class Name| This read-only field shows the name of the class to base the XML Schema generation on.  
Include parameter and return type of the following methods| 

  * When the checkbox is cleared, the parameter and return type of all the class methods will be reflected in the generated Schema.
  * Select this checkbox to have a list of the class methods displayed and specify the methods to be involved in Schema generation.

Selecting this checkbox enables the Parameter / return type of the following method and the Add to JAXB generation controls.  
Parameter / return type of the following method| This read-only field shows a list of all the methods of the current class.  
Add to JAXB generation| Select this check to have the parameter/return type of the corresponding method involved in Schema generation.  
Status| View the information in this read-only field to track and improve discrepancies when configuring the Schema generation procedure.  
  
08 October 2024

[Generate Java from XML Schema using JAXB Dialog](generate-java-from-xml-schema-using-jaxb-dialog.html)[Generate Java Code from XML Schema using XmlBeans Dialog](generate-java-code-from-xml-schema-using-xmlbeans-dialog.html)
