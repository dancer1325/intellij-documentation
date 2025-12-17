[//]: # (Source: https://www.jetbrains.com/help/idea/content-roots.html)
[//]: # (Downloaded: 2025-12-17 19:22:26)

## Configure folder structure

Folders within a content root can be assigned to several categories depending on the content that they keep.

### Configure folders in the Project tool window

  1. In the Project tool window (`Alt+1`), right-click a folder and select Mark Directory as.

  2. Select the necessary [category](#folder-categories). This way you can assign categories to subfolders as well.


![Marking a file as a plain text file](https://resources.jetbrains.com/help/img/idea/2025.3/ij_exclude_folder.png)

To restore the previous category of a folder, right-click this folder again, select Mark Directory as, and then select Unmark as <folder category>. For excluded folders, select Cancel Exclusion.

### Configure folders in Project Structure

Use these steps if you want to configure multiple folders.

  1. In the main menu, go to File | Project Structure or press `Ctrl+Alt+Shift+S` to open the Project Structure dialog.

  2. From the list on the left, select Modules.

In the middle section of the dialog, select the module for which you want to configure the folder structure. Then make sure that you are on the Sources tab.

  3. Select the folders for which you want to assign a [category](#folder-categories) and then click the corresponding button on the toolbar above the module tree.

![Configuring folders in Project Structure](https://resources.jetbrains.com/help/img/idea/2025.3/configure_folders_in_structure.png)



### Folder categories

  * ![Sources root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.sourceRoot.svg) Sources

This folder contains production code that should be compiled.

IntelliJ IDEA compiles the code within the Sources folder. Do not place configuration files (the .idea folder or its content and the .iml file) to this folder. For more information about different types of settings, refer to [Project, module, and global settings](working-with-projects.html#settings-types).

  * ![Generated Sources Root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.generatedSource.svg) Generated Sources

The IDE considers that files in the Generated Sources folder are generated automatically rather than written manually, and can be regenerated.

  * ![Test Sources Root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.testRoot.svg) Test Sources

These folders keep code related to testing separately from production code. Compilation results for sources and test sources are normally placed into different folders.

  * ![Generated Test Sources Root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.generatedTestRoot.svg) Generated Test Sources

The IDE considers that files in this folder are generated automatically rather than written manually, and can be regenerated.

  * ![Resources Root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.resourcesRoot.svg) Resources

(Java only) Resource files used in your application: images, configuration XML and properties files, and so on. During the build process, resource files are copied to the output folder as is by default. You can [Change the output path](#specify_output_path) for resource files in your project.

Similarly to sources, you can specify that your resources are generated. You can also specify which folder within the output folder your resources should be copied to.

  * ![Test Resources Root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.testResourcesRoot.svg) Test Resources

These folders are for resource files associated with your test sources.

  * ![Excluded](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.excludeRoot.svg) Excluded

Files in excluded folders are ignored by code completion, navigation and inspection. That is why when you exclude a folder that you don't need at the moment, you can increase the IDE performance. Normally, compilation output folders are marked as excluded.

Apart from excluding the entire folders, you can also [exclude specific files](#exclude-files).

Marking folders as excluded doesn't affect deployment. For more information about excluding files from deployment, refer to [Exclude files and folders from uploading and downloading](excluding-files-and-folders-from-deployment.html).



