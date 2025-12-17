[//]: # (Source: https://www.jetbrains.com/help/idea/managing-deployed-web-services.html)
[//]: # (Downloaded: 2025-12-17 19:31:50)

# Manage deployed Web services

IntelliJ IDEA provides the possibility to [view which Web services are currently deployed](#viewDeployedWS) as well as to [re-deploy and undeploy Web services](#manageTheListOfWS) without re-starting the application server.

These operations are enabled only when the corresponding server is running.

### Get a list of currently deployed Web services

  * In the main menu, go to Tools | XML WebServices and WSDL | Show Deployed Web Services. The Web services deployed under various application contexts are listed in the browser.

  * Open the [Deployment console](deployment-console.html) of the [Run](run-tool-window.html) tool window. The console shows which of the deployment artifacts are successfully deployed and which are not. Find the artifacts that constitute the Web services in question.




### Manage the list of deployed Web services

  * Open the [Deployment console](deployment-console.html) of the [Run](run-tool-window.html) tool window. The console shows which of the marked for deployment artifacts are successfully deployed and which are not. Find the artifacts that constitute the required Web services.

  * To set the deployment statuses up to date, click the Refresh Deployment Status button ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg).

  * To undeploy a Web service, select the relevant artifacts in the list and click the Undeploy button ![Undeploy](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.undeploy.svg).

  * To have IntelliJ IDEA deploy all the artifacts marked for deployment, click the Deploy All button ![Deploy All](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.deploy.svg).




17 June 2024

[Expose code as Web service](exposing-code-as-web-service.html)[Generate WSDL document from Java](generating-wsdl-document-from-java-code.html)
