[//]: # (Source: https://www.jetbrains.com/help/idea/generate-schema-from-instance-document-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:32)

# Generate Schema from Instance Document Dialog

In this dialog, specify the options for generating an XSD (XML Schema Definition) [Schema](https://www.w3schools.com/xml/schema_intro.asp) that describes the structure of the desired XML file.

  * This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

  * The menu item and the dialog are available when an XML document is opened in the active editor tab.




Item| Description  
---|---  
Instance document path| In this field, specify the full path to the XML document to be used as the basis for Schema generation.By default, the field shows the full path to the current file. To use another XML document, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired file in the dialog that opens.  
Result Schema file name| In this field, specify the name of the output file for the Schema to be generated. By default, the generated XSD Schema file will inherit the name of the instance document used and will have the XSD extension. If you type another name for the Schema to be generated, make sure the extension is correct.The default location for the generated Schema is the directory where the source XML instance document resides. To specify another location, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired path in the dialog that opens.  
Design type| Specify how to declare elements and complex types. The available options are:

  * Local elements / global complex types
  * Local elements / types
  * Global elements / local types

  
Detect simple content types| From this list, choose the type to render leaf text, which should be distinguished from the text used. The available options are:

  * String
  * Smart

  
Detect enumeration limit| In this field, type the number of occurrences to cause the Schema enumeration appearance. To suppress Schema enumeration, specify 0.  
  
28 June 2024

[Generate Instance Document from Schema Dialog](generate-instance-document-from-schema-dialog.html)[Create a new JavaFX project](javafx.html)
