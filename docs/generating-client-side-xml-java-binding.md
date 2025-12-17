[//]: # (Source: https://www.jetbrains.com/help/idea/generating-client-side-xml-java-binding.html)
[//]: # (Downloaded: 2025-12-17 19:27:40)

# Generate Client-side XML-Java binding

To develop well-formed and valid requests from your client to the target Web service, you need to know the available methods of the Web service, the data types it uses, the interface to the service, the acceptable format of requests, the format of generated responses, etc. All this data is presented in the [WSDL descriptor](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=/rzatz/51/webserv/wswsifattwsdl.htm) of the target Web service.

IntelliJ IDEA can generate the necessary client-side XML-Java bindings based on the desired WSDL descriptor, thus providing you with efficient coding assistance in developing client requests. You only need to specify the URL address of the WSDL descriptor, IntelliJ IDEA will retrieve the necessary data and generate Java classes.

Java code generation is configured in the [Generate Java Code From WSDL](generate-java-code-from-wsdl-or-wadl-dialog.html) dialog, that primarily opens upon enabling the Web service client development support.

### Configure generation of the client-side XML-Java binding

  1. Select the desired client module in the Project tool window and select Tools | XML WebServices and WSDL | Generate Java Code from WSDL from the main menu.

  2. In the Web Service WSDL URL field, specify the URL address of the desired Web service WSDL descriptor.

If the Status read only field informs you about a WSDL URL connection exception, make sure the target Web service is running and the URL address of its WSDL descriptor is correct.

  3. From the Output Path list, select the directory to place the generated files in.

  4. In the Package Prefix list, specify the package to place the compiled Java classes in.

  5. For the client side of an Apache Axis Web service, specify additional configuration options for the code generation process using the provided checkboxes.




11 October 2024

[Monitor SOAP messages](monitoring-soap-messages.html)[Web services](web-services.html)
