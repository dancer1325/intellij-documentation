[//]: # (Source: https://www.jetbrains.com/help/idea/exposing-code-as-web-service.html)
[//]: # (Downloaded: 2025-12-17 19:26:11)

# Expose code as Web service

Suppose, you have a piece of code that implements a certain functionality, and you want this functionality to be available on the Web through a specific protocol. In this case, you need to transform existing code into a Web service and deploy. The action updates the Web service descriptors and generates additional deployment code if needed. This action is required every time any Web service method signature is changed or a new method is added or removed.

### To expose a class

  1. Place the caret at the class name in the editor and press `Alt+Enter` or click the yellow bulb icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png). 

  2. From the suggestion list, choose Expose Class as Web Service.

  3. In the [Expose Class As Web Service](expose-class-as-web-service-dialog.html) dialog that opens, specify the following: 

     * The name and URL address of the Web service.

     * The protocol and encoding style used when accessing the public operations of the Web service.

     * The type information, including name, operations, parameters and data comprising the interface of the Web service.

IntelliJ IDEA automatically adds the service description to the server-config.wsdd file.




28 June 2024

[Enable web service development](preparing-to-develop-a-web-service.html)[Manage deployed Web services](managing-deployed-web-services.html)
