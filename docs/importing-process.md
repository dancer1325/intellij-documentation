[//]: # (Source: https://www.jetbrains.com/help/idea/importing-process.html)
[//]: # (Downloaded: 2025-12-17 19:29:22)

## Project import

A common scenario of working with a build tools project is that you already have an existing project stored somewhere and want to work with such project inside the IDE.

First, you need to ensure that you trust the source from which you open your project. If you don't trust the source, IntelliJ IDEA opens the project in the preview mode that contains limited information about your project. For more information about project security, refer to [Project security](project-security.html).

If you open that project from a trusted source inside the IDE, IntelliJ IDEA "imports" it. It means that IntelliJ IDEA not only opens your project, but also performs actions that integrate that project into the IDE.

Let's see what actually happens during the importing process:

  * IntelliJ IDEA executes code from build scripts in a separate Java process which is created with the selected [Maven](maven-support.html#maven_importer) or [Gradle](gradle-jvm-selection.html) JVM

  * Based on the build tool configuration files, IntelliJ IDEA configures the project structure. For example, it sets the source/resource/test source/test resource directories, and for each module it sets the Java compiler source and target levels

  * IntelliJ IDEA adds libraries to [module dependencies](working-with-module-dependencies.html) based on dependencies configured in the build configuration files, resolves dependencies between project modules, and synchronizes dependencies across the project;

  * IntelliJ IDEA sets the language level for the project;

  * For Gradle projects, IntelliJ IDEA also creates the IDE module for each [Gradle source set](https://docs.gradle.org/current/userguide/building_java_projects.html#sec:java_source_sets)

  * For Java Web modules, IntelliJ IDEA enables [Web Application Support](enabling-web-application-support.html) and creates the [Web Application artifacts](enabling-web-application-support.html#manage_app_artifacts)



