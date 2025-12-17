[//]: # (Source: https://www.jetbrains.com/help/idea/expose-class-as-web-service-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:10)

# Expose Class As Web Service dialog

The dialog is available only through a dedicated intention action. To invoke it, place the caret at the class name and press `Alt+Enter` or click the yellow bulb icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png).

Use the dialog to configure Web service WSDL generation for an entire class, with all its methods exposed as Web service operations and deployed. The contents of the dialog depend on the Web service type.

Item| Description| Web Service Type  
---|---|---  
Service Name| Use this list to specify the name of the service to be published (for example, empty text for `ROOT` context or `mycontext` for `/mycontext`).| Apache Axis  
Service Class Name| In this field, specify the class to expose as a Web service.| All  
Service Namespace| In this field, type the Web service namespace prefix.| Apache Axis  
Service Style| Use this list to specify the style of the WSDL document to be generated. The available options are: 

  * RPC \- select this option to have an rpc WSDL generated. This option is selected by default.
  * Document \- select this option to have a Document WSDL generated.
  * Wrapped \- select this option to have a WSDL generated using the wrapped approach. If you select this option, Literal is automatically pre-selected in the Use Items in Bindings list.

| Apache Axis  
Use of Items| From this list, select how the generated WSDL document should be used. The available options are: 

  * Literal \- when this option is selected, the representation of the XML for the request is defined by the XML Schema.
  * Encoded \- select this option to have the SOAP encoding specified in the generated WSDL.

| Apache Axis  
Target Module| | All  
Status| View the information in this read-only field to track and improve discrepancies.| All  
  
28 June 2024

[Web Services Reference](web-services-reference.html)[Generate WSDL from Java dialog](generate-wsdl-from-java-dialog.html)
