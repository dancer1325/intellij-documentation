[//]: # (Source: https://www.jetbrains.com/help/idea/generating-xml-schema-from-instance-document.html)
[//]: # (Downloaded: 2025-12-17 19:27:47)

# Generating XML schemas from instance documents

To suppress Schema enumeration, specify 0.

An [XSD (XML Schema Definition)](https://www.w3schools.com/xml/schema_intro.asp) is required for running [structure validation checks](validating-web-content-files.html) on a Web content file. IntelliJ IDEA can scan any XML file for the existing elements and attributes and generate a Schema for it.

### Generate a Schema based on an XML document

  1. With the desired XML document opened in the active editor tab, go to Tools | XML Actions | Generate XSD Schema from XML File in the main menu. The [Generate Schema From Instance Document](generate-schema-from-instance-document-dialog.html) dialog opens.

  2. In the Instance Document Path field, specify the location of the file to be used as the basis for Schema generation. By default, the field shows the full path to the current file. Accept this suggestion or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired file in the dialog that opens.

  3. In the Result Schema File Name field, specify the name of the output file to place the generated Schema in. 

IntelliJ IDEA suggests the name of the source XML document with the .xsd extension. If you type another name, make sure the extension is correct.

  4. Specify the location of the generated Schema. By default, the generated Schema file will be placed in the same directory as the source XML instance document. To specify another location, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired path in the dialog that opens.

  5. From the Design Type list, select the way to declare elements and complex types.

  6. From the Detect Simple Content Type list, select the type to use for leaf text.

  7. In the Detect Enumerations Limit field, type the number of occurrences to cause appearance of the Schema enumeration.




28 June 2024

[Generating instance documents from XML schemas](generating-instance-document-from-xml-schema.html)[Referencing XML schemas and DTDs](referencing-xml-schemas-and-dtds.html)
