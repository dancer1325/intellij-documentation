[//]: # (Source: https://www.jetbrains.com/help/idea/library.html)
[//]: # (Downloaded: 2025-12-17 19:31:20)

## Define a library

After you define a library and add it to module dependencies, the IDE will be supplying its contents to you as you write your code. IntelliJ IDEA will also use the code from the libraries to build and deploy your application.

You can also create a new library from the JAR files located within a project content root. Select these files in the Project tool window `Alt+1`, and then select Add as Library from the context menu.

### Define a global library

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`.

  2. Under Platform Settings, select Global Libraries.

  3. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select one of the following:

     * Select Java or Kotlin/JS to add a library from the files located on your computer.

     * Select From Maven to [download a library from Maven](#download-libraries-from-maven).

![Defining a global library](https://resources.jetbrains.com/help/img/idea/2025.3/define-global-library.png)

In this dialog, you can also: ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) [add classes to an existing library](#add_classes_to_libraries), ![Specify Documentation URL](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolbarDecorator.addLink.svg) [specify an external documentation URL](#add-library-docs), ![Exclude](https://resources.jetbrains.com/help/img/idea/2025.3/app.modules.addExcludedRoot.svg) [exclude items from a library](#excluded_lib_items), or ![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) remove a library.




References to global libraries are stored in the IDE [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory) in options | applicationLibraries.xml.

### Define a project library

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`.

  2. Under Project Settings, select Libraries.

  3. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select one of the following:

     * Select Java or Kotlin/JS to add a library from the files located on your computer.

     * Select From Maven to [download a library from Maven](#download-libraries-from-maven).

![Defining a project library](https://resources.jetbrains.com/help/img/idea/2025.3/define-project-library.png)
  4. Select the module or modules to which you want to add the new library.




In this dialog, you can also: ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) [add classes to an existing library](#add_classes_to_libraries), ![Specify Documentation URL](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolbarDecorator.addLink.svg) [specify an external documentation URL](#add-library-docs), ![Exclude](https://resources.jetbrains.com/help/img/idea/2025.3/app.modules.addExcludedRoot.svg) [exclude items from a library](#excluded_lib_items), or ![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) remove a library.

References to project libraries are stored together with the project in the .idea folder in libraries.

### Add a library to module dependencies

Global and project libraries are not available until you add them to module dependencies.

  1. In the main menu, go to File | Project Structure | Project Settings | Modules.

  2. Select the module for which you want to add a library and click Dependencies.

  3. Click the ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button and select Library. 

![Adding a new module library](https://resources.jetbrains.com/help/img/idea/2025.3/add-new-module-lib.png)
  4. In the dialog that opens, select a project or a global library that you want to add to the module.

Alternatively, click New Library and select the required option: you can add a Java and Kotlin libraries from files on your computer, or download a library from Maven.

![Adding a new module library](https://resources.jetbrains.com/help/img/idea/2025.3/add-new-module-lib2.png)



References to module libraries are stored in the module .iml file. This file is used for keeping module configuration. For more information about module files, refer to [Modules](creating-and-managing-modules.html).

### Download a library from Maven

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S` and click Libraries to add a project library or Global Libraries to add a global library.

  2. Click ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select From Maven.

  3. In the next dialog, specify the library artifact. If you don't know its exact name, enter the keywords and click ![Search](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.search.svg).

You can also specify another library location, and select whether you want to download transitive dependencies, source files, Javadoc files, or annotations.

![Downloading a library from Maven](https://resources.jetbrains.com/help/img/idea/2025.3/projects_libraries.png)



IntelliJ IDEA will download the library from Maven or Nexus public repositories. You can also configure a [custom remote repository](#configure-custom-remote-repo).

### Add classes to a library

Once the library is added, you can add more classes to it:

  1. In the main menu, go to File | Project Structure. Then click Global Libraries to modify a global library or Libraries to modify a project library.

To modify a module library, select File | Project Structure from the main menu and go to Modules | Dependencies. Select the library that you want to modify and click ![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg).

![Adding classes to a library](https://resources.jetbrains.com/help/img/idea/2025.3/add_classes_to_lib.png)
  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the classes you want to add in the dialog that opens.

For a Java library, these may be individual class and java files, directories and archives jar and zip containing such files,or directories with Java native libraries .dll, .so or .jnilib.

  3. IntelliJ IDEA will analyze the selected files and folders, and automatically assign their contents to the appropriate library categories (Classes, Sources, Documentation, Native Library Locations, and so on).

When IntelliJ IDEA cannot guess the category (for example, when you select an empty folder), a dialog will be shown, in which you will be able to specify the category yourself.




### Include specific transitive dependencies

If you want to include only specific transitive dependencies, you can use the library properties editor.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`, and go to Modules | Dependencies.

  2. Select the necessary Maven library and click ![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg).

  3. In the next dialog, click Edit, and then click Configure next to the Include transitive dependencies option.

  4. Select the dependencies you want to include in the library and click OK.



