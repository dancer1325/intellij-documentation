[//]: # (Source: https://www.jetbrains.com/help/idea/generating-wsdl-document-from-java-code.html)
[//]: # (Downloaded: 2025-12-17 19:27:46)

# Generate WSDL document from Java

The available functionality of a Web service, the ports to access them, the acceptable format of requests, the format of generated responses, and so on, are reflected in the Web service [WSDL descriptor](https://en.wikipedia.org/wiki/Web_Services_Description_Language), which is normally generated on the server during the Web service deployment. A major part of Web service client development is implementing generation of requests to the service and parsing responses from it in compliance with the WSDL descriptor settings.

Suppose you have developed a Web service and want its client side development start before the Web service itself is deployed, that is, before the WSDL descriptor is generated on the server. With IntelliJ IDEA, you can have it generated before deployment.

### Create a WSDL descriptor from Java code

  1. Select the desired class name in the editor.

  2. In the main menu, go to Tools | XML WebServices and WSDL | Generate WSDL From Java Code.

  3. In the [Generate WSDL From Java](generate-wsdl-from-java-dialog.html) dialog that opens, specify the following:

     * The name and URL address of the Web service.

     * The protocol and encoding style used when accessing the public operations of the Web service.

     * The type information, including name, operations, parameters and data comprising the interface of the Web service.

Click OK when ready.




11 October 2024

[Manage deployed Web services](managing-deployed-web-services.html)[Choose Servlet Class](choose-servlet-class.html)
