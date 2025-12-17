[//]: # (Source: https://www.jetbrains.com/help/idea/deployment-mappings-tab.html)
[//]: # (Downloaded: 2025-12-17 19:24:42)

# Deployment: Mappings Tab

In the Mappings tab, specify the mapping between a project opened in IntelliJ IDEA, the folder under the server document root that shall correspond to this project, and the URL path to it.

The easiest way is to map the entire project root folder to a folder under the server document root. The project folder structure in this case will be recreated on the server. 

Item| Description  
---|---  
Local path| In this field, specify the absolute path to the local project folder. IntelliJ IDEA automatically fills out this field with the path to the currently opened project. Type the path manually or click ![Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select the desired location in the Choose Local Path dialog that opens.  
Deployment path| In this field, specify a folder under the server document root where IntelliJ IDEA will upload the contents of the project folder specified in the Local path field. Deployment path is relative to the Folder (for local servers) or Root path (for remote servers) field specified in the Connection tab.If a folder with the specified name does not yet exist on the server, IntelliJ IDEA will create it when you trigger [project upload](uploading-and-downloading-files.html#manually).The field is not available for In-place server configurations.  
Web path| In this field, specify the URL path configured for the folder specified in Deployment path. You can use a slash (`/`) to point to the root folder, or leave the field blank if the directory is not accessible from the web. Web path is relative to the Web server URL specified in the Connection tab.  
![Add item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Click this button or press `Alt+Insert` to have a new line added to the list of mappings.  
![Remove item](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Click this button or press `Alt+Delete` to remove the selected mapping from the list.  
  
22 January 2025

[Deployment: Connection Tab](deployment-connection-tab.html)[Deployment: Excluded Paths Tab](deployment-excluded-paths-tab.html)
