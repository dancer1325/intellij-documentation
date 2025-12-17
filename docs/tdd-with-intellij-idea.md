[//]: # (Source: https://www.jetbrains.com/help/idea/tdd-with-intellij-idea.html)
[//]: # (Downloaded: 2025-12-17 20:04:00)

## Create a project

### Create a new project

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project. Otherwise, go to File | New | Project in the main menu.

  2. From the list on the left, select Java.

  3. Name the new project, for example: `MoodAnalyser` and change its location if necessary.

  4. Select Gradle as a build tool and Groovy as a DSL.

  5. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  6. Click Create.




IntelliJ IDEA creates a project with pre-configured structure and essential libraries. JUnit 5 will be added as a dependency to the build.gradle file.

### Create a new package

  1. Right-click the main | java folder in the Project tool window and select New | Package.

  2. Name the new package `com.example.demo` and press `Enter`.



