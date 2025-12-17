[//]: # (Source: https://www.jetbrains.com/help/idea/gradle-jvm-selection.html)
[//]: # (Downloaded: 2025-12-17 19:28:19)

# Gradle JVM selection

If you created or opened a Gradle project and the version of Gradle JVM in your project is not what you've expected, you can check the following procedures to see how IntelliJ IDEA chooses the specific Gradle JVM version.

Let us say you are [creating](gradle.html#gradle_create_project) a project.

### Resolve the Gradle JVM version for a new project

  1. If you use a [project SDK](sdk.html) which is JDK, then Gradle JVM will be equal to your project's SDK. Basically, Gradle JVM equals Project SDK.

  2. If the project's SDK equals JRE, then IntelliJ IDEA will use the same steps as in [opening](#jdk_existing_project) an existing Gradle project.

  3. If there is a Gradle wrapper, then IntelliJ IDEA will use the most compatible existing Gradle version on the machine. If you do not use the Gradle wrapper in your project, then Tooling API and the Gradle wrapper that Tooling API will generate is used.




When you [open](gradle.html#gradle_import_project_start) a Gradle project for the first time, IntelliJ IDEA checks several places one by one to establish what version of Gradle JVM to use.

### Resolve the Gradle JVM version for the existing project

  1. IntelliJ IDEA checks the `gradle.properties` file for the appropriate Gradle JVM specified in `org.gradle.java.home` and uses it for the project.

  2. Then it checks the `JAVA_HOME` environment variable.

  3. Then it checks the closest appropriate JDK version for the existing Gradle version.




When you add a module to your project, IntelliJ IDEA will do the following:

### Resolve the Gradle JVM version for a module

  1. IntelliJ IDEA will use the Gradle JVM version if there is one in other modules.

  2. If there is no Gradle JVM then IntelliJ IDEA will follow the same steps as in [Resolve the Gradle JVM version for the existing project](#jdk_existing_project). 

When you import a module, IntelliJ IDEA uses Gradle defined in the project. If it is not, then IntelliJ IDEA executes the same steps as in [opening](#jdk_existing_project) a project.




### Access the Gradle JVM settings

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Build, Execution, Deployment | Build Tools | Gradle.

  2. On the Gradle settings page, under the Gradle Projects section, use the [Gradle JVM criteria](gradle-settings.html#gradle_jvm) field to check the Gradle version used for importing a project.




06 November 2025

[Gradle dependencies](work-with-gradle-dependency-diagram.html)[Getting Started with Gradle](getting-started-with-gradle.html)
