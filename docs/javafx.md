[//]: # (Source: https://www.jetbrains.com/help/idea/javafx.html)
[//]: # (Downloaded: 2025-12-17 19:30:17)

## Package the application with jlink

JavaFX was removed from the JDK starting with Java 11. As a result, JavaFX libraries are no longer bundled with the JDK and are not automatically included when packaging your application into a JAR file.

To package your code with Java 11 and later, you can use the `jlink` tool that is bundled with the JDK. Maven and Gradle projects that you create in IntelliJ IDEA come with the corresponding tasks to call `jlink`.

This will build a folder with JRE and application executables. The resulting program will only work on the same operating system and architecture as the host. For example, Linux will produce Linux binaries, macOS will produce macOS binaries, and x64 will produce x64 binaries.

  * Press `Ctrl` twice to open Run Anything and run `mvn javafx:jlink`. 

![Run JLink with Maven](https://resources.jetbrains.com/help/img/idea/2025.3/javafx_package_maven.png)



The IDE places the application to the target | app folder.

![Run JLink with Maven](https://resources.jetbrains.com/help/img/idea/2025.3/javafx_package_maven_success.png)

  * Press `Ctrl` twice to open Run Anything and run `gradle clean jlink`. 

![Run JLink with Maven](https://resources.jetbrains.com/help/img/idea/2025.3/javafx_package_gradle.png)



The IDE places the application to the build | image folder.

![Run JLink with Maven](https://resources.jetbrains.com/help/img/idea/2025.3/javafx_package_gradle_success.png)
