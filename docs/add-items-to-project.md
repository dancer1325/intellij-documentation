[//]: # (Source: https://www.jetbrains.com/help/idea/add-items-to-project.html)
[//]: # (Downloaded: 2025-12-17 19:17:48)

## Create new items

### Create a new directory

  1. In the Project tool window (`Alt+1`), right-click the node in which you want to create a new directory and select New | Directory.

Alternatively, select the node and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. Then select Directory.

  2. Name the new directory and press `Enter`.

If you want to create several nested directories, specify their names separated with slashes, for example: folder/resources.

![Creating a new directory](https://resources.jetbrains.com/help/img/idea/2025.3/create-new-dir.png)



### Create a new package

Packages in Java are used for grouping classes that belong to the same category or provide similar functionality for structuring and organizing large applications with hundreds of classes.

  1. In the Project tool window (`Alt+1`), right-click the node within the [Sources Root](content-roots.html#folder-categories) ![the Sources root icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.sourceRoot.svg) or [Test Sources Root](content-roots.html#folder-categories) ![the Test Sources root](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.testRoot.svg) in which you want to create a new package, and click New | Package.

Alternatively, select the node and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. Then select Package.

  2. Name the new package and press `Enter`.

Write package names in lowercase letters. There are some other [naming conventions](https://www.oracle.com/technetwork/java/codeconventions-135099.html) for packages in Java that you should follow.

![Creating a new Java package](https://resources.jetbrains.com/help/img/idea/2025.3/create-new-package.png)



To assign a custom shortcut for creating new packages and directories, look for the Create new directory or package action under Main Menu | File | File Open Actions | Open Project Actions | New on the Keymap settings page `Ctrl+Alt+S`.

Learn about custom shortcuts from [Add a keyboard shortcut](configuring-keyboard-and-mouse-shortcuts.html#add-keyboard-shortcut).

### Create a new empty file

  1. In the Project tool window (`Alt+1`), right-click the node in which you want to create a new file and click New | File.

Alternatively, select the node and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. Then select File.

  2. Name the new file and specify its extension, for example: File.js, and press `Enter`.

If the extension you have specified is not associated with any of the file types recognized by IntelliJ IDEA, the [Register New File Type Association](creating-and-registering-file-types.html#register-new-association) dialog is displayed. In this dialog, you can associate the extension with one of the recognized file types.




### Create a new Java class

  1. In the Project tool window (`Alt+1`), right-click the node in which you want to create a new class and select New | Java Class.

Alternatively, select the node and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. Then select Java Class.

  2. Name the new class and press `Enter`.

Follow the Java [naming convention](https://www.oracle.com/technetwork/java/codeconventions-135099.html) as you create new classes.




Together with the file, IntelliJ IDEA automatically generates the class declaration.

This is done by means of file templates. Depending on the type of the file that you create, the IDE inserts initial code and formatting that is expected to be in all files of that type. For more information about how to use and configure templates, refer to [File templates](using-file-and-code-templates.html). 

You can create a class together with a package. To do so, press `Alt+Insert` in the Project tool window, select Java Class, and specify the fully qualified name of the class, for example: `com.example.helloworld.HelloWorld`. For more information, refer to [Create a package and a class](creating-and-running-your-first-java-application.html#create-package-and-class).

### Create a new module

Modules allow you to combine several technologies and frameworks in one application. In IntelliJ IDEA, you can create several modules in one project and each of them can be responsible for its own framework.

  1. Select the top-level directory in the Project tool window. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. Then select Module.

The New Module wizard opens.

  2. From the list on the left, select the language that you want to use in your application.

If you want to use a language that is not available in IntelliJ IDEA out of the box (for example, Python or PHP), click More via plugins and select the necessary option.

The IDE will open a dialog in which you can select and install the necessary language plugin. After that, you can close the dialog and keep configuring the new project.

  3. Name the new module.

  4. Select the build system that you want to use in your project: the native IntelliJ builder, [Maven](maven-support.html), or [Gradle](gradle.html).

For Gradle, you will also need to select a language for the build script: Groovy or Kotlin.

  5. Select a [JDK](sdk.html) that you want to use from the JDK list. You can use the project SDK or specify a new one.

  6. Click Create. 




For more information about modules in IntelliJ IDEA, refer to [Modules](creating-and-managing-modules.html).

### Customize the New File or Directory menu

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Menus and Toolbars.

  2. Start typing `new` in the right search bar.

  3. Reorder or remove items as you want them to appear in the New File or Directory menu and confirm the changes. 

![Customizing the New File or Directory menu](https://resources.jetbrains.com/help/img/idea/2025.3/ij_customize_new_file_menu.png)


