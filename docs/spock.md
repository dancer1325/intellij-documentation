[//]: # (Source: https://www.jetbrains.com/help/idea/spock.html)
[//]: # (Downloaded: 2025-12-17 20:02:58)

## Create a project

To see how the Spock framework works, create a regular Gradle project.

### Create a project for Spock

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project.

Otherwise, go to File | New | Project in the main menu.

  2. From the list on the left, select Java.

Since Spock is used for testing Java and Groovy, you can leave the default Java option. You can always add the Groovy language to your project later on.

![Spock new project](https://resources.jetbrains.com/help/img/idea/2025.3/spock_new_project.png)
  3. From the list of suggestions, add and configure the following options:

     * Name: add a name of the project you are creating. For example, spock-tutorial.

     * Location: add a path to the location of your project

     * Git repository: if you want to create and upload your project to Git, you can select this option.

     * Build System: select a build tool that you want to use in your project. For example, Gradle.

     * JDK: configure the project SDK. To develop Java-based applications, you need a JDK (Java Development Kit). 

If the necessary JDK is already defined in IntelliJ IDEA, select it from the list of detected JDKs.

If you don't have the necessary JDK on your computer, select Download JDK. In the next dialog, specify the JDK vendor, version, and change the installation path if required.

     * Gradle DSL: select the appropriate DSL for your project. Since with Spock you usually work with Java or Groovy, you can leave the suggested Gradle option.

If you need to configure any advanced settings, you can do so in the Advanced Settings section.

  4. After you finish selecting necessary options, click Create. 

IntelliJ IDEA creates a Gradle project, downloads the necessary dependencies, and sets up the appropriate project structure.



