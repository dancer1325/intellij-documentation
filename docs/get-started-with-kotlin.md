[//]: # (Source: https://www.jetbrains.com/help/idea/get-started-with-kotlin.html)
[//]: # (Downloaded: 2025-12-17 19:27:51)

## Create a Kotlin project

This is a general-purpose project without specific frameworks. You will be able to add the necessary frameworks and technologies later at any time.

  1. On the Welcome screen, click New Project. Alternatively, in the main menu, go to File | New | Project.

  2. From the list on the left, select Kotlin.

  3. Name the new project and change its location if necessary.

  4. Select the Create Git repository checkbox to place the new project under version control.

You will be able to do it later at any time.

![Creating a new project](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-new-project-idea.png)
  5. Select the IntelliJ build system. It's a native builder that doesn't require downloading additional artifacts.

If you want to create a more complex project that needs further configuration, select [Maven](maven-support.html) or [Gradle](gradle.html). For Gradle, choose a language for the build script: Groovy or Kotlin.

  6. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

If you don't know which distribution to choose, and you don't have specific requirements that instruct you to use one of the existing distributions, use Oracle OpenJDK.

For more information about JDK and how to install it, see the [Java Development Kit (JDK) guide](sdk.html#jdk).

  7. Enable the Add sample code option to create a file with a sample `Hello World!` application.

  8. Click Create.




After creating your project, you can start writing Kotlin code. See the [Create your first Kotlin app](create-your-first-kotlin-app.html#write-code) tutorial for a quick start.
