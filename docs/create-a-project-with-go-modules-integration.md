[//]: # (Source: https://www.jetbrains.com/help/idea/create-a-project-with-go-modules-integration.html)
[//]: # (Downloaded: 2025-12-17 19:22:45)

## Change the IML file location for Go projects

Make sure the [Go plugin](https://plugins.jetbrains.com/plugin/9568-go) is installed and enabled.

When you create a Go project in IntelliJ IDEA, you can specify a directory for the .iml file. By default, the file is created in the root directory of the project.

To change the IML file location for an existing Go project in IntelliJ IDEA, you need to update the modules.xml file inside the .idea directory.

### Change the IML file location for existing Go projects

  1. In the Project tool window, open the .idea folder of the project.

  2. Update the `fileurl` and `filepath` attributes in the modules.xml file so that both point to the new IML file location inside .idea/.

  3. Move the IML file into the .idea directory.

![Change the IML file location for existing Go projects](https://resources.jetbrains.com/help/img/idea/2025.3/go_change_the_iml_file_location_in_modules_xml.png)


