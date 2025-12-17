[//]: # (Source: https://www.jetbrains.com/help/idea/creating-run-debug-configuration-for-application-server.html)
[//]: # (Downloaded: 2025-12-17 19:23:37)

# Application server run configurations

To run or debug your applications on an application server, you need an application server [run/debug configuration](run-debug-configuration.html). This configuration can do several things for you:

  * Build the artifacts from your source code.

  * Start the application server locally or connect to a running local or remote server.

  * Deploy the artifacts to the server and open the relevant URL.

  * If you are debugging, it can start the app in debug mode and connect the debugger.




### Create an application server run configuration

  1. In the main menu, go to Run | Edit Configurations.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the run configuration type that corresponds to the application server that you will use.

     * Use a Local configuration to run a local instance of the application server and deploy the artifacts to it.

     * Use a Remote configuration to deploy artifacts to a running application server instance.

Even if you are connecting to a remote application server, you still need a local installation of this server configured under Build, Execution, Deployment | Application Servers as described in [Integration with application servers](configuring-and-managing-application-server-integration.html).




You can configure the application server for directly from the Run/Debug Configurations dialog. To configure the application server for this click Configure next to the Application server selector.

When you create the application server run configuration, it will likely show an error, saying that you need to specify the artifacts that you want to deploy. Once you do this, the configuration will add the Build artifact task to the list of Before launch tasks so that it will build the artifacts every time before deploying them. Here is how a properly configured application server run configuration might look:

![Tomcat run configuration done](https://resources.jetbrains.com/help/img/idea/2025.3/rest_ws_tomcat_run_config_url.png)

To run the configuration, press `Alt+Shift+F10` and select the created application server configuration.

Alternatively, if you have your run configuration selected in the main toolbar at the top, you can click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) or press `Shift+F10` to run it.

You can also use the [Services](services-tool-window.html#app-servers) tool window to list and manage all available application server running configurations.

17 June 2024

[Integration with application servers](configuring-and-managing-application-server-integration.html)[Run/Debug Configuration: GlassFish Server](run-debug-configuration-glassfish-server.html)
