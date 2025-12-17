[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-deployment-in-product.html)
[//]: # (Downloaded: 2025-12-17 20:04:42)

## Configure the deployment server

### Add a new server

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Deployment. 

Alternatively, go to Tools | Deployment | Configuration in the main menu.

  2. Click ![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the type of the server you want to create. In our case, it is Local or mounted folder.

![Add server dialog](https://resources.jetbrains.com/help/img/idea/2025.3/deployment_add_server.png)
  3. In the Create New Server dialog that opens, type the server name and click OK.




The new server is added, but it only shows the Web server URL http://localhost where you will actually browse your uploaded files.

### Specify the server root folder

  1. In the Folder field, specify the directory to which the project files will be uploaded.

In our case, this is the Users/jetbrains/deployment local folder. You can either type the path manually or press `Shift+Enter`.

  2. Disable the Visible only for this project option to be able to export this configuration later. 

![Deployment Connection Tab](https://resources.jetbrains.com/help/img/idea/2025.3/ij_deployment_connection_tab.png)



### Specify the deployment path

  1. Next, switch to the [Mappings tab](deployment-mappings-tab.html).

By default, the Local path field contains the path to the project root. However, you can select any other directory within your project tree. Let's use the default path.

  2. In the Deployment path field (which is by default empty), specify the folder on your server where IntelliJ IDEA will upload data from the folder specified in the Local path field.

In this example, it's Application. This path is specified relative to the web server root folder, which is Users/jetbrains/deployment.

  3. Leave the default / value for Web path.

![Deployment Mapping Tab](https://resources.jetbrains.com/help/img/idea/2025.3/ij_deployment_mapping_tab.png)



After you apply the changes, the server is ready to use.
