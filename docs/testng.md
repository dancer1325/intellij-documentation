[//]: # (Source: https://www.jetbrains.com/help/idea/testng.html)
[//]: # (Downloaded: 2025-12-17 20:04:16)

## Add TestNG to your project

  1. Open pom.xml in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In pom.xml, press `Alt+Insert` and select Dependency.

  3. In the dialog that opens, type `testNG` in the search field.

Locate the `org.testng:testng` dependency, select its version in the search results, and click Add.

  4. When the dependency is added to pom.xml, press `Ctrl+Shift+O` or click ![Reimport All Maven Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Maven tool window to import the changes. 




For more information about working with Maven projects, refer to [Maven](maven-support.html).

  1. Open build.gradle in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In build.gradle, press `Alt+Insert` and select Add Maven artifact dependency.

  3. In the dialog that opens, type `testNG` in the search field.

Locate the `org.testng:testng` dependency, select its version in the search results, and click Add.

  4. When the dependency is added to build.gradle, press `Ctrl+Shift+O` or click ![Reimport All Gradle Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Gradle tool window to import the changes.




For more information about working with Gradle projects, refer to [Gradle](gradle.html).

  1. In the main menu, go to File | Project Structure (`Ctrl+Alt+Shift+S`).

  2. Under Project Settings, select Libraries and click ![the New Project Library button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) | From Maven.

  3. In the dialog that opens, specify the necessary library artifact, for example: `org.testng:testng:6.14.3`.

  4. Apply the changes and close the dialog. 




The procedure above shows the manual way of adding a dependency. If you just start writing tests, IntelliJ IDEA [will automatically detect if the dependency is missing and prompt you to add it](testing.html#add-testing-libraries).
