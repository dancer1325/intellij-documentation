[//]: # (Source: https://www.jetbrains.com/help/idea/updating-applications-on-application-servers.html)
[//]: # (Downloaded: 2025-12-17 20:05:10)

# Update applications on application servers

When running or debugging an application, you can modify the source code and see the result of your changes without restarting the server. Depending on the type of artifacts and run configuration, this can either involve simple updates of resources and classes or rebuilding and redeploying the artifacts.

### Configure the application update options

If you have an [application server run configuration](creating-run-debug-configuration-for-application-server.html), you can specify what it should do when you [initiate an update](#update).

  1. In the main menu, go to Run | Edit Configurations.

  2. Open the [application server run configuration](creating-run-debug-configuration-for-application-server.html).

  3. Configure the following options:

     * On 'Update' action: Select what to do when you initiate an update.

     * Show dialog: Show a dialog with available options when you initiate an update. If this is disabled, IntelliJ IDEA will use the selected option without a dialog.

     * On frame deactivation: Select what to do when you switch from IntelliJ IDEA to a different application (for example, to a web browser).




The available update options depend on the type of artifacts (exploded or archived) and on the type of the run configuration (local or remote).

Option| Description| Available for  
---|---|---  
Update resources| Update all changed resources, such as HTML, JSP, JavaScript, CSS and images.| Exploded artifacts in local application server run configurations  
Update classes and resources| Update all changed resources and recompile all changed Java classes (EJBs, servlets, and so on).When debugging, IntelliJ IDEA will deploy and reload updated classes. For more information, refer to [Reload modified classes](altering-the-program-s-execution-flow.html#reload_classes). Otherwise, when running the application regularly, IntelliJ IDEA will only update the changed classes in the output folder. Whether it will deploy and reload such classes in the running application, depends on the capabilities of the Java runtime that you are using.| Exploded artifacts in local application server run configurations  
Hot swap classes| When debugging, IntelliJ IDEA will deploy and reload updated classes. For more information, refer to [Reload modified classes](altering-the-program-s-execution-flow.html#reload_classes). This option is not available for regularly running applications.| Archived artifacts in local application server run configurations and both exploded and archived artifacts in remote configurations.  
Redeploy| Rebuild and redeploy the application artifacts without restarting the server. The operation may be time-consuming.| Exploded and archived artifacts in local and remote application server run configurations  
Restart server| Restart the application server, rebuild and redeploy the artifacts. The operation may be very time-consuming.| Exploded and archived artifacts in local application server run configurations  
  
### Update a running application

When you launch the application server run configuration, and it successfully deploys and runs the application, you can modify the code and update your application in one of the following ways:

  * Press `Ctrl+F10`.

  * In the main menu, go to Run | Debugging Actions | Update application.

  * Click ![the Update Application button](https://resources.jetbrains.com/help/img/idea/2025.3/app.javaee.updateRunningApplication.svg) in the Run or Debug tool window.




If the necessary update option is associated with [frame deactivation](#frame_deactivation), the application will update automatically when you switch from IntelliJ IDEA to a different application (for example, a web browser).

17 June 2024

[Run/Debug Configuration: JBoss Server](run-debug-configuration-jboss-server.html)[Cloud Foundry](working-with-clouds.html)
