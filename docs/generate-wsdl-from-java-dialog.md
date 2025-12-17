[//]: # (Source: https://www.jetbrains.com/help/idea/generate-wsdl-from-java-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:37)

# Generate WSDL from Java dialog

Use the dialog to configure Web service WSDL generation and select the methods to be exposed as Web service operations and deployed. The contents of the dialog depend on the Web service type.

Item| Description| Web Service Type  
---|---|---  
Class to Generate WSDL For| Shows the name of the class.| All  
Web Service URL| Specify the URL address the Web service will be available at.| All  
Methods for Operation| Specify which methods of the selected class you want to be deployed as Web service operations.

  * Method to Expose: shows a list of all the methods within the selected class.
  * Add to Deployment: select the checkbox next to the methods you want to be deployed as operations.

If a method cannot be selected, a tooltip explains the reason.| Apache Axis  
Web Service Namespace| Specify the Web service namespace prefix.| Apache Axis  
SOAP Action| Select the value for the `soapAction` attribute of the `<wsdlsoap:operation />` field. The available options are:

  * Default: set the `soapAction` according to the operation's metadata (usually to "").
  * Operation: set the `soapAction` is to the operation's name.
  * None: set the `soapAction` is to "".

| Apache Axis  
Binding Style| Specify the style of the WSDL document to be generated. The available options are:

  * RPC: generate an rpc WSDL (selected by default).
  * Document: generate a Document WSDL.
  * Wrapped: generate a WSDL using the wrapped approach. If you select this option, Literal is automatically pre-selected in the Use Items in Bindings list.

| Apache Axis  
Use Items in Bindings| Select how the generated WSDL document should be used. The available options are:

  * Literal: define the representation of the XML for the request by the XML Schema.
  * Encoded: specify the SOAP encoding in the generated WSDL.

| Apache Axis  
Type Mapping Version| Specify the default [type mapping](http://publib.boulder.ibm.com/infocenter/iseries/v5r3/index.jsp?topic=/rzatz/51/webserv/wswsifattwsdl.htm) registry for mapping the Java class to an XML qualified name, using a specified Serializer. The available options are:

  * 1.1 indicates SOAP 1.1 JAX-RPC compliant.
  * 1.2 indicates SOAP 1.1 encoded.

| Apache Axis  
Status| This read-only field shows whether the specified URL address is correct.| All  
  
11 October 2024

[Expose Class As Web Service dialog](expose-class-as-web-service-dialog.html)[Generate Java Code from WSDL dialog](generate-java-code-from-wsdl-or-wadl-dialog.html)
