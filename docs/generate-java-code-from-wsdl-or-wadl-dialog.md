[//]: # (Source: https://www.jetbrains.com/help/idea/generate-java-code-from-wsdl-or-wadl-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:28)

# Generate Java Code from WSDL dialog

This functionality is available if you have installed and enabled the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws-) plugin.

The dialog opens after you create a Java module and [enable Web services client development](enabling-web-service-client-development-support.html) in it. To access the dialog at any time during development, select the desired client module in the Project view and choose Tools | XML WebServices and WSDL | Generate Java Code From WSDL from the main menu.

Use the Generate Java Code From WSDL dialog to generate the client-side XML-Java bindings based on the desired WSDL descriptor of the target Web service. Technically, IntelliJ IDEA generates Java code from WSDL using third party libraries. The command that control this process uses data that you specify in the Generate Java Code From WSDL dialog.

Item| Description| Web Service Client Type  
---|---|---  
Web service wsdl url| Specify the location of the target Web service WSDL descriptor.| All  
User Name and Password| Specify the credentials for accessing the WSDL URL address. The fields are mandatory if the WSDL location requires authentication.| JAX-WS  
Output Path| Specify the module source directory to place the generated files in.| All  
Package Prefix| Specify the package for the compiled Java classes.| All  
Output Mode| Specify whether you want to generate Java code only for the client side or for the server side as well.| Apache Axis  
Type Mapping Version| Specify the default [type mapping](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=/rzatz/51/webserv/wswsifattwsdl.htm) registry for mapping an XML qualified name to a Java class, using a specified Deserializer. The available options are:

  * 1.1
  * 1.2

| Apache Axis  
Allow Extensions| Generate Java code for the [extension points](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=/rzatz/51/webserv/wswsifattwsdl.htm) contained in the WSDL file.| All  
Generate TestCase| Generate an additional JUnit test case class for testing purposes.| Apache Axis  
Generate Classes for Schema Arrays| Specify whether to generate classes for schema arrays or use Java arrays.| Apache Axis  
Generate Unreferenced Elements| Generate Java code for unreferenced (declared in the schema but not used) elements as well.| Apache Axis  
Support Wrapped Document/Literal Style| Configure processing of "wrapped" document/literal, which is a document literal variation that wraps parameters as children of the root element.By default, this is enabled, and a set of conditions defines whether top-level elements are "unwrapped" and each component of the element should be treated as an argument of the operation. The following conditions apply to "unwrapped" elements:

  * An input message consists of single part.
  * This single part is an element.
  * The element has the same name as the operation.
  * The element's complex type has no attributes.

If disabled, there will be no special treatment for "wrapped" document/literal style operations.| Apache Axis  
Status| View the information in this read-only field to track and improve discrepancies when configuring the code generation procedure.| All  
  
11 October 2024

[Generate WSDL from Java dialog](generate-wsdl-from-java-dialog.html)[Monitor SOAP Messages dialog](monitor-soap-messages-dialog.html)
