[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-running-your-first-java-application.html)
[//]: # (Downloaded: 2025-12-17 19:23:24)

## Prepare a project

### Create a new Java project

In IntelliJ IDEA, a [project](creating-and-managing-projects.html) helps you organize your source code, tests, libraries that you use, build instructions, and your personal settings in a single unit.

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project.

Otherwise, go to File | New Project in the main menu.

  2. In the New Project wizard, select Java from the list on the left.

  3. Name the project (for example `HelloWorld`) and change the default location if necessary.

  4. We are not going to work with version control systems in this tutorial, so leave the Create Git repository option disabled.

  5. Make sure that IntelliJ is selected in Build system. 

![Creating a new Java project](https://resources.jetbrains.com/help/img/idea/2025.3/java-tutorial-new-project-npw.png)
  6. To develop Java applications in IntelliJ IDEA, you need the Java SDK (JDK).

If the necessary JDK is already defined in IntelliJ IDEA, select it from the JDK list.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory (for example, /Library/Java/JavaVirtualMachines/jdk-20.0.1.jdk).

![Creating the new project and adding the JDK](https://resources.jetbrains.com/help/img/idea/2025.3/java-t-create-new-project-npw.png)

If you do not have the necessary JDK on your computer, select Download JDK. In the next dialog, specify the JDK vendor (for example, OpenJDK), version, change the installation path if required, and click Download.

![Downloading a JDK when creating a project](https://resources.jetbrains.com/help/img/idea/2025.3/download-jdk.png)
  7. Leave the Add sample code option disabled as we are going to do everything from scratch in this tutorial. Click Create. 




After that, the IDE will create and load the new project for you.

### Create a package and a class

Packages are used for grouping together classes that belong to the same category or provide similar functionality as well as for structuring and organizing large applications with hundreds of classes.

  1. In the Project tool window, right-click the src folder, select New (or press `Alt+Insert`), and then select Java Class.

  2. In the Name field, type `com.example.helloworld.HelloWorld` and click OK.

IntelliJ IDEA creates the `com.example.helloworld` package and the `HelloWorld` class.




Together with the file, IntelliJ IDEA has automatically generated some contents for your class. In this case, the IDE has inserted the package statement and the class declaration.

This is done by means of file templates. Depending on the type of the file that you create, the IDE inserts initial code and formatting that is expected to be in all files of that type. For more information about how to use and configure templates, refer to [File templates](using-file-and-code-templates.html).

The Project tool window `Alt+1` displays the structure of your application and helps you browse the project.

In Java, there is a [naming convention](https://www.oracle.com/technetwork/java/codeconventions-135099.html) that you should follow when you name packages and classes.
