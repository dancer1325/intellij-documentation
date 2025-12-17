[//]: # (Source: https://www.jetbrains.com/help/idea/web-application-static-content.html)
[//]: # (Downloaded: 2025-12-17 20:06:42)

# Configure static content resources

Configuring static Web resources involves:

  1. [Specifying location of the static Web contents on the server](#mapping). 

After deployment, all the static content resources that implement the user interface should be located below the Web application root directory. By default, IntelliJ IDEA maps the target Web application root directory to the web folder which is created after you [enable Web development support](enabling-web-application-support.html). The default application home page is mapped to the index.jsp stub file which is also created automatically.

You can arrange your static content resources in a module in two ways:

     * Store the required resources and directories below the <project root>\web folder. After deployment, the entire folder hierarchy of these resources will be copied to the server below the application root.

     * Store the required resources locally wherever you may find suitable and [map them to folders](#mapping) on the server.

  2. [Including static Web contents in the artifact to be deployed](configure-web-app-deployment.html#addResources).




### Configure static Web content resources

  1. In the main menu, go to File | Project Structure dialog (`Ctrl+Alt+Shift+S`).

  2. Click Modules on the left-hand pane and expand the desired module.

  3. Click the Web facet. The right-hand pane of the dialog displays all the available settings.

  4. In the Web Resource Directories area, manage the list of mappings between the local folders with resources you need and the target directories on the server to deploy the resources to. The default mapping between the <project root>\web folder and the application root directory is already on the list:

     * To configure a mapping, click the New button. In the [Web Resource Directory Path](web-resource-directory-path-dialog.html) dialog that opens, specify the desired local folder and the target location relative to the application root folder. By default, IntelliJ IDEA maps the <project root>\web folder to the root folder of the application after deployment. For example, if you type a forward slash `/`, the files from the Web resource directory will be copied into the deployment root directory.

     * To edit a mapping, select it in the list, click the Edit button, and update the mapping in the [Web Resource Directory Path](web-resource-directory-path-dialog.html) dialog that opens.

     * To discard a mapping, select in the list and click the Remove button.




17 June 2024

[Populate Web modules](web-application-web-module-structure.html)[Create Web application elements](creating-and-configuring-web-application-elements.html)
