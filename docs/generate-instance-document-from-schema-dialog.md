[//]: # (Source: https://www.jetbrains.com/help/idea/generate-instance-document-from-schema-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:27)

# Generate Instance Document from Schema Dialog

In this dialog, specify the options for generating an XML file based on the XSD (XML Schema Definition) [Schema](https://www.w3schools.com/xml/schema_intro.asp) that describes its structure.

  * This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

  * The menu item and the dialog are available when an XML Schema is opened in the active editor tab.




Item| Description  
---|---  
Schema path| In this field, specify the location of the .xsd Schema file to be used as the basis for XML document generation.By default, the field shows the full path to the current file. To use another Schema, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired file in the dialog that opens.  
Instance document name| In this field, specify the name of the output XML file to be generated. By default, the generated XML file will inherit the name of the source Schema and will have the xml extension. If you type another name for the document to be generated, make sure the extension is correct.The default location for the generated document is the directory where the source .xsd Schema file resides. To specify another location, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired path in the dialog that opens.  
Element name| In this list, specify the local name of the global element to be used as the root of the generated document.  
Enable restriction check| Select this checkbox to have IntelliJ IDEA take restriction particles into consideration (if the specified Schema uses any).  
Enable unique check| Select this checkbox to have IntelliJ IDEA take uniqueness particles into consideration (if the specified Schema uses any).  
Status| View the information in this read-only field to track and improve discrepancies when configuring the generation procedure.  
  
28 June 2024

[Generate Java Code from XML Schema using XmlBeans Dialog](generate-java-code-from-xml-schema-using-xmlbeans-dialog.html)[Generate Schema from Instance Document Dialog](generate-schema-from-instance-document-dialog.html)
