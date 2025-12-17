[//]: # (Source: https://www.jetbrains.com/help/idea/validating-web-content-files.html)
[//]: # (Downloaded: 2025-12-17 20:06:01)

# Validating web content files

IntelliJ IDEA performs two different [validity](https://www.w3schools.com/xml/xml_validator.asp) checks:

  * On-the-fly validation is available for all Web content files and is performed as you edit the file. IntelliJ IDEA detects various violations of syntax requirements, such as unclosed tags, wrong end-tag name, duplicate tags, unresolved links, and so on. All encountered errors are highlighted in the editor.

However, this form of code validation is rather _soft_ , that is, not all requirements are taken into account.

  * Full validation involves structure validation in addition to syntax check. Full validation is available for files that are associated with an [XSD (XML Schema Definition) Schema](http://www.w3.org/XML/Schema) or contain a [Data Type Definition (DTD)](https://www.w3schools.com/xml/xml_dtd_intro.asp). IntelliJ IDEA checks whether the structure of your XML file complies with the structure defined in the corresponding DTD or Schema.

The results of full validation are provided as a Message View.




### Configure the default HTML language level

Normally, an HTML or an XHTML file has the `<!DOCTYPE>` declaration which states the language level of the used in the source code from the file. This language level is used as a standard against which the contents of the file are validated. If an HTML or an XHTML file does not have a `<!DOCTYPE>` declaration, the contents of the file will be validated against the default standard (schema).

  1. Press `Ctrl+Alt+S` to open settings and then select Languages & Frameworks | Schemas and DTDs | Default XML Schemas.

  2. In the Default HTML Language Level area, choose the default schema to validate HTML and XHTML files without a `<!DOCTYPE>` declaration. The available options are:

     * HTML 4 or HTML 5: select one of these options to have files treated as HTML 4 or HTML 5 and validated against one of these standards.

     * Other doctype: select this option to have HTML files by default validated against a custom DTD or schema and specify the URL of the DTD or schema to be used.

Note that code completion is available in this field: press `Ctrl+Space` to see the list of suggested URLs.

![Default HTML language level dialog](https://resources.jetbrains.com/help/img/idea/2025.3/defaultHtmlLangLevel.png)
  3. Choose the [XSD (XML Schema Definition) Schema](http://www.w3.org/XML/Schema) to validate XML files. The available options are:

     * XML Schema 1.1: for more information, refer to [W3C XML Schema Definition Language (XSD) 1.1 Part 1: Structures](http://www.w3.org/TR/xmlschema11-1/) and [W3C XML Schema Definition Language (XSD) 1.1 Part 2: Datatypes](http://www.w3.org/TR/xmlschema11-2/).

     * XML Schema 1.0: for more information, refer to [XML Schema Part 1: Structures Second Edition](http://www.w3.org/TR/xmlschema-1/) and [XML Schema Part 2: Datatypes Second Edition](http://www.w3.org/TR/xmlschema-2/).




### Configure the default schema for validating XML files

  1. Press `Ctrl+Alt+S` to open settings and then select Languages & Frameworks | Schemas and DTDs | Default XML Schemas.

  2. Under XML Schema version, choose the [XSD (XML Schema Definition) Schema](http://www.w3.org/XML/Schema) to validate XML files. The available options are:

     * XML Schema 1.1: for more information, refer to [W3C XML Schema Definition Language (XSD) 1.1 Part 1: Structures](http://www.w3.org/TR/xmlschema11-1/) and [W3C XML Schema Definition Language (XSD) 1.1 Part 2: Datatypes](http://www.w3.org/TR/xmlschema11-2/).

     * XML Schema 1.0: for more information, refer to [XML Schema Part 1: Structures Second Edition](http://www.w3.org/TR/xmlschema-1/) and [XML Schema Part 2: Datatypes Second Edition](http://www.w3.org/TR/xmlschema-2/).




### Run full validation on an XML file

  1. Open the desired XML file in the editor, or just select it in the [Project](project-tool-window.html) tool window.

  2. Right-click any code element in the editor and from the context menu, choose Validate.




08 October 2024

[XML](working-with-xml.html)[Generating DTD](generating-dtd.html)
