[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-gradle-dependency-diagram.html)
[//]: # (Downloaded: 2025-12-17 20:07:05)

## Generate Gradle dependencies

Any dependency added to the project is managed by Gradle. The best way to add or manage a dependency is in the build.gradle file. Dependencies that you set up manually inside IntelliJ IDEA [module settings](creating-and-managing-modules.html) will be discarded on the next Gradle project [reload](work-with-gradle-projects.html#gradle_refresh_project).

### Add a Gradle dependency

  1. Open the build.gradle file in the editor.

  2. Press `Alt+Insert` to open the Generate context menu.

  3. From the context menu, select Add Maven artifact dependency. 

![Add dependency](https://resources.jetbrains.com/help/img/idea/2025.3/add_dependency_gradle.png)

The Maven Artifact Search window opens.

  4. In the Maven Artifact Search window, in the search field, start typing the name of your dependency. In the list of results select the one you need and click Add. 

![Search Artifact](https://resources.jetbrains.com/help/img/idea/2025.3/search_artifact_gradle.png)
  5. [Reload](work-with-gradle-projects.html#gradle_refresh_project) your project.

IntelliJ IDEA adds a dependency to the build.gradle file.

![Build script: added dependency](https://resources.jetbrains.com/help/img/idea/2025.3/build_script_dependency.png)

IntelliJ IDEA also adds the dependency to the Dependencies node in the Gradle tool window and to the External Libraries in the Project tool window. 

![Gradle tool window and Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_project_tool_window.png)

If the added dependency has its own transitive dependencies, IntelliJ IDEA displays them in both tool windows. Besides the transitive dependencies, IntelliJ IDEA also indicates cyclic dependencies in the Gradle tool window.

![Gradle tool window: cyclic dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/cyclic_dependencies.png)

If you add a dependency configuration of the [source set](work-with-gradle-projects.html#gradle_source_sets), it will be displayed in the Gradle tool window as well.

![Source set dependency](https://resources.jetbrains.com/help/img/idea/2025.3/source_set_dependency.png)


