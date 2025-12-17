[//]: # (Source: https://www.jetbrains.com/help/idea/maven-support.html)
[//]: # (Downloaded: 2025-12-17 19:32:14)

## Change the JDK version in a Maven project

There are several places where you can change the JDK version that will affect not only your current project, but the whole application as well.

### Change the JDK version in the Project Structure

Changing the JDK version in the Project Structure dialog will only affect the current project.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`.

  2. In the dialog that opens, in Project SDK, specify the JDK version and click OK to save the changes. 

![Project Structure dialog / Project page](https://resources.jetbrains.com/help/img/idea/2025.3/maven_project_sdk.png)



### Change the JDK version for the Maven runner

When IntelliJ IDEA runs Maven goals, it will use the JDK version specified for the Maven runner. By default, IntelliJ IDEA uses the [project's JDK](#project_structure_maven).

Changing the JDK for the Maven runner will only affect the current project.

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Build, Execution, Deployment | Maven | Runner.

  2. On the [page](maven-runner.html) that opens, in the JRE field, select the JDK version. 

![Maven Settings / Runner page](https://resources.jetbrains.com/help/img/idea/2025.3/maven_jre.png)



### Change the JDK version for the Maven importer

Changing the JDK version for the Maven importer will affect the whole application since it is a part of the Maven global settings. If you want to use the same [JDK version](#project_structure_maven) as you use in your project for syncing or resolving dependencies, change the JDK version for the importer.

https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Dependency_Scope 

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Build, Execution, Deployment | Maven | Importing.

  2. On the [page](maven-importing.html) that opens, in the JDK for importer field, select the same JDK version as you used in the [Project Structure](#project_structure_maven) and click OK to save the changes. 

![Maven Settings / Importing page](https://resources.jetbrains.com/help/img/idea/2025.3/maven_jdk_importer.png)


