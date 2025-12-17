[//]: # (Source: https://www.jetbrains.com/help/idea/referencing-xml-schemas-and-dtds.html)
[//]: # (Downloaded: 2025-12-17 19:57:01)

# Referencing XML schemas and DTDs

Your XML file may reference an external XML schema (XSD) or DTD file, for example:

<root xmlns="http://www.example.org" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.example.org/xsds/example.xsd">

or

<!DOCTYPE root SYSTEM "http://www.example.org/dtds/example.dtd">

If the referenced URL or the namespace URI is not recognized, it's marked as an error. To solve the problem:

  1. Place the caret at the referenced URL and press `Alt+Enter`. 

![Referencing an unfamiliar URL](https://resources.jetbrains.com/help/img/idea/2025.3/reference-nonexist-url-xml.png)
  2. From the list of suggested options, select one of the following:

     * Fetch external resource. IntelliJ IDEA downloads the referenced file and associates it with the URL (or the namespace URI). The error highlighting disappears. The XML file is validated according to the downloaded schema or DTD. (The associations of the URLs and the namespace URIs with the schema and DTD files are shown on the [Schemas and DTDs page](settings-languages-schemas-and-dtds.html) in the Settings dialog.)

     * Manually set up external resource. Use this option when you already have an appropriate schema or DTD file available locally. The Map External Resource dialog will open, and you'll be able to select the file for the specified URL or namespace URI (for example, `http://www.example.org/xsds/example.xsd` or `http://www.example.org`). The result of the operation is the same as in the case of fetching the resource.

     * Ignore external resource. The URL or the namespace URI is added to the list of Ignored Schemas and DTDs. (This list is shown on the [Schemas and DTDs page](settings-languages-schemas-and-dtds.html) in the Settings dialog.) The error highlighting disappears. IntelliJ IDEA won't validate the XML file, however, it will check if the XML file is well-formed.

     * Add Xsi Schema Location for External Resource. This intention action lets you complete your root XML elements. If the namespace is already specified, IntelliJ IDEA can add a couple of missing attributes.




For example, if you have a fragment like this:

<root xmlns="http://www.example.org">

and you invoke the Add Xsi Schema Location for External Resource intention action on the value of the `xmlns` attribute, the result will be:

<root xmlns="http://www.example.org" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.example.org">

At this step, you can add the schema URL, and then map the URL (or the namespace URI) onto an appropriate schema file, or add the URL (or the URI) to the list of Ignored Schemas and DTDs.

30 July 2024

[Generating XML schemas from instance documents](generating-xml-schema-from-instance-document.html)[XML-Java Binding](xml-java-binding.html)
