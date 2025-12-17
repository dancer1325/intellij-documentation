[//]: # (Source: https://www.jetbrains.com/help/idea/settings-languages-default-xml-schemas.html)
[//]: # (Downloaded: 2025-12-17 20:01:13)

## Default HTML Language Level

Normally, an HTML or an XHTML file has the `<!DOCTYPE>` declaration which states the language level of the used in the source code from the file. This language level is used as a standard against which the contents of the file are validated. If an HTML or an XHTML file does not have a `<!DOCTYPE>` declaration, the contents of the file will be validated against the default standard (schema). In the Default HTML Language Level area, choose the default schema to validate HTML and XHTML files without a `<!DOCTYPE>` declaration. The available options are:

  * HTML 4 or HTML 5: select one of these options to have files treated as HTML 4 or HTML 5 and validated against one of these standards.

  * Other doctype: select this option to have HTML files by default validated against a custom DTD or schema and specify the URL of the DTD or schema to be used.

Note that code completion is available in this field: press `Ctrl+Space` to see the list of suggested URLs.

![Default HTML language level dialog](https://resources.jetbrains.com/help/img/idea/2025.3/defaultHtmlLangLevel.png)


