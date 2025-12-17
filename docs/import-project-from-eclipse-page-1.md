[//]: # (Source: https://www.jetbrains.com/help/idea/import-project-from-eclipse-page-1.html)
[//]: # (Downloaded: 2025-12-17 19:29:18)

## Import a project to IntelliJ IDEA

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click Open.

Otherwise, go to File | Open in the main menu.

  2. In the dialog that opens, select the directory in which your sources, libraries, and other assets are located and click Open.

  3. When you import or clone a project for the first time, IntelliJ IDEA analyzes it. If the IDE detects more than one configuration (for example, Eclipse and Gradle), it prompts you to select which configuration you want to use.

If the project that you are importing uses a build tool, such as [Maven](maven-support.html) or [Gradle](gradle.html), we recommend that you select the build tool configuration.

Select the necessary configuration and click OK.

![Dialog that prompts you to select how you want to import the project](https://resources.jetbrains.com/help/img/idea/2025.3/import-from-providers.png)

The IDE pre-configures the project according to your choice. For example, if you select Gradle, IntelliJ IDEA executes its build scripts, loads dependencies, and so on.

  4. If you have been working with another project, select whether you want to open the new project in a new dialog or in the current one.



