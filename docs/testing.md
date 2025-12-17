[//]: # (Source: https://www.jetbrains.com/help/idea/testing.html)
[//]: # (Downloaded: 2025-12-17 20:04:15)

## Add testing libraries

IntelliJ IDEA allows you to add missing libraries as you code: once the IDE detects that you're using some code from the library that is not yet added to your project, it will prompt you to download and install it.

![Adding a missing library via quick-fix](https://resources.jetbrains.com/help/img/idea/2025.3/add-lib-with-quickfix.png)

You can also [add libraries to your project manually](https://www.jetbrains.com/help/pycharm/installing-uninstalling-and-upgrading-packages.html). For example, this can be helpful if you need a specific library version or distribution.

### Manually add a testing library

Follow these steps to add a library if you're building your project with the native IntelliJ IDEA builder:

  1. In the main menu, go to File | Project Structure (`Ctrl+Alt+Shift+S`).

  2. Under Project Settings, select Libraries and click ![the New Project Library button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) | From Maven.

  3. In the dialog that opens, specify the necessary library artifact, for example: `org.junit.jupiter:junit-jupiter:5.9.1`.

  4. Apply the changes and close the dialog. 

![Manually adding a testing library to a project](https://resources.jetbrains.com/help/img/idea/2025.3/add-testlib-manually.png)



IntelliJ IDEA allows you to add missing libraries as you code: once the IDE detects that you're using some code from the library that is not added to your project yet, it will prompt you to download it. In this case, the IDE automatically adds the necessary dependencies to your pom.xml.

![Adding a missing library via quick-fix](https://resources.jetbrains.com/help/img/idea/2025.3/add-lib-with-quickfix.png)

You can also add libraries to your project manually. For example, this can be helpful if you need a specific library version or distribution.

### Add libraries using the Dependencies tool window

Follow these steps if you're using Maven in your project:

  1. In your pom.xml, press `Alt+Insert` and select Dependency.

  2. In the Maven Artifact Search tool window, type the name of the required dependency, for example: `org.junit.jupiter:junit-jupiter`. In the list of results, select the one you need and click Add.

![Adding a Maven dependency](https://resources.jetbrains.com/help/img/idea/2025.3/add-maven-tests.png)
  3. When the dependency is added to pom.xml, press `Ctrl+Shift+O` or click ![Reimport All Maven Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Maven tool window to import the changes.




For more information about working with Maven, refer to [Maven dependencies](work-with-maven-dependencies.html).

In Gradle projects, add the necessary dependencies to your build file manually.

  1. In your build.gradle, press `Alt+Insert` and select Add Maven artifact dependency.

  2. In the Maven Artifact Search tool window, type the name of the required dependency, for example: `org.junit.jupiter:junit-jupiter`. In the list of results, select the one you need and click Add.

![Adding a Maven dependency](https://resources.jetbrains.com/help/img/idea/2025.3/add-maven-tests.png)
  3. When the dependency is added to build.gradle, press `Ctrl+Shift+O` or click ![Reimport All Gradle Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Gradle tool window to import the changes.



