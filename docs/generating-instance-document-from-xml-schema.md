[//]: # (Source: https://www.jetbrains.com/help/idea/generating-instance-document-from-xml-schema.html)
[//]: # (Downloaded: 2025-12-17 19:27:43)

# Generating instance documents from XML schemas

  1. With the desired Schema .xsd file opened in the active editor tab, choose Tools | XML Actions | Generate XML Document from XSD Schema from the main menu. The [Generate Instance Document from Schema](generate-instance-document-from-schema-dialog.html) dialog opens.

  2. In the Schema Path field, specify the location of the Schema to base the XML document generation on. By default, the field shows the full path to the current file. Accept this suggestion or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired file in the dialog that opens.

  3. In the Instance Document Name field, specify the name of the output file to place the generated XML in. 

IntelliJ IDEA suggests the name of the source XML document with the xml extension. If you type another name, make sure the extension is correct.

  4. Specify the location of the generated document. By default, it will be placed in the same directory as the source Schema file. To specify another location, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired path in the dialog that opens.

  5. From the Element Name list, select the local name of the global element to be used as the root of the generated XML document.

  6. Specify whether to take restriction and uniqueness particles into consideration by selecting the corresponding checkboxes.




28 June 2024

[Generating DTD](generating-dtd.html)[Generating XML schemas from instance documents](generating-xml-schema-from-instance-document.html)
