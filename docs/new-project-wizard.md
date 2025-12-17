[//]: # (Source: https://www.jetbrains.com/help/idea/new-project-wizard.html)
[//]: # (Downloaded: 2025-12-17 19:33:02)

## New project without frameworks

This is a general-purpose project without specific frameworks. You will be able to add the necessary frameworks and technologies later at any time.

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project. Otherwise, go to File | New | Project in the main menu.

  2. From the list on the left, select the language that you want to use in your application.

If you want to use a language that is not available in IntelliJ IDEA out of the box (for example, Python or PHP), click More via plugins and select the necessary option.

The IDE will open a dialog in which you can select and install the necessary language plugin. After that, you can close the dialog and keep configuring the new project.

![Creating a new project](https://resources.jetbrains.com/help/img/idea/2025.3/create-new-project-npw.png)
  3. Name the new project and change its location if necessary.

  4. Select the Create Git repository checkbox to place the new project under version control.

You will be able to do it later at any time.

  5. Select the build system that you want to use in your project: the native IntelliJ builder, [Maven](maven-support.html), or [Gradle](gradle.html).

For Gradle, you will also need to select a language for the build script: Groovy or Kotlin.

  6. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  7. Enable the Add sample code option to create a class with a sample `HelloWorld` application.




### Other languages

  * [Go](create-a-project-with-go-modules-integration.html)

  * [Ruby](creating-and-running-your-first-language-project.html)

  * [PHP](php-specific-guidelines.html)

  * [Python](creating-empty-python-project.html)

  * [Scala](get-started-with-scala.html)

  * [Rust](rust-plugin.html)



