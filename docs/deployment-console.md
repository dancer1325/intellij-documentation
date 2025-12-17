[//]: # (Source: https://www.jetbrains.com/help/idea/deployment-console.html)
[//]: # (Downloaded: 2025-12-17 19:24:39)

# Deployment console

This console shows which of the configured and marked for deployment [artifacts](working-with-artifacts.html) are successfully deployed and which are not. Use the console to deploy and undeploy artifacts and configure their execution on the server.

Item| Tooltip and Shortcut| Description  
---|---|---  
![Artifact is deployed successfully](https://resources.jetbrains.com/help/img/idea/2025.3/deploymentConsoleArtifactDeployedSuccessfully.png)| Artifact is deployed successfully| This icon next to an artifact indicates that the artifact has been successfully deployed to the server.  
![Artifact is not deployed](https://resources.jetbrains.com/help/img/idea/2025.3/deploymentConsoleArtifactNotDeployed.png)| Artifact is not deployed| This icon next to an artifact indicates that the artifact has not been deployed to the server yet or has been undeployed from the server.  
![deploymentConsoleDeployAll.png](https://resources.jetbrains.com/help/img/idea/2025.3/deploymentConsoleDeployAll.png)| Deploy All| Click this button to have IntelliJ IDEA deploy all the artifacts from the list of items to be deployed in the Deployment tab of the [Run/Debug Configuration](run-debug-configurations-dialog.html) dialog.  
![deploymentConsoleUnDeploy.png](https://resources.jetbrains.com/help/img/idea/2025.3/deploymentConsoleUnDeploy.png)| Undeploy| Click this button to have the selected artifact undeployed from the server.  
![Refresh Deployment Status](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg)| `Ctrl+F5`Refresh Deployment Status| Click this button to synchronize the deployment status indications for artifacts with the server.  
![update_resources_on_frame_deactivation_icon.png](https://resources.jetbrains.com/help/img/idea/2025.3/update_resources_on_frame_deactivation_icon.png)| Update Resources On Frame Deactivation| Click this button if you want the application to be updated automatically when you switch from IntelliJ IDEA to a different application. (Switching to a different application is referred to as frame deactivation.)This button is a toggle that turns the corresponding option on or off. If enabled, the application assets to be updated are defined by the current setting of the On frame deactivation option in the [active run/debug configuration](run-debug-configurations-dialog.html).Note that by changing the state of the button you also change the setting of On frame deactivation in the current run/debug configuration. For example, if you disable the button, the setting changes to Do nothing.  
  
11 February 2024

[Run tool window](run-tool-window.html)[Logs tab](logs-tab.html)
